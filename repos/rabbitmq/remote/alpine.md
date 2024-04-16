## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:0cf2beefe9bd6c38adf0a118627aa8fbe201d645778890101a93718b9d7247eb
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
$ docker pull rabbitmq@sha256:0ef7e941411c6a843537a58134986dc5075d994dc499062f69c7f2984bb1e12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73596282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112bccaec3fe9905107a27bcdc897f7ba13d169be89be7b7d5d6828d5da953d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 17:36:45 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 12 Apr 2024 17:36:45 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 12 Apr 2024 17:36:45 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"26.2.4","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@26.2.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_VERSION=3.13.1
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 17:36:45 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.13.1","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.13.1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 12 Apr 2024 17:36:45 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 12 Apr 2024 17:36:45 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 17:36:45 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 12 Apr 2024 17:36:45 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a134be943e929c205b17a14377b8c2374815c5066c0b1341fd24c108c242f366`  
		Last Modified: Mon, 15 Apr 2024 17:56:47 GMT  
		Size: 41.6 MB (41555120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e6d7c26163ff91d00d3be9161141f7cab0ae2309880fd6ad1f073a45f6f1e5`  
		Last Modified: Mon, 15 Apr 2024 17:56:46 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83279fe65181538f7ad4f9f389daeb51d07df7fe6df14aca14ea999eb9915f2b`  
		Last Modified: Mon, 15 Apr 2024 17:56:46 GMT  
		Size: 7.6 MB (7567772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b6603ff894dfff57582a998206322e2fe248e89cc01db350a3225db2ef16dd`  
		Last Modified: Mon, 15 Apr 2024 17:56:46 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3c5d4d157599048b12cc9944d4e1eb903fa28da0c22bf1d20a0e9ee28b66f6`  
		Last Modified: Mon, 15 Apr 2024 17:56:47 GMT  
		Size: 2.4 MB (2405794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7800c58afc314fa9c72dc733ed4c17b549f57eff10edef3f43e9ff7f4d7245b8`  
		Last Modified: Mon, 15 Apr 2024 17:56:48 GMT  
		Size: 18.7 MB (18656339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3acf5ce02b1ba2a644df7b0790377c5aff80c408f0eb1ab0a2cf8ed7e4ac25`  
		Last Modified: Mon, 15 Apr 2024 17:56:48 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4322262e5e578da54798320f854d0cc622bc88610f35caa0306149cec1bf54`  
		Last Modified: Mon, 15 Apr 2024 17:56:49 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a34597f0eb6244c26816b8c444ec0ae522286e51616b4e31ab499a9dfb909c`  
		Last Modified: Mon, 15 Apr 2024 17:56:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6debe1f87983b8ca5a84d74ff96f6571727d1d7182993deaabc3233474452c90`  
		Last Modified: Mon, 15 Apr 2024 17:56:49 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c429bd1dbd4d2560652d16b542f9b1b50434533bae0e7195fa900490708a3216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6540955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33bfa45ecdfb3864ac8d80cc4b2908e0aa597b286b013e0dfd3ccab791d4fc2`

```dockerfile
```

-	Layers:
	-	`sha256:c72a2ab847b91fde64b04222ea82012c2b8ec9ba6ab789e5497ac31bd7468053`  
		Last Modified: Mon, 15 Apr 2024 17:56:46 GMT  
		Size: 908.0 KB (907954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4f85ec1d959ca8fac7a4f93654efb51bf623f8c13d5ebaab9fee97f91f5392`  
		Last Modified: Mon, 15 Apr 2024 17:56:46 GMT  
		Size: 2.8 MB (2782325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc2196a4fcace666dae31fc36625dad0553bc41e62d83b2a5d5d0d818369db1`  
		Last Modified: Mon, 15 Apr 2024 17:56:46 GMT  
		Size: 2.8 MB (2781432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49a8fdc8ec4576a49837a42abf821091d7ee54677e22a406ab909ca1a154c9d9`  
		Last Modified: Mon, 15 Apr 2024 17:56:46 GMT  
		Size: 69.2 KB (69244 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:ae1b30ff915337988e7ca83097bb1c37f8d4fa3ee0fa572822c57c309bac3ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62798672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bdeee6d4f2e730b70e94b84b631b3f4d1fdabf0ee0e30f8c12576d689a3920`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 17:36:45 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 12 Apr 2024 17:36:45 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 12 Apr 2024 17:36:45 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"26.2.4","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@26.2.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_VERSION=3.13.1
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 17:36:45 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.13.1","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.13.1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 12 Apr 2024 17:36:45 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 12 Apr 2024 17:36:45 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 17:36:45 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 12 Apr 2024 17:36:45 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee25eb60ef2614606c505a9396209fc0bb71c683447b3bd2a23044911befe7`  
		Last Modified: Mon, 15 Apr 2024 18:00:29 GMT  
		Size: 33.2 MB (33171827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce7051804ef01413a3d4c49e0c27e089c98de0d678ab2a3391057a8c4a1988e`  
		Last Modified: Mon, 15 Apr 2024 18:00:28 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd6e4d19bb5bf85c058b76236cf8bdccb189d4f433161332a88d2efaa0b26d2`  
		Last Modified: Mon, 15 Apr 2024 18:00:28 GMT  
		Size: 6.4 MB (6400969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638bc7eee998723dfda134181cf5041c9d9f8258693dfd08af80e05d38a6ccb0`  
		Last Modified: Mon, 15 Apr 2024 18:00:27 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622cdba0e289bed32a3d7b42d179bf7ba36b6a488acb8a8e5f86f631420737cf`  
		Last Modified: Mon, 15 Apr 2024 18:00:29 GMT  
		Size: 1.4 MB (1401663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34914cb3fe4a3358d63eabc05aa50cb098390e221c2c41df7f43be6a8ac6cfb`  
		Last Modified: Mon, 15 Apr 2024 18:00:30 GMT  
		Size: 18.7 MB (18656290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fbaab9a7e8dc3c4d88f02d7f657533492abfd487c9a52deeb984ee5527a819`  
		Last Modified: Mon, 15 Apr 2024 18:00:29 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375b19b789f84f8cbf6cb131b2a92f5d1961e6c60d2f5986be0235a1aefbb001`  
		Last Modified: Mon, 15 Apr 2024 18:00:31 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfd2ba1f96413b1c841b602093fb9b398ae9d1bdc01686ed7ec165362fcf478`  
		Last Modified: Mon, 15 Apr 2024 18:00:30 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015397586f464e134139dd0e5187de7f2296206ec6c0be6d013c1cce1031a304`  
		Last Modified: Mon, 15 Apr 2024 18:00:32 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e1182de03d545ad99a34996d319b7f56fe4866b3beba355cb6baedb3c2b11395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 KB (69242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c434fce24e393f2b985d8c2089243e928d182f8a72034b9b2b79f143a73b27`

```dockerfile
```

-	Layers:
	-	`sha256:0bb848d2ace6339ae2671104b01da3dc0377f645d38e4b2c82b8f92ec6466173`  
		Last Modified: Mon, 15 Apr 2024 18:00:27 GMT  
		Size: 69.2 KB (69242 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:ea028431806b3f5f25aede7b9c59107f95da5ee9f6a15c86365720adff23c5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62063040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ce9d4648554e5762f0a89a9889e0bf995498df523989a5e31efc2f883d62d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 17:36:45 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 12 Apr 2024 17:36:45 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 12 Apr 2024 17:36:45 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"26.2.4","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@26.2.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_VERSION=3.13.1
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 17:36:45 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.13.1","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.13.1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 12 Apr 2024 17:36:45 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 12 Apr 2024 17:36:45 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 17:36:45 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 12 Apr 2024 17:36:45 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a390b396cdbdc72047cf022630fba634224f57e54016d8ee6c32559e7aaa875c`  
		Last Modified: Mon, 15 Apr 2024 18:50:23 GMT  
		Size: 33.1 MB (33080425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f06c4170e0dc3f579623fc850a80a7e261811e707fa71b43a753cf2952718dd`  
		Last Modified: Mon, 15 Apr 2024 18:50:22 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806521fe90e6fd8690e11d0161103df0c37348fc05e03657e340d2b0531ac81b`  
		Last Modified: Mon, 15 Apr 2024 18:50:23 GMT  
		Size: 6.1 MB (6099235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e236b06a58568aeaa23d24993b6b32e3664ef4feb6e255c5832402f0f75f140`  
		Last Modified: Mon, 15 Apr 2024 18:50:23 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c141600f8703731adad3473755987843cf589dfd39f287bde3aca80702f68b6`  
		Last Modified: Mon, 15 Apr 2024 18:50:24 GMT  
		Size: 1.3 MB (1305602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f4dae70d4aeeb61410754599c05bd9baa459fe52d8abba2b7544c9bcacbfea`  
		Last Modified: Mon, 15 Apr 2024 18:50:24 GMT  
		Size: 18.7 MB (18656347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852919721fda34d43804e5dd31f392cdab3293aa4dcbf315f0a84c846339547a`  
		Last Modified: Mon, 15 Apr 2024 18:50:24 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a897d4e8b125f707e6d590a2e21767a534bca031e3eaf68bd074317661b64b05`  
		Last Modified: Mon, 15 Apr 2024 18:50:25 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6bffef0dbd9f62f124332084d3b9086696539a83e6aaaa6eec6b56473e001d`  
		Last Modified: Mon, 15 Apr 2024 18:50:25 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b261629ea1ec07d203ee2bef1f207072d67cd75756d0823af137237c313ed57`  
		Last Modified: Mon, 15 Apr 2024 18:50:25 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:855548345f5f0ac2932438c17aa87abb001eace991913a708d27d6c35e19f5e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6333176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed67141e52ecfe5ee9a6ca341335e71f756cabb3d25ee58ce54b26f654ba637`

```dockerfile
```

-	Layers:
	-	`sha256:8c9a419a1dc28c41d7bafeca1d05de249a9e7b690a05a4a96fba20e00158319f`  
		Last Modified: Mon, 15 Apr 2024 18:50:22 GMT  
		Size: 903.7 KB (903720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:866cc9b6344c5da08c9e26158480746a042382368adbaf263ef0544594247305`  
		Last Modified: Mon, 15 Apr 2024 18:50:23 GMT  
		Size: 2.7 MB (2680529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5567267e39e78dca1f84f83290362a5a66c39f7716aa753a44794661b4def14e`  
		Last Modified: Mon, 15 Apr 2024 18:50:23 GMT  
		Size: 2.7 MB (2679636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7d00e9a78ed3ff873dc03ce0346280bf0e7747a9bb1521b04bbc595aed3e766`  
		Last Modified: Mon, 15 Apr 2024 18:50:22 GMT  
		Size: 69.3 KB (69291 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:786237e28a8016f668c4a62d64a9766abaf8640db367532f511a552a851edb46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71360196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d6186f43f56455e85253d19f5248534e4cd7b9bd508521a2137b2241c31a0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 17:36:45 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 12 Apr 2024 17:36:45 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 12 Apr 2024 17:36:45 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"26.2.4","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@26.2.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_VERSION=3.13.1
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 17:36:45 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.13.1","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.13.1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 12 Apr 2024 17:36:45 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 12 Apr 2024 17:36:45 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 17:36:45 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 12 Apr 2024 17:36:45 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab2cbb658b084d94f4391c68f2a075ea64d11f4ba3e52fe1df79b80f921e0d0`  
		Last Modified: Mon, 15 Apr 2024 20:46:49 GMT  
		Size: 39.7 MB (39674340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27a4e3b21045f4cfd68447e23a4099840e61218e6c37e8dda6fb65165878b45`  
		Last Modified: Mon, 15 Apr 2024 20:46:47 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5816e59d80e7877d982034ed7b870e129597c0a9e1bb8ea78f8b6698a1c5938`  
		Last Modified: Mon, 15 Apr 2024 20:46:48 GMT  
		Size: 7.2 MB (7189420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4fa3f5fa8b770298c7e3c86a97e5a76591a41d678cda4c36987b4d0a075695`  
		Last Modified: Mon, 15 Apr 2024 20:46:47 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d213a025e4dccc728b06685a83b72610d5cfe2e3542ef295399ae46215b603`  
		Last Modified: Mon, 15 Apr 2024 20:46:49 GMT  
		Size: 2.5 MB (2489921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea91b44bfcf10e3cfe0db8ddfafe44f37f96942cfe19d41655bccf957b7909f5`  
		Last Modified: Mon, 15 Apr 2024 20:46:49 GMT  
		Size: 18.7 MB (18656272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdd6baac46fdc9b55af9c6c6baa5d20a61804e66c22ec41f3a85a851afd27a0`  
		Last Modified: Mon, 15 Apr 2024 20:46:49 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0d3a40bd848d15303b004bccddc63e457d3d3aee953b1568f6b39458a23a68`  
		Last Modified: Mon, 15 Apr 2024 20:46:50 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f4104bd55c8a14123d192ea8f49497b198684de41a144ff88387c1862733d4`  
		Last Modified: Mon, 15 Apr 2024 20:46:50 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c7e7ad30675e08e3ec37b69b56ee08603dce1378408537401be43cf1452767`  
		Last Modified: Mon, 15 Apr 2024 20:46:51 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:dd1becd744cf796f7a92ae77750cbacd757c0ba333462f827f2fc11c618d1847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6573002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31122c6a4215f0905a607ebc0684723add679a91d548451c46cc96d5d97aff8b`

```dockerfile
```

-	Layers:
	-	`sha256:43a62527cc3fab8b582f3f2db73ecd8e78b8faae1d27edd8d3b06ee1caa3685c`  
		Last Modified: Mon, 15 Apr 2024 20:46:48 GMT  
		Size: 908.0 KB (907965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:565ade561bbf1f2a4ef058d178edf33888231152d618e0b008b34389b3f6b00e`  
		Last Modified: Mon, 15 Apr 2024 20:46:48 GMT  
		Size: 2.8 MB (2798421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c64ed4110efbbdda0f04a121cb593169458fb3df7bc86abd7e5fa06b0ab4c718`  
		Last Modified: Mon, 15 Apr 2024 20:46:48 GMT  
		Size: 2.8 MB (2797528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52d37f65899d415c243544ba4757f8284c17cd212b0b7f08fb26952fb5225dec`  
		Last Modified: Mon, 15 Apr 2024 20:46:47 GMT  
		Size: 69.1 KB (69088 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:85aed915c2d28ca86a049f388d712bcd076dae86eb53c47d31804cd13792a42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64150434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c31766d68e99b10f3b400693fa9dcf8feda901814508ff74d742b51fb2a61d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 17:36:45 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 12 Apr 2024 17:36:45 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 12 Apr 2024 17:36:45 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"26.2.4","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@26.2.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_VERSION=3.13.1
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 17:36:45 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.13.1","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.13.1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 12 Apr 2024 17:36:45 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 12 Apr 2024 17:36:45 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 17:36:45 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 12 Apr 2024 17:36:45 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599e5035fe457fe874d09db9652cf9a35322bf4d731e27d99352d81087cb0ac4`  
		Last Modified: Mon, 15 Apr 2024 17:56:42 GMT  
		Size: 33.3 MB (33349427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979da947ca65b4be5c3cbaee9354d6024c5b552964444cfe218b49fbce234033`  
		Last Modified: Mon, 15 Apr 2024 17:56:40 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38382681835fa3421b16abfeaa2a7848979114bd2a960340f02ab7e3fa6ac719`  
		Last Modified: Mon, 15 Apr 2024 17:56:41 GMT  
		Size: 7.5 MB (7493801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bcc31f5171e03efd74d9891d3ae3589c0bee3e3ac5f4dfbad1150eac557016`  
		Last Modified: Mon, 15 Apr 2024 17:56:41 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e157df081ed434735ded060bc7171771b28f2695be91240f5159ad1b8abdb234`  
		Last Modified: Mon, 15 Apr 2024 17:56:42 GMT  
		Size: 1.4 MB (1404299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e932a0606cca674b21de2e1d8eb4af270723b0c3f3dcac56a3436a8c6d1933d`  
		Last Modified: Mon, 15 Apr 2024 17:56:43 GMT  
		Size: 18.7 MB (18656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7959025aaad05ead007c2a13301a13cbaf938b42f98096a2f521e996bf6bc999`  
		Last Modified: Mon, 15 Apr 2024 17:56:43 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d399d00ba0d5f61116f1c46b76e1aadf466cc47bda6fc0cd27eef1fb96b873a8`  
		Last Modified: Mon, 15 Apr 2024 17:56:43 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d131fceaa153f3a0702aac184e6aa232493b6ece5be838472e10c21295c392af`  
		Last Modified: Mon, 15 Apr 2024 17:56:43 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7ec809ede3469be47066385e333f23dd434426ab7b4393ba9cdc86db27aad9`  
		Last Modified: Mon, 15 Apr 2024 17:56:44 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0ba6ffbfad4fcb5219e2e0be5806b89a4b0eee50473c66a609867169fcdc8c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6517057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06241c06f93597b551f014e548fb0ff2f27ce97b51e78410ce1a89a11c88e4c`

```dockerfile
```

-	Layers:
	-	`sha256:fdfac4fca0da33558dfe85508f317a59545a57e50c0115daaf7a8ae542a30dc1`  
		Last Modified: Mon, 15 Apr 2024 17:56:41 GMT  
		Size: 903.7 KB (903659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1713a6c513612d71a027d8ef1501a6a3aa83dcb4279f00ee55159a53ccefa6b`  
		Last Modified: Mon, 15 Apr 2024 17:56:41 GMT  
		Size: 2.8 MB (2772549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:718bf4f29bd9bfad65f074dd7527af0e74ca974c8ba4c49fa62b7c8e53043f96`  
		Last Modified: Mon, 15 Apr 2024 17:56:41 GMT  
		Size: 2.8 MB (2771656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:176f57af281980025ffe581065ffcaf30d0cf27127e21c4c3656c6c8c0a89f77`  
		Last Modified: Mon, 15 Apr 2024 17:56:41 GMT  
		Size: 69.2 KB (69193 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:b8f9314e3184968f193391ae4964e4c5084e2e017bae6d3098ad77cbf203fd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65121133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f14639bf23a9c75d47b593fe3f905877428ce2513b3b600fcdc1f6b68a18e3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 17:36:45 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 12 Apr 2024 17:36:45 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 12 Apr 2024 17:36:45 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"26.2.4","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@26.2.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_VERSION=3.13.1
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 17:36:45 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.13.1","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.13.1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 12 Apr 2024 17:36:45 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 12 Apr 2024 17:36:45 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 17:36:45 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 12 Apr 2024 17:36:45 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399e568ce2f287eb2a7cea704937bd187bdf2e0daf47dfd6ebb0e9366eeb5b79`  
		Last Modified: Mon, 15 Apr 2024 18:18:13 GMT  
		Size: 33.6 MB (33606433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ec7e157ec9952641a764074b4440fd8da33c5998c648dd413468261a637d22`  
		Last Modified: Mon, 15 Apr 2024 18:18:12 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d339cfad6d9f19d41207976527238dc01af1ed563551141361d7d400770f8a2`  
		Last Modified: Mon, 15 Apr 2024 18:18:13 GMT  
		Size: 8.0 MB (7981813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83da811dffa2ff193fab8f081903930d6f83110096fc2f2be7ae6175a267669d`  
		Last Modified: Mon, 15 Apr 2024 18:18:13 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208ab648a8359a6d35122cbebe0f36b18471ea2d147d9de4b63a0dce82035232`  
		Last Modified: Mon, 15 Apr 2024 18:18:13 GMT  
		Size: 1.5 MB (1515666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571cc64aadf194a587ccf33485986cd1401089172475ab171f913ce0e5d2d6c4`  
		Last Modified: Mon, 15 Apr 2024 18:18:15 GMT  
		Size: 18.7 MB (18656329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a873f456ce08fa132cacdf40c142d8be97c7a54275c3bcf4c02c0e9ffe909a82`  
		Last Modified: Mon, 15 Apr 2024 18:18:15 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6c1b7d745631c62bc3e68bd6723a1bbc99fa55045e7622e3c94e2ba7aa2e13`  
		Last Modified: Mon, 15 Apr 2024 18:18:15 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa16eb4e5b2774dea2e71d3d3e9cb26cb0a37ddc889e854d0e20764b1aa292a6`  
		Last Modified: Mon, 15 Apr 2024 18:18:15 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2d99cdc5b360b32d35c5c64ecb973e2deb8e2ee83717a17f19aa3d519ab6c5`  
		Last Modified: Mon, 15 Apr 2024 18:18:16 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:67c410afae939e186def9d1958da6da8bcb051bdea7e58fd56763e2c276ddcea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6511865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1e8ee11927c78131ed613a31cb49962a97149f19ed9e799040416fd34e06c`

```dockerfile
```

-	Layers:
	-	`sha256:b80e5dfb814156a5d39e8d02d692d4e383625f8f733c75fa0a30cde9d5aa06f7`  
		Last Modified: Mon, 15 Apr 2024 18:18:12 GMT  
		Size: 901.8 KB (901764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6245a425242044cfe35acbe192e6c8e734315dc088155f7e8e7b0c517f54e8d7`  
		Last Modified: Mon, 15 Apr 2024 18:18:13 GMT  
		Size: 2.8 MB (2770928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cae7c0761894a4f822f915c9e2e46523f96bd573d54029cf6ee32f98472a38d`  
		Last Modified: Mon, 15 Apr 2024 18:18:13 GMT  
		Size: 2.8 MB (2770035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc03616b9ba928ebd04f72e896cfbd7c184763fa3fa917c814535abffad5cabb`  
		Last Modified: Mon, 15 Apr 2024 18:18:12 GMT  
		Size: 69.1 KB (69138 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:ae1c398d36c9626e6a80ca572d3ddc9c10d3f116a6a16ec91ccf45894309c546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63785463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a88271f9879f9618c2a681235be7e6445b19b9d5bcfbd81c9d005026f68c923`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 17:36:45 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 12 Apr 2024 17:36:45 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 12 Apr 2024 17:36:45 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"26.2.4","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@26.2.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_VERSION=3.13.1
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 12 Apr 2024 17:36:45 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 17:36:45 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.13.1","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.13.1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 12 Apr 2024 17:36:45 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 12 Apr 2024 17:36:45 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 12 Apr 2024 17:36:45 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Apr 2024 17:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 17:36:45 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 12 Apr 2024 17:36:45 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3283bf1cadfa07a10d4e64994eb1abfdf55feb7bd1f700db745d68415f1bcdd`  
		Last Modified: Tue, 16 Apr 2024 00:09:17 GMT  
		Size: 33.7 MB (33681032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add303bbe24d42b1c1e8396a37e3ca074dcaf9cc34525a5565875f90a56ad163`  
		Last Modified: Tue, 16 Apr 2024 00:09:16 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cd1e3d9c902a08ac8e4f2dfba26fd79f137e0b3fc6a5633e2288a0d34434ce`  
		Last Modified: Tue, 16 Apr 2024 00:09:17 GMT  
		Size: 6.7 MB (6706474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e89df3530c87350efc03e5e6c64b5d7e2be6ab7ca2464c25fbc0a85e71cb23`  
		Last Modified: Tue, 16 Apr 2024 00:09:16 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa0b835de7fe4be7d88ccf17bd657772d4f3be396100f33a15958f5af2bd08`  
		Last Modified: Tue, 16 Apr 2024 00:09:17 GMT  
		Size: 1.5 MB (1496493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa98734cb1dc1a4a405b4b52e216b337d2502dd2ffd41150884c47b4dda01bac`  
		Last Modified: Tue, 16 Apr 2024 00:09:18 GMT  
		Size: 18.7 MB (18656307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f84fc420e096438872dd5b3f2f38f64d5d430363c86603fa3f23d0d8165187`  
		Last Modified: Tue, 16 Apr 2024 00:09:18 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3028af6f489586a2c45ab083e6470c23ff5a0692170de6ea95f76f46a66f760c`  
		Last Modified: Tue, 16 Apr 2024 00:09:18 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7af28edcbc83393c6532d904abe1022d93a81b907e5cadd2fd01b426b1265c`  
		Last Modified: Tue, 16 Apr 2024 00:09:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5538e61140a567e4e4c83916c501ca345aab4c8c3c80a3675ff4b53290734dce`  
		Last Modified: Tue, 16 Apr 2024 00:09:19 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cb51aec9c5b4c940bb3b2b50a0273c749deccf6925bd9301adfcb28e62482c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6345949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3484b0916c11f1e2e6896a5342748f08fef42477edfcca182b757d7aa0eb4fac`

```dockerfile
```

-	Layers:
	-	`sha256:d22e9f2f87d5a9b430195898105a78482c5d0a5514119ec11118530ffade4201`  
		Last Modified: Tue, 16 Apr 2024 00:09:16 GMT  
		Size: 901.7 KB (901730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e68d0fb6048452f090758102b2990b60b24b10872ade8205170e6690bc87d5d`  
		Last Modified: Tue, 16 Apr 2024 00:09:16 GMT  
		Size: 2.7 MB (2688017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:935620d872eab5694bef8b3d3f455048e0c933ca2dbad99b2e300ec9851088d5`  
		Last Modified: Tue, 16 Apr 2024 00:09:16 GMT  
		Size: 2.7 MB (2687124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e96187f5cde03496b26aaf9ef656159928750c0fa39b91fb9238a8979d1ca8`  
		Last Modified: Tue, 16 Apr 2024 00:09:16 GMT  
		Size: 69.1 KB (69078 bytes)  
		MIME: application/vnd.in-toto+json
