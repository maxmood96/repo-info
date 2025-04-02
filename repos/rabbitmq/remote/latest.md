## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:cd4190a8fe0bd2142aa7e8557acbed287a0c1ad428eb639fe5697927fcf5cb9e
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
$ docker pull rabbitmq@sha256:3a49848d435aaf1a34a3577e6d24227acf6a2b844317eac7c9dabd36564a21ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107533830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bbf5c438e83bee4b6690eb8f54c110ef813eef729a5921bceb7b2667b2eed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 01 Apr 2025 23:12:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_VERSION=4.0.7
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 01 Apr 2025 23:12:40 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:12:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 01 Apr 2025 23:12:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcaa465b4a727b2033ef867ccf1568930c34f6508eef9c5b3b9f75e38c0da49`  
		Last Modified: Wed, 02 Apr 2025 00:01:10 GMT  
		Size: 46.2 MB (46234870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e1fd5eb2a1765cb80b4042f66a5a77537573e366cd648aca2feb0b0dcd2584`  
		Last Modified: Wed, 02 Apr 2025 00:01:09 GMT  
		Size: 8.2 MB (8171060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a8a4bf19c7df15a9b129e5be4d03d058ff0e57855873508bde806d45df16a5`  
		Last Modified: Wed, 02 Apr 2025 00:01:09 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29bf1008f9705b60cd572427526c6f26426dd80fb3d925af971bf5a258d0b2b`  
		Last Modified: Wed, 02 Apr 2025 00:01:10 GMT  
		Size: 23.4 MB (23362379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6303a889afd35036ba02eb5c3a5453d76b3e4dcaac673287b2776d1e48c731`  
		Last Modified: Wed, 02 Apr 2025 00:01:10 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acfeadb396cebbdf3f78f8fc07840a6e4eb43e81cd88fc8c20e9f7acfb2b155`  
		Last Modified: Wed, 02 Apr 2025 00:01:11 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8868906f712edea393bbcc72ed9bf664a403e4238becc0be5e100eae40cd215`  
		Last Modified: Wed, 02 Apr 2025 00:01:11 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cc551f93f29a509ff24b654cd27ea1edabb44471c554d8f09ec938adedf28b`  
		Last Modified: Wed, 02 Apr 2025 00:01:11 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a9d0d961234ec2c20dc5eb42f5756104e67bec6c27fc01530cc754af4c68547a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18192471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80688fa113032597af57d234b22ac400a0f6bdd3f04471ffef33dcc29b46429b`

```dockerfile
```

-	Layers:
	-	`sha256:ebdadbef34b3dd1cfea75720b23e66c3a71ab69457291660ef6b33a64bab09ec`  
		Last Modified: Wed, 02 Apr 2025 00:01:09 GMT  
		Size: 2.4 MB (2366087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2bce2b84fec0cb824930134fe34ae5bd8e98481863f1ad503abd541743887ab`  
		Last Modified: Wed, 02 Apr 2025 00:01:09 GMT  
		Size: 5.2 MB (5202860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eee79bfb65da6058dca556edb95403575e53c13b7e027b118015d12b9b6a821`  
		Last Modified: Wed, 02 Apr 2025 00:01:09 GMT  
		Size: 5.4 MB (5359095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b289c2d04bbef88a4dc0dbcdc2cdb4cf33486b43bf54ebb020401d35edcca8ec`  
		Last Modified: Wed, 02 Apr 2025 00:01:09 GMT  
		Size: 5.2 MB (5204602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9f31b478961851518d01b67bc33c53bb7310da0b562d1825b4d80e5c376965e`  
		Last Modified: Wed, 02 Apr 2025 00:01:10 GMT  
		Size: 59.8 KB (59827 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:b32f0dd8833424db7d00ff0a67ec2dc95d7ffa854565d640952746d4f165a869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89471212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a4743ee5fbd5b16f62e27401085ce83929c396c9fd20decf0bd8f579dec94a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:14 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:14 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:18 GMT
ADD file:22301ffa2fa465db7a0f07e0c3ddc488f07cc6a745c39e6f450fdbe37da97418 in / 
# Mon, 27 Jan 2025 04:14:18 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 01 Apr 2025 23:12:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_VERSION=4.0.7
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 01 Apr 2025 23:12:40 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:12:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 01 Apr 2025 23:12:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Mon, 27 Jan 2025 05:10:02 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7c35eae959155650e3b68800f59d999f2559b5c336f49e71d40b69cbcaca88`  
		Last Modified: Tue, 01 Apr 2025 23:59:07 GMT  
		Size: 33.3 MB (33267316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19a5a229228dc8069841297d859b03ff134bb906f7d2b2ec0350ee4f73a5862`  
		Last Modified: Tue, 01 Apr 2025 23:59:06 GMT  
		Size: 6.7 MB (6670897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7bcbca65abdd1e1c39c135095f7cee8fe0cfc21b3b17538f35f4254e627d7b`  
		Last Modified: Tue, 01 Apr 2025 23:59:05 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339ca3c6652fb1d8f4ee90fc5d2391206e2df2e2a1e631c47fccc80ef5df27f4`  
		Last Modified: Wed, 02 Apr 2025 00:04:54 GMT  
		Size: 22.6 MB (22646749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5202a259804faf66781cf93db76d84d1e8c3779a57aaa797cafad4bc6fe88455`  
		Last Modified: Wed, 02 Apr 2025 00:04:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c4cf30e870aabe716396fd38b26398e4a55d10a37f0d3145fc311e0c912a4f`  
		Last Modified: Wed, 02 Apr 2025 00:04:53 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6317b296d69cb5118e46609d55fab528db7dfefe525422c88aea6f7135e90211`  
		Last Modified: Wed, 02 Apr 2025 00:04:53 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e65dac7128061fb0369a434b99e920b6cb6b973b9298fd545a2a0442d08562`  
		Last Modified: Wed, 02 Apr 2025 00:04:54 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a731bc2248cf219408a0cd8f184e95654d5f1a9839a4ba635b764fa8a7fc4eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17654716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da175368f6c06f0ee83b62fcd72ea29c6126f711f34772d76c49be9aaf2a3b1d`

```dockerfile
```

-	Layers:
	-	`sha256:ca9ecef7104be0fa50d4c8e388d1f0f35478c7b26c0c3c50c3916a14e7d4c835`  
		Last Modified: Wed, 02 Apr 2025 00:04:53 GMT  
		Size: 2.4 MB (2366891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58aadc637f816035ed219f122d9b07f8354f91ce77b7b010dfc5f3b051cd3a64`  
		Last Modified: Wed, 02 Apr 2025 00:04:53 GMT  
		Size: 5.0 MB (5024125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c24e38e9ef6128620682d67f4d762eb210858494e69776251ca19857e8c0cec`  
		Last Modified: Wed, 02 Apr 2025 00:04:53 GMT  
		Size: 5.2 MB (5177813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ac70fb96d8a64f756fddfad7150c02f883e8615314135dc598ca63d27149ac3`  
		Last Modified: Wed, 02 Apr 2025 00:04:53 GMT  
		Size: 5.0 MB (5025867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc2121a80675a4cf48d7dc58b3467ecc4eea2d9f6c58a0da55d4a5459715e4fd`  
		Last Modified: Wed, 02 Apr 2025 00:04:54 GMT  
		Size: 60.0 KB (60020 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:6a7890250d62324ab5a5160396e54d24ea6882905af6fc1f7abe5acdaaf9fada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105249584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f732a2d5fa5c9e8bfe9b8f0e0258f5eabe86f7bcc4678c795fda06989b27e2a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 01 Apr 2025 23:12:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_VERSION=4.0.7
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 01 Apr 2025 23:12:40 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:12:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 01 Apr 2025 23:12:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876aad1332a13ec3fb78645f10401e390c422b4a60a0cadee0307e792f3382b7`  
		Last Modified: Tue, 01 Apr 2025 23:59:50 GMT  
		Size: 44.3 MB (44318180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbb93ab3a54ac33285c5d6f716c235afa1d7b7964ab8497771748458415b1af`  
		Last Modified: Tue, 01 Apr 2025 23:59:49 GMT  
		Size: 8.9 MB (8943292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ab714ce495e14c49d05e3a87b1b795a664a9821f0b710372c950734b15bd3c`  
		Last Modified: Tue, 01 Apr 2025 23:59:48 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9231c4205e1c9205a2703860cf012535c60469b9040aac26a4641e3f18e2331e`  
		Last Modified: Wed, 02 Apr 2025 00:08:07 GMT  
		Size: 23.1 MB (23083313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703141ee4e4a4341a08a053756f66bc3d757e214f6f3c88fbc94e38c5416a294`  
		Last Modified: Wed, 02 Apr 2025 00:08:05 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5430081ed7d447e297e8e2435b9948112cbe9329b10a5636ad2e2fc3a05d793e`  
		Last Modified: Wed, 02 Apr 2025 00:08:06 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51529086f8a2604aa9f4a8ad3326752540c9dda5e3b0761c3c4c402b0d6cd2f`  
		Last Modified: Wed, 02 Apr 2025 00:08:06 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1100b9c85394d55a3cb1b5c9e611a875febbf31699a30eb91ab7654b87228273`  
		Last Modified: Wed, 02 Apr 2025 00:08:06 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:dcca86cb10ab710efc96c343ee039dadb9a860c689bf0f8d1171bb9be1a0ad73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18252579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d60619d9fd7030fe5c501c5068059aa6826b512b5c79f16a9ef237cf454073`

```dockerfile
```

-	Layers:
	-	`sha256:8d31026f92c3c4ff052e2376f389ecc45a3834f87d9bdbecab78c6d637ef5de9`  
		Last Modified: Wed, 02 Apr 2025 00:08:06 GMT  
		Size: 2.4 MB (2367147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be6b85446d1dc2771839745617158ef8a2d96a21af7deeec97f38aae0adb9f17`  
		Last Modified: Wed, 02 Apr 2025 00:08:06 GMT  
		Size: 5.2 MB (5222457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80e5cd21fa76b712f3652333bc41df77f669a6b7e80253e9ba941f9d98aac832`  
		Last Modified: Wed, 02 Apr 2025 00:08:06 GMT  
		Size: 5.4 MB (5378710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cae5264d3c576e310cb98143cc88441f2c4f70db43a44918c6820f774dd46a8`  
		Last Modified: Wed, 02 Apr 2025 00:08:06 GMT  
		Size: 5.2 MB (5224199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7df79ce9979ebfa2c1d63b13ab0fb5302f30d393ec950b95fe1b127b96ed90e`  
		Last Modified: Wed, 02 Apr 2025 00:08:07 GMT  
		Size: 60.1 KB (60066 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:04bc6c0bf51d852e83fa21eecbfe6b1814cf83031a47c6c71e1f3c349df3887c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106121608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe3d99f0e9cf95ff785d5c730de82604bea7b2016629a9892cf2abac9b05b5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 01 Apr 2025 23:12:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_VERSION=4.0.7
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 01 Apr 2025 23:12:40 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:12:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 01 Apr 2025 23:12:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aacf73f6822bd28d5f8935f6519049e8de1a786fd490d4a02bb44f89d395bc6`  
		Last Modified: Wed, 02 Apr 2025 00:00:46 GMT  
		Size: 39.5 MB (39478797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ea6bdcc0f6b25b4e5cc7ce0cd41627e0f430d10c7e3ef39483f12b9733f754`  
		Last Modified: Wed, 02 Apr 2025 00:00:44 GMT  
		Size: 8.7 MB (8699423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c0ae04f4251155e0527acd02774fd721b05265da6c2f47b297cb544fad9298`  
		Last Modified: Wed, 02 Apr 2025 00:00:43 GMT  
		Size: 9.4 KB (9400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67950db969b8545989283a592b32388f84901367028faa72d6f459b57575ecfc`  
		Last Modified: Wed, 02 Apr 2025 00:10:51 GMT  
		Size: 23.5 MB (23542418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe236675ef7012aa11ce610afe38fb281c77d8da445514c7a27c820195091b8`  
		Last Modified: Wed, 02 Apr 2025 00:10:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7fb74a5a2bbe74143427ca63a0da69d9913734468983b6845d5712613d7aa8`  
		Last Modified: Wed, 02 Apr 2025 00:10:49 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273c03a830e73b77f26943704a3ff0fddd8c5df30a7c2cd6646b4a6b48678a7a`  
		Last Modified: Wed, 02 Apr 2025 00:10:49 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9b10de27968c0305b0aa59c850ec5a8953dda022b12373e545cd8e532bceee`  
		Last Modified: Wed, 02 Apr 2025 00:10:50 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9d09cc74590168b2334fa146e52e3eb2d4b84fa0afab36c60394748981eb0cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18109051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ae4cc6769c489081e0a046f030b1fdbd0bb07813c16bedd41f5f460475a014`

```dockerfile
```

-	Layers:
	-	`sha256:3953413a67327c620f4c06cf6d113b43891457fd4d0a66c9640246227834d240`  
		Last Modified: Wed, 02 Apr 2025 00:10:49 GMT  
		Size: 2.4 MB (2370442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05f4915e119041b6686e20c36a2403cfd74dfaab232fb580243300575de95842`  
		Last Modified: Wed, 02 Apr 2025 00:10:50 GMT  
		Size: 5.2 MB (5173571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7f8cb2bb879c1efc1ef057442ccb9766ebb63863d7357274eadd3d3fd5fa89b`  
		Last Modified: Wed, 02 Apr 2025 00:10:50 GMT  
		Size: 5.3 MB (5329836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a60756259ff8211b6126333ce0fd0a8e54e684beb5fe4db54252da467583bd6`  
		Last Modified: Wed, 02 Apr 2025 00:10:50 GMT  
		Size: 5.2 MB (5175313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1011553ca5c93e77a069b1a8b1c27b67c44ae32e6c79fde01135d8560ba41c3`  
		Last Modified: Wed, 02 Apr 2025 00:10:51 GMT  
		Size: 59.9 KB (59889 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:bc0a741fccb85fd43cf33d26f08ee5971571ddd192fa202fed6feee9ee919745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98886340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b44508e4a8e32c5fe560141e930bf652429525fcc0530779f29302f90587e43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 27 Jan 2025 04:46:38 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:46:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:46:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:46:39 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:47:10 GMT
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
# Mon, 27 Jan 2025 04:47:12 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 01 Apr 2025 23:12:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_VERSION=4.0.7
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 01 Apr 2025 23:12:40 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:12:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 01 Apr 2025 23:12:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Mon, 27 Jan 2025 05:10:15 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7caf74e10058f766ec0e33f6c0f2ea18dbbff2f83f8262817b4755f6ec8cb8`  
		Last Modified: Wed, 02 Apr 2025 00:28:34 GMT  
		Size: 35.1 MB (35121406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07fde529cc048edbf6bb53ff986bd2056511a47e81d7e0408c89254e2331701`  
		Last Modified: Wed, 02 Apr 2025 00:28:30 GMT  
		Size: 9.8 MB (9789660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2fb0520099c323ba3716c5472a9f64248f7c1c84a9dc686fc7a532d663cc1c`  
		Last Modified: Wed, 02 Apr 2025 00:28:27 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e72280ddd8ee49be0d3550b4c59d4d9b37acb9f8b3d58e00be399fb68e8bd8`  
		Last Modified: Wed, 02 Apr 2025 01:14:16 GMT  
		Size: 23.0 MB (22980122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c696746cffd01c11a9b61353a65c9faff6b3e102c5c9fd4a6f8cb4186ae41c`  
		Last Modified: Wed, 02 Apr 2025 01:14:13 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec02bc9b16807876f0a43771074f3780bb1ece5db63c090b211cf1f1e5faf90e`  
		Last Modified: Wed, 02 Apr 2025 01:14:13 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3caef6e565b6516e590a08b60f5c3a6e1fab22bc9cece91f7d8a4457fe18bbfd`  
		Last Modified: Wed, 02 Apr 2025 01:14:13 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3816ada00c620d27dd00331d59cf9beb9357678a73d5931b295fa9ba56419152`  
		Last Modified: Wed, 02 Apr 2025 01:14:14 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2fecb9091892ffd72c6350d573f36fb013cfa75a0cd64f4ec8f901f9d9e5b08d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18082685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2632a4eeced12a7b2155379e23910f59ee20c33222557d63fcbb1119912dec9a`

```dockerfile
```

-	Layers:
	-	`sha256:64cef85934f0eb97c52ff89e22bf1b6cde475794255d9aed2d5cbbb6e720370c`  
		Last Modified: Wed, 02 Apr 2025 01:14:09 GMT  
		Size: 2.4 MB (2358652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b76681c7f7c03e3acfc8b482ac3b8599c26b75a1cc5e38ecea2931a51fe51ccd`  
		Last Modified: Wed, 02 Apr 2025 01:14:09 GMT  
		Size: 5.2 MB (5169572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5453acd05409995d5c0b6664fa0ed13540ab1923dedb92e0405a8dbcb4d7c9ff`  
		Last Modified: Wed, 02 Apr 2025 01:14:09 GMT  
		Size: 5.3 MB (5323258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:127f09acde77e77398cb43c73547e6f5fbc69a7a2e072eadf7db363c20d7b1ba`  
		Last Modified: Wed, 02 Apr 2025 01:14:09 GMT  
		Size: 5.2 MB (5171314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59f9f7aaf680b01de8f73bfba4ee9b5a3d92b1790cf2f4cfc535f916aca7779a`  
		Last Modified: Wed, 02 Apr 2025 01:14:10 GMT  
		Size: 59.9 KB (59889 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:40dac614af40108c9e433d7e7ddfd3596ae03a11a87adb5d0a3b876a894acfd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99178279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616910b9169a9d116c97063d2f02563650440080c28fde1e2dab2956b3961fa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 27 Jan 2025 04:15:19 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:15:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:15:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:15:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:15:20 GMT
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Mon, 27 Jan 2025 04:15:20 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 01 Apr 2025 23:12:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_VERSION=4.0.7
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 01 Apr 2025 23:12:40 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:12:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 01 Apr 2025 23:12:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Mon, 27 Jan 2025 05:10:30 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c6accaf9b456effef59ed411830c29b3bc0ace54ca925f2e60fef84827f2f7`  
		Last Modified: Wed, 02 Apr 2025 00:00:04 GMT  
		Size: 38.6 MB (38553706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d57ac33723222b0c9f9310a74e6c3cf45b83e4550d565f46ff4ed3c2f57451`  
		Last Modified: Wed, 02 Apr 2025 00:00:04 GMT  
		Size: 7.6 MB (7551993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940c232baedac25e2886a8d88b6747f1706d7e4e1efdb75d9e3c2091d4d2ac68`  
		Last Modified: Wed, 02 Apr 2025 00:00:03 GMT  
		Size: 9.6 KB (9585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b056afe1e0e352bb00065406402b2d0b6395e5c9d0dc95b54d816269af488b`  
		Last Modified: Wed, 02 Apr 2025 00:10:16 GMT  
		Size: 23.0 MB (23033686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b478bbf6d34ad9880bf8e29b4ee517bc64c0b380b2dc59f21557aecf1bd82e`  
		Last Modified: Wed, 02 Apr 2025 00:10:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c31dd29c47489e6d178129ba651e85e858b7d9cd658b36259e82914c7553e5c`  
		Last Modified: Wed, 02 Apr 2025 00:10:15 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12849293057662ede6b1484f0e8ed9e72e70ce84ecb512c06a10dc5eef930205`  
		Last Modified: Wed, 02 Apr 2025 00:10:15 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2819f7fe3a7eb64b317aaad5e2b6a4ac4455a0d5cc568710e51c4797af988759`  
		Last Modified: Wed, 02 Apr 2025 00:10:16 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:729d5bb18689cbfbab462a38eb99c14b77cb732bc122dbe95d72bb056f04e216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17741049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b335defbe88b9ca40f3a7dab99aef8e87b68df6d3bef237222b56a33d11e399`

```dockerfile
```

-	Layers:
	-	`sha256:4d362d3d40cec6533c00d3c13ebe772dc53e91588a2507b139c5920993301899`  
		Last Modified: Wed, 02 Apr 2025 00:10:16 GMT  
		Size: 2.4 MB (2368934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c4cd708bd713d9a35f1cbbb09b7c6af2e75b848e27a3cb89d2bb77342fae40`  
		Last Modified: Wed, 02 Apr 2025 00:10:15 GMT  
		Size: 5.1 MB (5051437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf3cd746745b9a4ed9e00eb1d0e84deba871b47f20c6b05c26cb4b84ff598408`  
		Last Modified: Wed, 02 Apr 2025 00:10:16 GMT  
		Size: 5.2 MB (5207672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64873a206807f7fd2d8d4ad1ca1481a757ba9d828d13b3aa50ae3f3e7e884471`  
		Last Modified: Wed, 02 Apr 2025 00:10:15 GMT  
		Size: 5.1 MB (5053179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb7fe5967e23e70cc665a972b0acc6e788f725d1dc9c34f13beb85da0916f733`  
		Last Modified: Wed, 02 Apr 2025 00:10:16 GMT  
		Size: 59.8 KB (59827 bytes)  
		MIME: application/vnd.in-toto+json
