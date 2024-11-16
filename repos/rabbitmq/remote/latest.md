## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:69ae77844942b8b37d4eae9cb2c9b4173425e534ac6efcf00928756951774c3f
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
$ docker pull rabbitmq@sha256:32e16c01355c4af22da981ede96fe357ff5d33ee68478ba389db8a4ddbd7c937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104283316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152ffd7f55d350d98ec491206a0ecaae9707be48b10ec47fe4179f81e7c0cba8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:35:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_VERSION=4.0.3
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:35:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:35:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211e97f904c753a0a9e2db4596264959aa3c139b085764447d2f00362ae32f7f`  
		Last Modified: Sat, 16 Nov 2024 03:03:56 GMT  
		Size: 45.5 MB (45453366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d633cb09dfb6b185f2584d465e351ab124bdb860fea8df661d3d3a97ea5ba7`  
		Last Modified: Sat, 16 Nov 2024 03:03:55 GMT  
		Size: 8.2 MB (8169210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0357761da170b8d17e375db368919eaa18c91adec2968d2c5680e6cac10f63db`  
		Last Modified: Sat, 16 Nov 2024 03:03:55 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca95b127b98a6a1091634ffb248d8ecdd9d20529cee9e8e31bf0151274d7d42f`  
		Last Modified: Sat, 16 Nov 2024 03:03:55 GMT  
		Size: 20.9 MB (20897734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec3ceaa0dcba779aab3af5b80e900a718e0b5789332eb1fed8671f667638fcc`  
		Last Modified: Sat, 16 Nov 2024 03:03:56 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7037c52023fb797ea2327194526e1e205c5ef2b9a363ad0b58c2cb2b1cfd6677`  
		Last Modified: Sat, 16 Nov 2024 03:03:56 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d738327fa668a4bc0cea1ba22f7cc6175be0da3fda47a9831bb8070d55e2fd9d`  
		Last Modified: Sat, 16 Nov 2024 03:03:56 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a286d22c8dd8c2817f912bb9bbe83f4cebef78f581dad6b743b2628cec0be29`  
		Last Modified: Sat, 16 Nov 2024 03:03:56 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2cd702e9903eaa1413e8d5fc70b6f066daa28aad9ed200f9abdc89d416cf108e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18218273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e827e8c47683c21c5714fa374fdfe4949b94adfe223de166b11e57b716f4ec`

```dockerfile
```

-	Layers:
	-	`sha256:953eb04cf3c4f6a1a9a7361ce9d0189994e76e50ade386dddb84781f2a1f8402`  
		Last Modified: Sat, 16 Nov 2024 03:03:55 GMT  
		Size: 2.4 MB (2365049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:021d6bf5858310411fc4bc428490ac70e8445a38bcede0e27abb8f2e851264f1`  
		Last Modified: Sat, 16 Nov 2024 03:03:55 GMT  
		Size: 5.2 MB (5210915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de2d9204a87b6ab5f9dd1aae046c7c93a0971be74563ec1d7f83afe798784c65`  
		Last Modified: Sat, 16 Nov 2024 03:03:55 GMT  
		Size: 5.4 MB (5368422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d16dce3fd877a919028b0b11f27f19ed45a7e7aa93656b897317d0b1c2bc0d`  
		Last Modified: Sat, 16 Nov 2024 03:03:55 GMT  
		Size: 5.2 MB (5212649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:434eb3df5ade5b3040e7f3bacaf3e700b04fc7f65d17e74a61b81bc0bde5ee79`  
		Last Modified: Sat, 16 Nov 2024 03:03:56 GMT  
		Size: 61.2 KB (61238 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:6c0383d6a187dc824061568533d2640b8b23d888b3ebf973a0b383f8e5091561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87470697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6d1f498a5abd525bce6c8b18527d2a3ede2dc38d4ac084c753ced95279ad6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:48 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:48 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:51 GMT
ADD file:9ba898ef47e3bf423fea81a90820aff75f6eed50ba716f3cba79e91e03e5cbbb in / 
# Wed, 16 Oct 2024 09:25:51 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:35:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_VERSION=4.0.3
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:35:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:35:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:bca51b985bec22ed70905f426f055641ef48b89c81b90c99246fed6ff752a789`  
		Last Modified: Wed, 16 Oct 2024 12:48:18 GMT  
		Size: 26.9 MB (26869468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84000dc852aad33ee1b51d4d1a169af41a57566f5bb8a1ecd01eb6323cb02930`  
		Last Modified: Sat, 16 Nov 2024 03:12:42 GMT  
		Size: 33.1 MB (33123940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefbd82256e0e2bf807b9af63d00cb881dd15d7bd00f6fe793acc3d7868b72b5`  
		Last Modified: Sat, 16 Nov 2024 03:12:41 GMT  
		Size: 6.7 MB (6667929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e78ec9ce5910e2a53b2ceeca4ac4b3aaf15f2ecfb74e1f634d3bc91ff8cc45`  
		Last Modified: Sat, 16 Nov 2024 03:12:41 GMT  
		Size: 9.6 KB (9552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67994655ddd9ab43133c22ba3395bebb9bb3db5253eef998fdd857836f456af8`  
		Last Modified: Sat, 16 Nov 2024 03:12:42 GMT  
		Size: 20.8 MB (20798063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7aa475fc287564aebb8b6327a6d9ed634a6600b3f7316c5e01d6670ee43d9f`  
		Last Modified: Sat, 16 Nov 2024 03:12:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8af4298f4c46db6794f52c2041ddbe5606b94d0468b78f0ba6bd3741bcc9d7`  
		Last Modified: Sat, 16 Nov 2024 03:12:42 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9b853f5e6abe40605f534756cc600902e5e6159c7ea123eaf591bb1c0ce1ee`  
		Last Modified: Sat, 16 Nov 2024 03:12:43 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c888f1b4de601d634d6508762672f09145c450045a3df7ad525fbcd8bb9fa5d7`  
		Last Modified: Sat, 16 Nov 2024 03:12:43 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:773e518141fb4e49566a5a232f3b6257213ad920ff486a9d2e429823eaaf6485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17679601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3108f67add46d6d88610b127e6f00ecb4b14f42269bd95eae28b82443451a59`

```dockerfile
```

-	Layers:
	-	`sha256:a8f841a0fda0872abc26e4ee83d02e5bd4b2ff1eb0e2fb14003a0f4c2f866469`  
		Last Modified: Sat, 16 Nov 2024 03:12:41 GMT  
		Size: 2.4 MB (2365846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c159c55f458f06772fda291c58d68e1b1c732498b7f8711ffeba6ae46f4909c2`  
		Last Modified: Sat, 16 Nov 2024 03:12:41 GMT  
		Size: 5.0 MB (5031881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c847d327de5d91d8658b1f3c37deb0df0bdba743af603dded8eb27a0b67c615`  
		Last Modified: Sat, 16 Nov 2024 03:12:41 GMT  
		Size: 5.2 MB (5186829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a24644e3e03f335824db72f80e1cc465fda25d5e93a3a41a977741e8a8d6bc40`  
		Last Modified: Sat, 16 Nov 2024 03:12:41 GMT  
		Size: 5.0 MB (5033615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec8ce82340f713d53169ca13bf4a770a6d35245c63fda7e777d80bd57ee6f16c`  
		Last Modified: Sat, 16 Nov 2024 03:12:42 GMT  
		Size: 61.4 KB (61430 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:7d5706befc589ac4ae4f4fb103fcff0760cfae241d35b6ade2a1c5d05f098d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102138022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fa1b148edcda0a8c3b4c71f0dc12b36d9fb8b9ac4c5c733b562fbb529dd1bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:35:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_VERSION=4.0.3
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:35:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:35:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef084e46b4bc1e8342656ab4b35c0c1618fd669ab7a5db8de05cee37afef9080`  
		Last Modified: Sat, 16 Nov 2024 03:38:12 GMT  
		Size: 43.5 MB (43493174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba8d668074847a3e9d9a955f6fee84e3a5498c4a80d573696ca39e0f13ce6b9`  
		Last Modified: Sat, 16 Nov 2024 03:38:11 GMT  
		Size: 8.9 MB (8934200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdeb8c256562f2b4c8e41fad24babece4fa040b99221eaaef4475e6f47a8095`  
		Last Modified: Sat, 16 Nov 2024 03:38:10 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0f1d37d93de1759b773f4413adc67feaff3eff455be933a14215aea3d74b7c`  
		Last Modified: Sat, 16 Nov 2024 03:38:11 GMT  
		Size: 20.8 MB (20807014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccdec49b0261138b03ec092a5ea6a7feceed9f5a0d67608f036f44af40f5b5c`  
		Last Modified: Sat, 16 Nov 2024 03:38:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da5e4ce4e637e2ce08e140bd11b88d06e77184d887a1e0fc2bf30ed26038d1f`  
		Last Modified: Sat, 16 Nov 2024 03:38:12 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c88fe1ba22f686571a860e87aa090e455ed1d26ce9994a1adb0b2f3506fc95`  
		Last Modified: Sat, 16 Nov 2024 03:38:12 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39abd5419309d5dfbd4eaaf8204cef83ca43144ad5b52dae9d9de8fd3f6166e`  
		Last Modified: Sat, 16 Nov 2024 03:38:13 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1dfdc4a7d660cde1335bdc5d76d9134c974dd310a16fcd60b0fd3fe534cdb359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18278447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf40382f491cbcce57474d5d0421c34ebf75de3a08c6768d6942494c0b6833e`

```dockerfile
```

-	Layers:
	-	`sha256:8229ce94879999a4645c8604d8f438ca210fdf35e27483aa02eedfa3eda2fb94`  
		Last Modified: Sat, 16 Nov 2024 03:38:11 GMT  
		Size: 2.4 MB (2366109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a30467d5c4d5777bad85ab8651aadf54db996153b7f7fda3583ba3f067f95161`  
		Last Modified: Sat, 16 Nov 2024 03:38:11 GMT  
		Size: 5.2 MB (5230534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0bc80f7b598326ccd5f990d4e6db568531b6f5ec86b543a2eb5283434445875`  
		Last Modified: Sat, 16 Nov 2024 03:38:11 GMT  
		Size: 5.4 MB (5388059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360040861aabb5ffe5dca9d04c7ebbaefdd5ed0de1ef1132b0735ffe5d7d0495`  
		Last Modified: Sat, 16 Nov 2024 03:38:11 GMT  
		Size: 5.2 MB (5232268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5add1c5009c5f0c37930f3c25db88d0ffdb21d975d3d0f3fa0ef3915befc82ed`  
		Last Modified: Sat, 16 Nov 2024 03:38:12 GMT  
		Size: 61.5 KB (61477 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:ed005412da6bba58efca76a0e908fafef123de31174e96a7a049927c351a88cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103102200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b0b5f25d8216963c72c34430bcea36a1417198251433f2579997f8319111db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 16 Oct 2024 09:26:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:26:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:26:12 GMT
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Wed, 16 Oct 2024 09:26:12 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:35:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_VERSION=4.0.3
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:35:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:35:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471740acc39434c0359d1f610321ef4a5de0576a85b694d0d6ef2ff520e1fa4f`  
		Last Modified: Sat, 16 Nov 2024 03:38:24 GMT  
		Size: 39.2 MB (39154415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1631fcbf19233e5a4744523f15f8b9ae1e6ee81aab252138945ba081f44481`  
		Last Modified: Sat, 16 Nov 2024 03:38:23 GMT  
		Size: 8.7 MB (8689227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58fd8f309accefea26d96b32a50b2cb29d04330a9f79350971ba47c7f884b3d`  
		Last Modified: Sat, 16 Nov 2024 03:38:22 GMT  
		Size: 9.4 KB (9428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a6edef61f671ea8a3cacd3f7e14f2a932a4412bd099a818772b5546ed9d3b8`  
		Last Modified: Sat, 16 Nov 2024 03:38:23 GMT  
		Size: 20.9 MB (20858560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba90ab1c9fb7c25ffa5406ea614e819f28c2cf2316d6b9d9a31dc2908df40b53`  
		Last Modified: Sat, 16 Nov 2024 03:38:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0315f0d449edebc4707ad789c7146768a6ec0c6a17d3bafd3da8f4c7a54b4a02`  
		Last Modified: Sat, 16 Nov 2024 03:38:24 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2173cb7a104d4c469bba32b0c924c9cad5a7c3382812005d6fd370d0d103789`  
		Last Modified: Sat, 16 Nov 2024 03:38:24 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63de8f7bb3b41935cc7dfa9bfe9c2804e3d933c19a77bde5778e683b9c3a0bd4`  
		Last Modified: Sat, 16 Nov 2024 03:38:24 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b5615f385f6aa395e0c2308cf1a2816fd714ce7fbd53afadd6e03cb336da028d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18134606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81bfc4b5d42de2e2b9103a90d104b1dfdaa43d4a94c82bf3ef293cec82aefba2`

```dockerfile
```

-	Layers:
	-	`sha256:702c2f45772e674b5def1c8f7cb049503940ce547128907633814a1ded08ebc1`  
		Last Modified: Sat, 16 Nov 2024 03:38:22 GMT  
		Size: 2.4 MB (2369403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7d8bd50b843588800ce55a74a9adeb2ac05ac62f26c6e80c144f2bc45c41af3`  
		Last Modified: Sat, 16 Nov 2024 03:38:22 GMT  
		Size: 5.2 MB (5181544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b722dddc331c9d09561b7cd9b082c6780a599bcd0a07f75c5475691a1ed878e3`  
		Last Modified: Sat, 16 Nov 2024 03:38:22 GMT  
		Size: 5.3 MB (5339081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96ceb303416e1c7930022dadd1fd012162635101973a38596c4a8e341f8b676f`  
		Last Modified: Sat, 16 Nov 2024 03:38:22 GMT  
		Size: 5.2 MB (5183278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75d46e1fdadcc38a87db6d62e32d92aca8f74002e85dd5228a422b2bdbf76793`  
		Last Modified: Sat, 16 Nov 2024 03:38:23 GMT  
		Size: 61.3 KB (61300 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:1589d294ff8dfb01cb067b347956c87b509622ab9db0976ad1e4b3718caec98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96538027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd2dbc1d5bf0c4db7168ed293484c0f8a1b2d0bd4dbcf5d8a1633168f845841`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 16 Oct 2024 10:27:02 GMT
ARG RELEASE
# Wed, 16 Oct 2024 10:27:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 10:27:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 10:27:03 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 10:27:43 GMT
ADD file:c7a07ab82f7f269608b3c78a3d2b0cd74630ea7220aee252fb2a61f78978b08f in / 
# Wed, 16 Oct 2024 10:27:46 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:35:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_VERSION=4.0.3
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:35:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:35:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:ee732b5fddd0a964c04b11ad9b9ec9f70f7df9e1e96825973cdf803cf1fba8e5`  
		Last Modified: Wed, 16 Oct 2024 12:48:30 GMT  
		Size: 31.0 MB (30980747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369c548358a46b6af606c847a5204550b498df6eda76b5d0a25698f741c5858f`  
		Last Modified: Sat, 16 Nov 2024 07:38:19 GMT  
		Size: 35.0 MB (34951869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53364fcae230c3bb26b81f04780ec444c9de8ce5884bf0245c8d8f660388e9fa`  
		Last Modified: Sat, 16 Nov 2024 07:38:15 GMT  
		Size: 9.8 MB (9783435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70e25c2b6c583f41da8fc074dd9ba6d45e120a401383ea9fc1850cb2a3fd443`  
		Last Modified: Sat, 16 Nov 2024 07:38:12 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51da418b27a3e4638652722866bcec78597f6f250b1ec5d9da55be4f4679fee`  
		Last Modified: Sat, 16 Nov 2024 07:38:17 GMT  
		Size: 20.8 MB (20810765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5690490370a0722350f2129ed0863fac214e6ada4907cd44ae372ef1b0065a2`  
		Last Modified: Sat, 16 Nov 2024 07:38:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d40a510748240173ed8969ed492dc7102fe4a23a1cec3d4a750c4b47412c778`  
		Last Modified: Sat, 16 Nov 2024 07:38:14 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca526e9c2f6885a5323d85796ddc75c9ba67c523f6931969b3f653c4774c3cc`  
		Last Modified: Sat, 16 Nov 2024 07:38:15 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5522a375ae1fa4d6f9f780a21a2d8645a982f78717dcfc52aeaf92af0a76c849`  
		Last Modified: Sat, 16 Nov 2024 07:38:16 GMT  
		Size: 835.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2e522f970541a0cc7e2181466d9094a6d2697c54d657e134271eac27277c44c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18093113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b4c0e2fb1c35ab9336fbd9f793335034189b9b901372e86e7ccd72e00f0a32`

```dockerfile
```

-	Layers:
	-	`sha256:176e1e8214bc861415b929c9300da3287dffeae0aac5a358724698b79f05820e`  
		Last Modified: Sat, 16 Nov 2024 07:38:13 GMT  
		Size: 2.4 MB (2357633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:291e4e462765eda024e2c2b4c9bf7d656fc53dd3c15921dafc4b28829f5636ee`  
		Last Modified: Sat, 16 Nov 2024 07:38:14 GMT  
		Size: 5.2 MB (5172500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7349e6d0e457a06e9bbb34734298b0cb17e65bdcb25f79bc994780f5fda6640`  
		Last Modified: Sat, 16 Nov 2024 07:38:15 GMT  
		Size: 5.3 MB (5327446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:467fdd24f2bf276bb62a52df71b42c0f0645c8da78079b95b4ab647b6cfd69a1`  
		Last Modified: Sat, 16 Nov 2024 07:38:14 GMT  
		Size: 5.2 MB (5174234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:280a945d1fc75b4b1f01a7ada1e3e30fce1711eea2c4de90112f17524b813bae`  
		Last Modified: Sat, 16 Nov 2024 07:38:14 GMT  
		Size: 61.3 KB (61300 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:c59b79892563b52c8f6f80dcdbd6fd2cf3b7c2c0d7b0c3d06f547ef494a8ca0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96723426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b8be29d0406473b77a37f33943fefa36aba9c1fdf5c3d308d4ab2545ec7e3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:33 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:34 GMT
ADD file:1c592b6de2557bde912d6291330e1604327193966f24da30f3ecf513f06fd372 in / 
# Wed, 16 Oct 2024 09:25:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:35:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_VERSION=4.0.3
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:35:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:35:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4d3763c838a1509ac75e9b37aa0fba11067b054033fda0d642f7e32e542b7994`  
		Last Modified: Wed, 16 Oct 2024 12:48:36 GMT  
		Size: 30.0 MB (30021284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f628d644b7e82166f9c4dbbc2ce69ef8ed80265397361516a19826ba953c30`  
		Last Modified: Sat, 16 Nov 2024 03:20:07 GMT  
		Size: 38.3 MB (38263639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6e5378dbd3f9da14f0dd6b76bdfe9f8647b651971acc003da27fbb706a84c6`  
		Last Modified: Sat, 16 Nov 2024 03:20:06 GMT  
		Size: 7.5 MB (7546306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7e850bd6a9f21c2cdfec63f49a51772c9494a699dd7cf1217888aca83fdf91`  
		Last Modified: Sat, 16 Nov 2024 03:20:06 GMT  
		Size: 9.6 KB (9596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8c293e088ba085ee58b7bef5daf548b97441348ee94ebdd6308bbe5f394389`  
		Last Modified: Sat, 16 Nov 2024 03:20:07 GMT  
		Size: 20.9 MB (20880859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c65d57a86428247e8815237a6dd2b77c0ac8d922178a2175805ba139f9a051f`  
		Last Modified: Sat, 16 Nov 2024 03:20:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f691617111e9cb48948c0500e1ce34b4e93d3dc899ecee22ecf9d212a5ba9c`  
		Last Modified: Sat, 16 Nov 2024 03:20:08 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d933bfa1a30358eca507166909b24d22a99d1d3a140556e2776bb3339a1ce59`  
		Last Modified: Sat, 16 Nov 2024 03:20:08 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd825a7a4cdaa7ded6fa6256895e4f1cd284e0f7decef5ce8a6be72ba5f1785`  
		Last Modified: Sat, 16 Nov 2024 03:20:08 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:55416b1c4cfa68e144d2124ed12ad2a7bf5baee5e2d7f3b925dcfe402d3a5704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17764065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a48562db53c418e43e8c722a0639e5ea38bf2f1905a14e93aadd1dab1400cde`

```dockerfile
```

-	Layers:
	-	`sha256:148cc64d9514384f642649e8102d856333c061796267ea209a224e5753bb9799`  
		Last Modified: Sat, 16 Nov 2024 03:20:06 GMT  
		Size: 2.4 MB (2367163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:404bead9f5fb80da778c461f7977d96735e63862cc59b3175293f66d10f20251`  
		Last Modified: Sat, 16 Nov 2024 03:20:07 GMT  
		Size: 5.1 MB (5059243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe8cca34b3e2191067bf49dc098c91ff7903b4099b0228d70f168ceb411d7669`  
		Last Modified: Sat, 16 Nov 2024 03:20:07 GMT  
		Size: 5.2 MB (5215444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ceee9c73d1322ca6dd6a06ced1e95d3640ab865e593b674b8c9018e78886549`  
		Last Modified: Sat, 16 Nov 2024 03:20:06 GMT  
		Size: 5.1 MB (5060977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9eefaf0bf2f26f74bc69ac8b9991ddf32ccfe74906212efa4d22ff3aba9a580`  
		Last Modified: Sat, 16 Nov 2024 03:20:07 GMT  
		Size: 61.2 KB (61238 bytes)  
		MIME: application/vnd.in-toto+json
