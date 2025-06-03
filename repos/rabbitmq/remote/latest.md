## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:d5172fdc63a9d0e8b31c57b4b473f73c19f47b75ef0cf2a49af06a86f8c0541d
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
$ docker pull rabbitmq@sha256:f918ae176ae617e283c9241518897c2534b6f87b53d8d18fd64fa7b4bab0c754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115154216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae63eb17a2d670e2c744d9ec7cf8d9fc2a9780716c654fdf743b010c86e3b653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 08 May 2025 17:58:28 GMT
ARG RELEASE
# Thu, 08 May 2025 17:58:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 May 2025 17:58:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 May 2025 17:58:28 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 May 2025 17:58:28 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 08 May 2025 17:58:28 GMT
CMD ["/bin/bash"]
# Thu, 08 May 2025 17:58:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 08 May 2025 17:58:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_VERSION=4.1.0
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 08 May 2025 17:58:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 08 May 2025 17:58:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:58:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 08 May 2025 17:58:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Thu, 29 May 2025 06:11:31 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72b643807f35fbd13f8ab55f1d4e9b36753315fbc650a353bfc8245bf079e2f`  
		Last Modified: Tue, 03 Jun 2025 04:23:18 GMT  
		Size: 46.2 MB (46239842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58370b336d300d631776f5a514b65c32831456439705bd4ae5d6982acd9e02f`  
		Last Modified: Tue, 03 Jun 2025 04:23:17 GMT  
		Size: 8.2 MB (8171061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a4310b6e175f4429ff7df1686587b245a2d96479789da5cb52875e5adf0cdf`  
		Last Modified: Tue, 03 Jun 2025 04:23:17 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1becc9121a19e3c916f9c9fc0d17c1bf2f84d8cbb3ae8589555c164950705f81`  
		Last Modified: Tue, 03 Jun 2025 04:23:18 GMT  
		Size: 31.0 MB (31016763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b76b18c0a8f703ecf9deae8b057c2f371dcb0c34b59454828f1b4308c9a67c`  
		Last Modified: Tue, 03 Jun 2025 04:23:18 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a145b355c5a2f70be134e025d3f52c8601cbcda7bcc4e8f02be721495891206`  
		Last Modified: Tue, 03 Jun 2025 04:23:18 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b62986e75ec9b2ab102f85735c401adf6e90c60d28ce5ee194e1c31aece625`  
		Last Modified: Tue, 03 Jun 2025 04:23:19 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5dfdb7d1aa2433ea3e720f94230b1ae0b9ebf82d8b2fe33c56be5e5dd392e1`  
		Last Modified: Tue, 03 Jun 2025 04:23:19 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d6168a0707b222387bdb83448e417d67e6eec49b7b31df108af8fe1e096cc92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18339922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33727bb5ff289086792cb9e9eefd1c07ce3e40e8471d717e70a3f01200d1b6e0`

```dockerfile
```

-	Layers:
	-	`sha256:70906ff26b89c9baa9965be9984dd9fb96b83593ae7188ba370ae9b2c33621e2`  
		Last Modified: Tue, 03 Jun 2025 04:23:18 GMT  
		Size: 2.4 MB (2384810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6569ca41b5ddee9426e322878d65916172a0fbc4df3b16619756edd8c27989a4`  
		Last Modified: Tue, 03 Jun 2025 04:23:17 GMT  
		Size: 5.2 MB (5245766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:621ab63be79cba5fe8b147dc413afef95b29c045b7ac4fcb8d6c19d4934e8f76`  
		Last Modified: Tue, 03 Jun 2025 04:23:17 GMT  
		Size: 5.4 MB (5402011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:946af48ff2a54515b4c0361f631d60654e6906ad0799bf8fb0bbe9a2c0abcd31`  
		Last Modified: Tue, 03 Jun 2025 04:23:17 GMT  
		Size: 5.2 MB (5247508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cdcd7488870d7a65bd69635ae09459c39da79896dd9427bde52c3efada7b5a8`  
		Last Modified: Tue, 03 Jun 2025 04:23:18 GMT  
		Size: 59.8 KB (59827 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:bbddad657c5881531c301e7083d0f611d842ba0dec7b0d8b0658acbbb221fb1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97721989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafee0b2df4215fe8f5f07cfbdffbc282f8b9467bd560583fe349aea7193b356`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 08 May 2025 17:58:28 GMT
ARG RELEASE
# Thu, 08 May 2025 17:58:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 May 2025 17:58:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 May 2025 17:58:28 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 May 2025 17:58:28 GMT
ADD file:f5b71e3353c1f92a265c88e163d98b6fc00235db4d001763328933c4838f3576 in / 
# Thu, 08 May 2025 17:58:28 GMT
CMD ["/bin/bash"]
# Thu, 08 May 2025 17:58:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 08 May 2025 17:58:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_VERSION=4.1.0
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 08 May 2025 17:58:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 08 May 2025 17:58:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:58:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 08 May 2025 17:58:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:76393e3f1626a318c4984c6e6d91f17fe6888451b277b6cc175eab3a1032ebf5`  
		Last Modified: Thu, 29 May 2025 06:11:44 GMT  
		Size: 26.8 MB (26842221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2507819cd70f609acd1320ef96fdf0ba1c765b3a7c525c0b3eb331c5a5fec520`  
		Last Modified: Tue, 03 Jun 2025 04:34:14 GMT  
		Size: 33.3 MB (33278863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755cc63a303e452252c1896f024bab07e4e0211c069049406ed6081672b97a9a`  
		Last Modified: Tue, 03 Jun 2025 04:34:14 GMT  
		Size: 6.7 MB (6670887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451089b94ae2341c2baa9c16fc4be39a9484e343b102d6e4130e4afe716efe8`  
		Last Modified: Tue, 03 Jun 2025 04:34:13 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaace17a6287ee0d174b65d45a60fd6fa56ac91916d9a38e0f90fc1d216fcb2d`  
		Last Modified: Tue, 03 Jun 2025 04:34:15 GMT  
		Size: 30.9 MB (30918742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecf4eab7e2a787f49e8f1195cf6952d156b06ac165ab8ea461393bc5d088494`  
		Last Modified: Tue, 03 Jun 2025 04:34:14 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7a71d370a9bb49f993559687d6a8668e4f3f084ade435f3a6441893a63602`  
		Last Modified: Tue, 03 Jun 2025 04:34:15 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e286c11a9d9805eeafefa594f9282f263adc687303de3de2af4f5fb52b8abac`  
		Last Modified: Tue, 03 Jun 2025 04:34:15 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b80972953af290c05749b807b98798a243306fd9db7e55d2836bd4b84ddd782`  
		Last Modified: Tue, 03 Jun 2025 04:34:16 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ef608ae5cd6f0a96f18dfd4c8cb94d454ce03988c09272c0403ad849c97815e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17794649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2416977b3fe805a07ee7c3ef2e4efa531cc6cc07a2e0982f163c40031c261d97`

```dockerfile
```

-	Layers:
	-	`sha256:da9614e725c14eb9f032da5ea2c243b38d858aff0f44679ab78433e536025f9c`  
		Last Modified: Tue, 03 Jun 2025 04:34:14 GMT  
		Size: 2.4 MB (2385614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e914c6675792dd5524498d15fcddb9099d8501aa9a1c4a5997d0aed020cb439`  
		Last Modified: Tue, 03 Jun 2025 04:34:14 GMT  
		Size: 5.1 MB (5064525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:126fbfad42acfb53df407df5d1564c598668007206bed9d27d81ba40b2056d08`  
		Last Modified: Tue, 03 Jun 2025 04:34:14 GMT  
		Size: 5.2 MB (5218223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc9ecd4593bbbc902d307f5a248cf0c15260756397e544dc92514e1851e9fd9`  
		Last Modified: Tue, 03 Jun 2025 04:34:14 GMT  
		Size: 5.1 MB (5066267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11fc2fea24471125e7fb8673a438a0eab3f22dd902ca0f7fd63b6d9a3bfe9453`  
		Last Modified: Tue, 03 Jun 2025 04:34:15 GMT  
		Size: 60.0 KB (60020 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:6d7a6b0887fa81d3caab87accdd2d735afd5b95a3590b3e07d213f636978aba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113067334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2743833312b1e4d9fa385b598907f58b6c2e0885cc98e10af9d04e0976027d49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 08 May 2025 17:58:28 GMT
ARG RELEASE
# Thu, 08 May 2025 17:58:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 May 2025 17:58:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 May 2025 17:58:28 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 May 2025 17:58:28 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 08 May 2025 17:58:28 GMT
CMD ["/bin/bash"]
# Thu, 08 May 2025 17:58:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 08 May 2025 17:58:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_VERSION=4.1.0
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 08 May 2025 17:58:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 08 May 2025 17:58:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:58:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 08 May 2025 17:58:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Thu, 29 May 2025 06:11:37 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a93a601c57a4432a62741bdd4f21f35f5ed966cc63ca05727096979c267fd02`  
		Last Modified: Tue, 03 Jun 2025 05:39:59 GMT  
		Size: 44.3 MB (44335669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05a256c9542ad3ea063b7a9fa3a598234e77d1348cf11346e19eb30d2abc914`  
		Last Modified: Tue, 03 Jun 2025 05:39:58 GMT  
		Size: 8.9 MB (8943304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb098c05301dcd8149aa9fe0a04c0787594715562a58e1226dea4eb2a395dae`  
		Last Modified: Tue, 03 Jun 2025 05:39:58 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a654ba67be56f2be455892d4fe41f83209b6b2e1fb6c5e37ce79aa424cb1507`  
		Last Modified: Tue, 03 Jun 2025 05:39:59 GMT  
		Size: 30.9 MB (30925295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae1f424f50dea1b3e39603cf8211a7f555b86eb7384ae4ec7d6929f143850b2`  
		Last Modified: Tue, 03 Jun 2025 05:39:59 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bedc6dec0dd2447f6b2802e580deb700f960c57e1f8fb81a078a9ee0531b7d`  
		Last Modified: Tue, 03 Jun 2025 05:39:59 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3247dbf0b92c0b204eaee1975cd70f21ef069ddb272f5714029a83aa7804666`  
		Last Modified: Tue, 03 Jun 2025 05:40:00 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acccc358fa7068f0e2c665b029dd1b9eab069aaa1ed5bec06861245239e1f69b`  
		Last Modified: Tue, 03 Jun 2025 05:40:01 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:36f64b0e39a021e107973dedece0f66db760a2c4e82d89d93a8101e13ff45fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18398880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96918d9c7dce9beb707796691b421f780f9cc4b5ca832154aea8f0cd80022901`

```dockerfile
```

-	Layers:
	-	`sha256:3d4ed9cada2cdd9e0fd31784394b0f63d576d788de9832e62366f7afcd12ffa7`  
		Last Modified: Tue, 03 Jun 2025 05:39:58 GMT  
		Size: 2.4 MB (2385870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27439a56fb84d169aca54415e5b349fa956499aab083dee76856a7f8fd1f7750`  
		Last Modified: Tue, 03 Jun 2025 05:39:58 GMT  
		Size: 5.3 MB (5264980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d903a21f7ec711b3fbf25c94ecfce2687e9a77edf0a4ae54d9bf80c4099f6f`  
		Last Modified: Tue, 03 Jun 2025 05:39:58 GMT  
		Size: 5.4 MB (5421243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d572abaf9500b763b73fa163c4fe79bc68c42580053567e99acc60422ad545b7`  
		Last Modified: Tue, 03 Jun 2025 05:39:58 GMT  
		Size: 5.3 MB (5266722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:029edbd939e3577cd49b9fc922892d18d5b20207678b683cef714f6fb2a10f19`  
		Last Modified: Tue, 03 Jun 2025 05:39:59 GMT  
		Size: 60.1 KB (60065 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:01834b698009e7ad7b93629f3a0a1837fb2040cef5bde5890696385a457f329e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113493507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf64aaf43d9f5ccc12f308140cd6fe00113d25390f5874392f0f0a09a622519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 08 May 2025 17:58:28 GMT
ARG RELEASE
# Thu, 08 May 2025 17:58:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 May 2025 17:58:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 May 2025 17:58:28 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 May 2025 17:58:28 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Thu, 08 May 2025 17:58:28 GMT
CMD ["/bin/bash"]
# Thu, 08 May 2025 17:58:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 08 May 2025 17:58:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_VERSION=4.1.0
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 08 May 2025 17:58:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 08 May 2025 17:58:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:58:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 08 May 2025 17:58:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Thu, 29 May 2025 06:11:52 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d4eb945ed428195f82f385b4d6dd9fe4d872612e9cd8c9855ecc0655ff5bb8`  
		Last Modified: Tue, 03 Jun 2025 05:29:28 GMT  
		Size: 39.5 MB (39483050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599297fd90ab3f225b89e9c823c39db77da5bfd020347d23d248bb276969708`  
		Last Modified: Tue, 03 Jun 2025 05:29:28 GMT  
		Size: 8.7 MB (8699424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975fc23de78dcf1019b51dfaa20951906ca0bb670292a9cef19c040a35e36fa3`  
		Last Modified: Tue, 03 Jun 2025 05:29:26 GMT  
		Size: 9.4 KB (9436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840711fabe132d096508607ee93ff0814414ae18686ad16601be7a1359821958`  
		Last Modified: Tue, 03 Jun 2025 05:29:29 GMT  
		Size: 31.0 MB (30974639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0191734b2d6c89a31bff14db5617f8ecc8bd35a7f8e3e2ea90011bb97c3c740`  
		Last Modified: Tue, 03 Jun 2025 05:29:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd64628048f0709e89db590cea6294a3d2c012c1a92a48d522fc46c4e00de294`  
		Last Modified: Tue, 03 Jun 2025 05:29:28 GMT  
		Size: 107.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4a8876561d24970237347a472b9f84c17b24175a118ac4d65936b01d1ab7df`  
		Last Modified: Tue, 03 Jun 2025 05:29:29 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eee392bebe88090f724a075f67a127a8b6b717c37e8b7e955bcd9d96421ce1`  
		Last Modified: Tue, 03 Jun 2025 05:29:29 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b2f3796aae2662bdaae240a33c8a1d1e34f4301907eeecffec6acb0f84e546d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18254188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12fc4707b8456840ae9824338d024df3d7a56bdc138b3de1bfb1978ac06378e`

```dockerfile
```

-	Layers:
	-	`sha256:d6623d226776ba44d3793218f554278fcf2c9ef211adcced0a398585b2166c6b`  
		Last Modified: Tue, 03 Jun 2025 05:29:27 GMT  
		Size: 2.4 MB (2389263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6a515436c63073c3137b413112a06cc26c0c83447f730b3ed734334cd88c1af`  
		Last Modified: Tue, 03 Jun 2025 05:29:27 GMT  
		Size: 5.2 MB (5215673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60f406014db96264344608d7cf3b167b8ca8bb20d50964bf5512fd150e35a59a`  
		Last Modified: Tue, 03 Jun 2025 05:29:27 GMT  
		Size: 5.4 MB (5371948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bae4e004103b36a16b103811d74db80cb6e00e57a2b24071c8bfb3f7935860c3`  
		Last Modified: Tue, 03 Jun 2025 05:29:27 GMT  
		Size: 5.2 MB (5217415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d36b7b25567da301904f62052e48eb2b9e455dcf33c27dd60e41fe332ac357a`  
		Last Modified: Tue, 03 Jun 2025 05:29:28 GMT  
		Size: 59.9 KB (59889 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:8ddb4b6d18cab20b03f9fbade57a97a303507e9f091a08d9013a0009379e1229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106803234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8bcd1dc67ca2e895b5eeb467cea9d8cf0295da527cb3667aa338164f6ef0fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 08 May 2025 17:58:28 GMT
ARG RELEASE
# Thu, 08 May 2025 17:58:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 May 2025 17:58:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 May 2025 17:58:28 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 May 2025 17:58:28 GMT
ADD file:f68263cf915d0f5d61ab9caa83da511fc9ef55d936429cb8fb542906fc38a8fa in / 
# Thu, 08 May 2025 17:58:28 GMT
CMD ["/bin/bash"]
# Thu, 08 May 2025 17:58:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 08 May 2025 17:58:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_VERSION=4.1.0
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 08 May 2025 17:58:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 08 May 2025 17:58:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:58:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 08 May 2025 17:58:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4ac2db62b9f8401057b5c4ebae4764d70573ec599f6a1f0b5dc2c4491ed8e39a`  
		Last Modified: Thu, 29 May 2025 06:11:59 GMT  
		Size: 30.9 MB (30947484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47539be7c666063b2e279d47f30af02a367a8d2f47b3dc5c29bd624c224a6f28`  
		Last Modified: Tue, 03 Jun 2025 06:14:28 GMT  
		Size: 35.1 MB (35126418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa93a4caf6c73309037d7eae65bb697fc8594c83881d04639f0d4321eb40b801`  
		Last Modified: Tue, 03 Jun 2025 06:14:24 GMT  
		Size: 9.8 MB (9789666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4634d552545df508daf3fd4cb95a47fdd82c28dee70a65fdf05bec8feebdfd0b`  
		Last Modified: Tue, 03 Jun 2025 06:14:21 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8379c6ba131401950e6af5d1e9a8fe12ebce5cf410de7949d64955381c38f81a`  
		Last Modified: Tue, 03 Jun 2025 06:14:27 GMT  
		Size: 30.9 MB (30928477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8dc7dc2b571cc60d1d22dcc87db3ec2ff6e0caee33d2eca4870388bb7ba52c`  
		Last Modified: Tue, 03 Jun 2025 06:14:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ff01c3b0fcb4aef48f24a300302a0069a2e7f2f3cea6323e01f5fee3a590d`  
		Last Modified: Tue, 03 Jun 2025 06:14:24 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef69ff9a58a26120ef82ef5817d9203bc024a191bbd30ac39dbe7b9173d55fa`  
		Last Modified: Tue, 03 Jun 2025 06:14:25 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba4f41af891600c5996115a1616a0661412d7717d01a5c38b0db3447447f7b3`  
		Last Modified: Tue, 03 Jun 2025 06:14:25 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8a9bf0780f5d458e59b5a6f706c710e694b79d21210c553aaa3133833c1994c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18222910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c0cbb4c19fb4deeea800427032424a781ff604196b26510c93a031a0376fbd`

```dockerfile
```

-	Layers:
	-	`sha256:6512d3cbe3af5a3c1eb2f338ec759bc369efd4368178f16f1d09c0f3f69ee342`  
		Last Modified: Tue, 03 Jun 2025 06:14:22 GMT  
		Size: 2.4 MB (2377181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c358ac96300658d9ea40f3e410629cf76126157d434cf01c382eb671f10ec7`  
		Last Modified: Tue, 03 Jun 2025 06:14:23 GMT  
		Size: 5.2 MB (5210134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bb22cd9d155574916b675846bb40edb0bd18eeeda459ea10c05935ccf5b0024`  
		Last Modified: Tue, 03 Jun 2025 06:14:23 GMT  
		Size: 5.4 MB (5363830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3217ade6b7dbdbc8869f55d5c7436864aace64cdfd4cf78e1d032cf650de21`  
		Last Modified: Tue, 03 Jun 2025 06:14:23 GMT  
		Size: 5.2 MB (5211876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6198b28831ce7dd90b9b4f05740852f97b4939072c4eef352599c2ff1911785`  
		Last Modified: Tue, 03 Jun 2025 06:14:23 GMT  
		Size: 59.9 KB (59889 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:5f52ad81dac4f7abfa69eb8914ac21d1fff70862baa6d09c3815ea46f2fc5bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107053110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5badc303cc5c5f8aed1fd465a7eeac9fc6081fa39a53dcb8deccc2cd693f44e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 08 May 2025 17:58:28 GMT
ARG RELEASE
# Thu, 08 May 2025 17:58:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 May 2025 17:58:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 May 2025 17:58:28 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 May 2025 17:58:28 GMT
ADD file:b6b8557b3fef6c06eb943ce735f649cf7033ab3925e70e6b43901f1f29b4d5e9 in / 
# Thu, 08 May 2025 17:58:28 GMT
CMD ["/bin/bash"]
# Thu, 08 May 2025 17:58:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 08 May 2025 17:58:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_VERSION=4.1.0
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 08 May 2025 17:58:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 08 May 2025 17:58:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:58:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 08 May 2025 17:58:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7fa55ab2f467363da0197dee4a8e5af9e7ba7ef5686c6f0951bc509c387b765c`  
		Last Modified: Thu, 29 May 2025 06:12:06 GMT  
		Size: 29.9 MB (29930056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126ed9d4d1b86671be6871ec45a5e9a5fb783996b5b3150f348b9b946e6b7fa`  
		Last Modified: Tue, 03 Jun 2025 04:51:37 GMT  
		Size: 38.6 MB (38560516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adca5b8270498df624af8089e193dac34dbb8ba128c834fd4b849a8f5c0b99e8`  
		Last Modified: Tue, 03 Jun 2025 04:51:36 GMT  
		Size: 7.6 MB (7551989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f3092c4fe8ee674a19494a31c8f8757f48831d3ac4141330d44642f505597a`  
		Last Modified: Tue, 03 Jun 2025 04:51:36 GMT  
		Size: 9.6 KB (9646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d345e290da3a843551e2ed7605b40e777c3f5bb3453029c6284ef2a1680e40ac`  
		Last Modified: Tue, 03 Jun 2025 04:51:37 GMT  
		Size: 31.0 MB (30999156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b315f135ad661a1467f48173346fab744e31157320740bb04d08aada7a97f9b`  
		Last Modified: Tue, 03 Jun 2025 04:51:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5958318f941ea21e752ddc94adf70f968b5dd63c81781784cf70ae1a0c1c15`  
		Last Modified: Tue, 03 Jun 2025 04:51:37 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58da81a3795bd1f0bb5c4090939305195f7a9d80d37d2d33881952d891f0c3ed`  
		Last Modified: Tue, 03 Jun 2025 04:51:37 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d36032c0ffdd7e868d61186a9058943146fd8b96c2a6ee8b8ff58e2e5f1dd43`  
		Last Modified: Tue, 03 Jun 2025 04:51:38 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bd64d6addedc958a901045339df686e7623184e606f0090151b9394c4872825b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17880096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab51cf9d8edf14057174cd023037fb5fc36d26f9db5f48a2da82d2787fd2852`

```dockerfile
```

-	Layers:
	-	`sha256:44efb0e3623aa3f968c907cebe2d41866f022e4cbeb06bd1a07fb6fc0328906c`  
		Last Modified: Tue, 03 Jun 2025 04:51:36 GMT  
		Size: 2.4 MB (2386922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f79f66bcef1dc56d066879f67a5951a6b9a30b8bee17ed4ed784dd875e33f50`  
		Last Modified: Tue, 03 Jun 2025 04:51:36 GMT  
		Size: 5.1 MB (5092220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47ef2a043f1d94dfcd19cd5c93069c904cddb261bc6e222782100f7c4fcdb018`  
		Last Modified: Tue, 03 Jun 2025 04:51:36 GMT  
		Size: 5.2 MB (5247165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acb3c3c892afa769ea911d73544c3940f2497861b2c395f7bf76fb1ab1d07381`  
		Last Modified: Tue, 03 Jun 2025 04:51:36 GMT  
		Size: 5.1 MB (5093962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ab1ff7d76fcce3ff679b1af61a43bb749c0a8377f5aeabc4218a68e48e9020`  
		Last Modified: Tue, 03 Jun 2025 04:51:37 GMT  
		Size: 59.8 KB (59827 bytes)  
		MIME: application/vnd.in-toto+json
