## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:9de92946751becfd843f47322d28b7d58d525f5bbb39694b03b66740f4915f6b
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
$ docker pull rabbitmq@sha256:1cfcd1cdf4318598df854107035e7813816aa007d7267eba74a7fff8eae4745c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112962602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7c654d7ee063cc8c054b6550153df356a4cba1b7010cb6f8f1d979b5388320`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Thu, 12 Mar 2026 23:40:44 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 12 Mar 2026 23:40:44 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 12 Mar 2026 23:40:44 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 12 Mar 2026 23:40:44 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 12 Mar 2026 23:40:44 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Mar 2026 23:40:44 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 12 Mar 2026 23:40:46 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 12 Mar 2026 23:40:46 GMT
ENV RABBITMQ_VERSION=4.2.4
# Thu, 12 Mar 2026 23:40:46 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 12 Mar 2026 23:40:46 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 12 Mar 2026 23:40:46 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Mar 2026 23:41:08 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 12 Mar 2026 23:41:08 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 12 Mar 2026 23:41:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 12 Mar 2026 23:41:09 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 12 Mar 2026 23:41:09 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 12 Mar 2026 23:41:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 12 Mar 2026 23:41:09 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 12 Mar 2026 23:41:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 12 Mar 2026 23:41:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:41:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Mar 2026 23:41:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 12 Mar 2026 23:41:09 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b229f81a7125fc47389f7fc077c0a33145255527aa52fab410ebae91a9bcc6`  
		Last Modified: Thu, 12 Mar 2026 23:41:32 GMT  
		Size: 46.3 MB (46276558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ba7f0f74acb1ade7271dc4a80d5d008adeef5931b117ac23aae8f9469ff410`  
		Last Modified: Thu, 12 Mar 2026 23:41:30 GMT  
		Size: 9.0 MB (8985483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a8afee7a92b8365ead7cb8a82523e365ea11cf0269ec000153e15face4fe3d`  
		Last Modified: Thu, 12 Mar 2026 23:41:29 GMT  
		Size: 9.7 KB (9669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82c46731797e48cf1dc4f7c4aa0adbfa7fdb1e14b6589625aadc934378cdfc9`  
		Last Modified: Thu, 12 Mar 2026 23:41:31 GMT  
		Size: 28.0 MB (27961537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395b95c3ac69a2558ef05a1d320a6ee9bd77abf7cbb623b6d05c17dd891c071f`  
		Last Modified: Thu, 12 Mar 2026 23:41:31 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1fc15e88b37bc1440a078e60adc3f288a8c27f9c38ec387dda47142d8123ae`  
		Last Modified: Thu, 12 Mar 2026 23:41:31 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce70209a250612c710e8c5c9ce5589598b32ce8947802dad216081b24a769dfa`  
		Last Modified: Thu, 12 Mar 2026 23:41:32 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ec9ef1f0ccd9aed165ba52a017671ff5f9338bf0816e9c4641459beb789965`  
		Last Modified: Thu, 12 Mar 2026 23:41:33 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9389bae3664a74d9f9e34535161347763bcf521880eb7e3ce1e808222bace033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18840653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545a81a2407fc7170ebeb36132538a29e340553209203d6d9903915fd8eb426e`

```dockerfile
```

-	Layers:
	-	`sha256:b369b2232cd142e189ae4c205327dd278ae63396b25610b6f945e0b0bb83dd6a`  
		Last Modified: Thu, 12 Mar 2026 23:41:30 GMT  
		Size: 2.5 MB (2486599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deb93abfcafeafc7e79303f6533d7148179ef379f169faeeda25464570e92861`  
		Last Modified: Thu, 12 Mar 2026 23:41:30 GMT  
		Size: 5.4 MB (5378497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95699162b068bd7e62941ed37fdc4ccac8548b88932e742f7a32e90836206b2a`  
		Last Modified: Thu, 12 Mar 2026 23:41:30 GMT  
		Size: 5.5 MB (5535126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0464a22ec944ae1495a8408e15f6637fef0cfac389e77cc7fcd74aeb76b3f5da`  
		Last Modified: Thu, 12 Mar 2026 23:41:30 GMT  
		Size: 5.4 MB (5380239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac53ff51319284581736a5fbf88bea9c70cf562690f0cdb1d10f8269d71ce267`  
		Last Modified: Thu, 12 Mar 2026 23:41:31 GMT  
		Size: 60.2 KB (60192 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:d5758ecb58dd117947c5132efa0589fd0d30450f216070ed50ccf6931e92eb44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95344009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e26b93754f56c2eeceff4cc49d5c9b6c975e57fd41327c0b65ec85edea28e5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 10 Feb 2026 16:51:23 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:51:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:51:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:51:24 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:51:27 GMT
ADD file:9633092e110ed5475e9e31841bcc6e288ca09c116e102d75694089f384f549b3 in / 
# Tue, 10 Feb 2026 16:51:28 GMT
CMD ["/bin/bash"]
# Thu, 12 Mar 2026 23:51:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 12 Mar 2026 23:51:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 12 Mar 2026 23:51:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 12 Mar 2026 23:51:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 12 Mar 2026 23:51:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Mar 2026 23:51:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 12 Mar 2026 23:51:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 12 Mar 2026 23:51:42 GMT
ENV RABBITMQ_VERSION=4.2.4
# Thu, 12 Mar 2026 23:51:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 12 Mar 2026 23:51:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 12 Mar 2026 23:51:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Mar 2026 23:52:03 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 12 Mar 2026 23:52:04 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 12 Mar 2026 23:52:04 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 12 Mar 2026 23:52:04 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 12 Mar 2026 23:52:04 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 12 Mar 2026 23:52:04 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 12 Mar 2026 23:52:04 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 12 Mar 2026 23:52:04 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 12 Mar 2026 23:52:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:52:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Mar 2026 23:52:04 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 12 Mar 2026 23:52:04 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:dd135084b7c993802b7c1ba97d192c201727ddf710812c361d5441cb729f5c20`  
		Last Modified: Tue, 10 Feb 2026 17:41:49 GMT  
		Size: 26.9 MB (26855457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edc18782ea25719ce8ed8c489784fc05feda6039c610c00c17d558177022839`  
		Last Modified: Thu, 12 Mar 2026 23:52:29 GMT  
		Size: 33.3 MB (33314012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47475cf58b5df94f47f8c78427ad47ea871752e4dd347502c035dc1365de4be0`  
		Last Modified: Thu, 12 Mar 2026 23:52:28 GMT  
		Size: 7.3 MB (7301112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fae42988fcd158563b924ddcf7c354bc0884685b2c70329904ed9c2b51cad8`  
		Last Modified: Thu, 12 Mar 2026 23:52:27 GMT  
		Size: 9.7 KB (9742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83084e7def45f14f95668c8cfcbaa24316d665ceb3fb9cfb4b142208ce88748a`  
		Last Modified: Thu, 12 Mar 2026 23:52:29 GMT  
		Size: 27.9 MB (27861938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26e36d89c930a2e23da0a07dc8e5f32f9fa4af536895bdef9a1251e455ae8fd`  
		Last Modified: Thu, 12 Mar 2026 23:52:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06291e26ea7a8206e5b4b754b0fd34de1eca93d5f0ba7dd23803ceab372c8b50`  
		Last Modified: Thu, 12 Mar 2026 23:52:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8bf3d02cdedc9986af88bc504ac1572f79aa7591495704a7d012113309a8b6`  
		Last Modified: Thu, 12 Mar 2026 23:52:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ffb09a2df382c340f73c678faad96927bc643d370bf2d4585e82df847b0e1e`  
		Last Modified: Thu, 12 Mar 2026 23:52:30 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e50b9d9be06987e352d48adefec7ff64e1f9f5c22a705fa1e6d9f82ceba55434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18295375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6af04405356b5a9a83073bc863f7fadc339aeb92adb86227ebe67b439683827`

```dockerfile
```

-	Layers:
	-	`sha256:f68753e6e55691180f8b5f0215ab03ace7f745deeb98f6fb78643e422566d633`  
		Last Modified: Thu, 12 Mar 2026 23:52:27 GMT  
		Size: 2.5 MB (2487399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7372a083c15e00196bfd4aaa0bbaaed1c16b93a68fc2ed5dd40b03b75f229554`  
		Last Modified: Thu, 12 Mar 2026 23:52:27 GMT  
		Size: 5.2 MB (5197257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88c80cea0f2541055d6a5b16e7b0430f4276f9913ac6792eb99b0168bc0b962b`  
		Last Modified: Thu, 12 Mar 2026 23:52:27 GMT  
		Size: 5.4 MB (5351331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a302b561ee63f986016d0720b8ac14990141d561ad0a7b5011bb9799382aa516`  
		Last Modified: Thu, 12 Mar 2026 23:52:27 GMT  
		Size: 5.2 MB (5198999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc05fa2e342d787da7e54ef3aa6bd0a663476e7930d1529c402b350ecaa47549`  
		Last Modified: Thu, 12 Mar 2026 23:52:28 GMT  
		Size: 60.4 KB (60389 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:e67343c598f3fab51a9d7925909dea373fcaa2d77dc0d5bb8992d63c276ebfc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110839791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aedd5b5691c7cb233a8ea6a38ece65c63bce1dd8759937d900687723d6d469fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Thu, 12 Mar 2026 23:43:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 12 Mar 2026 23:43:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 12 Mar 2026 23:43:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 12 Mar 2026 23:43:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 12 Mar 2026 23:43:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Mar 2026 23:43:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 12 Mar 2026 23:43:56 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 12 Mar 2026 23:43:56 GMT
ENV RABBITMQ_VERSION=4.2.4
# Thu, 12 Mar 2026 23:43:56 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 12 Mar 2026 23:43:56 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 12 Mar 2026 23:43:56 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Mar 2026 23:44:18 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 12 Mar 2026 23:44:19 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 12 Mar 2026 23:44:19 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 12 Mar 2026 23:44:19 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 12 Mar 2026 23:44:19 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 12 Mar 2026 23:44:19 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 12 Mar 2026 23:44:19 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 12 Mar 2026 23:44:19 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 12 Mar 2026 23:44:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:44:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Mar 2026 23:44:19 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 12 Mar 2026 23:44:19 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa4cece72afdbe7366edf4080f3b0af5fd643f4e79468ae570d3f31eda17d32`  
		Last Modified: Thu, 12 Mar 2026 23:44:45 GMT  
		Size: 44.4 MB (44382402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241b089c5b0c3ba65d3c927b45ec87abf48dfed6c5714849f8d365eac8675cc1`  
		Last Modified: Thu, 12 Mar 2026 23:44:44 GMT  
		Size: 9.7 MB (9708967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e07011b0518fd43e074beadb3d666483c03ccb61d3846c2ddf70d0b31437cb`  
		Last Modified: Thu, 12 Mar 2026 23:44:43 GMT  
		Size: 9.6 KB (9638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f391374c3576edff73f75a9a5bedd70b5dfe9a8401555975fc926c840276be6`  
		Last Modified: Thu, 12 Mar 2026 23:44:45 GMT  
		Size: 27.9 MB (27871914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92e0da0fc84a81f0d3d92feaa30f1956b1ed342028f5c81f042e5ccab142a00`  
		Last Modified: Thu, 12 Mar 2026 23:44:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671520f6ed9eb91aecbd0b81ab612353b5ee39637c7906bd46b284d813b3fc03`  
		Last Modified: Thu, 12 Mar 2026 23:44:45 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60f115d05fe6cc7648a140032f450fffa6219890f2873f474e0555e7b1dd18b`  
		Last Modified: Thu, 12 Mar 2026 23:44:46 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0cb2e3c7aac68c2967bd13b186bfcbefb1eeaf618bf5723dc6ea63dfd2d7f4`  
		Last Modified: Thu, 12 Mar 2026 23:44:46 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6278589671fcf19f629c9ad80cec19dea55aa33c4ffdc03d11404c724121491c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18899621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed3bcccb260a61795e61e4e57831d2030ec8645a8d468dc8d2d35004ca40314`

```dockerfile
```

-	Layers:
	-	`sha256:042a31c396b8eda09786cf818c0174ec34c44bf55bfd2dfd1756fa6427c36241`  
		Last Modified: Thu, 12 Mar 2026 23:44:43 GMT  
		Size: 2.5 MB (2487659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7df258d8f12083ec2a7b23e435744b21c9cf1bb1847ed72bcaef4422661cff6d`  
		Last Modified: Thu, 12 Mar 2026 23:44:44 GMT  
		Size: 5.4 MB (5397714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5f157d0d945ceda57b68df217186ca159ad951a240c0f164f194a2436bc4699`  
		Last Modified: Thu, 12 Mar 2026 23:44:44 GMT  
		Size: 5.6 MB (5554361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9cea81b77bc0102ee5f5db2f9b6294d55f3eb3a2f073b0f3e4df825d56df57`  
		Last Modified: Thu, 12 Mar 2026 23:44:44 GMT  
		Size: 5.4 MB (5399456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ea92bd38f0908736186d6a52b1520cf91e8bad92160257e0876b3c24c41aff`  
		Last Modified: Thu, 12 Mar 2026 23:44:45 GMT  
		Size: 60.4 KB (60431 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:0c972ae19ed49abfc341feed7744bc5cf3cf16729809460a72ff9fea0774ba3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111353190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4574edf47c01b72d06f425ab42fadb3d108715c56b989f76eeff7bef28e8dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 00:51:04 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 13 Mar 2026 00:51:04 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 13 Mar 2026 00:51:04 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 13 Mar 2026 00:51:04 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 13 Mar 2026 00:51:04 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 00:51:04 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 13 Mar 2026 00:51:07 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 13 Mar 2026 00:51:07 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 13 Mar 2026 00:51:07 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 13 Mar 2026 00:51:07 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 13 Mar 2026 00:51:07 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 00:51:43 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 13 Mar 2026 00:51:45 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 13 Mar 2026 00:51:45 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 13 Mar 2026 00:51:45 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Mar 2026 00:51:45 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Mar 2026 00:51:45 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 13 Mar 2026 00:51:45 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 13 Mar 2026 00:51:46 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 13 Mar 2026 00:51:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 00:51:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 00:51:46 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 13 Mar 2026 00:51:46 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cdfcf10184904836e89d8692ee6b2e6d4523ffe34ee53d15ebcc276f57ea5b`  
		Last Modified: Fri, 13 Mar 2026 00:52:38 GMT  
		Size: 39.5 MB (39521265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0db9e2dd74ffb542b11bfe879b330d596391a57a87f0d1025fc495a8774cc4`  
		Last Modified: Fri, 13 Mar 2026 00:52:37 GMT  
		Size: 9.6 MB (9591922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd73f530a368eb8de2837769afe737efa61a6559f784012985da90ba7858e5d`  
		Last Modified: Fri, 13 Mar 2026 00:52:35 GMT  
		Size: 9.6 KB (9646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8faea42b0510efe3dbab5d01e007a025fd8268445d3c59ab0e7b3f6eaa8bc31`  
		Last Modified: Fri, 13 Mar 2026 00:52:37 GMT  
		Size: 27.9 MB (27921698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824c7c6061f864c4bb939efa8c89933ebc6b7610318dae6fc0749f7f74827c96`  
		Last Modified: Fri, 13 Mar 2026 00:52:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c83cf9a371dc5e36b5faa11bd5a1eebcca1e55752bf037d1647c058f3a74c85`  
		Last Modified: Fri, 13 Mar 2026 00:52:38 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ad6ffd8bef9a66df5e5c6c8b649802418df4324aca7b100bf360f51702dc2b`  
		Last Modified: Fri, 13 Mar 2026 00:52:38 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cbdfaffed3922ec7b3634f2b64be9bfe30f17de9c4b3643b5786a890e10265`  
		Last Modified: Fri, 13 Mar 2026 00:52:39 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ff7df8d8127f08d7c1efb54565c56190990f69151ef1bcaa33f123473212c2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18755012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b103a347cb72501155d4e68308b458440135cda4e0eb25d4ea39da0c9df2ad4`

```dockerfile
```

-	Layers:
	-	`sha256:83e9093f3f9f32573cd6ac3d3a05f10c59c35b0015399660e6db620483069b60`  
		Last Modified: Fri, 13 Mar 2026 00:52:36 GMT  
		Size: 2.5 MB (2491052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1abf22fa56c95f5c86ab7f50e4f1288bafa53255d2159e9dc27dc4c1db24cfc`  
		Last Modified: Fri, 13 Mar 2026 00:52:36 GMT  
		Size: 5.3 MB (5348435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97654f2fd1407cadd828accd162672bca1646a10e972c73aafb6027b18d62c2`  
		Last Modified: Fri, 13 Mar 2026 00:52:36 GMT  
		Size: 5.5 MB (5505094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b837a7d2290c2cc7c429de2067589f50beda70e5c80a3255720121b01d7b425`  
		Last Modified: Fri, 13 Mar 2026 00:52:36 GMT  
		Size: 5.4 MB (5350177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6cfd61b68ff8d9205315bc9366be30c18715db3d344f7888a85f94d91cc4234`  
		Last Modified: Fri, 13 Mar 2026 00:52:37 GMT  
		Size: 60.3 KB (60254 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:93eb0550f6e2273cd1b418b256cf67a4b66693859bef2751e4ef7edd934b5a8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104843423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56148872f44c2cf53299af045c536055e2c872585c882eda619cf0a8d01d4a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 10 Feb 2026 17:33:09 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:33:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:33:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:33:10 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 17:33:55 GMT
ADD file:b4821892707dbb5cc8e8eb3b4e757edc2d124db81fcdedfc3b244dcb5c1fa6c0 in / 
# Tue, 10 Feb 2026 17:34:00 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 21:05:32 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 13 Mar 2026 21:05:32 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 13 Mar 2026 21:05:32 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 13 Mar 2026 21:05:33 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 13 Mar 2026 21:05:33 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 21:05:33 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 13 Mar 2026 21:05:36 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 13 Mar 2026 21:05:36 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 13 Mar 2026 21:05:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 13 Mar 2026 21:05:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 13 Mar 2026 21:05:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 21:07:55 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 13 Mar 2026 21:08:04 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 13 Mar 2026 21:08:04 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 13 Mar 2026 21:08:04 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Mar 2026 21:08:04 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Mar 2026 21:08:04 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 13 Mar 2026 21:08:04 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 13 Mar 2026 21:08:04 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 13 Mar 2026 21:08:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 21:08:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 21:08:05 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 13 Mar 2026 21:08:05 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f2683d5e2cbe038b4f1178e139d507e705e0a3a566f8b9c89bf3484f426119af`  
		Last Modified: Tue, 10 Feb 2026 17:42:05 GMT  
		Size: 31.0 MB (30954431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14b0fd98874c5ea9440b6f4041f5d9f924f068fcad019fd46e77e82fe333b68`  
		Last Modified: Fri, 13 Mar 2026 21:14:38 GMT  
		Size: 35.2 MB (35174557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5567215dcaafcf4f3d7a09bf170dbc905e931df84c13cb7ba3e7660d2be8c402`  
		Last Modified: Fri, 13 Mar 2026 21:14:31 GMT  
		Size: 10.8 MB (10828919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea9699bf3b517ee4792ac34fb8bc46f03210de86ef089dee25ce234bdae4a0e`  
		Last Modified: Fri, 13 Mar 2026 21:14:25 GMT  
		Size: 9.7 KB (9703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c7ccf54945740572f89944882b141cc9476f7e27915505d32d523d79065937`  
		Last Modified: Fri, 13 Mar 2026 21:14:37 GMT  
		Size: 27.9 MB (27874063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a2b97141ec7a68f6744637af21f40add0d7478ef1f3c0b7fd5f24e1f349ee4`  
		Last Modified: Fri, 13 Mar 2026 21:14:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a22b6899574ab1e99e7fe13b7734fa186540090dea63b85f278e656bf8aa5e`  
		Last Modified: Fri, 13 Mar 2026 21:14:32 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1363c4b2705ce407ac4612ea6a535f30e773b63c50ccc1da5d35b5a8f655f7e3`  
		Last Modified: Fri, 13 Mar 2026 21:14:33 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847652964e681cc6bfdce07a52e58825f14324fc8535dfa46400adf6e86fccf0`  
		Last Modified: Fri, 13 Mar 2026 21:14:34 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f19dda857b5bfe9fa5287cc12f182dda5320676ceca232dd0a991dff69e92c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18723609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173b58f05f1c8cada1a3a8bcd1f55ae103d9c719239711c9ba56f1083d57a688`

```dockerfile
```

-	Layers:
	-	`sha256:eba40771abe87429aa96c69bf03e892c2192591e894d6f4636c7849330b87659`  
		Last Modified: Fri, 13 Mar 2026 21:14:28 GMT  
		Size: 2.5 MB (2478966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d6aadbe81fd703e4ddaa0c583cb667a7e4c43cce316dcfb8c4ab0dbb3b354e`  
		Last Modified: Fri, 13 Mar 2026 21:14:29 GMT  
		Size: 5.3 MB (5342856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6c9419b6fb7c7638ada9851995eb78bb9a637e7a425bf3763c5bb683c702dd6`  
		Last Modified: Fri, 13 Mar 2026 21:14:30 GMT  
		Size: 5.5 MB (5496928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb6fde80d69d3a787d6edc1b4b29f016f2875d0586f9f97a6d37849ab790704c`  
		Last Modified: Fri, 13 Mar 2026 21:14:29 GMT  
		Size: 5.3 MB (5344598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1632766c9c0e2096c5eb2bca8423b8739c6c56843e4876b91002bbe09b2fdde0`  
		Last Modified: Fri, 13 Mar 2026 21:14:31 GMT  
		Size: 60.3 KB (60261 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:e57252e7c5e21c9785de702a2ce5c6d0bd65599b136dae54bc6df4fcc80e0998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105095568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f1a7c264544d9c1156c21db6d5761ef78f7646a7c844ece08b405ec3739ee6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:51 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:52 GMT
ADD file:be1799101a7a15f881e3aebea1e86fa6a156760dc7688b1affe179e948814a3b in / 
# Tue, 10 Feb 2026 16:50:52 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 00:14:01 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 13 Mar 2026 00:14:01 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 13 Mar 2026 00:14:01 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 13 Mar 2026 00:14:01 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 13 Mar 2026 00:14:01 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 00:14:01 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 13 Mar 2026 00:14:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 13 Mar 2026 00:14:02 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 13 Mar 2026 00:14:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 13 Mar 2026 00:14:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 13 Mar 2026 00:14:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 00:14:19 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 13 Mar 2026 00:14:20 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 13 Mar 2026 00:14:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 13 Mar 2026 00:14:20 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Mar 2026 00:14:20 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Mar 2026 00:14:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 13 Mar 2026 00:14:20 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 13 Mar 2026 00:14:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 13 Mar 2026 00:14:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 00:14:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 00:14:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 13 Mar 2026 00:14:20 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8b6ba492713239cba0554ce53d24405e1285684fa64bcfb05df4af8037ba5836`  
		Last Modified: Tue, 10 Feb 2026 17:42:12 GMT  
		Size: 29.9 MB (29909784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd47d2bcc1fdf89d03a8d450bfac94b80babef66da004fc61a39c94b7875eee9`  
		Last Modified: Fri, 13 Mar 2026 00:15:01 GMT  
		Size: 38.6 MB (38615977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af85c89af5a0f2c5b53b3f78cab6d963bd0a5a39ca6143328c557470c0bee745`  
		Last Modified: Fri, 13 Mar 2026 00:15:00 GMT  
		Size: 8.6 MB (8613454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf146eada679cd62ff4846d075b0bd647f1bd26d5e330bbb0173fab438800bf`  
		Last Modified: Fri, 13 Mar 2026 00:14:59 GMT  
		Size: 9.8 KB (9804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05de6cbf9d5dc85a09599bf0980df2bf026ebd31d67b04e9f54bb9a403b3f59`  
		Last Modified: Fri, 13 Mar 2026 00:15:01 GMT  
		Size: 27.9 MB (27944799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92bcab7380c6cfe294a535170df98bd4ffd9ce07e3023d8b4ebfe9ad57b15b8`  
		Last Modified: Fri, 13 Mar 2026 00:15:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a695c3ce0b5837e9f3c4437eafa3f9bb03adfb42fe5e238e968f50fda84f69e`  
		Last Modified: Fri, 13 Mar 2026 00:15:01 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4620a7493093f06466d007ff6b5e33d4f01daf5e5e48fc5565e4f32d1140c55e`  
		Last Modified: Fri, 13 Mar 2026 00:15:01 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e647954db1e5dcde517423a864db67b3b149ec1cb36a8d1f78bb76966674b79e`  
		Last Modified: Fri, 13 Mar 2026 00:15:02 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b1296bb54f5b5d874ff95420d6f435cbf98945a970402c7a473431462342a259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18380751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e53b4ff32e3f5497df77896b1cd3c40f31a4b90a83bc792b2473d58be22c18b`

```dockerfile
```

-	Layers:
	-	`sha256:e5db13d1d758c2fcce70a88ab33e46e5cad4273fc8f69a9216b02ae3ba3de71b`  
		Last Modified: Fri, 13 Mar 2026 00:15:00 GMT  
		Size: 2.5 MB (2488709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d0df867d9d7846ffe444b61eb6a77e6f58d7b41f9b63c46d1d5a62e89971c63`  
		Last Modified: Fri, 13 Mar 2026 00:15:00 GMT  
		Size: 5.2 MB (5224928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34fa9db4a4c90462aaca7154e529e4df7a99ab3948df5dfe16450dd77be35c41`  
		Last Modified: Fri, 13 Mar 2026 00:15:00 GMT  
		Size: 5.4 MB (5380253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14ee88f0ba2f3fcb5b67adff5a37dd6eaacd14fd61d7f474c87fbda02c66cd1`  
		Last Modified: Fri, 13 Mar 2026 00:15:00 GMT  
		Size: 5.2 MB (5226670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae4fd6b44be796662360fdcf77de3fa5cfa068722537d844f7a950044a9b4568`  
		Last Modified: Fri, 13 Mar 2026 00:15:01 GMT  
		Size: 60.2 KB (60191 bytes)  
		MIME: application/vnd.in-toto+json
