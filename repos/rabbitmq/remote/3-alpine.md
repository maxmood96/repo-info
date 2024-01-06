## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:3ec3d5024703d285be97e4769b0cfb2053239f082501c10a18f04650fb4f708a
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
$ docker pull rabbitmq@sha256:e096538d49e9cf79e643956712038cf6cd97e7b003126727accf5cb9ba4b43b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71017413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9915f20a2123309a7a87c0b15b9921c2b6c84457b6d9bbefc7194444572379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 05 Jan 2024 21:27:24 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 05 Jan 2024 21:27:24 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff578378980d5d28e2b390655e1b8d47ba45e4ebae0e2d180b194870a32edfe2`  
		Last Modified: Sat, 06 Jan 2024 02:59:54 GMT  
		Size: 39.9 MB (39897411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3b222fba4cddaa16e950fbffc22084564ef1ae7ae016b285d364eef3d6c761`  
		Last Modified: Sat, 06 Jan 2024 02:59:53 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df490334d5aeeb73295e0563b47f15cbb9f431a03c216cbe3849f2321228650`  
		Last Modified: Sat, 06 Jan 2024 02:59:53 GMT  
		Size: 7.6 MB (7554061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a304a16b3356e2cf58f6a57c32b4301edf7cb6b43de0f6afac2192590c007d`  
		Last Modified: Sat, 06 Jan 2024 02:59:53 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cb5dfa36a851e3f23b46770da5b666a1094175ffba04fa2dcfbf7552da3442`  
		Last Modified: Sat, 06 Jan 2024 02:59:54 GMT  
		Size: 2.4 MB (2407903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a883a6407f2e3a66ca9d66c9fab16e141f951f8c2c10c2328c114b6b433bd01`  
		Last Modified: Sat, 06 Jan 2024 02:59:54 GMT  
		Size: 17.7 MB (17747031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcae30aa186931ea57fd59a5fbb4f2aa378c04ebba7285a5f6e752bfe898f48`  
		Last Modified: Sat, 06 Jan 2024 02:59:54 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebfff6aebec78747aee44b82701e84a43e47852d176c6a614e064097288a67d`  
		Last Modified: Sat, 06 Jan 2024 02:59:54 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78de07803ac482de9972da6411dd2f1f3f55eeffab23521edd32dbb993cfbf4`  
		Last Modified: Sat, 06 Jan 2024 02:59:55 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6849ea9ea9f45dcde10b99c171d4589bdf3d6f486257037fe423591a845d4ac7`  
		Last Modified: Sat, 06 Jan 2024 02:59:55 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c39f953d640eaa4a57f5fc88dec75feff408d0b4d85677378f7f4ce2b8c5e342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a405c14c74057bd2d0f8b03a5b4ef27f49e6fd26309c3ad93bc7d021ebf55b95`

```dockerfile
```

-	Layers:
	-	`sha256:6a69b04ef4dd013ce9335c66a08956d4208b3e64c8f106cb4409952623cc7fb6`  
		Last Modified: Sat, 06 Jan 2024 02:59:53 GMT  
		Size: 760.7 KB (760731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3561e4addb7fb2002231c8400d2568f3b1156d3af65dc8f8cb7e81a988e76898`  
		Last Modified: Sat, 06 Jan 2024 02:59:53 GMT  
		Size: 2.3 MB (2296534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b169c56eff1d7e44fc1f344e30c7ede11ef19bf6ce54214c58486a1fc474c6`  
		Last Modified: Sat, 06 Jan 2024 02:59:53 GMT  
		Size: 2.3 MB (2295644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc5d2856d7ed9a0d1786d0c7953b37f604f656da5b8ee59bf386a95dc682b05a`  
		Last Modified: Sat, 06 Jan 2024 02:59:53 GMT  
		Size: 69.3 KB (69277 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:4b11c782a10a6b1432eafa13d74246e8832a6a690d6179d825386be4cba961cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61128966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e533aa0199547e16c744b8bbe6a0a5d4e44c2448800b8a924cd300945be4794`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 12:05:27 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Dec 2023 12:05:27 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Dec 2023 12:05:27 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_VERSION=3.12.11
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 12:05:27 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.11","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.11?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Dec 2023 12:05:27 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Dec 2023 12:05:27 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 12:05:27 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Dec 2023 12:05:27 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c328ada3d750c074d3af3374a6203c6fbfdbc20e6e1408bfe54e5eb3eb7cb8`  
		Last Modified: Thu, 28 Dec 2023 10:44:17 GMT  
		Size: 32.4 MB (32426903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c294a2cf45cdfdf5d42a17713cdac5031d873e4d7544f61e460d7cb54633f`  
		Last Modified: Thu, 28 Dec 2023 10:44:15 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e562f27da533879f0fc7112b9ee51cbe593753ddee1febeb71aab2cc9fa72830`  
		Last Modified: Thu, 28 Dec 2023 10:44:16 GMT  
		Size: 6.4 MB (6384106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff8a28ddd18bf00c4f0624940c1d634a3e55854eba63860e45ff79d61c05063`  
		Last Modified: Thu, 28 Dec 2023 10:44:15 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117779ce866115313b4528e88b43df917fed9a445b70f68e9cf28438a731c0c8`  
		Last Modified: Thu, 28 Dec 2023 10:44:17 GMT  
		Size: 1.4 MB (1403727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086e0843776a54bc7c60cbb7bc1fd1189cfefda3a76f45cdfe061e642d750132`  
		Last Modified: Thu, 28 Dec 2023 10:44:17 GMT  
		Size: 17.7 MB (17746561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f60bdc34c6c078a9cfb1f906da8e4a146d2188c59d596d33f4cca2c5ea0367`  
		Last Modified: Thu, 28 Dec 2023 10:44:17 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c57ccbef63658aec34fc6fb20047a9fea7d7ee40d3f2d2350069d19999b8384`  
		Last Modified: Thu, 28 Dec 2023 10:44:18 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be99bd55285ecc0b1bf2169f2217035ef30d527c1119cc70a8145cc03a97a64`  
		Last Modified: Thu, 28 Dec 2023 10:44:18 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec6600354e0e4e14216c67ee6603fa34fbf04a6153e503e5b20c3a200e7ced6`  
		Last Modified: Thu, 28 Dec 2023 10:44:18 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6d1da565cab3d48cbe1fe5696baec82121a2b710bae44e50977e4a40106e855a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 KB (69109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ed267095b6213291c56894adb32ef0b9ea3acfd7d3dede8cc8972416ce6e3d`

```dockerfile
```

-	Layers:
	-	`sha256:93eb5e5295bed21777e83947cd9d6a9e41243a780ec3a538eed4cb8585ba8ba8`  
		Last Modified: Thu, 28 Dec 2023 10:44:15 GMT  
		Size: 69.1 KB (69109 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:e27e55a2a1cc60d628dd6dffe55b86761553b84309e84911f6bc951badddf23b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60397054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0594adb1eb61b04cb7c8aaecd8f0446e2a2b9bc7f2f9f5eedaa69f674ac9f40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 05 Jan 2024 21:27:24 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 05 Jan 2024 21:27:24 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2392e2c9d27e86124ca7e8e6a0f8e6ae052123d885444509a1fac73ce0fa7f08`  
		Last Modified: Tue, 19 Dec 2023 01:26:18 GMT  
		Size: 32.3 MB (32336634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d31b1b1875ee7752972c089ac2a1990838ee6b4c04981fa600d1c32c4fa74d`  
		Last Modified: Tue, 19 Dec 2023 01:26:16 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f06f5129e16dbc73acb1254dd9c908107b7dc088d0dd307bcc182e64da6d19d`  
		Last Modified: Tue, 19 Dec 2023 01:26:17 GMT  
		Size: 6.1 MB (6084850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd949a9b4bc330156c73ab7ee9f7affe6fa421db97c0d064d0b4f28624a253e5`  
		Last Modified: Tue, 19 Dec 2023 01:26:16 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c53431e47c14b95636fbeb22d913d94ece94cd5a6dbb12269ceaec34e78b657`  
		Last Modified: Tue, 19 Dec 2023 01:26:18 GMT  
		Size: 1.3 MB (1307590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1e850620087d7e38d5e95c9fe2eaaf0a3cd3001d6ac0be45438adb0340a129`  
		Last Modified: Sat, 06 Jan 2024 05:31:27 GMT  
		Size: 17.7 MB (17746757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0955026c88590d97f29f3ef3c27206cefb0aab1b3f9beaa4a4f13a91ea27c226`  
		Last Modified: Sat, 06 Jan 2024 05:31:26 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a258af9b6c310606b0d4f094deb26b77178d28f7b8613c73d730452d3458d55d`  
		Last Modified: Sat, 06 Jan 2024 05:31:26 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc023662dcb422c680f9d8f330324dfec729aad0952baba0d3237d9f9afd8d8`  
		Last Modified: Sat, 06 Jan 2024 05:31:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb75d1fd3921e824fcecaf40da3c807185d611d5afd3bf4bca393c973077a0b2`  
		Last Modified: Sat, 06 Jan 2024 05:31:27 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ff6f41625199e50197877ea1e9e838971ba600928a754d59048903e2533d93d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff05205f089442a07bf36cf7569325cbfb736a57544ba2242ccd99cca515a5ac`

```dockerfile
```

-	Layers:
	-	`sha256:76edd36c27e2ccbec3cf17b28de7e11cac13bc56860c1183d6a9f57e3d1b3369`  
		Last Modified: Sat, 06 Jan 2024 05:31:26 GMT  
		Size: 756.7 KB (756709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d71b052ac6c5648bc3809194373539f7cf82d0ec79d25c66e09644a3f896ed`  
		Last Modified: Sat, 06 Jan 2024 05:31:26 GMT  
		Size: 2.2 MB (2215090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb8aa0194c8473a24dd87166295c44c27e306594ca2a2eda4fe7de80cad16781`  
		Last Modified: Sat, 06 Jan 2024 05:31:26 GMT  
		Size: 2.2 MB (2214200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:152e3e12ed385c5f7fe5c3daa18e4cee6e90dc06b58f21dfa07d2322361a6acb`  
		Last Modified: Sat, 06 Jan 2024 05:31:26 GMT  
		Size: 69.3 KB (69324 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:3cf2b25161406cc6c53febe899bca904fdc203440cfcc8f9d2681ff65f741d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68683967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25425dba71ddbfcbc1dd30113049c9d35e6483cc881cfe44fe10d7e114c538b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 05 Jan 2024 21:27:24 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 05 Jan 2024 21:27:24 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3f6c6b83152805eb2e5113d6eb35b1475c7cd6bd414ae39919369ea34e0ea6`  
		Last Modified: Tue, 19 Dec 2023 01:20:06 GMT  
		Size: 37.9 MB (37914616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca704a5a588c3767cf6f69498f4c9e85a976ec5bfdda313b9050bb1833bdb147`  
		Last Modified: Tue, 19 Dec 2023 01:20:05 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286b89a80bec3b69ea5002a141e2c4fc630b976ffbdb45ee29851eb2fc1d42c3`  
		Last Modified: Tue, 19 Dec 2023 01:20:05 GMT  
		Size: 7.2 MB (7180445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568af80e8a6742fd91184ce4ad0e61d63f8b6f8192b2b4705a0d36f03c47c32c`  
		Last Modified: Tue, 19 Dec 2023 01:20:05 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67066722dee8291e4296eef6b885d1a22003c86a74397dca6fd3333b804423af`  
		Last Modified: Tue, 19 Dec 2023 01:20:06 GMT  
		Size: 2.5 MB (2491581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf9cf57cd5f51e96f53257e8ec6f2d4fe91663a6f584ae1a794e9585c574398`  
		Last Modified: Sat, 06 Jan 2024 05:57:23 GMT  
		Size: 17.7 MB (17747006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bb1efe4708154fcc8b4d355ef8f943b42c5a9ebe4d559a8ebbff3ed1f90d86`  
		Last Modified: Sat, 06 Jan 2024 05:57:22 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279b274d61e8d21580cce959a5641cc6ab35d50b143088574719a598d6992890`  
		Last Modified: Sat, 06 Jan 2024 05:57:22 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe048a218ed036e64c88b4b0b07de1218d3c798b65c12bf6f77a0883b34e5ad`  
		Last Modified: Sat, 06 Jan 2024 05:57:22 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66723282be5556ee4ffdfb7bd71a4da020f684b70433f4936b80b73e3996f61d`  
		Last Modified: Sat, 06 Jan 2024 05:57:23 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f95551f0f47ae03181b33f982c9ff6115ba4347f18c2a390072a8ebde6051fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2b9c265b5ccfadaabfab94ae3c9193a1423276d135aec32988d2fed813e2ad`

```dockerfile
```

-	Layers:
	-	`sha256:91705d56823fc3e4d4a289f4fa3e40ef308d4cf19049505d8a9b29d4a71b18e7`  
		Last Modified: Sat, 06 Jan 2024 05:57:22 GMT  
		Size: 760.7 KB (760742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe19726142ebb18e1248864b054de2c68f9e8aa791f63646504c91401d51fc9`  
		Last Modified: Sat, 06 Jan 2024 05:57:23 GMT  
		Size: 2.3 MB (2309980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9910beb447ec521e9118799d76d16d19cda5803e5074f4091ad2ecec9c48d31a`  
		Last Modified: Sat, 06 Jan 2024 05:57:23 GMT  
		Size: 2.3 MB (2309090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c80844fb6dc1d732d4fc2043e599828cc1d1822ace1502cb32ad2a7cb929d222`  
		Last Modified: Sat, 06 Jan 2024 05:57:22 GMT  
		Size: 69.1 KB (69121 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:579770839bf51162766daa5ab24b3efb2c5b2d51b77bd46cb88fd984068faab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62493820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7f5bd95f22952d823ac84fe4ef9ca7ea18e710e9cbe6fb812107e789bc8dbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 05 Jan 2024 21:27:24 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 05 Jan 2024 21:27:24 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16be9c1b3368bb9507de5523d8d9c798c4d05c1e8507798f8668e07dbe989bcb`  
		Last Modified: Sat, 06 Jan 2024 02:59:34 GMT  
		Size: 32.6 MB (32612656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a59f0e6afb14238a53c78b32c9dc0cd1b8d15d2da9a8d7b4f92b38256396698`  
		Last Modified: Sat, 06 Jan 2024 02:59:32 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6400f8bf9acb9665bc07d476eeb9c822ae7f9a6e78d297a0031095f80479487c`  
		Last Modified: Sat, 06 Jan 2024 02:59:33 GMT  
		Size: 7.5 MB (7481068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d22681da7237f78dcb21ad999673af2f391b072da5d1c6b8a8159047c15d52`  
		Last Modified: Sat, 06 Jan 2024 02:59:32 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3086b77dab1fd5153bfb7dbcb523ce1f8977fb3a9102696c4f3b5979663e1024`  
		Last Modified: Sat, 06 Jan 2024 02:59:34 GMT  
		Size: 1.4 MB (1406633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b483ff409c035b463237b04f774c88d904ba6a18ea2d035986f18179b7bc4dd`  
		Last Modified: Sat, 06 Jan 2024 02:59:35 GMT  
		Size: 17.7 MB (17746818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6906344ed3438c3e103c50e070dba38ccfbf94c7a4ecc295ff484b13bf8845e2`  
		Last Modified: Sat, 06 Jan 2024 02:59:35 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e901eeff11137cd633f0fcf6931c60e0f6ac49a9b4b5b467cc958e286f3cf6`  
		Last Modified: Sat, 06 Jan 2024 02:59:35 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7c299624e9f14fa7639b7dc51fb0d770f92a8ba5a13195a82b62d3d5b3fb29`  
		Last Modified: Sat, 06 Jan 2024 02:59:35 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5cc9eab13a69c8fcc570b6ddceabcac6ebb55a709bf0325e302a95764c2d98`  
		Last Modified: Sat, 06 Jan 2024 02:59:36 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7c7c565ca656748a81d9c936df48eb3fd22d9be59e8afa49e00c9399efb07b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5401680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c9cf4389c852c58461cbe9c67af04d5d235c7132cab402bf9bfdd33e38fb9d`

```dockerfile
```

-	Layers:
	-	`sha256:74388bb860ac02a845f09b547728fda503a0fcd89c1f3d65b4c5a937c425585d`  
		Last Modified: Sat, 06 Jan 2024 02:59:33 GMT  
		Size: 756.6 KB (756648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2087fa58d8af7537a6d6a8babd78ecb4fd495ea47b5ff33e72612893a2d0524`  
		Last Modified: Sat, 06 Jan 2024 02:59:33 GMT  
		Size: 2.3 MB (2288348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9583b97f1cdf5d1801d3dddf9dd8185398f899e5f07d5ec4c70fb09c15a35e4e`  
		Last Modified: Sat, 06 Jan 2024 02:59:33 GMT  
		Size: 2.3 MB (2287458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37cb117187eb8f5dfa21cad1b636e27c72b9661678505709fe854de376adb05e`  
		Last Modified: Sat, 06 Jan 2024 02:59:32 GMT  
		Size: 69.2 KB (69226 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:8847bfee7b71d7d5e006140c87a61712c6e67c25151260d77e1b98709244879a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63421599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104e47bac2e3e3081736608b4299568caccd6a63feaac06a0ca792e51d7e8e56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 05 Jan 2024 21:27:24 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 05 Jan 2024 21:27:24 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e18033781df51e3a28370871ffe433ee3c517e63d80002f10780a329d62897d`  
		Last Modified: Tue, 19 Dec 2023 01:19:06 GMT  
		Size: 32.8 MB (32829753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee5a9a206848b8435df614c1a9656e406c359fc8ac8376e4a8bc94c9af4a0ed`  
		Last Modified: Tue, 19 Dec 2023 01:19:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e2d79d5d6d4f38ded59ba485831dd4f4481b9410ec6292125ff803ab0bfd00`  
		Last Modified: Tue, 19 Dec 2023 01:19:06 GMT  
		Size: 8.0 MB (7967022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2b74c9fb3275044cc54e33ab263b71c298a38d41b07e7b5a83ed932e446fdc`  
		Last Modified: Tue, 19 Dec 2023 01:19:05 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef336b46c5c7e058ac6048ad1763b4a7f56213bf84e57c6c6dc46b0b97f5e1d`  
		Last Modified: Tue, 19 Dec 2023 01:19:07 GMT  
		Size: 1.5 MB (1517323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d65e7b266999ee932dbe609485137942debed74c31f6674a36b372aa2c3f411`  
		Last Modified: Sat, 06 Jan 2024 03:24:59 GMT  
		Size: 17.7 MB (17746725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b6aacf4e92afd69ad631085bf3c51f16679d34314b1febab5688fe85d0460`  
		Last Modified: Sat, 06 Jan 2024 03:24:58 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acafd47b7f5be6568dc796feb1238b6899c23547db40a2866905cbd5c7f9f218`  
		Last Modified: Sat, 06 Jan 2024 03:24:58 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a71def966d73134608d74aa6b263b24bffecbf9c7f07089c7c7c406bf2bd3ae`  
		Last Modified: Sat, 06 Jan 2024 03:24:58 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddb5041fc9119f70303c1a584c61654b1e226d52c85418372dcccc19e3accf7`  
		Last Modified: Sat, 06 Jan 2024 03:24:59 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cfdc95b5ee6fa0676a11122fbaa302cf4d0a87c324845e11cffa5f5954556551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebba942af9b265208f0e4151957ccb3f0c1460595997c22abf9b3669b9e62eba`

```dockerfile
```

-	Layers:
	-	`sha256:c4fe4ba3df417b4c74bed89fbba59bc52cb30483a26f7beb43d9ecb5c532a560`  
		Last Modified: Sat, 06 Jan 2024 03:24:58 GMT  
		Size: 755.1 KB (755071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10d67c056a3fe089bdf7ea2eb51489d192e14a5b34212e3cc1ee0923361f9f3c`  
		Last Modified: Sat, 06 Jan 2024 03:24:58 GMT  
		Size: 2.3 MB (2287999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9daa4170488bd8f9b11a510aef81e9cfa90c254c7756e8eb10065755d5cd0211`  
		Last Modified: Sat, 06 Jan 2024 03:24:58 GMT  
		Size: 2.3 MB (2287109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d7f6a044d305dfc3ee52c5521ac1df2e755e6a77e86798d6a1ff1f1e57ec65`  
		Last Modified: Sat, 06 Jan 2024 03:24:58 GMT  
		Size: 69.2 KB (69171 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:d863d2bd05769f2e2b74f33fcc661f287c37694a9e81b40ce42b7cc77b9dcc26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62106196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d6a86caef4b260e91d67f81d88105d954f595f77bcbe8099fe4f1e7540fec8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 05 Jan 2024 21:27:24 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 05 Jan 2024 21:27:24 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bab8234efa28a5ccfce9900554b077de591980001319c90390fb819b20f4d2`  
		Last Modified: Tue, 19 Dec 2023 01:18:19 GMT  
		Size: 32.9 MB (32919466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09aec38dd8d2c55f0f0080cd935b4310f66cf0c3349f086a43755025dc7fdfb2`  
		Last Modified: Tue, 19 Dec 2023 01:18:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e15625661b90cb4afdcd50046b0bcad43c979843e122cfcac13d3ba813c27e`  
		Last Modified: Tue, 19 Dec 2023 01:18:18 GMT  
		Size: 6.7 MB (6696961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa90cb02b56a7344049c65e2b68b2b90aec741d3e6754b1019b8ec4f57eb1590`  
		Last Modified: Tue, 19 Dec 2023 01:18:19 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320b826531725b3ea40023906d3b5490a123bdd16b32146a0669fd70af58fdfd`  
		Last Modified: Tue, 19 Dec 2023 01:18:19 GMT  
		Size: 1.5 MB (1498160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0417d6b664205bcefc3194870b9e67e1ed6915da3252b4646ba3641ff0e7576`  
		Last Modified: Sat, 06 Jan 2024 03:17:30 GMT  
		Size: 17.7 MB (17746740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e0ba12a7f85adaa1164a1845f7e99b444e46868ee630607eb5203092b54114`  
		Last Modified: Sat, 06 Jan 2024 03:17:29 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01a0b927d916626b505e4727c03edde116a1ea5dc4ebed3f3a95b05256c0a16`  
		Last Modified: Sat, 06 Jan 2024 03:17:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efe9cf60dcc73e940cd244dda924bc6231e09267bfa9386f18d4cbb397ae4c5`  
		Last Modified: Sat, 06 Jan 2024 03:17:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a6a69dfe54db2fd3f79668effa9c7271e77da6b89d0125f129da3cc0f8691`  
		Last Modified: Sat, 06 Jan 2024 03:17:30 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:10be35b415469e4014e9cd0e8aa3b50eb048bafe1edba638738dee21e0153989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9da944b66dfcef00357513cc6abe4fb4d10d477c5f6a2d6c6fa2f83c77abc09`

```dockerfile
```

-	Layers:
	-	`sha256:de25e51c08ef5bc0849ec9c6618d90b1f2fed98640dac43aaf77d3aa883bf0b8`  
		Last Modified: Sat, 06 Jan 2024 03:17:29 GMT  
		Size: 755.0 KB (755037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e24adff9e8ef790d44fadb1ed832246812962830f0cf9049b1f207ca085b5a88`  
		Last Modified: Sat, 06 Jan 2024 03:17:29 GMT  
		Size: 2.2 MB (2220034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9641ced85b88304c4c0a842f2d6f0034ab3ef3fd298b602429620fff522a5d8a`  
		Last Modified: Sat, 06 Jan 2024 03:17:29 GMT  
		Size: 2.2 MB (2219144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6663fc1c7c6abb0fbda4ce43346702d66585d8daade69d92108b9162ab9932e6`  
		Last Modified: Sat, 06 Jan 2024 03:17:29 GMT  
		Size: 69.1 KB (69111 bytes)  
		MIME: application/vnd.in-toto+json
