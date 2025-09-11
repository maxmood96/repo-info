## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:4b83b585f7c1e6607ea96427c6338848adb92f47052cea2ec82dd7d46e91f0b2
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
$ docker pull rabbitmq@sha256:053908155c02c3604e152fedb7e0738b8d3789bfbc07e13a49699f7589653ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111397493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4109765b068068defa2ebbe7a5331ca9c254b60cb90e64053410b6143c0f45f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Wed, 10 Sep 2025 17:55:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:55:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:55:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_VERSION=4.1.4
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:55:42 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:55:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:55:42 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:55:42 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:55:42 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1657dc0d9d369278d09ca080cbc26c8fe58db814f1463c5ca90c338fe9995650`  
		Last Modified: Wed, 10 Sep 2025 23:40:13 GMT  
		Size: 46.3 MB (46251597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4341c35f1ac19d68e6913f74323f7440ccec35f9683428ede526bb3006df7de2`  
		Last Modified: Wed, 10 Sep 2025 23:40:08 GMT  
		Size: 8.2 MB (8173842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e582adf10fc2b18b355ee4f3940c4204021240ca3a2e824d2d416ece1b719e36`  
		Last Modified: Wed, 10 Sep 2025 23:40:08 GMT  
		Size: 9.5 KB (9456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc55ee2fb7e2acf303530e606859e2e3c8b0c2cf7e644c80eaa9902854fe485`  
		Last Modified: Wed, 10 Sep 2025 23:40:15 GMT  
		Size: 27.2 MB (27237790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ca3313fb13bf7644e65459c4f148c172df0e8cc53b936d788740e144820d54`  
		Last Modified: Wed, 10 Sep 2025 23:40:08 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ff7ca27ef3d6dc18b8623ff753a7025d54c7ab5bf0b47a763fab8a9995b1a4`  
		Last Modified: Wed, 10 Sep 2025 23:40:08 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7643ed928d9db1fb3789407f106d998779f68d8ed9242c6d4543f9702cebbfe`  
		Last Modified: Wed, 10 Sep 2025 23:44:52 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee93b11dbe7855af9107742606e58e6b72c09b95b89064a42daf07009bb9d273`  
		Last Modified: Wed, 10 Sep 2025 23:44:52 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bcd04866f4dbdb00f02915ce24c2e8db86ca716a5931706eb6b60ed4456ed932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18837282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5fe466198d8d3744d241eb73c31eebe7a7064de6ef125387ed432ec45eff2df`

```dockerfile
```

-	Layers:
	-	`sha256:73ae86f679fa4238db9db841f225d3658ce90e81ef21efe4a36bf9fd0835b70d`  
		Last Modified: Thu, 11 Sep 2025 00:53:42 GMT  
		Size: 2.5 MB (2483940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e7b339c8d1cd0d574bc76fbc3f09168225e0bc723404be4ead2018fa6993371`  
		Last Modified: Thu, 11 Sep 2025 00:53:44 GMT  
		Size: 5.4 MB (5378385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85983e771c07ca223707b77feed928921d552ffec88794fbd5fcf5956281b038`  
		Last Modified: Thu, 11 Sep 2025 00:53:48 GMT  
		Size: 5.5 MB (5534990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e47e77d0afd60e7e218309b202bf3ed958638d1b8133678315a30b634255df`  
		Last Modified: Thu, 11 Sep 2025 00:53:50 GMT  
		Size: 5.4 MB (5380127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:475228b4730d93b99963773488d9b4fa7f760aa8d01be2037d87717644fb3f75`  
		Last Modified: Thu, 11 Sep 2025 00:53:51 GMT  
		Size: 59.8 KB (59840 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:7cbeb3833409d21f0b2090ab159d630165e34cbe45db6c43d11160f6adc1f511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93945204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53cd6fe6bfc21d6fc1370a1eea902650dfc384db95fbbfd4fa02e7aa632968e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:22 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:22 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:25 GMT
ADD file:cd43b2c2117454679b981355ba71c009d527d1ebe0a6c3fc69420af222fd6ee7 in / 
# Tue, 19 Aug 2025 14:38:25 GMT
CMD ["/bin/bash"]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Sep 2025 17:05:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_VERSION=4.1.4
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 17:05:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Sep 2025 17:05:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4e823e9332188e662391782d0d87ba101759880efca7a17d9a5a20e8906cc8d7`  
		Last Modified: Tue, 19 Aug 2025 17:59:44 GMT  
		Size: 26.9 MB (26851104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc91fbc73bc08cbe1c7ac8d48978f74126a12bf17b5cd6d6bb135e31b958d08f`  
		Last Modified: Tue, 02 Sep 2025 00:27:03 GMT  
		Size: 33.3 MB (33273013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317f409f8faa44978c1fb6c992da2b412dc2cec5103e0c8aaa81450d97ca7ea`  
		Last Modified: Tue, 02 Sep 2025 00:27:01 GMT  
		Size: 6.7 MB (6670174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9660810db00d3a97a74b84e1e6b602791dbc8c27defd1d1094a12c950edd1cde`  
		Last Modified: Tue, 02 Sep 2025 00:27:00 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf3c0cec57275d453abeeb9c07dc8d797159627405c9fbdc67bd50893b72427`  
		Last Modified: Tue, 02 Sep 2025 19:08:56 GMT  
		Size: 27.1 MB (27139633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0893b3854488b1e7866ad9563f097b0b885f21f8ac7648dcc1a7b653a0d7373`  
		Last Modified: Tue, 02 Sep 2025 19:08:39 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a56f845fca378710ac7fd7f55362127dd914ba4b3bfaf3da2fcfe3a072254bb`  
		Last Modified: Tue, 02 Sep 2025 19:08:39 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a35623f4b1073f81b10eb6f6c2c31ef5af6bc0e74c49ee20f53daaed24851`  
		Last Modified: Tue, 02 Sep 2025 19:08:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2eec1615a4848b7d9fbadbb3bcb6b19fd6e59c70b588e30f9aa7f9c95e6996`  
		Last Modified: Tue, 02 Sep 2025 19:08:39 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:33d5ddefd330b4489fe56f8980e3bdb348ef6e1331a609afc34cf70a34ead67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18292029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103f31ab3b89314e41471af95109ed83733c9bb074e6000e1f72f1d89b35b29c`

```dockerfile
```

-	Layers:
	-	`sha256:08f89cca0d2588441039a41803da64f2a84545727ac193d98b1fe4f2087d47b5`  
		Last Modified: Tue, 02 Sep 2025 21:53:05 GMT  
		Size: 2.5 MB (2484728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4488189cbfb43f21ef21d15c8e6cfe3750cc315b5025df977f765dd33d561f1`  
		Last Modified: Tue, 02 Sep 2025 21:53:06 GMT  
		Size: 5.2 MB (5197165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a31e44a4d856d41544dbb011e8466486a5590a11b0ca67592f3fc734efa00eb`  
		Last Modified: Tue, 02 Sep 2025 21:53:08 GMT  
		Size: 5.4 MB (5351195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e46b70b818d2bcf61c932fda19fd834c3617c4f4d5906c7c59d90e75d9b692c`  
		Last Modified: Tue, 02 Sep 2025 21:53:09 GMT  
		Size: 5.2 MB (5198907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ec0198ee09b7b13080453d2e4e2ea85b8f0a9e7576f4c62dfd392ea81e84d14`  
		Last Modified: Tue, 02 Sep 2025 21:53:11 GMT  
		Size: 60.0 KB (60034 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:54f557e6051235f6408cca6cba408360d3f280bf8cc758915873ef167bb8c92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109309549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f151520c9717495a4939f5ac91583d193d2c03a247e105645d9a906b8a1e9a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Wed, 10 Sep 2025 17:55:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:55:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:55:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_VERSION=4.1.4
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:55:42 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:55:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:55:42 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:55:42 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:55:42 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de8f16e5dc790034eec7a639b07420fcbc1d2a083f413c5d87c949baaf54109`  
		Last Modified: Wed, 10 Sep 2025 23:43:02 GMT  
		Size: 44.3 MB (44340416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14281d7758a4cd5a7f9b719c9c708047352dcd3dbad5a46d6fe2fd7fb567fb6`  
		Last Modified: Wed, 10 Sep 2025 23:42:59 GMT  
		Size: 9.0 MB (8950470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca70d1447f9b2163b8dbae9bee080fa4e0f1923344986415f07f524db56e96c2`  
		Last Modified: Wed, 10 Sep 2025 23:42:59 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef395a6194df387a579b9dc7004195cabe52e2708f29ef9b115b5cf46bbea4e`  
		Last Modified: Wed, 10 Sep 2025 23:43:00 GMT  
		Size: 27.1 MB (27147259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a29e34fc543eae3316f1484adef95cfb3a03e4e69d372767d3d87b292e4329`  
		Last Modified: Wed, 10 Sep 2025 23:42:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e6e3a417fb827e66af0450424db3671d115b2b52994c0a656a54929b7fa840`  
		Last Modified: Wed, 10 Sep 2025 23:42:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53b1fec19d4fb077b374d8351853d19201af9799b584df374f192960235cd83`  
		Last Modified: Wed, 10 Sep 2025 23:43:00 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7beca0bd8a25286aef55e8b7a721103c13a414b2451e76d036767db6aaa6f60`  
		Last Modified: Wed, 10 Sep 2025 23:43:00 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2dd3f02234744e579997af01693e932122af0a262256409a3cb52330947eedab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18896263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633aae7dda632ca02fbcec15f005fb6e427d7f0e33d090229d3fb0d6a5fa7dc0`

```dockerfile
```

-	Layers:
	-	`sha256:181c16727840925f5d8e22421cb9172b549a58e151884a948ab3be266eb234ab`  
		Last Modified: Thu, 11 Sep 2025 00:54:07 GMT  
		Size: 2.5 MB (2485000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4632d59e26a3c64a7e823be4d66afe43f17ddd299827c469ffc1f5bd9cc84cb7`  
		Last Modified: Thu, 11 Sep 2025 00:54:09 GMT  
		Size: 5.4 MB (5397606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c643aa61225a572dbe0ff83e156162ebafbe4d532842ee7cfc4aa50945fd2ae`  
		Last Modified: Thu, 11 Sep 2025 00:54:10 GMT  
		Size: 5.6 MB (5554229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd089a462bb017d6ad424a8081db9959e6cefbf3c8891a88734ad057ef13763f`  
		Last Modified: Thu, 11 Sep 2025 00:54:11 GMT  
		Size: 5.4 MB (5399348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2d558828cec831a24fe7d2c6162a52109bea7aff1fec43a1067407cd6b6b2c6`  
		Last Modified: Thu, 11 Sep 2025 00:54:12 GMT  
		Size: 60.1 KB (60080 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:93a3a02baf65b82ba2df03562ac0b15fed1d2ef923dfcfcf5dad8b0977b17d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.7 MB (109741963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170e313593644ca12b577589220757c0ce09fbf3df7726e3a363031e817c5725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Aug 2025 14:40:27 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:40:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:40:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:40:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:40:31 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 19 Aug 2025 14:40:31 GMT
CMD ["/bin/bash"]
# Wed, 10 Sep 2025 17:55:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:55:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:55:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_VERSION=4.1.4
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:55:42 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:55:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:55:42 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:55:42 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:55:42 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587018be1ae2fb115c60d55a618d09e1e1eadfe33e94da4d7c08c78837ba627b`  
		Last Modified: Wed, 10 Sep 2025 23:41:33 GMT  
		Size: 39.5 MB (39503748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191bcce8f10c06e97e5639f6fb356b40dcdacdae8aab2897c8dfbb9ea2789edd`  
		Last Modified: Wed, 10 Sep 2025 23:41:33 GMT  
		Size: 8.7 MB (8700502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7ee7f9ee0fc9832c6a8882237199f49eb982d72c66cc892518c44b99e62eb9`  
		Last Modified: Wed, 10 Sep 2025 23:41:31 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fbc6c3f60622e49b9bba1e7afca49aab148d75563948b95e95dfba701a787b`  
		Last Modified: Wed, 10 Sep 2025 23:52:40 GMT  
		Size: 27.2 MB (27196982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8473d1b45341289b78ac8a170c99d764501adbd17d33a9d15094fb5e2188e582`  
		Last Modified: Wed, 10 Sep 2025 23:52:36 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2eba22b7b540fcf5c0c84171e6049500a89cdf8a36c53ff4dcd8b64c74de2a5`  
		Last Modified: Wed, 10 Sep 2025 23:52:37 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75be9d48f445d711162145e16b6e129a45a2c366c208c3419c4797cfcffff34d`  
		Last Modified: Wed, 10 Sep 2025 23:52:37 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da18ed3501383ad6267f68c0fd58bcda06a18450a2df54508b21d73d92e83b6d`  
		Last Modified: Wed, 10 Sep 2025 23:52:37 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3aadc626ebc387fe633cf520d3ca02da01ae57adf026e56634e37ba3a798e485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18751654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe28924f98b7f8fdd5fcc83bd03ada11a257825b6a4087650d7204f4960a385d`

```dockerfile
```

-	Layers:
	-	`sha256:ca39c4f97c492df8d958f2f8fe1cb02494efd8daa6b641bdc8dc08bd415ae40f`  
		Last Modified: Thu, 11 Sep 2025 00:54:21 GMT  
		Size: 2.5 MB (2488393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb26cafb354aec590b793c1ed133f2908574e67bb91047d339579915ad30230`  
		Last Modified: Thu, 11 Sep 2025 00:54:23 GMT  
		Size: 5.3 MB (5348327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a5b491126ab9ee1b55901e92bac06360feb582ccc861b3ae8d99469ff25dffd`  
		Last Modified: Thu, 11 Sep 2025 00:54:24 GMT  
		Size: 5.5 MB (5504962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff37f07d471c705ae2b54c634a31f8d0ded7ba1d7ba0e4af38c6817c4702734`  
		Last Modified: Thu, 11 Sep 2025 00:54:25 GMT  
		Size: 5.4 MB (5350069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70802731e8afeccb6673fc0d699519d7835c4099fd73d8ddbc20a94e0303bcb8`  
		Last Modified: Thu, 11 Sep 2025 00:54:26 GMT  
		Size: 59.9 KB (59903 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:571935b87cbd2a2cc52e4d935efc0ceb76d1d6118493acbe88daffaa41ecdc06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103054900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78864a433f5b1156234e8188b5abbca7f8c9784bdc68c09081f7781d7f603e04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Aug 2025 15:03:23 GMT
ARG RELEASE
# Tue, 19 Aug 2025 15:03:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 15:03:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 15:03:24 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 15:04:04 GMT
ADD file:0b905a81cc9e876b16249002e7c59885fde69ab451fd1b6e5768dd8a4b2a9d1d in / 
# Tue, 19 Aug 2025 15:04:08 GMT
CMD ["/bin/bash"]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Sep 2025 17:05:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_VERSION=4.1.4
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 17:05:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Sep 2025 17:05:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6d2d7ce17575561a3deb2625d73936f72b9f13abdb7e3366b85dbb55c4289f94`  
		Last Modified: Wed, 03 Sep 2025 03:54:05 GMT  
		Size: 31.0 MB (30951461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef23a68f9329e90d9492ea374bf2fa48c9b0f7e97e434fc5ae30c8339220186c`  
		Last Modified: Wed, 03 Sep 2025 17:19:50 GMT  
		Size: 35.2 MB (35150433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f47b8b55002275359367a00a227c74675b4f412a343307384dddb5f343bc7d3`  
		Last Modified: Wed, 03 Sep 2025 17:19:47 GMT  
		Size: 9.8 MB (9791859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a422d814eda22341c2ee583e56d51e0aba19988f6a2bd1f2f1938b25d83ede93`  
		Last Modified: Wed, 03 Sep 2025 17:19:47 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536a8f70158d0861485aab101b45c212ac1ffefc9ffd18f19c4b5e132c813441`  
		Last Modified: Wed, 03 Sep 2025 17:30:51 GMT  
		Size: 27.1 MB (27149938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414b161d38b0dad0ec8f4f83916a2ba72ce11d716e2cf5c96f36ab224752e853`  
		Last Modified: Wed, 03 Sep 2025 17:30:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af706fbc25c46eb8274c291ffd7f30872da99e1782ec215e7ffca294252b4f39`  
		Last Modified: Wed, 03 Sep 2025 17:30:48 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295c5e1aec1858225f601ef2560d197fe945b58c53e75efefebc73fe5dad1d1d`  
		Last Modified: Wed, 03 Sep 2025 17:30:48 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8982af22217e2663a8f4013764f26477fd9afb1f4813c97163d92430376ad27`  
		Last Modified: Wed, 03 Sep 2025 17:30:49 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:942ff5ed436b00e4f3fcb9b6b70236ddedfc55b8a430ed063e0c6d2b9cfe5915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18720248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8f390aebddaab15621681c3989e02e1755ef865e277416478f60cc7490e3cd`

```dockerfile
```

-	Layers:
	-	`sha256:fd0ac6dea02f7eb2b3cc86931726b17f9fd767c927923845e686592a0680808b`  
		Last Modified: Wed, 03 Sep 2025 18:53:07 GMT  
		Size: 2.5 MB (2476295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a6e8e4f3d4a36c20ebf55359e61f975e80cb164206ae05a582d6469005de2d`  
		Last Modified: Wed, 03 Sep 2025 18:53:09 GMT  
		Size: 5.3 MB (5342760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f4dbe693c16f2eaf40320e160ca385569125e01dbb393dc6d119cd4c1c33bca`  
		Last Modified: Wed, 03 Sep 2025 18:53:10 GMT  
		Size: 5.5 MB (5496788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea146fdd0fa51c19564e88ff6d124b200c1e533536bda3b33c81e26c60011c9`  
		Last Modified: Wed, 03 Sep 2025 18:53:11 GMT  
		Size: 5.3 MB (5344502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9182f9b73acff43dbbb6f14e1f95c070a57a299cb006cb03de879c7694479b39`  
		Last Modified: Wed, 03 Sep 2025 18:53:12 GMT  
		Size: 59.9 KB (59903 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:98ba62e8f9f5b8b904ee14fbcd4482cb5c659c88ca7969e1724557e1265c8c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103287039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f544de6295b67aae670fab55ac8eee713072d05feed268b0c892e1eb6d94d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Aug 2025 14:39:38 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:39:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:39:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:39:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:39:40 GMT
ADD file:9c3c50a7bf89c14623163f11927acdf7c8624c7519f83f2d95bf5a99ea4d21f9 in / 
# Tue, 19 Aug 2025 14:39:40 GMT
CMD ["/bin/bash"]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Sep 2025 17:05:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_VERSION=4.1.4
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 17:05:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Sep 2025 17:05:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:80a64b6a7d961af355cc1a24ce954958de51e8bc2fb336684c1fbec689663c29`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 29.9 MB (29933009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5913276cafee4d9fc2115a2e9b3123e36ec063f8acf70f0460b4ea5733bb46`  
		Last Modified: Tue, 02 Sep 2025 00:42:55 GMT  
		Size: 38.6 MB (38567294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bb17a23119034d4e524f69cfa6789a9d3ccc88f93d7a343bbde6708e17b7f0`  
		Last Modified: Tue, 02 Sep 2025 00:42:44 GMT  
		Size: 7.6 MB (7556015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3f38e48e6c19d180fd361dc3cdf096e7d8552521c387f3d14583230d73c3f4`  
		Last Modified: Tue, 02 Sep 2025 00:42:42 GMT  
		Size: 9.6 KB (9606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3b5d672a1cd2e995681771f38d77465f1028dcdb723c4c62eb63d842959c42`  
		Last Modified: Wed, 03 Sep 2025 20:16:17 GMT  
		Size: 27.2 MB (27219365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8244301ed93c5b0729fca060dd9174ead9a8920909d972053d8f39c4837f343`  
		Last Modified: Wed, 03 Sep 2025 20:16:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091fe5bad484083e19fd80b74ae7025227347a9d83d188aad1d09d6fa58da4f6`  
		Last Modified: Wed, 03 Sep 2025 20:16:13 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb981eab7a5d83c2f9ebaee31f676276f6c7ac666f1b896fabb7956c86d88d5e`  
		Last Modified: Wed, 03 Sep 2025 20:16:13 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3003df26898d29a21d5cb5f1ab856324c78417280ac0435ab481484330c32af`  
		Last Modified: Wed, 03 Sep 2025 20:16:13 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:13dfc999f9e41655ad559a603925df5aca5aa2324fb2b29548d0579be205d6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18377398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff57eab36649e5dee5e140e3312c5b2119e7348be26028d67c8e2be6aec66452`

```dockerfile
```

-	Layers:
	-	`sha256:9c107795957e7d607a7bfbb8ae04bc67fdeb4685c7ce661cbc3426d2ba05d2ae`  
		Last Modified: Wed, 03 Sep 2025 21:53:19 GMT  
		Size: 2.5 MB (2486038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a365283726edc224e79e5fc5d49df094bc904333f64c94cccbcce8ea3ad19441`  
		Last Modified: Wed, 03 Sep 2025 21:53:22 GMT  
		Size: 5.2 MB (5224832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4107147823cd623b6e210c469519211e76b23fa44b4a631cfecd70b240f7d67`  
		Last Modified: Wed, 03 Sep 2025 21:53:27 GMT  
		Size: 5.4 MB (5380113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d39ed02361f8d50cee62a9814187c2f4eca1fc7fd2f1b5560db9521897417bc7`  
		Last Modified: Wed, 03 Sep 2025 21:53:28 GMT  
		Size: 5.2 MB (5226574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd614cd49c5a3f30d067d19bd629cb3165de194e728aa5a1102d73adbf5f6fc`  
		Last Modified: Wed, 03 Sep 2025 21:53:29 GMT  
		Size: 59.8 KB (59841 bytes)  
		MIME: application/vnd.in-toto+json
