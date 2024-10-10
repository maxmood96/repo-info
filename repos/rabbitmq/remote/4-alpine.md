## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:8df2399a2a195dca9bfaed6037e655bb70383d619de532aad670f651f2d5b1ba
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
$ docker pull rabbitmq@sha256:7cfaf12a05023c3c6c992f137e8d752d860a64ce40b4991e9973a437492c06df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74033745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b7ecb1708ac4478620fde38f2ed564438ded8a4e379ede8858e8916a8eb21e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 09 Oct 2024 11:34:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_VERSION=4.0.2
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 09 Oct 2024 11:34:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 09 Oct 2024 11:34:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf55fc5373296bdd8f7658ae66968dd4886786dd0a3bbe0b37d35d09da794bbc`  
		Last Modified: Wed, 09 Oct 2024 23:06:07 GMT  
		Size: 41.6 MB (41579934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9657c5f3b83f262cac05675d447781c8fde7b1cc3e3f41e31db5b55943e640c9`  
		Last Modified: Wed, 09 Oct 2024 23:06:06 GMT  
		Size: 8.3 MB (8284844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27abce07d6a1681bc3f1a5bc76601995a9b9ade45e862d98e6ddb9ade7f5b7b6`  
		Last Modified: Wed, 09 Oct 2024 23:06:06 GMT  
		Size: 2.2 MB (2234331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f6e1c8fa85c4c6095b473961032758ba72d959f1d7715d3fda99b498870af1`  
		Last Modified: Wed, 09 Oct 2024 23:06:07 GMT  
		Size: 18.3 MB (18309082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f10dd288b8644f5f8d901c19f23398baeb169beeafbcc821845537e44ccf6ba`  
		Last Modified: Wed, 09 Oct 2024 23:06:07 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d87ab1cf14430934885f9737a79b93d09734e230bc87a3674eb5a42f1c9799`  
		Last Modified: Wed, 09 Oct 2024 23:06:07 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad9de59df017f6516540f6b27c79ed6854be061a1115b2b7f845f6a78a92ab5`  
		Last Modified: Wed, 09 Oct 2024 23:06:08 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ecdde64545639c0bc0e6a803c7b47b63653f6605b579e2eae9a51331afc3d4`  
		Last Modified: Wed, 09 Oct 2024 23:06:08 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6553592e2a87fc964b0537183805584e74faacc7d37a3b14009b9491f09f82c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6427833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12cc0d9bb1664b1173ecc98d6278f971bd78b4e9eb127451372fd53f28adc227`

```dockerfile
```

-	Layers:
	-	`sha256:4ed4a1ee683da00ffdef0d7cb96a26c765dc8e7e459904b4b7945306161f298f`  
		Last Modified: Wed, 09 Oct 2024 23:06:06 GMT  
		Size: 642.5 KB (642452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75d891b9603e62ae415ed0d28f916d55129dd2e7a4e4905df191005c3fbfa666`  
		Last Modified: Wed, 09 Oct 2024 23:06:06 GMT  
		Size: 2.9 MB (2931610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75551dd400bdb93652b2204a53632a800c2577ed1c78ee480da8502b24038ade`  
		Last Modified: Wed, 09 Oct 2024 23:06:06 GMT  
		Size: 2.8 MB (2794101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4d790acfdff51b52c170a4a8d1d7ab836482b69dbbf166dc18f7f12a77bf24b`  
		Last Modified: Wed, 09 Oct 2024 23:06:06 GMT  
		Size: 59.7 KB (59670 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:db492d0b92a1c764d9e6c1a0b7826469c22c926659fffae59530fd02a861c5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63183917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0376d5b42b01839cf2f57aead34a9e3e6c4eb173fe29a91c6c2ddda62045a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 09 Oct 2024 11:34:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_VERSION=4.0.2
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 09 Oct 2024 11:34:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 09 Oct 2024 11:34:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed534a69666bd022097e876968b2ab66b463d0be3df4d7a61cdadf3e699f4930`  
		Last Modified: Wed, 09 Oct 2024 23:02:25 GMT  
		Size: 33.2 MB (33196705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eff7390bbe7c995763ffdc9d2291fe825e45188f9c74da10eb086693e66623`  
		Last Modified: Wed, 09 Oct 2024 23:02:24 GMT  
		Size: 7.1 MB (7079928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1b129092755c094b08e0e8eb9f420e3aedbcc5c997b01086238adf06e015c6`  
		Last Modified: Wed, 09 Oct 2024 23:02:24 GMT  
		Size: 1.2 MB (1230053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6630db2e8572e8655a5e174023e3b7fbb7e640491a84a358edfe8c72afc5cb7`  
		Last Modified: Wed, 09 Oct 2024 23:02:25 GMT  
		Size: 18.3 MB (18308979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb9c1ea58be98a3206f59cc21de8f3cd473eea72a78b49cf8e50b8b0348668e`  
		Last Modified: Wed, 09 Oct 2024 23:02:25 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b510041286cfe269f514b7fcb827811b88e1b1ecc6dc54b0755d8ebc3bcf36b`  
		Last Modified: Wed, 09 Oct 2024 23:02:25 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aca7be0ab3217dcb6dae04921c3000d6d0b0e027c16aeb778ce77a150607766`  
		Last Modified: Wed, 09 Oct 2024 23:02:26 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da557f5c628f0b7434d7f439f07dc543d260a565dd1cafbec857eab857b32f5c`  
		Last Modified: Wed, 09 Oct 2024 23:02:26 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:63b89cd06736fb603fcce025af26f1a5036815b9063a35b7219c09c6a375d3ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 KB (59638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b75232e3f28a5302daea335af9176962b02d95d0e1db381cc8a6c49d15a79eb`

```dockerfile
```

-	Layers:
	-	`sha256:53849e1a7063188fbfe2553fc4c0d07ef79d5b7bcd08ae6a7889af24b4f9e1fc`  
		Last Modified: Wed, 09 Oct 2024 23:02:23 GMT  
		Size: 59.6 KB (59638 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:9f5fb7b00e63744c4303ea973e60f15123e1268659cdf44fb265e2b16052b740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62348182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3db08177b165b2a7c7839c54478c2e82b3e1d47d21e0294a22386b79c625b28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 09 Oct 2024 11:34:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_VERSION=4.0.2
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 09 Oct 2024 11:34:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 09 Oct 2024 11:34:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1f67f28e10afeeb5df7b753ce3c23c80e4e4ae97ea19ca8709eaf48c068734`  
		Last Modified: Wed, 09 Oct 2024 23:10:27 GMT  
		Size: 33.1 MB (33092591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb5bb9d41ac48da80a09bcb8fa50d5dcef44144067bd047330d564dc74e86ef`  
		Last Modified: Wed, 09 Oct 2024 23:10:26 GMT  
		Size: 6.7 MB (6716586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f58409d17f8213ead54ed35d31298ac48b082e7d85b04e8db73806bb292cee7`  
		Last Modified: Wed, 09 Oct 2024 23:10:26 GMT  
		Size: 1.1 MB (1132947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad992a4f720a13377317c27de72fb11e96e2ae138cc103359d23298f74bed9b`  
		Last Modified: Wed, 09 Oct 2024 23:10:27 GMT  
		Size: 18.3 MB (18308813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13df8d0e4e97d921efd1fddb7c9ac509e1bb1be5c1a7fc54986029dc0135de9`  
		Last Modified: Wed, 09 Oct 2024 23:10:27 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b35a79ad032968a868d310fc38fc441a595e1e4172afa13787871e592b7bde6`  
		Last Modified: Wed, 09 Oct 2024 23:10:28 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f62fda2621c5b3b7c46761224ae60cb0519798c8a986ed69cb16dbe3f3010`  
		Last Modified: Wed, 09 Oct 2024 23:10:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e16f027fd71bba14404ac6fdd8b84e7cef8985ace339399fd2bafd1bf9dd50b`  
		Last Modified: Wed, 09 Oct 2024 23:10:28 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f436a7d1129949c569999afb91a2808bbcbc7473ec62f51446fe45baccc5d635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6221522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd5b8c7613d5a7e586b7de4038bff54e605998a3fc5eb3d5643acd28d616a14`

```dockerfile
```

-	Layers:
	-	`sha256:2b5bf393dd42e76611e6e3595b3b0d52b820089e5c16e5a1b67b6fe82ae07dd7`  
		Last Modified: Wed, 09 Oct 2024 23:10:26 GMT  
		Size: 638.4 KB (638417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:311bd1264cf7a167003a13d2362379a3ee57c7da4400906c84f5a4e312a4da12`  
		Last Modified: Wed, 09 Oct 2024 23:10:26 GMT  
		Size: 2.8 MB (2830938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71de1992eaf96c7d76e39efeb97ccbd033fce77eb4715e8226877940c5fcebf7`  
		Last Modified: Wed, 09 Oct 2024 23:10:26 GMT  
		Size: 2.7 MB (2692310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e44912ff76af7d63ffc5cd00f6052acf9da062b0f4424e8ee6a1a43ecd8c8aae`  
		Last Modified: Wed, 09 Oct 2024 23:10:26 GMT  
		Size: 59.9 KB (59857 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:da055328473269139022cea36c6159f03c281095c5eab70e05550f8379f3d709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73409224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ca00e1598c2d8ae00317a43d93815e227d711c22e5995cf917fb86bf6fdb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 09 Oct 2024 11:34:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_VERSION=4.0.2
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 09 Oct 2024 11:34:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 09 Oct 2024 11:34:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dd0fedca3a17179cb65d292514d9e5e38984126a794fb25c2d90ee8f939395`  
		Last Modified: Wed, 09 Oct 2024 23:13:25 GMT  
		Size: 39.7 MB (39693537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a0adb5b179620c713a2a9b89c503d480e94a60a3a427991cb9e46682773e29`  
		Last Modified: Wed, 09 Oct 2024 23:13:25 GMT  
		Size: 9.0 MB (8995937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d29ac149ba8ca99d18911526655bc8fafce02694421047863c8ab60662577`  
		Last Modified: Wed, 09 Oct 2024 23:13:24 GMT  
		Size: 2.3 MB (2321280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4211b0e014272175b221a29d61bf36ed1628843001724f9bf560bb05fe38ce60`  
		Last Modified: Wed, 09 Oct 2024 23:13:25 GMT  
		Size: 18.3 MB (18309082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a8ec127ba82cd312ee55b32313c240cbf84a9e664f97716b0a4c9479d1495d`  
		Last Modified: Wed, 09 Oct 2024 23:13:25 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4edb406e2703dae7e096fc8673f21e697d78285cb7241d75f6489f5e7ee1b54`  
		Last Modified: Wed, 09 Oct 2024 23:13:26 GMT  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2277919ec4d5f6bcaa61716fa3897423806b24ad8183754fdb9ee951e4182c`  
		Last Modified: Wed, 09 Oct 2024 23:13:26 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89978ebd6e4f3e52f38345cd200fd0987530423d39b1dc59d8899a251b6570fd`  
		Last Modified: Wed, 09 Oct 2024 23:13:26 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a621a17f9c5b69db0629614b4b3cf63f4c9ef126d1da2bf6f08b74cfcd11c390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6462150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68400a92ed91391e24ed32953a270116a62804f103f18851856496dc6c49e223`

```dockerfile
```

-	Layers:
	-	`sha256:64a0ecacc717881b7c9e711858d34237bd8cb89c172bf99fae6b0d68d30f51c7`  
		Last Modified: Wed, 09 Oct 2024 23:13:24 GMT  
		Size: 643.1 KB (643140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db3d926d9a54ff53a7f8fef14ddd2cfbc2aec9c287dc8cbc5dca42233649969b`  
		Last Modified: Wed, 09 Oct 2024 23:13:24 GMT  
		Size: 2.9 MB (2948865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3909ec74df18bbb3b32aae4d09f7e6b48c56e3bce491871461d7b0ad664a00f2`  
		Last Modified: Wed, 09 Oct 2024 23:13:24 GMT  
		Size: 2.8 MB (2810243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88fa5eb61623aa590b6e4e8c4a46e5f7230e0715d43a5544d1e0758087c15bda`  
		Last Modified: Wed, 09 Oct 2024 23:13:24 GMT  
		Size: 59.9 KB (59902 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:139cb419ebb0decce00a8f4771e134af9d5f09be99ad404617ef0e219eeb3620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64696147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4f902cb079fc64e7551cf52cdeed7d4eaba044f1a047d767f910d5ac88432b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 09 Oct 2024 11:34:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_VERSION=4.0.2
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 09 Oct 2024 11:34:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 09 Oct 2024 11:34:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e313efd353bb437752d28d413000b1e21b708e9253c3ee50bb6f32c38e7897`  
		Last Modified: Wed, 09 Oct 2024 23:05:50 GMT  
		Size: 33.4 MB (33359948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f12ea150375d801477bc00da3b2aa950fb5bc162fa22896aa41f130142f144`  
		Last Modified: Wed, 09 Oct 2024 23:05:49 GMT  
		Size: 8.3 MB (8324937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7063803ad7eb5f1661ee9da752f172ccfb347f3fc3f9b567a8fd3e66a7215b4b`  
		Last Modified: Wed, 09 Oct 2024 23:05:49 GMT  
		Size: 1.2 MB (1231512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a2c55326cc5240f4b509bd4f92ee494d8bc5b42f8c697de87a0ae8754218f4`  
		Last Modified: Wed, 09 Oct 2024 23:05:50 GMT  
		Size: 18.3 MB (18308836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1c00e853a2540ded1cb04b673f171f5285c7cb003c316c424549081a4ef523`  
		Last Modified: Wed, 09 Oct 2024 23:05:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dcba44ed23f414147761b5c6f6a7b9528484ae7d0de847219adb52583f4521`  
		Last Modified: Wed, 09 Oct 2024 23:05:50 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95d7057cf1c48a0f25234c4db9350f5f4c73fe36415c47e75e5d5c8fa2e9e61`  
		Last Modified: Wed, 09 Oct 2024 23:05:51 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51955e6d72fa838fb4b77879e68cad839cf8af55234ddfac3d8765897fe9ee13`  
		Last Modified: Wed, 09 Oct 2024 23:05:51 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bfcf25279841d894f0dcfcb5dc95bfdb8c16871af262862cfea0ccd39857f3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6403497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f048d83b678c5be571a6897d3668e03da9ed526552b85f46cfc5cfc9d89473`

```dockerfile
```

-	Layers:
	-	`sha256:af9f303da5b4b306665603e37e36eb082a01bfbc5941476320df258f163ee60f`  
		Last Modified: Wed, 09 Oct 2024 23:05:49 GMT  
		Size: 637.7 KB (637724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9716d81f3d6041fafe7c2303fd0f79598dc9385780154dca69f5392d81d75536`  
		Last Modified: Wed, 09 Oct 2024 23:05:49 GMT  
		Size: 2.9 MB (2921828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc37df32d68ff288c9f1b313b945c36034d1a7af75b278341d87fe4fe840b3ba`  
		Last Modified: Wed, 09 Oct 2024 23:05:49 GMT  
		Size: 2.8 MB (2784323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d499068bbba1a64959b0d7edef81eee120403999c62b393df174f66a4ab2a6a9`  
		Last Modified: Wed, 09 Oct 2024 23:05:49 GMT  
		Size: 59.6 KB (59622 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:861e72333537b01f5210c96d299fdff93efb6ffa492e9233681e98996851e79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65682194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cddda9df9c038a90138c505cb1b018efb6d051ee1b6740ae9e8963dfe70d6b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 09 Oct 2024 11:34:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_VERSION=4.0.2
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 09 Oct 2024 11:34:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 09 Oct 2024 11:34:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c3725fd5f7e57bc4f1a96f26eb2059163ea872bc99ce3b7e95323e120196f0`  
		Last Modified: Wed, 09 Oct 2024 23:07:09 GMT  
		Size: 33.6 MB (33619115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f1da942a53dc6c8e0ca86a5e6d5923f854652d8006323e22e238ff1bcc04f7`  
		Last Modified: Wed, 09 Oct 2024 23:07:08 GMT  
		Size: 8.8 MB (8834111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508bcf4da01d6bdf49a1a973b4ae84b89efb8a395cbc74ca213d48f8edb78dcc`  
		Last Modified: Wed, 09 Oct 2024 23:07:08 GMT  
		Size: 1.3 MB (1346113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be35d6ad5aa399be7bdc55716f2e6f89bf9514e0538c89eeea691def70053d1`  
		Last Modified: Wed, 09 Oct 2024 23:07:08 GMT  
		Size: 18.3 MB (18308684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f26e793c557c8e891bd1630a0e15eb0e1292404c9557b61d44b87eb6ed7e50`  
		Last Modified: Wed, 09 Oct 2024 23:07:09 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a3a2fae83d1e64e99b86b39dd587f9c091b8791fccbe0299b2d1c56393be65`  
		Last Modified: Wed, 09 Oct 2024 23:07:09 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6f3d5cfcdea77fe3859734d11531b5208e18ce49b1b1d80b3d41092d94f04b`  
		Last Modified: Wed, 09 Oct 2024 23:07:10 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eca6ee6b2a0d8307f3c2ad143128b1ef711e2092154beb078621c12b011f544`  
		Last Modified: Wed, 09 Oct 2024 23:07:10 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2f6e5da83622097e617b0a912be5e4f5799a9fbadae839bd8f7ef95d7aef588a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85e6e2e8972a5e247dafa20beab54bbd31594ff15a837d1803a0a5e7e7f1bb2`

```dockerfile
```

-	Layers:
	-	`sha256:ad2fb4b7385209fb73c77e69ef6180bff212535e7381e9003e48e69ad943d373`  
		Last Modified: Wed, 09 Oct 2024 23:07:07 GMT  
		Size: 636.5 KB (636461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a74c226ff72dc687c433e39fe1bf52e71b0493b1475b572c638250e128b27c21`  
		Last Modified: Wed, 09 Oct 2024 23:07:08 GMT  
		Size: 2.9 MB (2921343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdeb15ffc3d62d3374285bca5f6dbbadd475f1e1a57c71177f405991b2a72e22`  
		Last Modified: Wed, 09 Oct 2024 23:07:07 GMT  
		Size: 2.8 MB (2782709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3deddac317f6addea19ade1a02ec683b755bef25da7cf2f0ef6260c01c94c9a2`  
		Last Modified: Wed, 09 Oct 2024 23:07:07 GMT  
		Size: 59.7 KB (59726 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:d4c2d5247a06a2fe699af7fbad24b806c2b9ec541c2455776c80943c04289a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67397258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d15122d2d6007ef95ff92a6bb086c6245a994658b4fd215eb08e7c759a8c4dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 09 Oct 2024 11:34:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_VERSION=4.0.2
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 09 Oct 2024 11:34:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 09 Oct 2024 11:34:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cb7009e10a8373603194c86e272035a9e7a0dbefb7c7861625a3a1ba9d2dee`  
		Last Modified: Thu, 10 Oct 2024 01:35:07 GMT  
		Size: 34.6 MB (34577584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1109d7df9129e6afafd5d03ef57f307fd040222d78e4d0b84f2faefaa26854`  
		Last Modified: Thu, 10 Oct 2024 01:35:03 GMT  
		Size: 9.9 MB (9866563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e60063055b8b0eb14d51996060e0937f12d29664fadae40e9df2eec1b2cc61`  
		Last Modified: Thu, 10 Oct 2024 01:35:02 GMT  
		Size: 1.3 MB (1270917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dd1f31c02b979593b87af4ec25b087a75e8c0b2f6a11ca7e7f3ebcd1b89776`  
		Last Modified: Thu, 10 Oct 2024 01:35:05 GMT  
		Size: 18.3 MB (18308993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6995c3cbffda65dc578c1842e39c23b86a35b1fe7ee6986a9cc8b8d78d9371e5`  
		Last Modified: Thu, 10 Oct 2024 01:35:03 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6488b53c20f1bb05d8d5675ae992f441e7e96f1d7979959d2f8a5adb89a6e2ca`  
		Last Modified: Thu, 10 Oct 2024 01:35:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e13e72ad6b6751f51f8436273c6da1325bca65327268a5a66c3dbf808b70e27`  
		Last Modified: Thu, 10 Oct 2024 01:35:05 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f34543b104eacd4df0c20d1699adfcc9a0506f9cdff92966319c776ef56c7da`  
		Last Modified: Thu, 10 Oct 2024 01:35:05 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3dbed965392b91b25a0109d1aa1eeb9493cd521d87710be0678cb225eae19f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6435340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ff5f02a189d2a7db5670ba821fab6344181faff1c364afe8d104537a1173ed`

```dockerfile
```

-	Layers:
	-	`sha256:65b7bd5d5daa5fc5f542bb36d155ecc19c3f57f7e75e5e196547bc7eee5ae655`  
		Last Modified: Thu, 10 Oct 2024 01:35:02 GMT  
		Size: 639.3 KB (639304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f00e83cffbf46790451894a872c56a5afb812c3939b96e8893f7e00a9c6831ca`  
		Last Modified: Thu, 10 Oct 2024 01:35:02 GMT  
		Size: 2.9 MB (2937466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:990300e9b74f4c9d1691a87d7f8d4f4c892bc69034adf69cdfefc6eba142d1ab`  
		Last Modified: Thu, 10 Oct 2024 01:35:02 GMT  
		Size: 2.8 MB (2798844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3acc3558956b8e7b60070fc3f0d00df6c7ba0200dfc1440f0ff1ffc51d34ea`  
		Last Modified: Thu, 10 Oct 2024 01:35:01 GMT  
		Size: 59.7 KB (59726 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:4cdd9808798c96ac3286cc6de8055d9e30c9960059218199d49585ea4ab29657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64270195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a14d7ccc65aed94375dbefbf16b11b90568e0bf7bc07a95b93af1f85ef3a8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 09 Oct 2024 11:34:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_VERSION=4.0.2
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 09 Oct 2024 11:34:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 09 Oct 2024 11:34:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b045940514f9cfd17b1037a792b5167041c3475400b7ccaa5c1bb0bef2bbc9`  
		Last Modified: Wed, 09 Oct 2024 23:10:07 GMT  
		Size: 33.7 MB (33690961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adc1031e8a15301a663696d51b3dd38581a5d4e618510411c0ed38b7c795386`  
		Last Modified: Wed, 09 Oct 2024 23:10:06 GMT  
		Size: 7.5 MB (7481820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516480edf240888d77ca795cd0c38729b3e62520a347721e4ec4614f3be8b542`  
		Last Modified: Wed, 09 Oct 2024 23:10:06 GMT  
		Size: 1.3 MB (1325185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ce251c770ddbc6f339850df632d122b195546f01e11f0726675fd9aac9b06a`  
		Last Modified: Wed, 09 Oct 2024 23:10:06 GMT  
		Size: 18.3 MB (18308878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472672ea75ebdcf9ed582b1ad12cb1bd103f59db94d19beb8e1696f3c4cf1cc4`  
		Last Modified: Wed, 09 Oct 2024 23:10:07 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f60ffe4ca0a38013f02c57ad679eb45a95a71da71a4cb9d96269a3e45d833ad`  
		Last Modified: Wed, 09 Oct 2024 23:10:07 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760595f46b4cbd011585d9fc4497441c19ac620a29c4626ba86e26248e001f9d`  
		Last Modified: Wed, 09 Oct 2024 23:10:07 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb5ae32a2189685eb95be3e146e0089c8d0e123433b6832898075ec23c70720`  
		Last Modified: Wed, 09 Oct 2024 23:10:07 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a7a153cfa4a0a9bb204f7e6e8fd3fbe432a22df48c0f6a71c1e6495c7ebbf670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6234285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe4a79c9b9f8d6752b9dd424ebfd6fc1ac217625abf46fd95021e8bbe98b239`

```dockerfile
```

-	Layers:
	-	`sha256:7c5c25800412bd28f232d4c5779704c1022d15cb202450cde3682c140c51f75e`  
		Last Modified: Wed, 09 Oct 2024 23:10:05 GMT  
		Size: 636.4 KB (636427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8a2a91d0afd3a2ea3c55243d8eac03c23c4e2bc096cb342649381f582b6fbd`  
		Last Modified: Wed, 09 Oct 2024 23:10:06 GMT  
		Size: 2.8 MB (2838396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ef8248f14353f682e3bbb0f855bd913bb788af5cffd379276e4566b3a8d0f34`  
		Last Modified: Wed, 09 Oct 2024 23:10:06 GMT  
		Size: 2.7 MB (2699792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7253e6678556d67160a03624a29254bc0d83be96c42421b3738ea9565bdef186`  
		Last Modified: Wed, 09 Oct 2024 23:10:05 GMT  
		Size: 59.7 KB (59670 bytes)  
		MIME: application/vnd.in-toto+json
