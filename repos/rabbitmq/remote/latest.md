## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:fb4b55518e24ec0bc72b11dc9986553c6fb555fb78dc9af3d8885d8a106e6b2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rabbitmq:latest` - linux; amd64

```console
$ docker pull rabbitmq@sha256:5446af87075b2e1cb9676cd2c7406616fa3754b7c252e77cd0a6983da89661a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104636495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec60adc9a43b77a0424dbc434d6d66b48fb39b55c8ce21f6220f98d43becaa0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 25 Jun 2024 11:05:22 GMT
ARG RELEASE
# Tue, 25 Jun 2024 11:05:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Jun 2024 11:05:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Jun 2024 11:05:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Jun 2024 11:05:22 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 25 Jun 2024 11:05:22 GMT
CMD ["/bin/bash"]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 25 Jun 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.3
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 25 Jun 2024 11:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 25 Jun 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4876daddbf944ffb4d9f3cfd91ca4e09617c607c972506843d5d095085a029f7`  
		Last Modified: Tue, 02 Jul 2024 03:20:40 GMT  
		Size: 46.0 MB (46017221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f132dacddba4200a253e7c64b910194bafd7f806fb54f656cafffeaf0b2c1b8`  
		Last Modified: Tue, 02 Jul 2024 03:20:39 GMT  
		Size: 7.5 MB (7483843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac5d3f9c2e200ec3a2e42d75dc36abf6967b48f93a01b359b6cc148a70c70ba`  
		Last Modified: Tue, 02 Jul 2024 03:20:39 GMT  
		Size: 10.7 KB (10715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2758cbe5a6a589b6c490e8c762eee0394e68e3171a25192e002f5c8990b715d8`  
		Last Modified: Tue, 02 Jul 2024 03:20:39 GMT  
		Size: 21.6 MB (21588915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672fbc730d9898ed99633c7b49415a3cd891d6fa259b2c885b0c4ce5f088e955`  
		Last Modified: Tue, 02 Jul 2024 03:20:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4841fd0117c606aa813942a17533d4912d42880b273f2a200eaf35863b1047`  
		Last Modified: Tue, 02 Jul 2024 03:20:40 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9a1348b7b6b4496b2e54274626887a3e9e9304a40e57f16f325f134dace35b`  
		Last Modified: Tue, 02 Jul 2024 03:20:40 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5303bdaacb8c58641149fa75e03e5b63a8e6b9dfd24ac25c7e30d9f3af22bb5`  
		Last Modified: Tue, 02 Jul 2024 03:20:40 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bdc7767ead406a997e56ba63330b2e7f924d84904c6f5b4617735c7029b43d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18553925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbe1e070b7bc5668925997d903b6094b0726e8697e89c25abf25984b620c79c`

```dockerfile
```

-	Layers:
	-	`sha256:fc747c134fb35b47ec8a0890e7d4b2d8188cb273ab26866664c1b7796c5e7a28`  
		Last Modified: Tue, 02 Jul 2024 03:20:39 GMT  
		Size: 2.9 MB (2884445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:419630819119300048ae6fb9107e296b5196920d863cf114afc841b55e1b0f1b`  
		Last Modified: Tue, 02 Jul 2024 03:20:39 GMT  
		Size: 5.2 MB (5160717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82917f5857f69ef4588a7e2b0ee220e31e937f68c1a2aa56fd81ddbcb2143a7f`  
		Last Modified: Tue, 02 Jul 2024 03:20:39 GMT  
		Size: 5.3 MB (5285294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df1cfe3f2cdf49bc0eb06ce9323cd9d10e97523c0524daf5bebdc4eadc1d8e1a`  
		Last Modified: Tue, 02 Jul 2024 03:20:39 GMT  
		Size: 5.2 MB (5162091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbd01637c7fb484281beae12de71dc785a4e3ef1016893461447124d7810799e`  
		Last Modified: Tue, 02 Jul 2024 03:20:40 GMT  
		Size: 61.4 KB (61378 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:fbc68dcfe9f2b4db7eba4d7a892f49109c890d28c339572ab37424eab350c0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87730547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9897f878a42727b531f15e11941c72bfe1bf104d72f0697329ecb3a23e69c331`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 25 Jun 2024 11:05:22 GMT
ARG RELEASE
# Tue, 25 Jun 2024 11:05:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Jun 2024 11:05:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Jun 2024 11:05:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Jun 2024 11:05:22 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Tue, 25 Jun 2024 11:05:22 GMT
CMD ["/bin/bash"]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 25 Jun 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.3
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 25 Jun 2024 11:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 25 Jun 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f6d2cceb710e897ef3b81e28ea21268aa6d28deae90ac1ab9602ff738c88a650`  
		Last Modified: Thu, 27 Jun 2024 20:18:40 GMT  
		Size: 26.6 MB (26638444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43943d8892639acaecade0ac121e17588ef70d441851709ea2ea38583a2e9b02`  
		Last Modified: Wed, 03 Jul 2024 00:13:55 GMT  
		Size: 33.5 MB (33497597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a110c906ee09e45bee4507c444c1d8fd20f15ff19000c4e245ee5a9fe867fd74`  
		Last Modified: Wed, 03 Jul 2024 00:13:55 GMT  
		Size: 6.1 MB (6077355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56672f68b9b4f585cebfcc64518ef69b276b4bd8e98eaf0c6bd7199fd53a140`  
		Last Modified: Wed, 03 Jul 2024 00:13:54 GMT  
		Size: 10.7 KB (10699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6fdd3b4f13f5d14a605c1f1d6a93b36db9a01bc31e9815369911095a7bbfc6`  
		Last Modified: Wed, 03 Jul 2024 00:13:56 GMT  
		Size: 21.5 MB (21504700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffae6fb63139d0c63f7154f7245f5d42f8dbb167e3b9fcde5d7b76f07c31966`  
		Last Modified: Wed, 03 Jul 2024 00:13:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c10bbfe93ef5e7235ff1dbaa7cba51b7a6931edc627688071f204c4bbe1050a`  
		Last Modified: Wed, 03 Jul 2024 00:13:56 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4106129de91494da3e76afd7deae49da7deae257a58e4320fcaf88a10224240`  
		Last Modified: Wed, 03 Jul 2024 00:13:57 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c022984cf85d2b17fc03d4ac5935c6603e2fd438280d2cda8e94c1dd5f1b72d`  
		Last Modified: Wed, 03 Jul 2024 00:13:57 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:16d4bc11f5ea105fa942be1890806dae63d21f4475186295eb1fe470e262e27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18009729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e8abed72fa1576ae8e0f3c6eccfd5f80e66004cbd0a196402b10ef35448115`

```dockerfile
```

-	Layers:
	-	`sha256:5b48536b21d5388d13d27cc2e296bb23161ef226c003556863666c9645b1f65d`  
		Last Modified: Wed, 03 Jul 2024 00:13:54 GMT  
		Size: 2.9 MB (2885108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a91934c47eaae918319d8cc1b4eb57447a9c18daf5fb39a6840956a524b7679`  
		Last Modified: Wed, 03 Jul 2024 00:13:54 GMT  
		Size: 5.0 MB (4979870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e13d308994bcbbf4b4677f6f28a843e0829b8a208dc0e5284f37c8e5723c7199`  
		Last Modified: Wed, 03 Jul 2024 00:13:54 GMT  
		Size: 5.1 MB (5101943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:524e4c57f4f7a618a553c714ff2bfd00718d2d32e6ce6e6dbb650e1411f30382`  
		Last Modified: Wed, 03 Jul 2024 00:13:54 GMT  
		Size: 5.0 MB (4981244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8fc3986d3e09df75d143d388c9bb9b9451921ca45255532f58b085f5b25c990`  
		Last Modified: Wed, 03 Jul 2024 00:13:56 GMT  
		Size: 61.6 KB (61564 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:2e193113ead88754c12cf876eed644c2bce1e14c2c47e5b76788dca879fffad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100091274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb5c5610cce5aac916ecd9a30ef63950d63c7f25b8e71bc28a221dd9c7b63d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 25 Jun 2024 11:05:22 GMT
ARG RELEASE
# Tue, 25 Jun 2024 11:05:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Jun 2024 11:05:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Jun 2024 11:05:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Jun 2024 11:05:22 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Tue, 25 Jun 2024 11:05:22 GMT
CMD ["/bin/bash"]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 25 Jun 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.3
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 25 Jun 2024 11:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 25 Jun 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841c7debea38643b1448ee0b0f5a20dd2d352a4798fef5bd53006351144fdd3e`  
		Last Modified: Tue, 02 Jul 2024 22:55:29 GMT  
		Size: 44.1 MB (44089611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbee6e225309433351bfe95f421beb68f17ef039e08669cc4dbaecd3e7a6f6ad`  
		Last Modified: Tue, 02 Jul 2024 22:55:28 GMT  
		Size: 7.1 MB (7133044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f985412444972eec31ba7ee305980d05c4bc6ba6bb5bc315ec4d6ddd9c4119`  
		Last Modified: Tue, 02 Jul 2024 22:55:27 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3963ca21a1dd7370e96767287cd7d9782fd9a35a7db0608c31e3097abe300b6e`  
		Last Modified: Tue, 02 Jul 2024 22:55:28 GMT  
		Size: 21.5 MB (21496149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a9a59a20c0e7ed8b16ee11ee65fe0a478a47dc0f21937b188d5588f7aece1a`  
		Last Modified: Tue, 02 Jul 2024 22:55:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b5aac481875c094b614390394083e07ce24b530da9faac79ffae083892288a`  
		Last Modified: Tue, 02 Jul 2024 22:55:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a87f0ba5153f05bdaa31d2f2fabb99bf3decb5e12d2ff25cdd4776e9a7f8129`  
		Last Modified: Tue, 02 Jul 2024 22:55:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005225a31d1f9ec042910c88833ca1fee2c28e8eed000b49b49d078ed7aedf22`  
		Last Modified: Tue, 02 Jul 2024 22:55:29 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:536439ae249d3f29558f97d813980f21ad2e069fde6575ffdfa56068327c2486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18542093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c197df87eaca2fa0a4140c9bcae1c02815fd92086d41728bbabdd9ba0041d1fc`

```dockerfile
```

-	Layers:
	-	`sha256:249a01559e87f32b0621bca453ab88ad1f2a9267d44d43078ea518b3fedf250c`  
		Last Modified: Tue, 02 Jul 2024 22:55:27 GMT  
		Size: 2.9 MB (2884717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f164a61e6425b98fbd3052a26c31537b7e15a17125990b7c05df4dd1ecae70e7`  
		Last Modified: Tue, 02 Jul 2024 22:55:28 GMT  
		Size: 5.2 MB (5156578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e1c4f2cc12c624f25b2887570f8b6d90c4fb3291784effcf79acd5175bf895f`  
		Last Modified: Tue, 02 Jul 2024 22:55:28 GMT  
		Size: 5.3 MB (5281167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881aca3d627db35e226aafd9987968b9d050d551120d9d13f9807841117e3d45`  
		Last Modified: Tue, 02 Jul 2024 22:55:27 GMT  
		Size: 5.2 MB (5157952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfdc024f1ad683eee74ae1f5477db8658d2a21a706516ea3bc30cd3b0cf48b91`  
		Last Modified: Tue, 02 Jul 2024 22:55:28 GMT  
		Size: 61.7 KB (61679 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:b15b1979a679ad337ebbef569670bb58a958b23961812e950119931e7f930d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103464280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d331bd3b937f566b0c6e44046f13b5c3620ae23667b49a460db72ae5f40a512`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 25 Jun 2024 11:05:22 GMT
ARG RELEASE
# Tue, 25 Jun 2024 11:05:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Jun 2024 11:05:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Jun 2024 11:05:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Jun 2024 11:05:22 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Tue, 25 Jun 2024 11:05:22 GMT
CMD ["/bin/bash"]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 25 Jun 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.3
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 25 Jun 2024 11:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 25 Jun 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb761c3b153703b2d6a0cca9b4b1a0893864b79f1f4b437c03fa45fdfd6aa9e`  
		Last Modified: Tue, 02 Jul 2024 19:59:21 GMT  
		Size: 39.6 MB (39598453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2982e1b76065c06482fe58bfa4b9dc7996c59988ac39649b56bb0c5177293700`  
		Last Modified: Tue, 02 Jul 2024 19:59:20 GMT  
		Size: 7.9 MB (7868576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201cc41ce7dbd4038ee1560aeef2a1e196a02cda9b422b06d9ad865f9eee8e8e`  
		Last Modified: Tue, 02 Jul 2024 19:59:19 GMT  
		Size: 10.7 KB (10711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f336d73384cd0e4af395b555203b0526bfa30d4b3042d138952d86804087be`  
		Last Modified: Tue, 02 Jul 2024 19:59:20 GMT  
		Size: 21.5 MB (21523708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9455bd13848079a074fce6c0e44fc682d9d1d311a0ca155462502da016b31221`  
		Last Modified: Tue, 02 Jul 2024 19:59:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a9e44528a206111cc0c73209ddf5e9d8919de5bc5ab313a9bfd748217b2109`  
		Last Modified: Tue, 02 Jul 2024 19:59:21 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eed929c8cb124a8b497a2e0e3a39df0101e76c6166985921584cbf6831a882`  
		Last Modified: Tue, 02 Jul 2024 19:59:21 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada7be030c217b2bbd85ca1b17c9df776dde1263011e6e1fd2ffc9fb5f60954b`  
		Last Modified: Tue, 02 Jul 2024 19:59:21 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7ba6157e2608c6839b663c097fb7fac6d64b28bacb182b27a19fabe7f9d5a6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18440167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59740ff05d077c1c4290c0711b4f7c6a6ad2807660a6a5e63f34159a34c72ecc`

```dockerfile
```

-	Layers:
	-	`sha256:deaefb9568ac0a85f1998a8aba232e51a6cd5b67ae7077ba174947c1c06712e8`  
		Last Modified: Tue, 02 Jul 2024 19:59:19 GMT  
		Size: 2.9 MB (2888202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5e7f0051c42b083457355d3b57699f608c63cceae92a185e4c7d294929e0ce2`  
		Last Modified: Tue, 02 Jul 2024 19:59:19 GMT  
		Size: 5.1 MB (5121888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdf0f02095db5a365d350c81e07a4cb7782ae751ea427e3e986c5362a9e248a9`  
		Last Modified: Tue, 02 Jul 2024 19:59:19 GMT  
		Size: 5.2 MB (5245381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91a5052cfa4ec6043d4958e1424d60cb8a188d5c59eb993f6a3a466cc29724d4`  
		Last Modified: Tue, 02 Jul 2024 19:59:19 GMT  
		Size: 5.1 MB (5123262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:032b6b4a2f3d3be6e283099109a90aef3b2ddca2f157e982038984d1516d8fcc`  
		Last Modified: Tue, 02 Jul 2024 19:59:20 GMT  
		Size: 61.4 KB (61434 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:2ce02349a3b072f85be5eb15225061bd26a1ca35abb4e46eb0249d21f71f13fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94341251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc92ccbe12d7995b3a5ac558bcd33192f204313a4604929a9085c1e1545d1ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 25 Jun 2024 11:05:22 GMT
ARG RELEASE
# Tue, 25 Jun 2024 11:05:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Jun 2024 11:05:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Jun 2024 11:05:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Jun 2024 11:05:22 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Tue, 25 Jun 2024 11:05:22 GMT
CMD ["/bin/bash"]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 25 Jun 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.3
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 25 Jun 2024 11:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 25 Jun 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9414f2a6b9d142f5ee5a4dc404276ed100ddba4dbe1e522174237d9f6d61b3b3`  
		Last Modified: Tue, 02 Jul 2024 10:17:21 GMT  
		Size: 38.2 MB (38235912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830c9e200b9883650cbc2908bf341af1cafb2cad0f4d09a67aa27655eb3e7b7c`  
		Last Modified: Tue, 02 Jul 2024 10:17:20 GMT  
		Size: 6.5 MB (6535437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8b3318f3a4c7f6391b33737e71bab6a3e90842102e39de398d9291c75391b0`  
		Last Modified: Tue, 02 Jul 2024 10:17:19 GMT  
		Size: 10.7 KB (10748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e453040bf8a4abc87da4215b358ab3798cd1356f7a420b153567d4ad5cb381`  
		Last Modified: Tue, 02 Jul 2024 10:17:21 GMT  
		Size: 21.6 MB (21556870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d319a506b1688689e296c5e8984848efdfc7e1653980f01d85c3d201b6f5754f`  
		Last Modified: Tue, 02 Jul 2024 10:17:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e9e0719365679fc94a4af64a0c9bc1fc5046a5705db1c97333ed9fbe7349e`  
		Last Modified: Tue, 02 Jul 2024 10:17:21 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdb178689dd755b7812b73779da3bc66bfa87423b1995147603ea975ed997a2`  
		Last Modified: Tue, 02 Jul 2024 10:17:21 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb9da630d98194d48f0b1f552d68d22e023f398039fd8566a38b083cf91967e`  
		Last Modified: Tue, 02 Jul 2024 10:17:22 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3fd2a30984b4601cd3d76d374799e12cdd42624b8dfd6e7e40290885f4efacd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18081278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b429987dc71f01e5fc995aae833e69c1c2bf281e4b99b914e8cfced22b9366b9`

```dockerfile
```

-	Layers:
	-	`sha256:ac6e2b9b4ff944caf158777ae1bc0a064913a2181e3f85e70df55039ffbef0f7`  
		Last Modified: Tue, 02 Jul 2024 10:17:20 GMT  
		Size: 2.9 MB (2886052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b3e6ffbe42eacb84b05465f4003068754964cf3621f05b6d9230a642808297`  
		Last Modified: Tue, 02 Jul 2024 10:17:20 GMT  
		Size: 5.0 MB (5002997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce2560aadf37022e1ea1488a7fabf880fcf0eed646032a0f8e4ffe51d756965a`  
		Last Modified: Tue, 02 Jul 2024 10:17:20 GMT  
		Size: 5.1 MB (5126480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf05f22ba71e1d606d1c6d80df4a235902c36c32fa37d1be13337fb5de2a2844`  
		Last Modified: Tue, 02 Jul 2024 10:17:20 GMT  
		Size: 5.0 MB (5004371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdfd8e11b525a7b6ff435d4c7c9fe88eaca601a665bf1b59e68a480481b065ab`  
		Last Modified: Tue, 02 Jul 2024 10:17:21 GMT  
		Size: 61.4 KB (61378 bytes)  
		MIME: application/vnd.in-toto+json
