## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:4fc6a2c182ab768f233f602a965684e1db91f0b01562d4efa5ca35de8db148db
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
$ docker pull rabbitmq@sha256:a1fb6ba3eff9a226074940f27beccfd2e4de989d3d4ebb0b1272e9f78aa44dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107264831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3aa0cf66f6986cd49153e5b33ec5ea67c985595bc988a3c249140dac0011d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 28 Jan 2025 21:27:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_VERSION=4.0.5
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 28 Jan 2025 21:27:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 28 Jan 2025 21:27:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9d8cdae0bfdbcb9216751b7083c71c801fef19eacbf6213c49c65109d7d49c`  
		Last Modified: Wed, 29 Jan 2025 00:33:18 GMT  
		Size: 48.4 MB (48409559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a3f66ab885804bad9467aea7b2c7d20b8ca2df81d0e07d80d2d679f3fdab30`  
		Last Modified: Wed, 29 Jan 2025 00:33:17 GMT  
		Size: 8.2 MB (8169285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a6cbddab14a2f8b6a4673025842fac29a15aa6d5aadc39a038d67e75ec625`  
		Last Modified: Wed, 29 Jan 2025 00:33:18 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a04a89a0d52a7a2d1dd632ebb160ed45afcbb3eb000436d8e3673a64fafa49`  
		Last Modified: Wed, 29 Jan 2025 00:33:18 GMT  
		Size: 20.9 MB (20922780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed804c5d0e7bb97ad4ca54ee811eb2f93d7a39e2a0a339cf5e70e2eb00581734`  
		Last Modified: Wed, 29 Jan 2025 00:33:18 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c7470e7775471726f454ca6121c6a26f0c95721eeab9ace18ebe53c49c311`  
		Last Modified: Wed, 29 Jan 2025 00:33:19 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d938ff824fed991d0d120548cf6234bf9845ad67005d3d002057aaca1644a`  
		Last Modified: Wed, 29 Jan 2025 00:33:19 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febd59dd43dfc4acefef3e1bcc0aa5a2fef36246ffe7c523abe001035d1e8c14`  
		Last Modified: Wed, 29 Jan 2025 00:33:19 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2146d993eb5c7fc64ea6c7a9164e52125ca0e9a02cff5b97766c3e472384eed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17926251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377c68e5f8c81a4bf9c46e1b9e7039c6af12e072791e5fe293e1a0cda2e09f71`

```dockerfile
```

-	Layers:
	-	`sha256:484c999a6c11fcbaa78a5f2113cc3eb62d5d833d197e26c32a4f323bce5ea5e1`  
		Last Modified: Wed, 29 Jan 2025 00:33:17 GMT  
		Size: 2.2 MB (2245159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b67c398d2652d6bf22246b8973c620fe94ccbec900316e682fa7ee8236786cc`  
		Last Modified: Wed, 29 Jan 2025 00:33:17 GMT  
		Size: 5.2 MB (5204130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a69bcdba756cb349e8430e3558b642b07ec09895b7463de352b649dcb77a28b`  
		Last Modified: Wed, 29 Jan 2025 00:33:17 GMT  
		Size: 5.2 MB (5211348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c178c74c938282a08c1ccb0a4c5ee98735e4147798df36d2c36c883bd64b9887`  
		Last Modified: Wed, 29 Jan 2025 00:33:17 GMT  
		Size: 5.2 MB (5205872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:341bf0483ccf0e09f77e1784ac8c0cdd2fcf1702a5de037c18fb741a474af18b`  
		Last Modified: Wed, 29 Jan 2025 00:33:18 GMT  
		Size: 59.7 KB (59742 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:02b390ccd2b19affe3b3ff8b94f41584be8d33134fbbbf02e075f345aea7a5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89819855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b1efc980f8bdc31cdcb136bd130321fb0e1bc3d57e7ea6ea6f234eaf79f533`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:50 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:53 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Tue, 19 Nov 2024 16:18:53 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 28 Jan 2025 21:27:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_VERSION=4.0.5
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 28 Jan 2025 21:27:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 28 Jan 2025 21:27:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddbe0fa0ca64bcd247be40bee928e934c0900148f9c757cb0e8d29f68579d49`  
		Last Modified: Wed, 29 Jan 2025 00:34:07 GMT  
		Size: 35.4 MB (35445401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a564914538c5bc366150ddf7111a42ebd75e9f9d96245d825e5c6fb93bbe47`  
		Last Modified: Wed, 29 Jan 2025 00:34:06 GMT  
		Size: 6.7 MB (6668105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d131e21e20cd8eca791b4d665fe37142b67723f37fb3ca13794d5061b0fbd772`  
		Last Modified: Wed, 29 Jan 2025 00:34:06 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258de73350d024bc2b39ae8a393c21cd6d7600a68d1d763db77ea49b5d599670`  
		Last Modified: Wed, 29 Jan 2025 00:40:15 GMT  
		Size: 20.8 MB (20825439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd637b134fa4730f6ce8481e138a3c14ca4f05f246914b2776fd477a007910b7`  
		Last Modified: Wed, 29 Jan 2025 00:40:14 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcc398e4d560a6ecf9ca416d3851979f0bea8ba12b745ec7a3253323beb6efb`  
		Last Modified: Wed, 29 Jan 2025 00:40:14 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e7c0bd91f2aa75079134abeae4a083cb5493352d2f38f86a6e4a8ae5e02ebd`  
		Last Modified: Wed, 29 Jan 2025 00:40:14 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9423f0e5ba2568439a898c9678b6def69b948887eed29b3b57b34685afb120e`  
		Last Modified: Wed, 29 Jan 2025 00:40:15 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6c59b486ef826497438c525e66cc5b2233830cc602ba7e79969fad5d287e3eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17657664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3448460299638d79fb0f5d4a82853c7387b5ae83736c1c5f3de131658a9686d`

```dockerfile
```

-	Layers:
	-	`sha256:a18b16f4c8a9d3b3cf7ba54197cd1edc9a34efde15c457d4e8c31e8467ab601b`  
		Last Modified: Wed, 29 Jan 2025 00:40:14 GMT  
		Size: 2.4 MB (2365507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446c7ec6f0e3a618c2208cd6170ac7e82f666b19950328dbcd2a65185e573dfb`  
		Last Modified: Wed, 29 Jan 2025 00:40:14 GMT  
		Size: 5.0 MB (5025395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d921fad037a7c717662d076b38e2cee835b744eb7ff3216c9663d21e971d6baf`  
		Last Modified: Wed, 29 Jan 2025 00:40:14 GMT  
		Size: 5.2 MB (5179690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa0aa6fee9407b4f2d1eae95c3ba8582d3b981016ef466d664ba05087d30e76e`  
		Last Modified: Wed, 29 Jan 2025 00:40:14 GMT  
		Size: 5.0 MB (5027137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c05019b8803aa35c09b84b1a9b1541c97d05e1d20653672ff44515aed85577`  
		Last Modified: Wed, 29 Jan 2025 00:40:15 GMT  
		Size: 59.9 KB (59935 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:46be2c2715ea415550db3278ec0c07685376e10a4e8f140747ad3a5bbd9822fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105164474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675f67710353445fd483701431ca62e52b87e255326cadeb2dc2a283bc551402`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 28 Jan 2025 21:27:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_VERSION=4.0.5
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 28 Jan 2025 21:27:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 28 Jan 2025 21:27:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52299e8730d11af6eb71f33b5c16790dae4bb4959ed39906fc96caca2c82e821`  
		Last Modified: Wed, 29 Jan 2025 00:46:47 GMT  
		Size: 46.5 MB (46493171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfe2da4ebaba3053af2ca724275efde70b702f3b62906aba3a2c688da09b33b`  
		Last Modified: Wed, 29 Jan 2025 00:46:46 GMT  
		Size: 8.9 MB (8934957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905d928b7e4fd4f2d74836057463713dfb2fce6b1efd79e739f9fd039604882d`  
		Last Modified: Wed, 29 Jan 2025 00:46:45 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48aba1b68919f476c74a7d8ad55c183c400dfe5a6fc94cd76d399ee3a8523fa8`  
		Last Modified: Wed, 29 Jan 2025 00:55:02 GMT  
		Size: 20.8 MB (20832468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa93f18d41f04fbbdff3047160e6948cfedb7c93d79efb336f7b2a0f84d1d5b2`  
		Last Modified: Wed, 29 Jan 2025 00:55:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264553379a3a76a701874b9a3231cb63a56a4e0ea2f8cacf0655edd979f04c79`  
		Last Modified: Wed, 29 Jan 2025 00:55:01 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835f34527f4da6765945ef2c4e2b06fedf08622089ed3c2fbe767d2e1b0abc72`  
		Last Modified: Wed, 29 Jan 2025 00:55:01 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df14d10b2d576101d93c7f96027ab614362557e3e0c61ac1b220b71fdeb96af2`  
		Last Modified: Wed, 29 Jan 2025 00:55:02 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2b7905f27dc1c363e2376ab26439ca41567cb6bf76ed311fd52b0caa276bf909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18255527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aecd608c0ea7d0eb72e38f1017e62bd588172294d8092dc55d81d60b1b5699d5`

```dockerfile
```

-	Layers:
	-	`sha256:fdeb79a53d0dd76c61ec76368e8df3a1e9c98b0e953ba6e5347fd855d9127463`  
		Last Modified: Wed, 29 Jan 2025 00:55:01 GMT  
		Size: 2.4 MB (2365763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e10b7302c3fbc7af2be59aa77fb721f056a763c784386d4863a869191bf5ed62`  
		Last Modified: Wed, 29 Jan 2025 00:55:01 GMT  
		Size: 5.2 MB (5223727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16045ef83d48c3c4f2d7057d6b3481e8dc13e6e7408a3122161e484aa6543ea8`  
		Last Modified: Wed, 29 Jan 2025 00:55:01 GMT  
		Size: 5.4 MB (5380587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48b5ec1d8f2c1544862fe3339a9d34414c7936751f932865e680049f06b4cf31`  
		Last Modified: Wed, 29 Jan 2025 00:55:01 GMT  
		Size: 5.2 MB (5225469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee90d1a2022b026166ff0086ed9ee0e32bd036e290c8a6f195589420f7df145`  
		Last Modified: Wed, 29 Jan 2025 00:55:02 GMT  
		Size: 60.0 KB (59981 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:90e630cb4ed763594cb38bee80882744ef59cc017486fd9d08cf10c6c9f63bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105608322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05db007289ff9675325c81ef2314d4dce75e8f5f3aad1f6f7f1c95833fcee65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 28 Jan 2025 21:27:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_VERSION=4.0.5
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 28 Jan 2025 21:27:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 28 Jan 2025 21:27:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cadad09c52fdbf44decc403a4ab6082060224014f1082854e01a1a7f5d3981f`  
		Last Modified: Wed, 29 Jan 2025 00:58:33 GMT  
		Size: 41.6 MB (41637000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb9f7be9b5b4cbf6f594b895573e0fdbb3020f04243a231409187e8ff591bfd`  
		Last Modified: Wed, 29 Jan 2025 00:58:32 GMT  
		Size: 8.7 MB (8689882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6706769334970294d65b0d1529bdf615cf3e6a523894522867af35ebcc4742a5`  
		Last Modified: Wed, 29 Jan 2025 00:58:31 GMT  
		Size: 9.4 KB (9435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad2b9fa6f9fb2627d54040b417bed0a0b27780179da8a00c0011235af34b08a`  
		Last Modified: Wed, 29 Jan 2025 01:08:35 GMT  
		Size: 20.9 MB (20881442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca1e04cf0fcf8a8b9c1b0b0ea90d4a03107fc158b1812239bbd0d1ab78cb87c`  
		Last Modified: Wed, 29 Jan 2025 01:08:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7e952c1e8efb8c94b410d2d0ab03c9ef1dd9ed4a653f176142ec36df7efd1f`  
		Last Modified: Wed, 29 Jan 2025 01:08:34 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345be45a87d55ac5e05739bd1828e200cf6312841bebb598e2233d82c441e955`  
		Last Modified: Wed, 29 Jan 2025 01:08:34 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1109820e67077781456ae50628baf7de18e392c97f726cd245b0865fd4ce7209`  
		Last Modified: Wed, 29 Jan 2025 01:08:35 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:74ee8a79baf318525dd6a9d36645314ddcb9c94a95d3fb51a58974d76b09c5bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18111999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd5622df40fbbd5302f4db919ed99975ee3e9704e6595a29ad25f2de1664dfa`

```dockerfile
```

-	Layers:
	-	`sha256:236449721c15e157dc1342ca399dad8938ad8d9fd0d1df2fe05dcad5b02cd31e`  
		Last Modified: Wed, 29 Jan 2025 01:08:34 GMT  
		Size: 2.4 MB (2369058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f27de7cad5592e19db1511bb2658f8d13bca4da09897a47f3241807730c3527d`  
		Last Modified: Wed, 29 Jan 2025 01:08:34 GMT  
		Size: 5.2 MB (5174841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99e14dc35294759dcf5140141f87c6942e61c08c376f7c17dadbd92c57ce266f`  
		Last Modified: Wed, 29 Jan 2025 01:08:34 GMT  
		Size: 5.3 MB (5331713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b35e89648bc6040d10a185a2cc26998ab01bf20fe7d3a17bdb89dbac1b501845`  
		Last Modified: Wed, 29 Jan 2025 01:08:34 GMT  
		Size: 5.2 MB (5176583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fab264448a2a0056476a6569898ebfcbb687d6e670ff42e8183d3892c924d485`  
		Last Modified: Wed, 29 Jan 2025 01:08:35 GMT  
		Size: 59.8 KB (59804 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:fd751bd3cc731e0d6d564d6fbf702d0a4914fc1974eb02e08781d12f9a2a4729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98902849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd0177683b80426b792925e0527883aec7d5dca79e12932bb5d51a73886b6ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 16:33:48 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:33:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:33:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:33:49 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:34:25 GMT
ADD file:23c2e341d6cf3572f2762ef1304c406cf6d4f5ee8ee8719ef289a3b75a8323aa in / 
# Tue, 19 Nov 2024 16:34:27 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 28 Jan 2025 21:27:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_VERSION=4.0.5
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 28 Jan 2025 21:27:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 28 Jan 2025 21:27:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:0dcc8c973ba119a0fb5275114fd0456179bba1132bdc69f2afa4e1c4a235c540`  
		Last Modified: Tue, 19 Nov 2024 17:38:52 GMT  
		Size: 31.0 MB (30980838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3eeb39d66e9a8e77660b2714f3ba13fcefa8b5b90abe0593a7585780c35d1d`  
		Last Modified: Wed, 29 Jan 2025 01:41:33 GMT  
		Size: 37.3 MB (37292087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829a259e6eea4ed880c8b37981d90df14491ce05912c2349be4b03a68ec51ee9`  
		Last Modified: Wed, 29 Jan 2025 01:41:29 GMT  
		Size: 9.8 MB (9785121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2bbbfe4bdfe09d58061d168bb6fa6de75ecabf0871e5b63e100c533201b89d`  
		Last Modified: Wed, 29 Jan 2025 01:41:26 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aae2271e2b3c67a79a9b7e5d97674dc2e9c3f4afb432e61d3b0d0a184e08f35`  
		Last Modified: Wed, 29 Jan 2025 03:17:47 GMT  
		Size: 20.8 MB (20833559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38e910ad16bab7d380567bcb231ec1be5669a9c0db31f60a2256aaf0681dfeb`  
		Last Modified: Wed, 29 Jan 2025 03:17:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c958ca88ac0206918b00ce65d1b183dbfc86e17a78b0abcefc74e7de1618d0d`  
		Last Modified: Wed, 29 Jan 2025 03:17:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b23c72be65eaf8e35db1f83fb9333a24e425e1ecd786f9b8d2ad341a8df734`  
		Last Modified: Wed, 29 Jan 2025 03:17:44 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a1388096e52dcc590017ee3515797114a23c990b4d6bf0e336793365950604`  
		Last Modified: Wed, 29 Jan 2025 03:17:45 GMT  
		Size: 835.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:de4da6c7f12ed27797d37580ba3b690f3b619af14b7dde5f5ad15d9ffce54d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18085633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139470d88207ae8f1577082e24cfc561e1a89e1ac70376edf5df6970a6b2c1b4`

```dockerfile
```

-	Layers:
	-	`sha256:a93eab8ef819fd57fc5a1cdf5bd3adcd3dddf44315d2fe1fbc2c04e1c51aa666`  
		Last Modified: Wed, 29 Jan 2025 03:17:44 GMT  
		Size: 2.4 MB (2357268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24ecf73128c045a744476372dda9bacc8544b78aa118098cc5d623e715525011`  
		Last Modified: Wed, 29 Jan 2025 03:17:45 GMT  
		Size: 5.2 MB (5170842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc5b89c46ba4e808853961413bbefdc991943b9b027de9275eecd70415d130b2`  
		Last Modified: Wed, 29 Jan 2025 03:17:45 GMT  
		Size: 5.3 MB (5325135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd784da89371288c0f4ee5011dda9e32d5cf33bc8d347f2a391c999084af13bf`  
		Last Modified: Wed, 29 Jan 2025 03:17:45 GMT  
		Size: 5.2 MB (5172584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90c14bc0cecf19611cb7e1052f8b23ad31de2b28a82216a4cead848431cd7f89`  
		Last Modified: Wed, 29 Jan 2025 03:17:45 GMT  
		Size: 59.8 KB (59804 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:803d546d4b0d6bf0e98c54c7b37d64215ec990f69defcb5360b9bcbc28788c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99211250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba49da1c1788d95e6f1e892acf0101096e0d37fee52f2f63b8c846bf3e7d611`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:14 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:16 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Tue, 19 Nov 2024 16:18:16 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 28 Jan 2025 21:27:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_VERSION=4.0.5
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 28 Jan 2025 21:27:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 28 Jan 2025 21:27:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965e29136c0040e37abbc80a6accd48640ce74eb7aeda66ce0aa16698c5c0cd8`  
		Last Modified: Wed, 29 Jan 2025 00:50:24 GMT  
		Size: 40.7 MB (40729114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13f00b9fcaef34a53fe78c034076f777ddcb89aa23fc24922cc58a8c87fa107`  
		Last Modified: Wed, 29 Jan 2025 00:50:23 GMT  
		Size: 7.5 MB (7546466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e68b5fa2a4586323b16f1cae2f3664d3c85773ea6450673bc81d2d406ced6b`  
		Last Modified: Wed, 29 Jan 2025 00:50:23 GMT  
		Size: 9.6 KB (9599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457003a14ccc5aa75e3b453b94bddb97ad4183ce291732ed864985dcda0e2c75`  
		Last Modified: Wed, 29 Jan 2025 01:01:47 GMT  
		Size: 20.9 MB (20903492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f362644e0dbafb92e06907290b574a88ba542bf1c5562fd4f65ffa03b151c14b`  
		Last Modified: Wed, 29 Jan 2025 01:01:47 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6e270ae5cceda2c7a574e6f0e52d9a7d61dd5cfd131a7195af0c4fa8cd2814`  
		Last Modified: Wed, 29 Jan 2025 01:01:47 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc2b19646336d401b4a3d081627ea905f312682605ea652e1702c12a90bbc72`  
		Last Modified: Wed, 29 Jan 2025 01:01:47 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1e513c9481efcef38d62171303f14904cde1561459c51d3205ca024b9d3291`  
		Last Modified: Wed, 29 Jan 2025 01:01:47 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:48d5b5e7b5585483a0d18fd87796c70cf45f4f8b7d7ab3b662d9127bcec42051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17741962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa202eef118d0bf11b949d4488468c47ed563a50fed674510ba9e4ac49137f2b`

```dockerfile
```

-	Layers:
	-	`sha256:5110b033d5d3dd01e0b3873295d515afea420969a69e15ad62002d8dafe0304e`  
		Last Modified: Wed, 29 Jan 2025 01:01:46 GMT  
		Size: 2.4 MB (2366815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ddbd2d6f5b17f8287c2a215a7385cbb3599489baf6c9b1589ebdf9409a28e70`  
		Last Modified: Wed, 29 Jan 2025 01:01:46 GMT  
		Size: 5.1 MB (5052707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:682c9774b6e8caaac16205dc71bba4447ded11200fdca7d22d108bc8ea4285d0`  
		Last Modified: Wed, 29 Jan 2025 01:01:46 GMT  
		Size: 5.2 MB (5208249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abaa6becb3ba11d319805a2db5bceb55c9aa9786e2810ecc2ce68cdddecacebb`  
		Last Modified: Wed, 29 Jan 2025 01:01:46 GMT  
		Size: 5.1 MB (5054449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b20b5ff80574525ce70fb4e9632b231f7fbb3bc8e7285a5fbf9efa1433304e6c`  
		Last Modified: Wed, 29 Jan 2025 01:01:47 GMT  
		Size: 59.7 KB (59742 bytes)  
		MIME: application/vnd.in-toto+json
