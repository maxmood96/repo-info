## `rabbitmq:management-alpine`

```console
$ docker pull rabbitmq@sha256:f3e570e2dfb9b33d9fd78319c025beab502248df61ae3b15361429d2acaf3506
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

### `rabbitmq:management-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:5a363267eb38f268bc5c03a33fbc4fffdcbb1bfa279a0b0e16cce853f4734c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86285922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afe0f92dbaa99500f8fa3c902ff936fd328a27a5bb4ba685c1232e2d502d441`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 02 Jun 2023 21:59:28 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Fri, 02 Jun 2023 21:59:28 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 21:59:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 02 Jun 2023 21:59:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 02 Jun 2023 21:59:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 02 Jun 2023 21:59:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 02 Jun 2023 21:59:28 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 21:59:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 02 Jun 2023 21:59:28 GMT
CMD ["rabbitmq-server"]
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3fddea8cbf8d0039ec2b7ea577a3f845c95c936b6abebd3e13453488a9f6d8`  
		Last Modified: Thu, 01 Feb 2024 19:04:25 GMT  
		Size: 39.9 MB (39897481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87904c1c30f73828f44552e5e853914eecae59ed2b5f85f718b1aba1c7f1146e`  
		Last Modified: Thu, 01 Feb 2024 19:04:25 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856916e86e80c3a80455b51f68a09579099ac1e1dd21bb2154074075b81dc41`  
		Last Modified: Thu, 01 Feb 2024 19:04:25 GMT  
		Size: 7.6 MB (7567780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d9d4619e5314a56fce3d850d3c47a7451c0f781652d7ad0a6e268bbc9e75cd`  
		Last Modified: Thu, 01 Feb 2024 19:04:25 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c278258231657a965a66098523956cb8942c2320cec113319ae19f1ff9de35fe`  
		Last Modified: Thu, 01 Feb 2024 19:04:26 GMT  
		Size: 2.4 MB (2407915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093b0a1a17d7bb000107b414059b248366079c11394da24a51d79f4f86c225b4`  
		Last Modified: Thu, 01 Feb 2024 19:04:26 GMT  
		Size: 17.7 MB (17747240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a8d7c9658d666c0728e596ca45a6d41953399a4b21300ea5e222dc8eeefeb`  
		Last Modified: Thu, 01 Feb 2024 19:04:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986c4207d6db97b12c81ce7125c94181bb106a0228ecf7c0ad328114efa5b86f`  
		Last Modified: Thu, 01 Feb 2024 19:04:27 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf42a611102787f0ac7a1354926d0fa46025953b44190f17f4f22edc15f87d83`  
		Last Modified: Thu, 01 Feb 2024 19:04:27 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028c0985fff990d37d8b37f79beed749355cadee4542fdce40fea12c508f642a`  
		Last Modified: Thu, 01 Feb 2024 19:04:27 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631d1d716549e7bbf4c767dccaebed5a86aad72539e6ccfcf6151564b744f3e9`  
		Last Modified: Thu, 01 Feb 2024 19:57:01 GMT  
		Size: 15.3 MB (15254251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7ac3494d21f2f55e67d448f762fa7f46e8ca94ef3154ec8c2670885d31b08ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1666528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09743ec64043e10ef9e1ce81d7a4aacf0b53f759972731674d0d757510a916a9`

```dockerfile
```

-	Layers:
	-	`sha256:61dd19656d15172cbed2ba71c00ab4d50c58bc61827673d8e991eb6e9aecdc34`  
		Last Modified: Thu, 01 Feb 2024 19:57:00 GMT  
		Size: 1.7 MB (1653048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a67c4e98c411773666fb7b981e47ddf6d40834b566709debaaf943873202efeb`  
		Last Modified: Thu, 01 Feb 2024 19:57:00 GMT  
		Size: 13.5 KB (13480 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:7b3f604b122b619bbf79bfa1738b84fcdaa257ed946fc9eea8c939167589753c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77074713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d80927f9b7e55d76632823de87957ebec030691e1eb11b094e56221cf40d658`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 02 Jun 2023 21:59:28 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 02 Jun 2023 21:59:28 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 21:59:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 02 Jun 2023 21:59:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 02 Jun 2023 21:59:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 02 Jun 2023 21:59:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 02 Jun 2023 21:59:28 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 21:59:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 02 Jun 2023 21:59:28 GMT
CMD ["rabbitmq-server"]
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff26be4bf0ae00cae062d3c1e5ccc8e94e0acdaae952ee10863cfe699c2cfcf`  
		Last Modified: Thu, 01 Feb 2024 19:18:28 GMT  
		Size: 32.4 MB (32427017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d45b266fffa28354a7eafd941613665fad6b110e731276b7c4a0406279a7e78`  
		Last Modified: Thu, 01 Feb 2024 19:18:27 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb727a49f515121ddd9f0fa5ff2964cc5763ff04e08d507952ecf45e86951349`  
		Last Modified: Thu, 01 Feb 2024 19:18:28 GMT  
		Size: 6.4 MB (6400965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540a650fe488a617c865f8a0cd1b5edb5a970113a36db6d33a0caad7ca191a74`  
		Last Modified: Thu, 01 Feb 2024 19:18:27 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec7d8c72ad88109f038a6d66da573e1fde1d66ddb5d179ba7d86220278df0db`  
		Last Modified: Thu, 01 Feb 2024 19:18:28 GMT  
		Size: 1.4 MB (1403703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f55e7658aef99011d22d95f4853073b5a1cf68a4a289462667e501dc0c7cd8a`  
		Last Modified: Thu, 01 Feb 2024 19:18:30 GMT  
		Size: 17.7 MB (17747124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b993db0e550f9204dbaab7df6df77a166030cdcc09bbe56d3764714be9cb28`  
		Last Modified: Thu, 01 Feb 2024 19:18:29 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe7d926f8463ad6e64ea5204a7e3df0da3fac59a8f93a4af6fa06c1936d0d61`  
		Last Modified: Thu, 01 Feb 2024 19:18:30 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349701b6a216466b474d9a95ae560264dffe6853e322653445c3d5cc984f5cce`  
		Last Modified: Thu, 01 Feb 2024 19:18:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681e56aa533feb696611ae5b527f3e0cbd7b190fb7c8e351b5dce942abe25234`  
		Last Modified: Thu, 01 Feb 2024 19:18:30 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b75414a7c9f138d3efad3b29320e3ee7a98104da24036635a3f35e03e6d9de`  
		Last Modified: Thu, 01 Feb 2024 20:12:24 GMT  
		Size: 15.9 MB (15927982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:52b5ada055210dd917ccea466386105f507b7bd862ee1df9731faddc03da7050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9f41c0f15bc8fada1a601f3219e30b8ac085f3e9caeb57c8d01e4e750331c7`

```dockerfile
```

-	Layers:
	-	`sha256:3d943352035e5397dcca4db68b41b01486fb33ec5096b2b2d2a871abb92ae921`  
		Last Modified: Thu, 01 Feb 2024 20:12:22 GMT  
		Size: 13.4 KB (13359 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:4893a3adea29b0171028f6acf83fa5d638113bd28abc089f7a05e5fd89c3b719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75980383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097294bfa5e55b64b9244746431049affede98938b8e5d7acceaa5329d6d6d41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 02 Jun 2023 21:59:28 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Fri, 02 Jun 2023 21:59:28 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 21:59:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 02 Jun 2023 21:59:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 02 Jun 2023 21:59:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 02 Jun 2023 21:59:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 02 Jun 2023 21:59:28 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 21:59:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 02 Jun 2023 21:59:28 GMT
CMD ["rabbitmq-server"]
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
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
	-	`sha256:514886462504f01182e2a80568c8d3649f35623caa3ac464d0131d4d81827990`  
		Last Modified: Sat, 03 Feb 2024 20:12:59 GMT  
		Size: 15.6 MB (15567807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:647b984a369fcb17948c60d5357c2332432a88d3b08bd1d8a5c410f1baced83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1664811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7295c9bb03c71df7c311ada72316d5fbc51a88fd1abc4e76b4a1f5387cd0f36c`

```dockerfile
```

-	Layers:
	-	`sha256:93046a007bfbaeeee91aa7fba3e3baec561c8911f28d8e4366a3edbbf4b5998f`  
		Last Modified: Sat, 03 Feb 2024 20:12:58 GMT  
		Size: 1.7 MB (1651237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a900439d0bd848a4846bc4ebe9fb9107b48f0bfe9a8b929b49fa41443f73663`  
		Last Modified: Sat, 03 Feb 2024 20:12:58 GMT  
		Size: 13.6 KB (13574 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:6fe3006b8d25c8fd690850dea1c64721d03ecc40a1d4a6ecd81f7e6cfe88399b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84108667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86bd2a43e1ab7ff0a68ba4cb7b3ead320e92858965b290e449612c9eb4da0b1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 02 Jun 2023 21:59:28 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 02 Jun 2023 21:59:28 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 21:59:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 02 Jun 2023 21:59:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 02 Jun 2023 21:59:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 02 Jun 2023 21:59:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 02 Jun 2023 21:59:28 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 21:59:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 02 Jun 2023 21:59:28 GMT
CMD ["rabbitmq-server"]
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
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
	-	`sha256:b9b7adf41315d00600f8d8a5b8afe82ceb4013f2541ad3a9a621a84b59a33a17`  
		Last Modified: Sat, 03 Feb 2024 09:37:17 GMT  
		Size: 15.4 MB (15417063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:39276e3d135093f0f388a28284f4b2e1c4544b4445688cb7991220948a82be7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1664556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9818f37a9332bc737ca7d1af1500879f41e17550c2f1d82911d246d2cebc7d`

```dockerfile
```

-	Layers:
	-	`sha256:e1131dde544887d40db00d41ac9acfb05198ee9db64a7b4fd0a07cef2d72770e`  
		Last Modified: Sat, 03 Feb 2024 09:37:16 GMT  
		Size: 1.7 MB (1651042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea905231682d0b3fe9ea68e1f54d970ecd6931279e9a6bcd13cdd7b7de472ac4`  
		Last Modified: Sat, 03 Feb 2024 09:37:16 GMT  
		Size: 13.5 KB (13514 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:9f19cb59dfac793ab000c9c38db53f29a3d2804462c5488d1c63f106702c8010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79194586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4a86c6d706bae00e697d1f673f1883cf4a443d134f0f7971598d613c11e1f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 02 Jun 2023 21:59:28 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Fri, 02 Jun 2023 21:59:28 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 21:59:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 02 Jun 2023 21:59:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 02 Jun 2023 21:59:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 02 Jun 2023 21:59:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 02 Jun 2023 21:59:28 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 21:59:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 02 Jun 2023 21:59:28 GMT
CMD ["rabbitmq-server"]
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deb0d916d940ff67aa8c7e14831de6850ca4ec8f7d55d567a7a62278624b4f2`  
		Last Modified: Thu, 01 Feb 2024 19:03:58 GMT  
		Size: 32.6 MB (32612514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede568fbc99834c8ec9720843e00d1b2d3b8e6761e0a9bfad009ab0f96c81b64`  
		Last Modified: Thu, 01 Feb 2024 19:03:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abfcf725c88cb4028c0e505275a4c27690f78a906ea941682a99422ae4788a7`  
		Last Modified: Thu, 01 Feb 2024 19:03:57 GMT  
		Size: 7.5 MB (7493817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b703c8a37d15905b7aeac4f9aa3f933947b1d99dd070389d215ceed1e9809a`  
		Last Modified: Thu, 01 Feb 2024 19:03:57 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680cd2bc0842851124966c93d2eaec652e2f703ebcda58725d862ada9e7289b`  
		Last Modified: Thu, 01 Feb 2024 19:03:58 GMT  
		Size: 1.4 MB (1406670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eea14220dfc56a87670c9c53e7c6792f1ce3929e971bd1aab4d702adbd2e38`  
		Last Modified: Thu, 01 Feb 2024 19:03:59 GMT  
		Size: 17.7 MB (17746908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875fb2532c17b5e8acdcf27f0906526e97fc5913703f609ed809e36491b106e9`  
		Last Modified: Thu, 01 Feb 2024 19:03:59 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb3311456f41e30a2aaa8f77457b007b14e1aabaabd28c10ee4ea3422d6ce27`  
		Last Modified: Thu, 01 Feb 2024 19:03:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8f4a2f19f77a04b9703208eebe66fbd8ea655f0978936bd7c129146d8f8bcc`  
		Last Modified: Thu, 01 Feb 2024 19:04:00 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4489ab2d6f972039a832fbe16faaa0f4c8406ac213232bb295a506fa17ec6615`  
		Last Modified: Thu, 01 Feb 2024 19:04:00 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5316bf7b3e86379065957919e4d2d1c1eabb32747d41ec9255f54b9ea1717e`  
		Last Modified: Thu, 01 Feb 2024 19:56:51 GMT  
		Size: 16.7 MB (16688056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8aa8cf1b241162917f311500f9138e54e01216d5200f8be8b24ad76d63071d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1666300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7763db95599a9cc6670a5e1a8c939067186edcd3ec5067c577a4bde04114b4d`

```dockerfile
```

-	Layers:
	-	`sha256:9b373725e040e4e18e14806a748d095d058dd3ef8ceb8c7aadb8f7ab1b842e98`  
		Last Modified: Thu, 01 Feb 2024 19:56:51 GMT  
		Size: 1.7 MB (1652853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be123703dda22404aa66a93ba23646e4436770261c572c13a1bf041c136a4c60`  
		Last Modified: Thu, 01 Feb 2024 19:56:50 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:45c0029b7e7420bf6923a25212da32815be9cc5ebc96da6342d1183e838b6afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80187292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de248904e4a87e340ca7e26c48f7e43afd3d19347f48ab88fa4f465c84fd263`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 02 Jun 2023 21:59:28 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Fri, 02 Jun 2023 21:59:28 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 21:59:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 02 Jun 2023 21:59:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 02 Jun 2023 21:59:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 02 Jun 2023 21:59:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 02 Jun 2023 21:59:28 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 21:59:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 02 Jun 2023 21:59:28 GMT
CMD ["rabbitmq-server"]
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52ff7107cc9efa46406031dff0083e79223159cab38e73180d77b3c2078fe7b`  
		Last Modified: Fri, 02 Feb 2024 20:54:23 GMT  
		Size: 32.8 MB (32830042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3227c4d4e67114435df999234cd6654040b497e6f99fe4bf7c04e8fc9e0c8c7f`  
		Last Modified: Fri, 02 Feb 2024 20:54:21 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457949671059ccc2ed8afd5bad0415b4b007e3bf070feaad0f078404e4af81a8`  
		Last Modified: Fri, 02 Feb 2024 20:54:22 GMT  
		Size: 8.0 MB (7981849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443f37c43e034c1c3fd0420001e5b2b781e126d05e7080316f019eef0ec30f0e`  
		Last Modified: Fri, 02 Feb 2024 20:54:21 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079bd71cd2d2cb5aecf318ce5c8b90a94e55ce7dc4a5f8a7d7885b2896b0f79d`  
		Last Modified: Fri, 02 Feb 2024 20:54:23 GMT  
		Size: 1.5 MB (1515586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b7b217eab0738955f5a2d24cd216fa30179b656bb7cb9fb3d207c02eec64e1`  
		Last Modified: Fri, 02 Feb 2024 20:54:24 GMT  
		Size: 17.7 MB (17746920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42df4920863541e5e006aed467dbb69e9f02238039b750c994ab9df876084da8`  
		Last Modified: Fri, 02 Feb 2024 20:54:23 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d652b3f5cd5076cee75cd26f56f5aaa29b1dd92fbbbf48f81bc6a28422758e3a`  
		Last Modified: Fri, 02 Feb 2024 20:54:25 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0530c798186e5c67ea7ea87ab356e776b5656bad6f417c751d61f1aaa83d57c7`  
		Last Modified: Fri, 02 Feb 2024 20:54:25 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0ee0cb8bf2adfad3a77c5284a1d30e07f33c1993557bc775bfb7acfe277364`  
		Last Modified: Fri, 02 Feb 2024 20:54:25 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500861a73a0361393bb9746e7c54f6bcdc43f59268132dbad0279e7f2cd09aeb`  
		Last Modified: Sat, 03 Feb 2024 01:40:48 GMT  
		Size: 16.8 MB (16751997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:dd7a159bf0e619fdb1364dc7fe8daf77175ea0c8e68838080a6e53bdd68273ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1663311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068558a15524331f0242d5a684d00cbe41bd85a1355430f5e12b54f887015bd9`

```dockerfile
```

-	Layers:
	-	`sha256:7e8e5c3ea9c101eba3a75a0a449328ab75aa4240912f8ff8a5311c242540303e`  
		Last Modified: Sat, 03 Feb 2024 01:40:47 GMT  
		Size: 1.6 MB (1649769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42582664010fa7a5e4ea06a0f4157eb51af29031f96cca8be16ee502a08b7d4e`  
		Last Modified: Sat, 03 Feb 2024 01:40:47 GMT  
		Size: 13.5 KB (13542 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:c371570102b1e1c57b1167e2279e23921ef7644b5e7a73975993fee3bbb8b8fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78819427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b1791a03abc2ba454b736ab420dd7a50f3ba519ae56e79513fd7beff4df320`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 02 Jun 2023 21:59:28 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Fri, 02 Jun 2023 21:59:28 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 21:59:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 02 Jun 2023 21:59:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 02 Jun 2023 21:59:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 02 Jun 2023 21:59:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 02 Jun 2023 21:59:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 02 Jun 2023 21:59:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 02 Jun 2023 21:59:28 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 21:59:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 02 Jun 2023 21:59:28 GMT
CMD ["rabbitmq-server"]
# Fri, 02 Jun 2023 21:59:28 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 02 Jun 2023 21:59:28 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
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
	-	`sha256:059159d4a8d231cd4030cabdc65aacc92e607e2734456447bdc2b87236f48ab2`  
		Last Modified: Thu, 08 Feb 2024 19:18:12 GMT  
		Size: 16.7 MB (16704882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a85c2367b79f8a81bb9e5ac7d2fed122202b8f9bffd836052d56dfeab3627ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1660999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2badb7ccf4b1117f3e2935d886247f42597720d2b5ec6a51bc600405c4e5e272`

```dockerfile
```

-	Layers:
	-	`sha256:75b0c3dce67eac0eac2dd725494f7aecc97db0335129d266cb25d71f63f16a14`  
		Last Modified: Thu, 08 Feb 2024 19:18:11 GMT  
		Size: 1.6 MB (1649225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:139d54af4bc4872162dcf54fdf7aca3058b22ff109d271faf4a9f8d67e87acfd`  
		Last Modified: Thu, 08 Feb 2024 19:18:11 GMT  
		Size: 11.8 KB (11774 bytes)  
		MIME: application/vnd.in-toto+json
