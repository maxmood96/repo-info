## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:b9faa9067fe84cc0aba795945b52a09b41a4e4ad8925924beb904f16d6bbef84
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
$ docker pull rabbitmq@sha256:2abf7852adf3ed228e8364dd70cbfcd9a70b757b03726f4b506239c5d5c13c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75401928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff18c3853690fb1532d46de5d48fe72fced3a7ea198ddd678d213d10a976e52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 04 Apr 2025 11:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 04 Apr 2025 11:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 04 Apr 2025 11:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_VERSION=4.0.8
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 11:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 04 Apr 2025 11:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 04 Apr 2025 11:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 11:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 04 Apr 2025 11:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3175f2cfc596b2ecad16d3d3bc3e2b84e0954433fc90b6f1fafd7e7f94d5d7f`  
		Last Modified: Fri, 04 Apr 2025 17:34:00 GMT  
		Size: 42.8 MB (42831810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a652a1105f32ae890d87050dcc888fdf921a27d458df396f734208106142ea6a`  
		Last Modified: Fri, 04 Apr 2025 17:34:01 GMT  
		Size: 8.3 MB (8311653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e53d78eefe2a9d856556642bf495b83d51bd215fa948e526a286a70601da68`  
		Last Modified: Fri, 04 Apr 2025 17:34:00 GMT  
		Size: 2.3 MB (2279386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e3d9acf95a08fc99373f8979801ea37ce70ad5e190297893ce68c9fa382c2c`  
		Last Modified: Fri, 04 Apr 2025 17:34:00 GMT  
		Size: 18.3 MB (18335084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c143c78b29361286e2d11c5a3cc77838e3dc44d114a907db2cb5cf6333a5d4`  
		Last Modified: Fri, 04 Apr 2025 17:34:01 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9f3bce447d7450f3ec8bfda24800f89b198d77d9cf17b4e97a0f0bc9729a53`  
		Last Modified: Fri, 04 Apr 2025 17:34:01 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1272a8a76ca90cab8b7d0b0e7d2926a6bd472940f171eed8dc969d9fa8d6e531`  
		Last Modified: Fri, 04 Apr 2025 17:34:02 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa08c2ffdf9b113788142dad51a68abaaa4d6c40fbeca8e92eb0e7876f6d2dc8`  
		Last Modified: Fri, 04 Apr 2025 17:34:02 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6d7da5f616d8cd13cc34984dd7b57e72ee3f6dcdf7ac0db53fae59cc336befc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6726524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290d0514be402b69df76fcd6d064f6da456da0dd00511dd303310109ce833de8`

```dockerfile
```

-	Layers:
	-	`sha256:b7c62de2030c2a18e49d59bb710aca7d75ac07dd4fc04ae705ad9227d631e3c0`  
		Last Modified: Fri, 04 Apr 2025 17:34:00 GMT  
		Size: 657.2 KB (657214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0ada1a077bf026b9b5e3647a72461db7be2dd72675a2087702b2e8506539f8`  
		Last Modified: Fri, 04 Apr 2025 17:34:00 GMT  
		Size: 3.1 MB (3081286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700da6a3efe47296b34d3a2d8d77b4787da5d9dd4566d917b6a726f79d1cc1d7`  
		Last Modified: Fri, 04 Apr 2025 17:34:00 GMT  
		Size: 2.9 MB (2928081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd32ca6b087a865011812207d321e837217912e81770d08192d2a784efa24ee2`  
		Last Modified: Fri, 04 Apr 2025 17:34:00 GMT  
		Size: 59.9 KB (59943 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:22d19e427b9eb489e49504c12d116e279012b9808d6dc2ab8f4c60e7160bce4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63453597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dbb75b76a6c670e3cbb76cbcfcb896bba3d0bfd40d2b5cf35f4cddef2abebb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 04 Apr 2025 11:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 04 Apr 2025 11:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 04 Apr 2025 11:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_VERSION=4.0.8
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 11:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 04 Apr 2025 11:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 04 Apr 2025 11:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 11:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 04 Apr 2025 11:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fc7de5297f460eb8edbb34d2fa88470349312b717c45c18d4cccc10ef15f94`  
		Last Modified: Fri, 04 Apr 2025 17:30:56 GMT  
		Size: 33.4 MB (33427362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41b00ee5464b93d67fdf77837de86033b382261212c42a17526a10a5bbf3f0e`  
		Last Modified: Fri, 04 Apr 2025 17:30:56 GMT  
		Size: 7.1 MB (7097958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6196f0e9a4a2e32bae325452b9da3e6ef9f612848be7ccf84ab3446472ba0a8`  
		Last Modified: Fri, 04 Apr 2025 17:30:55 GMT  
		Size: 1.2 MB (1226979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7f542e9531ab20b9b811fc55bde6531b0c57f607ab6b85823b8bc4cef96df8`  
		Last Modified: Fri, 04 Apr 2025 17:31:25 GMT  
		Size: 18.3 MB (18334822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3eadc24dcd449d6e6e9e3c5c67ef9b87c0d97c09fe10cf74851034f5ba72d4`  
		Last Modified: Fri, 04 Apr 2025 17:31:24 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab39ce21f3706593e2cfdd1c7770d3fbfd5e9f90542d47d1d41040c805ee6a3`  
		Last Modified: Fri, 04 Apr 2025 17:31:24 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc3873d031e65f3277951b34a399c73b7a3067c6fee7ab5cbbca2d58537c144`  
		Last Modified: Fri, 04 Apr 2025 17:31:24 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7865e250c8d7634fc2f5ba7e20155871c0093b9ade82f20c8748a5035908de`  
		Last Modified: Fri, 04 Apr 2025 17:31:25 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:be05dbe03dccc550371cad374f44d5e828ef7e7d44084e94244fdf213334da36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 KB (59921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db068f912b132c26c40e636fbdc74b0a329f85b7f9281d8fe78b80346dbfe6a9`

```dockerfile
```

-	Layers:
	-	`sha256:70c6641fe293bd14a5a8e64b41bb00d50837f28e7a4f4ce81cc85977e2c22927`  
		Last Modified: Fri, 04 Apr 2025 17:31:23 GMT  
		Size: 59.9 KB (59921 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:ebf2ce75e62f398443070db14f473b0e33a010355bc5f43fadd9cbc29958b724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62681018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f914a0df335c01eb1a965c3327cf9949a6fa3daaf3bd1125202dec2649f3da1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 04 Apr 2025 11:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 04 Apr 2025 11:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 04 Apr 2025 11:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_VERSION=4.0.8
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 11:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 04 Apr 2025 11:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 04 Apr 2025 11:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 11:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 04 Apr 2025 11:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180687ec158ecb9d2287088070115c5d94d14aea357ed2cb35ec5a1fd15a1a84`  
		Last Modified: Fri, 04 Apr 2025 17:35:53 GMT  
		Size: 33.4 MB (33370046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8497ebbbc56f64557a9607867ff3739a5e4a1df46ed0cf9df1c0f271463ad5ae`  
		Last Modified: Fri, 04 Apr 2025 17:35:52 GMT  
		Size: 6.7 MB (6742225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91faa9fbaa189690893c27b0422c385dd52ef1dfd84283d57cd33790ff76a365`  
		Last Modified: Fri, 04 Apr 2025 17:35:52 GMT  
		Size: 1.1 MB (1134773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94cee552de2a2dc72c845d34281b9024034557d99f9279039ebda168143d936`  
		Last Modified: Fri, 04 Apr 2025 17:37:58 GMT  
		Size: 18.3 MB (18334109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf1d41615a5488bc01dfe1ce2f78755c70170411c549f3a789238fb5a86a8c2`  
		Last Modified: Fri, 04 Apr 2025 17:37:57 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bf6790072562f2c47baec5c1df0e5724859355cb28b453452320e875056eda`  
		Last Modified: Fri, 04 Apr 2025 17:37:57 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd1c1960127b4409fc8e2dd78f0949e7b5a23ced89d47f3a447ed5aee18fe62`  
		Last Modified: Fri, 04 Apr 2025 17:37:57 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771b7ac9451fd93e05339bc98802218ab2c3bb7025d7642cc42ea9870a334c73`  
		Last Modified: Fri, 04 Apr 2025 17:37:58 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f9eecdf09b6e543f49e8331ff61286854d7c484dd2cb91b50cb01465c93e076a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6493243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e674cccee3230d87fa9cfbe9ab8b87be7f317d4c74ed4ecdeaeef6c8269e079`

```dockerfile
```

-	Layers:
	-	`sha256:19e5ea5963f02fd6a5b3d20d01aa787af97d7ca7083e7526c3f2e38882b03431`  
		Last Modified: Fri, 04 Apr 2025 17:37:57 GMT  
		Size: 653.4 KB (653359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e0ebb042eb52e23b52c4109ab8edf7a045708c1ceeb5bd456710b2f206f884`  
		Last Modified: Fri, 04 Apr 2025 17:37:57 GMT  
		Size: 3.0 MB (2967140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6abce04786091e0b62d32a1538be079a4173e28a3ef71f0d9bb2d81e9d38198`  
		Last Modified: Fri, 04 Apr 2025 17:37:57 GMT  
		Size: 2.8 MB (2812610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dd820f44fa23ddcc366e4cd331b07b5d3aba8a9f1ab3e251f900b8192e5d855`  
		Last Modified: Fri, 04 Apr 2025 17:37:57 GMT  
		Size: 60.1 KB (60134 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:6d6acfb76b8f2e7423aa71dd5c89f7869ee41503c77477ce9167413dbd67ae0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74516796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4f358b75c64432775dc1c4c52a74623faff4860a78d63cb896f201e2616382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 04 Apr 2025 11:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 04 Apr 2025 11:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 04 Apr 2025 11:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_VERSION=4.0.8
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 11:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 04 Apr 2025 11:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 04 Apr 2025 11:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 11:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 04 Apr 2025 11:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2251d7ee84d45b0bdd9970a00917e4b880a98aa128625bd4b685de277ded942d`  
		Last Modified: Fri, 04 Apr 2025 17:34:57 GMT  
		Size: 40.8 MB (40828335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1788585587bd74793dad0ba1fe3509c1607432cf99f340c602eef34a144769d7`  
		Last Modified: Fri, 04 Apr 2025 17:34:56 GMT  
		Size: 9.0 MB (9034847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3f4a2b0f8fd35a8569f9b8edb1ec7d251b5ff202e166c0d0962cd5be884d7d`  
		Last Modified: Fri, 04 Apr 2025 17:34:56 GMT  
		Size: 2.3 MB (2323897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08e9826592ed28cc0201a49624da130147b1a70610797e427b3b4287a180f87`  
		Last Modified: Fri, 04 Apr 2025 17:43:22 GMT  
		Size: 18.3 MB (18334942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0462207c454e24dfc61b46dd4c365104dc5a80aa1f3eb9f2bc270f300e2ab4fb`  
		Last Modified: Fri, 04 Apr 2025 17:43:22 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db5a60c19564e44d25e043ea53e38a88f9f4ba89e048e0e2d72357a42d4acb4`  
		Last Modified: Fri, 04 Apr 2025 17:43:22 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d3a5767da6977c8065fb8fdd3ebab3f34015ca71293dc6b924adc38a1cc28a`  
		Last Modified: Fri, 04 Apr 2025 17:43:22 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cf661552a11785cd5a02722955d0914bd37c74ab8be595cbaf4823e679abc3`  
		Last Modified: Fri, 04 Apr 2025 17:43:23 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f47b22b5d91c8ca528d25694e44f20883e01745b4ac75cbf8c21539e49819dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6835853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa7c2791b4326c94792fa512fd5a98df8f04dbbdfe4d348efce920949c4da1f`

```dockerfile
```

-	Layers:
	-	`sha256:751f5950bd6482a449b7db4a0d87d85ebad04e1f1df11ec79a02aeef05854864`  
		Last Modified: Fri, 04 Apr 2025 17:43:22 GMT  
		Size: 658.0 KB (658005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b8629d2d2be65eae8e21c1ce2a939646f2a05902d7a8830e30ff0b2d73e6bc`  
		Last Modified: Fri, 04 Apr 2025 17:43:22 GMT  
		Size: 3.1 MB (3136095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:639c6492e80c758e3beb304014281fa0d78c2668543c51e94e4eae32562bcc73`  
		Last Modified: Fri, 04 Apr 2025 17:43:22 GMT  
		Size: 3.0 MB (2981571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78892b3210275744909fad91027629670436f9ab63e0584acb88283b25993b7a`  
		Last Modified: Fri, 04 Apr 2025 17:43:22 GMT  
		Size: 60.2 KB (60182 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:e3b024234e7155d043fe6ab22381b55f37110104533b4ecd526f1a1214b0cc5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64870529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8892e9f6cdab68804d317352fbd56338059af11409131596e2b900e6419996cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 04 Apr 2025 11:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 04 Apr 2025 11:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 04 Apr 2025 11:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_VERSION=4.0.8
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 11:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 04 Apr 2025 11:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 04 Apr 2025 11:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 11:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 04 Apr 2025 11:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3650a3e480162d98cd9c57eb1eaba694d59bce49e4924ec95fe3e146ae1b9378`  
		Last Modified: Fri, 04 Apr 2025 17:34:11 GMT  
		Size: 33.5 MB (33515582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d371b4b6238067cc8825f197619ec4bccb825fc1d8a1120f97cb056ab45c328`  
		Last Modified: Fri, 04 Apr 2025 17:34:10 GMT  
		Size: 8.3 MB (8324825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5beee324e18d71ef58548a0fc88da1751866cdfc51b3ecdfccc0360dd29543b1`  
		Last Modified: Fri, 04 Apr 2025 17:34:10 GMT  
		Size: 1.2 MB (1230635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df63dfa065880cf02686b9947150686cd5565c0186fdcb1b5586c7ea6368a8f2`  
		Last Modified: Fri, 04 Apr 2025 17:34:11 GMT  
		Size: 18.3 MB (18334128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726b6e028de1df3774c5cd492029d4d4c5e307bed963b715cb2b6ce98a8554ac`  
		Last Modified: Fri, 04 Apr 2025 17:34:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad964f162bd7e210b800e0e4c503c99c44832f4e2b1e92709e19d3a29750bfc7`  
		Last Modified: Fri, 04 Apr 2025 17:34:12 GMT  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e9d92b5c33bcd896583b93c80266d9cc2d12626472c42989027b04e94f8caf`  
		Last Modified: Fri, 04 Apr 2025 17:34:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16053261277c3135fc023e7b5c86dc7078c14d2ab9053a6ae9c1f2a51af8ba4`  
		Last Modified: Fri, 04 Apr 2025 17:34:12 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a44d7a11699593da394ba3f694e4a1aa8ee759cdb93a42ff765d1e194625cf9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6699719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267301a44f593ab511a6ab6162a32295b69930adc603c36b2e4371874af388ec`

```dockerfile
```

-	Layers:
	-	`sha256:05b7589b8b2e570acb894c4b5d92cd1bb84693ea3d6f5b6de88f0665bb4e3d40`  
		Last Modified: Fri, 04 Apr 2025 17:34:10 GMT  
		Size: 652.6 KB (652563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a7cfe8fb8187e7a6f53e63c521e3f8b07405f8126acbb350997f5c02c8871ec`  
		Last Modified: Fri, 04 Apr 2025 17:34:10 GMT  
		Size: 3.1 MB (3070232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e6b421467dd56fdac1b07df6f37d71444d0840d0a3ba028cbc21cfcaf7a2d94`  
		Last Modified: Fri, 04 Apr 2025 17:34:10 GMT  
		Size: 2.9 MB (2917031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16d92a0049d8d85f961aeb97cc3841a752a2af1a2e7289231df5b26d7197b3e0`  
		Last Modified: Fri, 04 Apr 2025 17:34:10 GMT  
		Size: 59.9 KB (59893 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:6012dec48c303b96c0bd4d7ba2855fec2ef2126620d1236111eabb66585b58ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66004714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5134d2035292a5f200b86724459f52a89417722cc14523fd9e3db7d91ce8059d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 04 Apr 2025 11:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 04 Apr 2025 11:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 04 Apr 2025 11:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_VERSION=4.0.8
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 11:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 04 Apr 2025 11:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 04 Apr 2025 11:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 11:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 04 Apr 2025 11:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf0b50985a98f5f48b42152548faf6af18ac38a88706ae0c365f624b42b47ee`  
		Last Modified: Fri, 04 Apr 2025 17:37:51 GMT  
		Size: 33.9 MB (33899682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552a198c365f89aba2dbe30fb5c15cc46ef03ac40ba877819c81e692d624e789`  
		Last Modified: Fri, 04 Apr 2025 17:37:50 GMT  
		Size: 8.8 MB (8848316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f3388b78bc78ae30f55fb2b933f7b66f8e730c9bf19130eba2a3d88750b637`  
		Last Modified: Fri, 04 Apr 2025 17:37:50 GMT  
		Size: 1.3 MB (1346513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2a9d480f62ee2b66c5768d6ce4be09dc66d93d33a86f177760720f7fe80064`  
		Last Modified: Fri, 04 Apr 2025 17:48:18 GMT  
		Size: 18.3 MB (18334105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d30aeb1e543d394c019e8334ad946d50e8e5949120b1962567ce2f11f4531c`  
		Last Modified: Fri, 04 Apr 2025 17:48:18 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095bd3aef3c9c74320ec7b90805ec683079a185ce5a08dc4d2a1c3f07f03342d`  
		Last Modified: Fri, 04 Apr 2025 17:48:17 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc9234e73deec66fa89a53d17542bf82807aa1f447aa89a81e803dd5809ae9c`  
		Last Modified: Fri, 04 Apr 2025 17:48:18 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21afe589096a7134cad895963a24d7ea88cd013194a57631234c8ca4d79d69b1`  
		Last Modified: Fri, 04 Apr 2025 17:48:19 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e9efb8950622c2c8ac42992cf82cc5db52fe77b8c233a861ead5480226851485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6731523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f6811256cd3e13568a65f6526f93bc9f6a28593fe0a8f293c7907680067534`

```dockerfile
```

-	Layers:
	-	`sha256:fe136370cce8a07e3f41d327bb220cf5844aafabdaf5308b03887b3542877610`  
		Last Modified: Fri, 04 Apr 2025 17:48:18 GMT  
		Size: 651.4 KB (651406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eceead0dd102561760fb8203e1b5a323aa35ad2d5771409fc626a08a45911fa6`  
		Last Modified: Fri, 04 Apr 2025 17:48:18 GMT  
		Size: 3.1 MB (3087324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60e9a1aa8ab3a357733d358cccd9c79358e39323e6c3e09ceb994ff02c70b666`  
		Last Modified: Fri, 04 Apr 2025 17:48:18 GMT  
		Size: 2.9 MB (2932788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c694bfeedc54cfa327efbd8d3a0fe0fc3ab87279ada959f4b4eb3db63419b0c3`  
		Last Modified: Fri, 04 Apr 2025 17:48:17 GMT  
		Size: 60.0 KB (60005 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:7ff6541ff890b18f5d3648ff6f834dfdb0fd4341b5784427836536725ea5881f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67689666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5896d6caf675c48142f8f27411702199cc73b9f1ba2026cbc25ecbf6cc361b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Apr 2025 11:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_VERSION=4.0.8
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Apr 2025 11:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Apr 2025 11:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d174e7cb9aeee95e3f6d1a16883b54f2b2c3a01758251a8f3b67830e863d160a`  
		Last Modified: Wed, 02 Apr 2025 01:05:10 GMT  
		Size: 34.9 MB (34876429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bf4b61f3f0a6cfa05907c859822d7aed7eaa682bf5881a9f7f89b507914649`  
		Last Modified: Wed, 02 Apr 2025 01:05:06 GMT  
		Size: 9.9 MB (9858935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38450cd746523c751db6769bc9d0dfb4f0466bd51db8375b278ca1abcddd481b`  
		Last Modified: Wed, 02 Apr 2025 01:05:05 GMT  
		Size: 1.3 MB (1266438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7370a6afa4f426b3d9a8fd8a5d7b8dc32dd13d80f481942b13cef28193406ee9`  
		Last Modified: Thu, 03 Apr 2025 22:22:28 GMT  
		Size: 18.3 MB (18334676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b96bd073a55d8e56a9c6c2f4d0d4d6f583b9c5b610c0011d6ad07ccfc8aacf1`  
		Last Modified: Thu, 03 Apr 2025 22:22:25 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91a8448d50966228a4dc0dcc139c0d3d46997fc5540b7b70d14021acd02e4fb`  
		Last Modified: Thu, 03 Apr 2025 22:22:25 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc1010639b9d889e4435cf2d30e5f82812956d31adaa7acdd1d0eba479a404c`  
		Last Modified: Thu, 03 Apr 2025 22:22:25 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8569e33273086ebff07745b786ac33bb9af3da0dc8187047c88f2014b2677ce8`  
		Last Modified: Thu, 03 Apr 2025 22:22:26 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f9c92db50228175fb8ce8ba10f79960119b30d3b9ae6d3bfa862cf9f2bf6bda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6809621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4f01f7b913f81cbf2177ac59a3c3b2fba12552cba265970d01d8a63bc83231`

```dockerfile
```

-	Layers:
	-	`sha256:5ea86a568ddc46c6bdf64def5817f3b6bbee450075ca1a649392d1158e85056a`  
		Last Modified: Thu, 03 Apr 2025 22:22:25 GMT  
		Size: 654.2 KB (654192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39f1ab38425a49130db7c333542e4f3a23be87cb92f040a85b3207e96913c3ca`  
		Last Modified: Thu, 03 Apr 2025 22:22:26 GMT  
		Size: 3.1 MB (3124969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d658414021bb40e49641478fde50b1e52c57f841856165147de60c8da00c7726`  
		Last Modified: Thu, 03 Apr 2025 22:22:26 GMT  
		Size: 3.0 MB (2970455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5be4d658687bb82d5487f73be4a837a1451c8f1aa15f0ad62e0782198a382a28`  
		Last Modified: Thu, 03 Apr 2025 22:22:25 GMT  
		Size: 60.0 KB (60005 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:17a6684232d02fcd9459fd384e5d64ffdb7f45b120a9a2133220c02c7c452404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64582332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93273adea68b2236625742ff091022dca34b91ab0c39fe3de33b7af14921e29b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 04 Apr 2025 11:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 04 Apr 2025 11:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 04 Apr 2025 11:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_VERSION=4.0.8
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 04 Apr 2025 11:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 11:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 04 Apr 2025 11:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 04 Apr 2025 11:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 04 Apr 2025 11:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Apr 2025 11:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 11:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 04 Apr 2025 11:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bf66b1363d88a7620717d176ba66d674c65f6270b81b7aebc7907b6836a842`  
		Last Modified: Fri, 04 Apr 2025 17:37:01 GMT  
		Size: 33.9 MB (33943333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843d95895a498cd3885d74586b5fb129c3c8b70d9b7b76fe809e0812527fe3aa`  
		Last Modified: Fri, 04 Apr 2025 17:37:00 GMT  
		Size: 7.5 MB (7510958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8faf0699b7af16f5df4fef4f139869a7abe8e4a5b8c058809ba7005da7f136a`  
		Last Modified: Fri, 04 Apr 2025 17:37:00 GMT  
		Size: 1.3 MB (1324678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1f191c39d2857500a4c79327854673233c314af07860109e91a9e367d579a2`  
		Last Modified: Fri, 04 Apr 2025 17:46:56 GMT  
		Size: 18.3 MB (18334051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4cdb11efa1a7f45b710b7db2de4d4dcc9bf74732ddc50b81768574e5fc7b63`  
		Last Modified: Fri, 04 Apr 2025 17:46:55 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c0db6e6a87adeedefc1bca222664f921f99a49b1eb17cca11ccd2846026590`  
		Last Modified: Fri, 04 Apr 2025 17:46:55 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16df6c9d395c8b6b38c53ca2d13f7adb63987b44cb7a872b9c818d03f33a3536`  
		Last Modified: Fri, 04 Apr 2025 17:46:55 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e25f92e808787485083ef89983f670c8a94363332f8c9f11a65283242f0ea1c`  
		Last Modified: Fri, 04 Apr 2025 17:46:56 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9e213826c02d0b0b4fc8f6ee3034696b96a2d873b1e40991cd859711198db59f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6511391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c446ea0d9b132a8faf29ab39f8250ed7e0a0bf2c834c9c8465aa6db39394c21`

```dockerfile
```

-	Layers:
	-	`sha256:efd46c01eb8d97754871ae1e67018ea12d1786e3bcf0076705d31bff600a21e6`  
		Last Modified: Fri, 04 Apr 2025 17:46:55 GMT  
		Size: 651.4 KB (651372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bddbf14546a58ffc3d8b3e654c660187f19cbb07ae5c9ff23060835a4d63a0bc`  
		Last Modified: Fri, 04 Apr 2025 17:46:55 GMT  
		Size: 3.0 MB (2977291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55bfc11692378a1cb7bf46c8dadc1eb90ef4365bf2c5ae2139f30d27bc3edecf`  
		Last Modified: Fri, 04 Apr 2025 17:46:55 GMT  
		Size: 2.8 MB (2822785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6e924efb917e8b23cdfb1104246338fbc83973a553d61fa578033fae3ac42b3`  
		Last Modified: Fri, 04 Apr 2025 17:46:55 GMT  
		Size: 59.9 KB (59943 bytes)  
		MIME: application/vnd.in-toto+json
