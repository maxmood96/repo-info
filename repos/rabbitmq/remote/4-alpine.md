## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:983dde86f7817c2f333f091207015e675e2399069f3767916d7021fbb08a6226
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
$ docker pull rabbitmq@sha256:e06eb1a9e4988b337bf53289aa1b7cccfe9541d029e419c7db19bb182a1077c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84063606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f398510d76166cfb9c86a29cbe2be9c8a8b6df6e8a0debd28430439b77561290`
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

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:36f99c6a9ccb7908acc52d4570dcf48d806246bfecc952f3f25f63c8451a25fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6963410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d79857bafac3c5892f1d3afa9c943005c4887cae449e4b0176eaa69cdec0088`

```dockerfile
```

-	Layers:
	-	`sha256:5fff4c8bc8510d343e7c58b2165328bce2ba4ea1e3350b443117be3507bee8dd`  
		Last Modified: Thu, 23 Apr 2026 17:23:07 GMT  
		Size: 675.8 KB (675809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:542fc084d6ddca646df369374744e4db175d6ddb0ed571dbf7c7d926fa37a934`  
		Last Modified: Thu, 23 Apr 2026 17:23:08 GMT  
		Size: 3.2 MB (3190509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d876d812ee0eee1764a583103689e6626223318e0ef527961ec7c9a5437dda4`  
		Last Modified: Thu, 23 Apr 2026 17:23:07 GMT  
		Size: 3.0 MB (3036779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af02260d71d1dc1d0183abed63a6fcaddf6e129ee6bf82d70c206ebe2d53a3b`  
		Last Modified: Thu, 23 Apr 2026 17:23:07 GMT  
		Size: 60.3 KB (60313 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:6643e9b9f35eaefc0d0d98c9685fb2e75b2e302ac9c3614029c756a2ee693ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72259616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901578cd55fde8fed86c1b7d2eeae4ea49056edb03db7ab131ec44514cac4173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2026 17:20:38 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 23 Apr 2026 17:20:38 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 23 Apr 2026 17:20:38 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 23 Apr 2026 17:20:39 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 23 Apr 2026 17:20:39 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:20:39 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:20:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 23 Apr 2026 17:20:42 GMT
ENV RABBITMQ_VERSION=4.3.0
# Thu, 23 Apr 2026 17:20:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 23 Apr 2026 17:20:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 23 Apr 2026 17:20:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:20:51 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 23 Apr 2026 17:20:53 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 23 Apr 2026 17:20:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 23 Apr 2026 17:20:54 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:20:54 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 23 Apr 2026 17:20:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 23 Apr 2026 17:20:54 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 23 Apr 2026 17:20:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 23 Apr 2026 17:20:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 17:20:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 17:20:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 23 Apr 2026 17:20:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856e812cb002f923c520392d01fdb48a225d8acc76ad40fc4c0dfcccf5446b3c`  
		Last Modified: Thu, 23 Apr 2026 17:21:02 GMT  
		Size: 33.5 MB (33519418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af13a0ed9dbf95bd27dd587fc655e161b41029cced36f33fdf5de67752158ce`  
		Last Modified: Thu, 23 Apr 2026 17:21:00 GMT  
		Size: 7.9 MB (7856495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6592aca240a93e664a4010facd07601ae1fd951481a4c991cbe19bed89a3c8`  
		Last Modified: Thu, 23 Apr 2026 17:21:00 GMT  
		Size: 1.4 MB (1404406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b84ed78ec4e3369a1470b15a22cd446a89d21c9680251790d6367d24c10aa6d`  
		Last Modified: Thu, 23 Apr 2026 17:21:01 GMT  
		Size: 25.9 MB (25905681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9844a4e54e9edc1706cb346d5ea27ec5f4a78cf3bdc643c7c65fd730a1d6be0b`  
		Last Modified: Thu, 23 Apr 2026 17:21:01 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771b84b2291195a7b7906de58e65c043149323885d09ad4680396dc26ad12de2`  
		Last Modified: Thu, 23 Apr 2026 17:21:02 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3180a289ff309c4ad6049b41c91ce1d7f908037351f4b405bb58371bdab794`  
		Last Modified: Thu, 23 Apr 2026 17:21:02 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0740a47f0b4c9ad87c54d6dabf9e60bff5efe331a567c332c746018c656f53`  
		Last Modified: Thu, 23 Apr 2026 17:21:03 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:197ea38679f949d0c5e1e2b585868ab4ef537e1b4971d1cf1421085cec3fcd47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 KB (60295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3955bb460cfd05dbdf38f6f42e9052918fe3618d5dde7dd6a18877b384621aa1`

```dockerfile
```

-	Layers:
	-	`sha256:c060d998e105c00dcea7afa853fcbcda2f50bac88be411c06b7b4d453af00fa1`  
		Last Modified: Thu, 23 Apr 2026 17:21:00 GMT  
		Size: 60.3 KB (60295 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:83cc001f8c1177fb99c68e8085da0e85e13b0226d98a0489af48d60c86293ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71353226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e1f334beb555ef47084d265b3b695fdb0de55a297490bb1883a67b8381ad5c`
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

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e80a1242998c10a9f7dcfd09f6ae60c7a0b9363fae154527153b13722bde550d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f259cca3e681dd934af792676afb8f0c4a2142de928312caab459e3cfe52935`

```dockerfile
```

-	Layers:
	-	`sha256:52da238ea31725fa318f2c4a9e3328792439724066e39ad06bb4b3ffb43a6ef2`  
		Last Modified: Thu, 23 Apr 2026 17:22:32 GMT  
		Size: 671.0 KB (670952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68fd750f034c9a05b4b6b69d9e6878415b00407a24ae2bf039e93826e1082fc9`  
		Last Modified: Thu, 23 Apr 2026 17:22:32 GMT  
		Size: 3.1 MB (3057001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c605b5be45971c9b2dbdecf1fa9f8b817b032451898244ee72764dfd68640c43`  
		Last Modified: Thu, 23 Apr 2026 17:22:32 GMT  
		Size: 2.9 MB (2901941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8b672d3ae82c7a26904bb16a15e73065a5b934c09892fd1315be4eeaf38d703`  
		Last Modified: Thu, 23 Apr 2026 17:22:32 GMT  
		Size: 60.5 KB (60510 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:acfd9079c1c08b1083e8d8b8781edbd8c999347b39f6b89e8ed8ff73ca86412f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83091428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42e6ae1393521dc538647e7104289a22ceca743bdb0ef8d16aeba373102a57d`
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

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0da6fd7235727e63f9d253df2193b185a322f0bb52612aa6469755aef615aef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7036388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512f1dec36c183fca4cfc568c4901e68e7e2f89521a17dd563d4b0cdfa99d967`

```dockerfile
```

-	Layers:
	-	`sha256:a6a2f3692a683505f62d1b753b4ce58eef14f28c42bd7ae9158994079ff66715`  
		Last Modified: Thu, 23 Apr 2026 17:22:09 GMT  
		Size: 676.0 KB (675952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35538d51b5138d3c13ba3493bfbc10f3699aca74e77e08dbf592355379cd5905`  
		Last Modified: Thu, 23 Apr 2026 17:22:10 GMT  
		Size: 3.2 MB (3227469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d68c759093599d5751ef6d0154cd77ff141adede9c456dd2b4cfd6d04df606ee`  
		Last Modified: Thu, 23 Apr 2026 17:22:10 GMT  
		Size: 3.1 MB (3072415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751409b478d612b160b11a4952b9e2c42401989c6a2107e6b99dbbc9fdd748ad`  
		Last Modified: Thu, 23 Apr 2026 17:22:09 GMT  
		Size: 60.6 KB (60552 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:7af67573caa55e5d4ebbbc82986b9c0e8b9ec118bb8b124c08b3c16c0d5e700e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73195279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d4effde533b6e9994fca13cba374d2caa74e41747380fb7ba9e65dae60a189`
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

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bac6bd9646e7aa0fda04ff5245279b5761aa2c5c1da8a47686c59a4aa420f484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6914801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b317d5d01ff04dc66a580f052f59d4d862631f0da369919a410bf881dff47f98`

```dockerfile
```

-	Layers:
	-	`sha256:35df4fef95bd18bc25d9848af683c49aef79c7ba99346f3a8dfdd8ef8af5ed2c`  
		Last Modified: Tue, 21 Apr 2026 22:29:44 GMT  
		Size: 670.7 KB (670740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b7c734e50301805e44ea266f2b35d4fa3737aec39c8f82fc48d5b28a699e029`  
		Last Modified: Tue, 21 Apr 2026 22:29:44 GMT  
		Size: 3.2 MB (3168762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b86feda63f4cf1e1b0e475723be8e14abac847ad679e29802defe5a815d2d607`  
		Last Modified: Tue, 21 Apr 2026 22:29:44 GMT  
		Size: 3.0 MB (3015036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c49cc7cc425038cd161d80f965b8898dee0bba254da5f3ca55bb67733645c0d6`  
		Last Modified: Tue, 21 Apr 2026 22:29:44 GMT  
		Size: 60.3 KB (60263 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:4421c778a6c4cc167e499829c1731cb0ecb354f02087cc4d5bff6e70b9893daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75334075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8e977b493806f276886e941845bb1e842d02ee983a64374e670d35c918a1e5`
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
ENV RABBITMQ_VERSION=4.3.0
# Tue, 21 Apr 2026 22:28:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 21 Apr 2026 22:28:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 21 Apr 2026 22:28:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:16:36 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 23 Apr 2026 17:16:38 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 23 Apr 2026 17:16:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 23 Apr 2026 17:16:38 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:16:38 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 23 Apr 2026 17:16:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 23 Apr 2026 17:16:38 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 23 Apr 2026 17:16:39 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 23 Apr 2026 17:16:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 17:16:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 17:16:39 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 23 Apr 2026 17:16:39 GMT
CMD ["rabbitmq-server"]
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
	-	`sha256:237614a3564a022b35e292dc724b15f61c076de1779ebfd2fa579888ed0ed03a`  
		Last Modified: Thu, 23 Apr 2026 17:22:10 GMT  
		Size: 25.9 MB (25905475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1761762fac767feebde1a4956596538b8d9d4ad7febd99d45eb0cddb61e485ef`  
		Last Modified: Thu, 23 Apr 2026 17:22:09 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c416de57d0e4883f52528209ad3db27c080df1bcf0ce106b157db5f106c9d812`  
		Last Modified: Thu, 23 Apr 2026 17:22:09 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58efd5032baabbb340c4313fa998adb5a63ad104b239f07b35a6af0f48347af`  
		Last Modified: Thu, 23 Apr 2026 17:22:09 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1548dd9da376fc0cfdf8a61f6ccc1096db2287eeed232533e6d7bae5353f0833`  
		Last Modified: Thu, 23 Apr 2026 17:22:10 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:eedafe7dbba0dd49ae3e1bb9c866b0562dbf15c6473158c2519e643e11aca97d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6938066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4f97d4df10e13d1662cc469020b7d7ce17909533d97367344cb03294eeea98`

```dockerfile
```

-	Layers:
	-	`sha256:142e4025228ed5fe56af615751742dd1c1255ffaea5d2d6a28c0a185cf0d7e78`  
		Last Modified: Thu, 23 Apr 2026 17:22:09 GMT  
		Size: 670.9 KB (670949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08c4b0d1a3168b26d2ae2f79cb50c58330a830e6ca112c6eaee126ff22059171`  
		Last Modified: Thu, 23 Apr 2026 17:22:09 GMT  
		Size: 3.2 MB (3180904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a751758b0694841b14067bfdc6297344038379d9fcdb991f05be040948b09e3d`  
		Last Modified: Thu, 23 Apr 2026 17:22:10 GMT  
		Size: 3.0 MB (3025838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a47050eaa9ad65a05f0870385529249813479d40fb80d007494b902294d475c`  
		Last Modified: Thu, 23 Apr 2026 17:22:09 GMT  
		Size: 60.4 KB (60375 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:78d7a6b84db60df16025e76360bf7ea235a8cd7b9df3c83a669e5c052e7ea0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78766074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fabf0fc99523e175d1a008279f18dcaabdb8c39c1eb4ec5c4e338d6aab3bdb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 05:13:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 22 Apr 2026 05:13:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 22 Apr 2026 05:13:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 22 Apr 2026 05:13:43 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 22 Apr 2026 05:13:43 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 05:13:43 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 22 Apr 2026 05:13:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 22 Apr 2026 05:13:55 GMT
ENV RABBITMQ_VERSION=4.2.5
# Wed, 22 Apr 2026 05:13:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 22 Apr 2026 05:13:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 22 Apr 2026 05:13:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 05:32:15 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 22 Apr 2026 05:32:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 22 Apr 2026 05:32:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 22 Apr 2026 05:32:26 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 22 Apr 2026 05:32:26 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 22 Apr 2026 05:32:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 22 Apr 2026 05:32:26 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 22 Apr 2026 05:32:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 22 Apr 2026 05:32:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 05:32:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 05:32:27 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 22 Apr 2026 05:32:27 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7284d49606fd8c9ded6e25796a5ad27b9e244b31297cc29534b9bdee49ef3a70`  
		Last Modified: Wed, 22 Apr 2026 05:20:23 GMT  
		Size: 37.5 MB (37522961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5eebf0555295aa4ed26459e2ade5294de5efa786d39c6e1347cb6f531e2c60a`  
		Last Modified: Wed, 22 Apr 2026 05:20:16 GMT  
		Size: 10.8 MB (10787537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140184dfa92cc52240860bed267a85fda593c871da39645b662022532ab667c0`  
		Last Modified: Wed, 22 Apr 2026 05:20:12 GMT  
		Size: 1.4 MB (1449763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b9c4949b9df6325de2397bb8cfc7677ddd02deb093dba445bf2d364aa68029`  
		Last Modified: Wed, 22 Apr 2026 05:36:39 GMT  
		Size: 25.4 MB (25416407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaba9abe4d5758e8ccd1add217b97845c81cc300a5c9d71da3a347bd3996681`  
		Last Modified: Wed, 22 Apr 2026 05:36:35 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e4a51c2adaa9f39ddf36e2fae791bdd5cd54ab2e56d2c5c9a1c8eb3009a030`  
		Last Modified: Wed, 22 Apr 2026 05:36:35 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f23298348aeec91eeacc3ddddbd751551c1cbeb2e2b67f0fb2d17d0d348ce1`  
		Last Modified: Wed, 22 Apr 2026 05:36:35 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cca044c3225936a8191f0b321a1f813043a1c44d5fedf1c6327ff7ea3a9718`  
		Last Modified: Wed, 22 Apr 2026 05:36:37 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:48a341ce3b6c5ddf7089619684a84d7c5960a8a1ff8c14e012f45ea09d33eb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7017219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea16f0740a41b282983829131d26c77bc505eb59898ccb7a2769d702af36ea8`

```dockerfile
```

-	Layers:
	-	`sha256:e1029c45aa6028f572e530ebbf87a86c16e2b6cdb907beb9d450faa58500af0b`  
		Last Modified: Wed, 22 Apr 2026 05:36:35 GMT  
		Size: 673.9 KB (673854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:986eb09a3fef2565e54a5968d2506e9438f99627b9cac2474ccad52d39c9189b`  
		Last Modified: Wed, 22 Apr 2026 05:36:35 GMT  
		Size: 3.2 MB (3219019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4bbeecaf732377d0d868f5bd3b534a6ee79609ab9336282200fc060aaa793fe`  
		Last Modified: Wed, 22 Apr 2026 05:36:36 GMT  
		Size: 3.1 MB (3063965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8a86718e57bf4687ae07efb6463e890ea11b8de0efd4a221f771806353e318b`  
		Last Modified: Wed, 22 Apr 2026 05:36:35 GMT  
		Size: 60.4 KB (60381 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:399c0adf1f38077ccbcff3310937124051f1f3aa2b46e028423c5306cf05f946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72953964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706297a7718f7dc74d0391929f5dfa60d6e0e0b7ff18e3ec0b5b8d27c85a5447`
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

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1e8b8aa8fa4e7d4d55daf6c5290c7c1c1420331c2e50cc950a09151b4c11f1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6714384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad059886e2f7024e4c4cdef01baaacc98067bdc343b64979482b6fce427a190`

```dockerfile
```

-	Layers:
	-	`sha256:73575de82ca91ce578685664e1fd41615269d549f36d583a42947b85932787ed`  
		Last Modified: Tue, 21 Apr 2026 22:30:36 GMT  
		Size: 670.9 KB (670851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0927727922208fc2b93ebba6782a854d5c9d08dbfd7506f78ec9cf9f3d51fd`  
		Last Modified: Tue, 21 Apr 2026 22:30:36 GMT  
		Size: 3.1 MB (3069128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e4453d19ef455585183af4e58978a1659d04780fc17ffadb2aff9644f4b4f1`  
		Last Modified: Tue, 21 Apr 2026 22:30:36 GMT  
		Size: 2.9 MB (2914092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6f542482168e0358b5763fba9d6fa8112ae431d9dd818c8def9b253da1e747`  
		Last Modified: Tue, 21 Apr 2026 22:30:36 GMT  
		Size: 60.3 KB (60313 bytes)  
		MIME: application/vnd.in-toto+json
