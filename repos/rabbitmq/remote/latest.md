## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:3799a91bcea4080aba5a0a0cf6aea0307a22a67a24f129053b7db52975de1a01
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
$ docker pull rabbitmq@sha256:2ef5eeeca7c59bf3bc9246107a52a55bf1bcb985cff1c5c5fb17cd1ee310d0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87731879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83db6653a0d37aa35385d2bf8438c0a5a38e3aadd6cfb851c78ee0d6bef452d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 03 Jun 2024 10:36:14 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:36:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:36:23 GMT
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
# Mon, 03 Jun 2024 10:36:24 GMT
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
	-	`sha256:a7d6949ac966fed9a061428466d68cc616d739583d012661c3c826f017b64981`  
		Last Modified: Mon, 03 Jun 2024 10:46:59 GMT  
		Size: 26.6 MB (26639042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0bdbc0f25bbff55e48c20545ce8a89e2e6f95a0cc8f14c22f246a6e751fd1a`  
		Last Modified: Tue, 25 Jun 2024 23:04:50 GMT  
		Size: 33.5 MB (33497519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128651c0c62d865026b4eb74ab2d2902682ecdbce8f6163254b22ecae2d0ca73`  
		Last Modified: Tue, 25 Jun 2024 23:04:49 GMT  
		Size: 6.1 MB (6077330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18843e16fc6203359a16eafc4f87f06c89cea9ece57e48f089bae1d1689977e4`  
		Last Modified: Tue, 25 Jun 2024 23:04:48 GMT  
		Size: 10.7 KB (10727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4ed1110b7aeb8e7bb835777b1515ac5393d5866475eefbec429045435ac9d8`  
		Last Modified: Tue, 25 Jun 2024 23:04:50 GMT  
		Size: 21.5 MB (21505508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22332bb790935d767f5148e6b08559b49dbe383c75750cb39cf2e6cb0e624cf`  
		Last Modified: Tue, 25 Jun 2024 23:04:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b96643ba31553100cdf17d6222d9a794af376aa4fde09bffee8340df548336c`  
		Last Modified: Tue, 25 Jun 2024 23:04:50 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f7e6161de83b06e421c1a6f4654d49b4c52b3c7687e8be987d0b2627615149`  
		Last Modified: Tue, 25 Jun 2024 23:04:51 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dd5bf910dfb4a2cc67c369a1573b64ae21e6b31599e914e48672ea524748e2`  
		Last Modified: Tue, 25 Jun 2024 23:04:51 GMT  
		Size: 837.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:58ee520d428cc86644f4ac7f92183faf5f2933335f3f1ba4c9af7c70c8d1fe2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18009717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac8c3513304c5792fd7a642caea40a0ec80baacceff18ff78ff80fd3b95be3a`

```dockerfile
```

-	Layers:
	-	`sha256:375dce45ed830b3bd8b8d5ac6c900a4aa070e414806a21f5c46aed56a155602a`  
		Last Modified: Tue, 25 Jun 2024 23:04:49 GMT  
		Size: 2.9 MB (2885108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c244301a8985ca56fb7bac31219a6dce612568064c930ecfce037bc6f3e9d0`  
		Last Modified: Tue, 25 Jun 2024 23:04:49 GMT  
		Size: 5.0 MB (4979866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:123b76205c3edb47126c3bc43272ab66ad7463fea54a85ddfe29fe3f1ae9e7a3`  
		Last Modified: Tue, 25 Jun 2024 23:04:49 GMT  
		Size: 5.1 MB (5101939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe568042c80b36c9881492fd3cef395f6a8b27699664483dc6e7568b0dccc0b`  
		Last Modified: Tue, 25 Jun 2024 23:04:49 GMT  
		Size: 5.0 MB (4981240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d5b70e85c4f102c1210b7ce70c11bd8d539e41fe19872e1350c72834ba1cbb2`  
		Last Modified: Tue, 25 Jun 2024 23:04:50 GMT  
		Size: 61.6 KB (61564 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:d266f09759216c23930d20c62d889347d355e953cd50c4cc487c0d7c5dec38f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100094551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3818a309c68117aadcfd389c0d1ea466fd4bd8a083165c1de060d4f222e3445`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2b1204d9b12b9f62d4682ff4efee5af710284e24e1f1baa40e7bad3b682cdb`  
		Last Modified: Tue, 25 Jun 2024 23:45:04 GMT  
		Size: 44.1 MB (44089614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daee8a9aeba9da7a2fd0d784def0fb7c42651747035efd6347c696ea19b4edb`  
		Last Modified: Tue, 25 Jun 2024 23:45:04 GMT  
		Size: 7.1 MB (7133053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c991c043aefce68d753e0ea072540011395ac45e7f53de6cff1e9f472cd5285`  
		Last Modified: Tue, 25 Jun 2024 23:45:03 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07723356596b6a1ed649c231dcb864ffc0af5857c4c61f1bb0947483a8fe5422`  
		Last Modified: Tue, 25 Jun 2024 23:45:04 GMT  
		Size: 21.5 MB (21497625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a8239c56915f0fc309ef4111e8411322134b9640552f0781d42eb0ee7fe045`  
		Last Modified: Tue, 25 Jun 2024 23:45:04 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeb679ae401c3eebcea0b6c08d04f0f0069a8e2c293f27741999b71a59f584b`  
		Last Modified: Tue, 25 Jun 2024 23:45:05 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0176b5a5df08f0be43768b5ed264f0c06d0e541f5f289701a95f897f9b7ff2c`  
		Last Modified: Tue, 25 Jun 2024 23:45:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43185b159d4041f3aafe2adbbf05abb4f62e305c2df5af6ba576856214589b70`  
		Last Modified: Tue, 25 Jun 2024 23:45:06 GMT  
		Size: 837.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:de9a7946388441aa38a49a7e8783b16c4fa9e56dbc668daedae2c6092976d253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18542081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552879ee4b014e9abb886656df7521dadb37b33beafc822598cf05207b00fcff`

```dockerfile
```

-	Layers:
	-	`sha256:b95e2401fce8f125a4f45a68a0ba4ccf5211a38f4c98cc9ca59972130a5d6e04`  
		Last Modified: Tue, 25 Jun 2024 23:45:03 GMT  
		Size: 2.9 MB (2884717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:160845be5c621b78ee6e72c14b2786996d096f44f766b60e3b50261d064507f4`  
		Last Modified: Tue, 25 Jun 2024 23:45:04 GMT  
		Size: 5.2 MB (5156574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9ad49df4e9e4930705d7d271b19b24f3490e8d62400e9b64cad004b26890e61`  
		Last Modified: Tue, 25 Jun 2024 23:45:03 GMT  
		Size: 5.3 MB (5281163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3afcbf465524e9e2a2ad3a0599b20b2a1b7ee265600c58f5e5e92ce89c050db5`  
		Last Modified: Tue, 25 Jun 2024 23:45:03 GMT  
		Size: 5.2 MB (5157948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7b9732c8d2bb974f2e2cdf252127dd853127dbb06680f031e41f9a70144748`  
		Last Modified: Tue, 25 Jun 2024 23:45:05 GMT  
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
