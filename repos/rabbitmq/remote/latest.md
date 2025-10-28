## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:b130aba932e372e92b37b1fc49230515ea7823ab598ec67511fb8f85d5531809
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rabbitmq:latest` - linux; amd64

```console
$ docker pull rabbitmq@sha256:3e54efdb4dacec6040b62cc997c9b905b6be8eb0fd1eacfc81d07226a1735d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (111990633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9829747dba1c16fffa864656e780ce444ddc0bdc77b7d746642dca17d6e4e505`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Oct 2025 17:33:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 27 Oct 2025 17:33:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 27 Oct 2025 17:33:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 27 Oct 2025 17:33:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_VERSION=4.2.0
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 27 Oct 2025 17:33:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 17:33:26 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 27 Oct 2025 17:33:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 27 Oct 2025 17:33:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 27 Oct 2025 17:33:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Oct 2025 17:33:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 27 Oct 2025 17:33:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a581c2da383e8c1e1ce0e6ad4a924b0e8d2ace2156091036d2b155773b52b6`  
		Last Modified: Mon, 27 Oct 2025 21:15:46 GMT  
		Size: 46.3 MB (46251756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd4a86daf961635e8a9fe918ea8e87f53e62222b8669ef6c960bda4eef6585f`  
		Last Modified: Mon, 27 Oct 2025 21:15:43 GMT  
		Size: 8.2 MB (8174787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6998be7836e37b6c1be2c1158337a4b28e7a6834b08dc4a211a3ab58d2101118`  
		Last Modified: Mon, 27 Oct 2025 21:15:42 GMT  
		Size: 9.5 KB (9477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737ff4b9bdaeb44c06bab6ba818dccef8dd479ed43a0a6fdc29674384b51a764`  
		Last Modified: Mon, 27 Oct 2025 21:15:45 GMT  
		Size: 27.8 MB (27829722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126c1dcc580cf90d69b8441dd5e1d4049db4c3e4e24f705011721854c8145dbd`  
		Last Modified: Mon, 27 Oct 2025 21:15:42 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac78f009ada9e0555b6f70bafdbd37c2aba6b393a49aebad1ddaceb5f828c63a`  
		Last Modified: Mon, 27 Oct 2025 21:15:42 GMT  
		Size: 107.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee801cd3c49bdd9bbbb799b9180bfbb632feaa60799bc4bbb33a3944a6f5ef75`  
		Last Modified: Mon, 27 Oct 2025 21:15:42 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ec279f656a5e25475967fe2a1f1717658fc0d13b5b8b014763dde324e7a930`  
		Last Modified: Mon, 27 Oct 2025 21:15:42 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bffb0509c73939ed853cc5606ec770781db9b7a19bf20351967b52a63807a7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18841206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fc061c07bb31147589ff9bb61cb70705395cc23512b95881f9629e777149fb`

```dockerfile
```

-	Layers:
	-	`sha256:66cceea183b0ed02c30e27d0637a65406312427252a3a488521c33b9e86cebd3`  
		Last Modified: Tue, 28 Oct 2025 00:52:49 GMT  
		Size: 2.5 MB (2487851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3fa975a5d884d13b9d9e2ef66920dcfa59168b544f495892df2e97c592320f`  
		Last Modified: Tue, 28 Oct 2025 00:52:50 GMT  
		Size: 5.4 MB (5378389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba2861d4870d4747f8164ce285c3e9991d75d387ed8b8d54c043ab7f4a6b348`  
		Last Modified: Tue, 28 Oct 2025 00:52:52 GMT  
		Size: 5.5 MB (5534994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb990e6ca113e3524cdafaebab298f3dbce9004b4c88ea1ac43a00511f5bcfd9`  
		Last Modified: Tue, 28 Oct 2025 00:52:53 GMT  
		Size: 5.4 MB (5380131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf80a443853fcd95e305aefb2aa2eed86ed1b02bca3409f3e5586e7a7653b3f`  
		Last Modified: Tue, 28 Oct 2025 00:52:55 GMT  
		Size: 59.8 KB (59841 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:69597de70826e347ee451e9f504939928288e23ec82019475a904ab06f9c22d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94543642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d05a0c20abea4800929147590106ab83fe98c0058b6376c78e722a52e18b81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:27 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:31 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 01 Oct 2025 13:02:31 GMT
CMD ["/bin/bash"]
# Mon, 27 Oct 2025 17:33:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 27 Oct 2025 17:33:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 27 Oct 2025 17:33:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 27 Oct 2025 17:33:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_VERSION=4.2.0
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 27 Oct 2025 17:33:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 17:33:26 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 27 Oct 2025 17:33:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 27 Oct 2025 17:33:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 27 Oct 2025 17:33:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Oct 2025 17:33:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 27 Oct 2025 17:33:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d78371d1f9329a47ebb764fbfb0016a7c942d699b2d204a82bd53c5fa6a02d7`  
		Last Modified: Mon, 27 Oct 2025 21:17:49 GMT  
		Size: 33.3 MB (33277872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e0307d682e3d9bd513ba223075a65a4404de13e5e493839cbeb5616aabbb8a`  
		Last Modified: Mon, 27 Oct 2025 21:17:48 GMT  
		Size: 6.7 MB (6671030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87e9d569edbbabee770b9f0d3dbe0c8bdd5ff98a069464bc2edc4a045115760`  
		Last Modified: Mon, 27 Oct 2025 21:17:46 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc11692d3587e25d02159617d6a5b8da53a35648950ef62126717a498c474de`  
		Last Modified: Mon, 27 Oct 2025 21:17:48 GMT  
		Size: 27.7 MB (27731735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3fbbf07c4bebefbecd15943a2e6f14c1d4feb983be09b860cb0a09b254dfa9`  
		Last Modified: Mon, 27 Oct 2025 21:17:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de2ba2fd32e12622c1c6c6b7671e1f7d815f345da7637b382a279990f1d7056`  
		Last Modified: Mon, 27 Oct 2025 21:17:46 GMT  
		Size: 107.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a799176ed9d23aba9149bdf71d0bb5efecde5557d11be033c899e0e066c5de4b`  
		Last Modified: Mon, 27 Oct 2025 21:17:46 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1987533263085e5bb378292e3c8f1ffa6ad6bb9cdc40bb6c1c321cbc4f4915c1`  
		Last Modified: Mon, 27 Oct 2025 21:17:46 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:77b288d7b99cbba1c5223b2effd88c74f44cc8e9b4aa63f36a5099ea77291627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18295988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3387a297d1c0ad97867259f8602e8405408cd54152885c2f97ff1f6c3fce4c`

```dockerfile
```

-	Layers:
	-	`sha256:f98422ae8e2e6ada996ca61101d8ba526fd763c2ba33439ca52d3188f50fb9e3`  
		Last Modified: Tue, 28 Oct 2025 00:53:02 GMT  
		Size: 2.5 MB (2488651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b916e7452269e4173ef2edabfb510f170ae8be5a9d8d82b3ace3f4303699b80`  
		Last Modified: Tue, 28 Oct 2025 00:53:03 GMT  
		Size: 5.2 MB (5197169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:924366eb7e80e8dc6a4e7f85926eb4cfa022ce24a4c50d3994f0293972d8bf87`  
		Last Modified: Tue, 28 Oct 2025 00:53:05 GMT  
		Size: 5.4 MB (5351219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f52bfa9123fdf1539b774ec5ca10d846473f2772a9b1e588ef22dbe8b5a47218`  
		Last Modified: Tue, 28 Oct 2025 00:53:06 GMT  
		Size: 5.2 MB (5198911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a368e83d133c4fffa2e9a5a52977d2cc247955c0382049c98eb9c1b539b54a76`  
		Last Modified: Tue, 28 Oct 2025 00:53:07 GMT  
		Size: 60.0 KB (60038 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:2c1a94c797b686a20513c68cac5e327159eb2330354b788a98c3c6d7482f0fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109899081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4665fd14b09f63dbd94b80de8dd6dac055c4af012a295d36bf4b66a0fc5634b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Mon, 27 Oct 2025 17:33:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 27 Oct 2025 17:33:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 27 Oct 2025 17:33:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 27 Oct 2025 17:33:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_VERSION=4.2.0
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 27 Oct 2025 17:33:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 17:33:26 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 27 Oct 2025 17:33:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 27 Oct 2025 17:33:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 27 Oct 2025 17:33:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Oct 2025 17:33:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 27 Oct 2025 17:33:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093755ebe708f5762c1cfcd47fa93247fb8d1c959c3f07743fdb4dc0567c5e5f`  
		Last Modified: Mon, 27 Oct 2025 21:15:30 GMT  
		Size: 44.3 MB (44340433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4138758646456366fd1c3f9512b510cc02297d1112dd25107888d9d34b6bcd1`  
		Last Modified: Mon, 27 Oct 2025 21:15:27 GMT  
		Size: 8.9 MB (8946831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e14bd110e1c1913aa25b7e1a9fbebcae02fd51941b6ed9957a9683ea95fa97d`  
		Last Modified: Mon, 27 Oct 2025 21:15:26 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6196d06d40ca82c78bb043f14499b9d8506cb6de1debf6217c3b0c07342d43cb`  
		Last Modified: Mon, 27 Oct 2025 21:15:28 GMT  
		Size: 27.7 MB (27738944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5386857fbad27b7748e5bc98799c6c3995e9604ffad0ce3dae5ecd47d81ac570`  
		Last Modified: Mon, 27 Oct 2025 21:15:26 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1437ece171ae97f16adcd848ffc96fa63cc6e8a0b0b9a988f56a23ece7cb66`  
		Last Modified: Mon, 27 Oct 2025 21:15:26 GMT  
		Size: 107.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0478d1a20b8b863a98f22f65e1753bb406c644836bb327cb2f2f2a8e6971ee02`  
		Last Modified: Mon, 27 Oct 2025 21:15:26 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b25b09a73d372d68fb8aecdbae6173dbdde2630db0c529ddd9c575b8e831dab`  
		Last Modified: Mon, 27 Oct 2025 21:15:26 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4bea7f789d894eb382daa687bcb56db1fb720de167a1aa1f9f62edc0720dc523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18900186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966fb2c64dea0f188dd7d561c879acd6ef924495256b6cc0b42907b0d477096b`

```dockerfile
```

-	Layers:
	-	`sha256:1ff1418b78f6af6966daa1bc990fd04567444890becb45b7c073581ebaa2594f`  
		Last Modified: Tue, 28 Oct 2025 00:53:15 GMT  
		Size: 2.5 MB (2488911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e7f1778cfb54bdc91f7f50be99394f0d5b0fcf43185f19554dd112d6e51139`  
		Last Modified: Tue, 28 Oct 2025 00:53:16 GMT  
		Size: 5.4 MB (5397610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2af7bee7195485fce701c6c32fe4279e577d277b220f117f5353cbc45097323`  
		Last Modified: Tue, 28 Oct 2025 00:53:19 GMT  
		Size: 5.6 MB (5554233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c4036beb9cb27249e8d4a397d37d871c6c7ed8049f97b5a483b9649f21c4c5`  
		Last Modified: Tue, 28 Oct 2025 00:53:20 GMT  
		Size: 5.4 MB (5399352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0762a5d3f49672c40ac2b9c1ff663f94881901c6e443923ffc50ad4338787dec`  
		Last Modified: Tue, 28 Oct 2025 00:53:21 GMT  
		Size: 60.1 KB (60080 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:a79eb2edea0ca2a807850ceb26b47b0299f9cff4a79d998c1178f4d4a3952501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110309278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91032e4eed09318240c4d750c4d59c21fd4c7750a936e1a81ad11425c7b60fe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Mon, 27 Oct 2025 17:33:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 27 Oct 2025 17:33:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 27 Oct 2025 17:33:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 27 Oct 2025 17:33:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_VERSION=4.2.0
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 27 Oct 2025 17:33:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 17:33:26 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 27 Oct 2025 17:33:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 27 Oct 2025 17:33:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 27 Oct 2025 17:33:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Oct 2025 17:33:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 27 Oct 2025 17:33:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2004b174a07d3b44a8bd9a0596cc0e149169afe32ef6b01ad03c7033e27ec81d`  
		Last Modified: Thu, 09 Oct 2025 22:20:14 GMT  
		Size: 39.5 MB (39502945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cb8f4e8a42c909ee73e09c07942a48a08874ce1f5a285fc50a116c19ecd05e`  
		Last Modified: Thu, 09 Oct 2025 22:20:12 GMT  
		Size: 8.7 MB (8701416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c767a341b0db8822a1331fd47aab76559b8587235dc3a2149468c046531bdbe5`  
		Last Modified: Thu, 09 Oct 2025 22:20:12 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46b1c1c5fc75d8d9783f807fd065260f95da43caca299ac74de567c2c7f63ce`  
		Last Modified: Mon, 27 Oct 2025 21:26:45 GMT  
		Size: 27.8 MB (27790232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf71c31e24b0d39ebc8f328a41262a94ff1e4d1213a93563b0b3aabafd935fc`  
		Last Modified: Mon, 27 Oct 2025 21:26:41 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eb2a30a8697b47e33d137a1d2ec3fc5adc2e9c0900ba9bf27017396794b3f7`  
		Last Modified: Mon, 27 Oct 2025 21:26:41 GMT  
		Size: 107.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c6358a89cff14230e605723040c60327842efdc3e541dacea27b59c300cc05`  
		Last Modified: Mon, 27 Oct 2025 21:26:41 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1921b919bd406406cf4cd0f04fb321ae52f7372abbc9e2b222ac0b8f6cc3d1a7`  
		Last Modified: Mon, 27 Oct 2025 21:26:41 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5f573fdd9d40d4192c19ef42be2ca1f016b3ddd0abe3792206eca9c8e0617a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18755577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6cd8df41f884dc9f90e043b968379bc559d60f41c8e2d0bf788c2dff0c5815`

```dockerfile
```

-	Layers:
	-	`sha256:62877167bb9a54de671d24e6f0975234068832bc9c7591b86e8fb41608d4bdea`  
		Last Modified: Tue, 28 Oct 2025 00:53:29 GMT  
		Size: 2.5 MB (2492304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:340c5ad8bd0f26058ee5912ec97323217aebc5cfb1c1a3a03ae37becc947fbd1`  
		Last Modified: Tue, 28 Oct 2025 00:53:30 GMT  
		Size: 5.3 MB (5348331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9188962ba6b51c484991b92a609e2109a74f86a9692bba7eead509efefd4f35e`  
		Last Modified: Tue, 28 Oct 2025 00:53:31 GMT  
		Size: 5.5 MB (5504966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0daf3c999428e767308d16a5971d12577fc70546a8600f7380af7f10e9c1b339`  
		Last Modified: Tue, 28 Oct 2025 00:53:33 GMT  
		Size: 5.4 MB (5350073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa9bb8d7345f267ed7ec1cbeb4daa9f948ed103a95dfc0fee8e109c69e78e68`  
		Last Modified: Tue, 28 Oct 2025 00:53:33 GMT  
		Size: 59.9 KB (59903 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:bb4ae25e1b11ebf53a028030f458cf11eaabe9750816271fe7b31218c64d7cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103056013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e779590673587cd6405745d394de2f07c479513f0ccc297df73be46c9ef4116`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 30 Sep 2025 17:30:16 GMT
ARG RELEASE
# Tue, 30 Sep 2025 17:30:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 17:30:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 17:30:16 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 17:30:16 GMT
ADD file:857dc87fbafae31881cff8c69aed267a033f5df226dd351ee89de918ad5678ce in / 
# Tue, 30 Sep 2025 17:30:16 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 17:30:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 30 Sep 2025 17:30:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 30 Sep 2025 17:30:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 30 Sep 2025 17:30:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 30 Sep 2025 17:30:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Sep 2025 17:30:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 30 Sep 2025 17:30:16 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 30 Sep 2025 17:30:16 GMT
ENV RABBITMQ_VERSION=4.1.4
# Tue, 30 Sep 2025 17:30:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 30 Sep 2025 17:30:16 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 30 Sep 2025 17:30:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Sep 2025 17:30:16 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 30 Sep 2025 17:30:16 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 30 Sep 2025 17:30:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 30 Sep 2025 17:30:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 30 Sep 2025 17:30:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 30 Sep 2025 17:30:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Sep 2025 17:30:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 30 Sep 2025 17:30:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 17:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 17:30:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 30 Sep 2025 17:30:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:ff47a256ba51b80e9880bc96be4ac2f094c47e0fcd7eec71bab85787cfa54b8b`  
		Last Modified: Mon, 13 Oct 2025 04:10:18 GMT  
		Size: 31.0 MB (30951381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb215f3d8309dbd90bffaf47a735d20998a64621dcd51d8e628d33850996b126`  
		Last Modified: Wed, 15 Oct 2025 17:10:30 GMT  
		Size: 35.1 MB (35149747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2205d1a9b137ba67ba92c3f3423e6f9ebd072802eca76d325d08c35b8210a19d`  
		Last Modified: Wed, 15 Oct 2025 17:10:26 GMT  
		Size: 9.8 MB (9792678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a7e77c9f3a33f075cafd557d3b7976d905751ccccaa44a65892b43de51765d`  
		Last Modified: Wed, 15 Oct 2025 17:10:24 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddc2a25a71aac75b44bbf90c1ecf40b49d6e0d5c189efbaca7f78ccafad842b`  
		Last Modified: Wed, 15 Oct 2025 17:20:44 GMT  
		Size: 27.2 MB (27150968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31a9d701498de45635892f484e98c7dfa01299a463b2a38ccdb854d055024f2`  
		Last Modified: Wed, 15 Oct 2025 17:20:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48011a278044c0bcf085e6f4058b9151c1bc1092206d6bafc79a976d5d52ec1f`  
		Last Modified: Wed, 15 Oct 2025 17:20:42 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1388cd445ad3740337ff7cf745d3378089dc01a77643416ff1d1cbea3ef9fbe8`  
		Last Modified: Wed, 15 Oct 2025 17:20:42 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7815f786f27d440b2767c44ad5097bc34183e5b656832e05d21111715161a4`  
		Last Modified: Wed, 15 Oct 2025 17:20:42 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4d87ec971f842c463e1c59a5a64bd01c2762f678ffe89770a084bc65b3d3a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18720295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efc8b15899c3b5d7de0cddd5d6070edaaba8c8400f853544a1e65f27247722e`

```dockerfile
```

-	Layers:
	-	`sha256:eece4d2f13d5421b6cd528ff1368591b2d004095c9d77caf653c1635b0cc91d4`  
		Last Modified: Wed, 15 Oct 2025 18:53:03 GMT  
		Size: 2.5 MB (2476311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26569d3db8d293b1175bfd255059d65332c12fd00fade3649f0c5e09ff9b0762`  
		Last Modified: Wed, 15 Oct 2025 18:53:05 GMT  
		Size: 5.3 MB (5342764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ed463f9c5ba99a258720533290570925a7a186a2e2ec41fd2dbce73961ac4c5`  
		Last Modified: Wed, 15 Oct 2025 18:53:06 GMT  
		Size: 5.5 MB (5496812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:576b32e10372dd795083ccaf0769f9905187d103d1975a8ec4c30ebda36c2a2a`  
		Last Modified: Wed, 15 Oct 2025 18:53:07 GMT  
		Size: 5.3 MB (5344506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61f08d37bf1d630d2ea8af68f57f65a427df2f1e272b7e120a45a6970160f758`  
		Last Modified: Wed, 15 Oct 2025 18:53:08 GMT  
		Size: 59.9 KB (59902 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:3dde9d6a7a2f48097b500049da86d97082752bca60f2238e35953c400bbb0842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103857581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26332622b7944769d8e74007e6572eb9a0c9b1b2f788087fdfe374060c0bf85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:05 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:07 GMT
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
# Wed, 01 Oct 2025 13:02:07 GMT
CMD ["/bin/bash"]
# Mon, 27 Oct 2025 17:33:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 27 Oct 2025 17:33:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 27 Oct 2025 17:33:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 27 Oct 2025 17:33:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_VERSION=4.2.0
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 27 Oct 2025 17:33:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 27 Oct 2025 17:33:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 17:33:26 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 27 Oct 2025 17:33:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 27 Oct 2025 17:33:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 27 Oct 2025 17:33:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Oct 2025 17:33:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Oct 2025 17:33:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 27 Oct 2025 17:33:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfef216f89f75dd22246310dedeacb61378035af439cf98de2054cd8fb12cb52`  
		Last Modified: Thu, 09 Oct 2025 21:52:36 GMT  
		Size: 38.6 MB (38570069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b34c7124f578d91d47c14d9e1b176d568cfd09df610ead304f0ef78de75cdf`  
		Last Modified: Thu, 09 Oct 2025 21:52:33 GMT  
		Size: 7.6 MB (7556901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7538ff595c88776dc6d53df2cfd438aaafc0845c1551f2ad5aa284aebb414d`  
		Last Modified: Thu, 09 Oct 2025 21:52:33 GMT  
		Size: 9.6 KB (9591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b3404a16f6118935dea12f5e2109aa56a78ecc63bb63997e6bf905363f9c95`  
		Last Modified: Mon, 27 Oct 2025 21:23:33 GMT  
		Size: 27.8 MB (27813129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ee101b005bea958c1d973c6b0e94d6eab9f041745caeeee084c0d3915dbd48`  
		Last Modified: Mon, 27 Oct 2025 21:23:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df989e4674c18080a80e88068c6903ed5f710d1c7b82080cbffb0d396d3ab3`  
		Last Modified: Mon, 27 Oct 2025 21:23:32 GMT  
		Size: 107.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb06cd6504773a2ec6537dd0171cd9ecd2f035b5ccc160ce146be21afa34e7d`  
		Last Modified: Mon, 27 Oct 2025 21:23:32 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dc6f6f6cd24f0c9b364d4fa7323d4d010420e90585244148722489c628e9d9`  
		Last Modified: Mon, 27 Oct 2025 21:23:32 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:665ed985c8166204c719ab289825857dc5e01c80d7bb64e819d79e8066435f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18381353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57be69eda143eca5d6a4c02f1072c5ce1165e5c6f6413b20ecc247d3be21f6ef`

```dockerfile
```

-	Layers:
	-	`sha256:a74b7b0577be5d8a3b8e4ec51be05b8d5357ae7cecd8496e3865a3bae08bae9f`  
		Last Modified: Tue, 28 Oct 2025 00:53:48 GMT  
		Size: 2.5 MB (2489961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:137caae4f5b73f3631947c3d28041a80f3171b69bd9fa1f938122aeeafe5d67d`  
		Last Modified: Tue, 28 Oct 2025 00:53:50 GMT  
		Size: 5.2 MB (5224836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9c7342283accf214ea8a48fb286effe92689f75ede28912f8907f8592870f85`  
		Last Modified: Tue, 28 Oct 2025 00:53:51 GMT  
		Size: 5.4 MB (5380137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a1ea7f7d869ebc87e258096f76276dd3c9b79ba4fb362de3d21ecbb5cd20ee9`  
		Last Modified: Tue, 28 Oct 2025 00:53:52 GMT  
		Size: 5.2 MB (5226578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e1da4f803681b6303ace5d321041ed985e7746f39afd99a44a9afe7fbc28bd8`  
		Last Modified: Tue, 28 Oct 2025 00:53:53 GMT  
		Size: 59.8 KB (59841 bytes)  
		MIME: application/vnd.in-toto+json
