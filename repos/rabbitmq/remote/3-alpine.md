## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:9d2e3d1dbbdf2a78f731217bd5088ae2e6a8d41de332f62dd246856d95adff3c
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

### `rabbitmq:3-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:002df5ea94173888b1094a9a723a8a090bd78897c561335442b3af4c2dfa4167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71030277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb18c652f6987c8b0e2517da798373cb61d73c7c2e1b74bd8622e9899c4d61da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 09 Feb 2024 12:44:02 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 09 Feb 2024 12:44:02 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 09 Feb 2024 12:44:02 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.9","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.9?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 12:44:02 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 09 Feb 2024 12:44:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 09 Feb 2024 12:44:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 09 Feb 2024 12:44:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 09 Feb 2024 12:44:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 12:44:02 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 09 Feb 2024 12:44:02 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 09 Feb 2024 12:44:02 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 09 Feb 2024 12:44:02 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Feb 2024 12:44:02 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 09 Feb 2024 12:44:02 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c2471e94ed109ea1254f31becf4ebca62a2de6f12d2b095a6a1862058f6abb`  
		Last Modified: Mon, 12 Feb 2024 22:02:22 GMT  
		Size: 39.9 MB (39898376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0100967e995e1ce792e082670ae187f784845e91e80314c6a0fd7f10a6b7407f`  
		Last Modified: Mon, 12 Feb 2024 22:02:22 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49815d6ccbdabb69ca8e5951e32f87eecc3b7f6fa3c5520a2fd5f4a6754a9728`  
		Last Modified: Mon, 12 Feb 2024 22:02:22 GMT  
		Size: 7.6 MB (7567762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602301217ed0910f78854e9abfbf8d759b884f65bafa8a529472bf534f562ac2`  
		Last Modified: Mon, 12 Feb 2024 22:02:22 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53e7e13d5e3d48f9a67dc2e7debb15f86944958c6333ed482c4247a314ff073`  
		Last Modified: Mon, 12 Feb 2024 22:02:23 GMT  
		Size: 2.4 MB (2405779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2a10f37ce93c426212042ae73de7fb423e78df21daaafcb77e4f9422edc3bc`  
		Last Modified: Mon, 12 Feb 2024 22:02:23 GMT  
		Size: 17.7 MB (17747107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9094bb2b6137a8ab3c238a6629db4aa16d414d297deda43c0e9849dc358704`  
		Last Modified: Mon, 12 Feb 2024 22:02:23 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bd06c4e0f7a585c5d7aaa0be12244d6e8bc3a1bdbe82a977b0bc390dbe29dd`  
		Last Modified: Mon, 12 Feb 2024 22:02:24 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58d99af7a0b732c2237113efb9239470c5febf32a5fb2f0a04e049a84af0324`  
		Last Modified: Mon, 12 Feb 2024 22:02:24 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b6ba7eb16c9963fda325f6bfaba2711324ea347974cab2f7060bde855e4147`  
		Last Modified: Mon, 12 Feb 2024 22:02:24 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2fb01cd4254a7595b379c14b66850bcdced1b287dcb4b2f49268faed1cf97208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5442980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6b4e6f3bdf8640ad9b2584e7970662bac0875e5e908f8d5c40dc3111c8df34`

```dockerfile
```

-	Layers:
	-	`sha256:f7dd3015a5cd482b80aeefecc967e56b02cdc6600275231b0c269decde342787`  
		Last Modified: Mon, 12 Feb 2024 22:02:22 GMT  
		Size: 759.6 KB (759580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d980cfb796dc1e0369669865cb8292c88f7655531e35fa5cb71788bc1da7942f`  
		Last Modified: Mon, 12 Feb 2024 22:02:22 GMT  
		Size: 2.3 MB (2317109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fc049750f50e857270ab443bcf629118e6b1f7629c796591f2c49de27cdb6b`  
		Last Modified: Mon, 12 Feb 2024 22:02:22 GMT  
		Size: 2.3 MB (2297014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53687b4de405d6911fe4917f10ae1bfa5ed6fae575c76ed90cc17d82693728e3`  
		Last Modified: Mon, 12 Feb 2024 22:02:23 GMT  
		Size: 69.3 KB (69277 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:9ffd9bd7c4e3f654fe423f519c3b5c9fc48a28ff3d280d352a6cb3b9dfc43fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61144068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0db2f6b526e163bacdbef1b73c74682c40821a1f373c8d1a285f74b8d96e12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 09 Feb 2024 12:44:02 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 09 Feb 2024 12:44:02 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 09 Feb 2024 12:44:02 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.9","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.9?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 12:44:02 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 09 Feb 2024 12:44:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 09 Feb 2024 12:44:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 09 Feb 2024 12:44:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 09 Feb 2024 12:44:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 12:44:02 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 09 Feb 2024 12:44:02 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 09 Feb 2024 12:44:02 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 09 Feb 2024 12:44:02 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Feb 2024 12:44:02 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 09 Feb 2024 12:44:02 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5236ecdc3cf3c1e84010e8a18851d1d83dcc0682de0f7a7f359bd8d795d3b06f`  
		Last Modified: Mon, 12 Feb 2024 22:57:02 GMT  
		Size: 32.4 MB (32426587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d894f266f0aed331949a423c044d293d4011641630ab985926c966319ef30980`  
		Last Modified: Mon, 12 Feb 2024 22:57:01 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e1d99620a82a85fa84c9cadf01fa9a38753a683febe635a82cfddca47455f6`  
		Last Modified: Mon, 12 Feb 2024 22:57:02 GMT  
		Size: 6.4 MB (6401001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d410515455f1c02bb27c272452e5600c6a5de3d7d260ff7bd1b13a7b1a80e1d`  
		Last Modified: Mon, 12 Feb 2024 22:57:01 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48704108d9fd221d62d9ef92810f1dce58e90f69d6443b12b0911957c2235ec5`  
		Last Modified: Mon, 12 Feb 2024 22:57:03 GMT  
		Size: 1.4 MB (1401629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffc0fc7c10821ac44fb759542183ddd1f38d54af30804c4f7a01ae20d62dee3`  
		Last Modified: Mon, 12 Feb 2024 22:57:04 GMT  
		Size: 17.7 MB (17746930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbedeb1d9e6b0cc9394c5888155be6cd79cc67a2f7fe8a582108fe48215f1ac`  
		Last Modified: Mon, 12 Feb 2024 22:57:03 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09761c924a7851ec6f25619475c9a3b9a3e40aec567fb3e24b13d03f1541b4c`  
		Last Modified: Mon, 12 Feb 2024 22:57:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a11d8a7eaf1546e909c6f895232ee685ac78a3831cf0fe04a137de1c79d6fc`  
		Last Modified: Mon, 12 Feb 2024 22:57:04 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac3f6ab3481ad1447ed77aa6c4486160f8c28fced227ed756d3589dab2edf2e`  
		Last Modified: Mon, 12 Feb 2024 22:57:04 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cbc9be2d3a724b59f65636033d933daca3318c94153989faf61581efb4392fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 KB (69275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b6b802175ef2f77533bea409f03debdaf23cc44ae03c96ee3f893e9396809e`

```dockerfile
```

-	Layers:
	-	`sha256:1fe586f714f86be1f8e86c1c0db4369ac87677fd0597c03bf2b2cdd0103eb3e2`  
		Last Modified: Mon, 12 Feb 2024 22:57:01 GMT  
		Size: 69.3 KB (69275 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:72832fb9b3afaea025ed462bfbc906f7bdd0b33d1ea56fb043ac8f3c09be067f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60412576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736bdbb80d397540f086952d87dc1fdf8dafa53a5e4b24749919ee62982f9b77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 30 Jan 2024 18:57:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_VERSION=3.12.12
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jan 2024 18:57:54 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 30 Jan 2024 18:57:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9225f595343f45321f44479c7a9258eff26ac101b1f86d95539c9b7d38487f8`  
		Last Modified: Fri, 02 Feb 2024 09:49:09 GMT  
		Size: 32.3 MB (32336933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb964044625e07a36d0318501ca2d523e34167d2e868ec844a29b657cc03a201`  
		Last Modified: Fri, 02 Feb 2024 09:49:08 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98f7544180859eb674fdf173f5d8053feb57f0e022b40c7aaa914d00bff0301`  
		Last Modified: Fri, 02 Feb 2024 09:49:09 GMT  
		Size: 6.1 MB (6099273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739914bff9996a07fc73d2f578fb6e805759c8f66d69d89fb3f9f0e6c677414a`  
		Last Modified: Fri, 02 Feb 2024 09:49:09 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6729d20e3046f92f64c303f5bd4013b8cc80359cefb869ed1c9733afae1a11f3`  
		Last Modified: Fri, 02 Feb 2024 09:49:09 GMT  
		Size: 1.3 MB (1308048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e85f1325a4f68bc58c0e5b56208dc759ec62b9d93f36f27cf6806aaf3c2f3e9`  
		Last Modified: Fri, 02 Feb 2024 09:49:10 GMT  
		Size: 17.7 MB (17746892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3978f17b7644190d01adb433c802827486613fe34b30564d7111aa4b99ed4b`  
		Last Modified: Fri, 02 Feb 2024 09:49:10 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b00fb46432f1d1e1ef9203da6b407640a87bbf42dbc4669f0778154de9bb7`  
		Last Modified: Fri, 02 Feb 2024 09:49:11 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0b86c77458cba042e3fd41bf5146459e312230ed952eeee3e2ed6faf6432bb`  
		Last Modified: Fri, 02 Feb 2024 09:49:11 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b846637d29d7c8663f65f975c5df5ee87d910772c49d91703a1125704030a2`  
		Last Modified: Fri, 02 Feb 2024 09:49:11 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0232ee7fa23e44315c6f7241c9827440a63c98b09b98c32d6519163ec6f17474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261b056694b8a22b769aabd2407b9a26cbee7c57a5fa3814cd01c4f4f8fef782`

```dockerfile
```

-	Layers:
	-	`sha256:9ee369bf8b40437a24841c2cd58f39f9bc3338773e46e8db5cb4eb9606e4b4fa`  
		Last Modified: Fri, 02 Feb 2024 09:49:09 GMT  
		Size: 757.7 KB (757660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b92f05b4b1091faf82b76dbfd476d42e60e709dfda024dfaabe22ef44f46a10b`  
		Last Modified: Fri, 02 Feb 2024 09:49:08 GMT  
		Size: 2.2 MB (2216460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ad9f30dafdda0a5073d487de92c84580f986e0851703b7b9b8f204959282ffb`  
		Last Modified: Fri, 02 Feb 2024 09:49:08 GMT  
		Size: 2.2 MB (2215570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:254f9853c5c14fd9928c84aea4eedbb8b936973d933a39f94022e91c4ea302f1`  
		Last Modified: Fri, 02 Feb 2024 09:49:08 GMT  
		Size: 69.5 KB (69490 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:2f9fcd514c95d3fb0c104eb4f9efb45b7fc9c302ea371a57fab53e8d6c6d6249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68691604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eeb081a48951536cc398a2b4bbec5e3c62f3e373f17ae05a2bdc296039084bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 30 Jan 2024 18:57:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_VERSION=3.12.12
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jan 2024 18:57:54 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 30 Jan 2024 18:57:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4fe0abe408e1518f9d5b17c3282b529a5b5ea981f2d8caa3a241204af6ada1`  
		Last Modified: Fri, 02 Feb 2024 18:25:29 GMT  
		Size: 37.9 MB (37914672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfae2bd54586df2e84e8a2cabe7b8e4dbf5d56771da6b185ca1de4795460b785`  
		Last Modified: Fri, 02 Feb 2024 18:25:28 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931b6347a3feb55b3e86c48d91f9615d3363a8e4b1affb0288e16dbf60a7bedc`  
		Last Modified: Fri, 02 Feb 2024 18:25:28 GMT  
		Size: 7.2 MB (7189426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4251bd180856830ac9aca33b1d5c2af63839637ff081ebfb94d3d0b88da7b191`  
		Last Modified: Fri, 02 Feb 2024 18:25:28 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eddc4aa204eee2adbabd308a49377fbfd78ed341a8002071cc8c3aa9d9c8e65`  
		Last Modified: Fri, 02 Feb 2024 18:25:29 GMT  
		Size: 2.5 MB (2489853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7d1598a3044dea21013914315fbba79a4e3b53d7690bf82a0a38f9f8690273`  
		Last Modified: Fri, 02 Feb 2024 18:25:30 GMT  
		Size: 17.7 MB (17747412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0988a9ba40162cf895f49fe14834dfe4734e70f486202f2ebec6982fd5e4c783`  
		Last Modified: Fri, 02 Feb 2024 18:25:30 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5451a31bb41ad7aab56109cf87a2120ba12ed8ae271ed0563c37936b859eb60d`  
		Last Modified: Fri, 02 Feb 2024 18:25:30 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f967db87b3560b8cdf30f3b3602840ec03fb5616a606394cae281730397f8bf`  
		Last Modified: Fri, 02 Feb 2024 18:25:31 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11d8755d99afa392c03184118d9ccd54061c848d3fa4cdd29e68ada2d503bbf`  
		Last Modified: Fri, 02 Feb 2024 18:25:31 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b6cadc747db97df29a8fba4800d5cc61634721bfc8d6a4ba8211769b04d5ffd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5452790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd6246f12fa9a754c45024fbe1a1cf5a07a9fd70426b7d2d7d859714aa217dd`

```dockerfile
```

-	Layers:
	-	`sha256:c54ec8c4853f06eb33ce3ad28dd065a90c15a7c64cbab7137f1d0f1f11099e06`  
		Last Modified: Fri, 02 Feb 2024 18:25:28 GMT  
		Size: 761.7 KB (761693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4faa20ec72e22b86379d9a9d28660571081c68bd8518942cb67d0ebf742f3bfe`  
		Last Modified: Fri, 02 Feb 2024 18:25:28 GMT  
		Size: 2.3 MB (2311350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80127f4072fe5454af3895b0ccca2cbfefb53b9494093cf5150d2c8aa63435b9`  
		Last Modified: Fri, 02 Feb 2024 18:25:28 GMT  
		Size: 2.3 MB (2310460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f2abaff7cd2eec8a009319800c29a22254947b1b9d2a0052d1b4dd31b180be`  
		Last Modified: Fri, 02 Feb 2024 18:25:28 GMT  
		Size: 69.3 KB (69287 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:8a7c96556aaf108e0139966712444c16a466ee41fa3e98a372dc657a8b69f769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62509617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9dd157d2646503cca75cce0c619e784ddd5c949e1d3d85b28f5f5761335f35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Fri, 09 Feb 2024 12:44:02 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 09 Feb 2024 12:44:02 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 09 Feb 2024 12:44:02 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.9","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.9?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 12:44:02 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 09 Feb 2024 12:44:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 09 Feb 2024 12:44:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 09 Feb 2024 12:44:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 09 Feb 2024 12:44:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 12:44:02 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 09 Feb 2024 12:44:02 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 09 Feb 2024 12:44:02 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 09 Feb 2024 12:44:02 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Feb 2024 12:44:02 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 09 Feb 2024 12:44:02 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cf477ee8f96f9ef747b955bb7d5c1018397659909c2261c28cb13fcadac6fe`  
		Last Modified: Mon, 12 Feb 2024 22:02:12 GMT  
		Size: 32.6 MB (32618049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece1c6c58058cd01ca8f6a604bfa1e7d6eede5e0d2e5e53d442402d2ecfec6da`  
		Last Modified: Mon, 12 Feb 2024 22:02:10 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf5f63e3acb158c8f71e3db6859f2d6490a8321de8d089058abb1c343dd7eea`  
		Last Modified: Mon, 12 Feb 2024 22:02:10 GMT  
		Size: 7.5 MB (7493837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cea92afe3819f401ed367832cf18a065cd71a22c8b07a92c167174157545ab`  
		Last Modified: Mon, 12 Feb 2024 22:02:10 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58e04f02572fe07ba25c5a7fa02b943f49c9cc722248d66b708cd46c072b368`  
		Last Modified: Mon, 12 Feb 2024 22:02:11 GMT  
		Size: 1.4 MB (1404283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89dce5c86faa418c5b2ed3939b0c7d60314af727e83be017cdb06f49383d4a8`  
		Last Modified: Mon, 12 Feb 2024 22:02:12 GMT  
		Size: 17.7 MB (17746834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8850bc0c867e1a67df61ed3a57f1ba6fb0b9eba9f7778730d6f8bc9df04059ef`  
		Last Modified: Mon, 12 Feb 2024 22:02:11 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891f5c7a085a9578e567f58bfeee6a9c6ba5b29716f963eced7292263fb5890e`  
		Last Modified: Mon, 12 Feb 2024 22:02:12 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9984f11d904333adaba2134aee6e087ca68a6b38171bf62a55184c107e0456c9`  
		Last Modified: Mon, 12 Feb 2024 22:02:12 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb73f3869234faefd39a91aeeaad15c8c1ab823cce6366986be3e4ba9129e739`  
		Last Modified: Mon, 12 Feb 2024 22:02:13 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:216bdcb576408de43dc2108b445f191d90431b1fa650c62f2c880d2e248facae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2307ff14650f110991a1f50ea93a68c1b80bffb9600d1a544a957b81f020da2c`

```dockerfile
```

-	Layers:
	-	`sha256:805f244e78118460323b7df7ddb9269211745abbb218976effba03a3e1699106`  
		Last Modified: Mon, 12 Feb 2024 22:02:10 GMT  
		Size: 755.5 KB (755497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7970b18bd145349ff8a9fff3edfd1d4322cc7d902a6e1ce3e3777343cca2028d`  
		Last Modified: Mon, 12 Feb 2024 22:02:10 GMT  
		Size: 2.3 MB (2308921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c75310bb6f8382c803d1e33bf5fe8004cbf93683bb385343d7116a3b089df0`  
		Last Modified: Mon, 12 Feb 2024 22:02:10 GMT  
		Size: 2.3 MB (2288828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18411d88080c8d4b4c532507eae53cb31d794d097128818592cec6a0e99dfc70`  
		Last Modified: Mon, 12 Feb 2024 22:02:10 GMT  
		Size: 69.2 KB (69226 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:8458b0ce82917d272cec994e104feb45a130f23a1396b33d23409c06a987a3f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63440317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c030639891596854527480e8404c6dd06178a56ad90c482b90287864b2759d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 09 Feb 2024 12:44:02 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 09 Feb 2024 12:44:02 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 09 Feb 2024 12:44:02 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.9","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.9?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 12:44:02 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 09 Feb 2024 12:44:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 09 Feb 2024 12:44:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 09 Feb 2024 12:44:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 09 Feb 2024 12:44:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 12:44:02 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 09 Feb 2024 12:44:02 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 09 Feb 2024 12:44:02 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 09 Feb 2024 12:44:02 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Feb 2024 12:44:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Feb 2024 12:44:02 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 09 Feb 2024 12:44:02 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e335159a2276c9988becfbb6423cca08a510777a9fdaf599fb74623ba62b02d`  
		Last Modified: Tue, 13 Feb 2024 08:07:21 GMT  
		Size: 32.8 MB (32835138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3909baa213f0def285710349e930e5e888712a2520a0765a31fa371788458891`  
		Last Modified: Tue, 13 Feb 2024 08:07:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81146222aed182c9abf62bd96425449ca51fee42cc5cccc745152f5968736a49`  
		Last Modified: Tue, 13 Feb 2024 08:07:20 GMT  
		Size: 8.0 MB (7981827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09823f3a1947e24eac88ca95a23f49be8cfb51b805873a64db2a2aaa08cf0447`  
		Last Modified: Tue, 13 Feb 2024 08:07:20 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f227839ee93824d2060bbaec0e478eb1e8d4ab47fab3d45a6c234fe88b53afeb`  
		Last Modified: Tue, 13 Feb 2024 08:07:21 GMT  
		Size: 1.5 MB (1515629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7d3c56a01f2e5f1ff600df50b8520daf1deda126b45e0dad5c0ad160f20b44`  
		Last Modified: Tue, 13 Feb 2024 08:07:22 GMT  
		Size: 17.7 MB (17746828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c298ad13c3244b8585be89fab0d84f2f91ffc63b59cc31e2cee34677accaa3`  
		Last Modified: Tue, 13 Feb 2024 08:07:22 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2fffa37494e2f2dac75c055210c8ff407e3194bf40e012147fff42f48d4889`  
		Last Modified: Tue, 13 Feb 2024 08:07:22 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d883c3ec5df93024bbfc799229b4742412225ffa5bfbde06b976d990d7326fa`  
		Last Modified: Tue, 13 Feb 2024 08:07:22 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72adcf07065e279baec1f5f0a81b6dc7bcc5a5925ba39e8e810eb71c6e08c06`  
		Last Modified: Tue, 13 Feb 2024 08:07:24 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:60e970d963e76cd69e3f46c359b6010f0b0a0d337e5decdffa24bffff88b9ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5420320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5054860ea3efbcfa66435e93a2a65c053d4e892228b6c8779912bacb6885827a`

```dockerfile
```

-	Layers:
	-	`sha256:83d7e6fec63e44fc8e011ca8386ee8cfb85c8df88b653a2e2aeb047a22c9c8f4`  
		Last Modified: Tue, 13 Feb 2024 08:07:20 GMT  
		Size: 753.9 KB (753920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501ec5b2ca617b4bf89b8f31228ea7d76cb804df236e7c552eb3c1cf5729b877`  
		Last Modified: Tue, 13 Feb 2024 08:07:20 GMT  
		Size: 2.3 MB (2308584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d727d075c756303b9b2c5bcb4a9ee7c00e59bed06de64292dec5bd0ea4569ff3`  
		Last Modified: Tue, 13 Feb 2024 08:07:20 GMT  
		Size: 2.3 MB (2288479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2b5ddaafbf4aff90f209791cb4ac554bc40cf8a42776ee50ae4102930a8361e`  
		Last Modified: Tue, 13 Feb 2024 08:07:19 GMT  
		Size: 69.3 KB (69337 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:b50681393dbe8550f7b4a380a2b05246954f884b21ab990ec9a4c3a81dd2e7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62114545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbb2d5bb76315953b7d144489838321f59afe237d1cfadf22b4fc4534c11e11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 30 Jan 2024 18:57:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_VERSION=3.12.12
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jan 2024 18:57:54 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 30 Jan 2024 18:57:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06be0986b9eff9752f3a48c70bc07192c641e4fcf044c57c9de523eebadb6448`  
		Last Modified: Wed, 07 Feb 2024 11:28:59 GMT  
		Size: 32.9 MB (32919513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd79b5fed8f15a36a4d97e5e665a55c7466a3170f82f84d36898adbc32f948d`  
		Last Modified: Wed, 07 Feb 2024 11:28:58 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a23574c1e33b866e62cf72c75d67d77508ea79d8b0c4985c7c07ac70902826a`  
		Last Modified: Wed, 07 Feb 2024 11:28:58 GMT  
		Size: 6.7 MB (6706485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7e07eaa653101a74b6bd754af40c554a651088fe1f0783a9f74838516a5fb7`  
		Last Modified: Wed, 07 Feb 2024 11:28:58 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763267c447434fbd06f6b5b1d91887da61eab71bbe5992bf46bc9fbb4cb4752d`  
		Last Modified: Wed, 07 Feb 2024 11:28:59 GMT  
		Size: 1.5 MB (1496465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4c542daa7805d3162b90f1a9b4ee4b89bcd78db065652f1ea86e65aee385bb`  
		Last Modified: Wed, 07 Feb 2024 11:28:59 GMT  
		Size: 17.7 MB (17746915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7793ed18cc9d754a27d4774a83c0a8fd37142e107e8857dde50db4dd003b139f`  
		Last Modified: Wed, 07 Feb 2024 11:28:59 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2c0d2a1f1151a7272842bd2b29d900057ab128f21a0d5639675a3696f96046`  
		Last Modified: Wed, 07 Feb 2024 11:28:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909b94a45a92e983285ffdb4ace51fe8d0b74200036362314cb109b0e874fe4b`  
		Last Modified: Wed, 07 Feb 2024 11:29:00 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3a50bf70071a86bf571c19069f77acdf73c91edf15c15b5b31719ac729c838`  
		Last Modified: Wed, 07 Feb 2024 11:29:00 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:536e86758c7e2269a3cfbd11c79c036789a2d8ed3ed27e474871ce067270ac65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5284286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae39da84c9d036fe133f30d970e807d66c96b9ff9db10dc29280b45a26ac7aea`

```dockerfile
```

-	Layers:
	-	`sha256:5c00820f35b3ff4c278326c56a4e60e59ebde2ccd63b7a2c1497e6e1fdded1dd`  
		Last Modified: Wed, 07 Feb 2024 11:28:58 GMT  
		Size: 753.9 KB (753886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601512f694fec1184f9ad133a686b8470a6db227d04a8bc74d97e01f0bacccc1`  
		Last Modified: Wed, 07 Feb 2024 11:28:58 GMT  
		Size: 2.2 MB (2240609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a39d3d13404cfa00e2eb37b745bf42835570a32188768780d0a66e418d93d271`  
		Last Modified: Wed, 07 Feb 2024 11:28:58 GMT  
		Size: 2.2 MB (2220514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c5f275dbe30d7a58714ce87619efa112e67c3837e549b9f4ee9f0142e2799ef`  
		Last Modified: Wed, 07 Feb 2024 11:28:58 GMT  
		Size: 69.3 KB (69277 bytes)  
		MIME: application/vnd.in-toto+json
