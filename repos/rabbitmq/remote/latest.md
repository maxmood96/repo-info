## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:e13ecd985720e68aa280601632cfd253df78dd8faf923da434107171c114eeb6
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
$ docker pull rabbitmq@sha256:7ff0811ff6863ab89b3909ac31280d14f71f5e871a3532bc27bdaa1a0a95e3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.7 MB (109706418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcff5d11b2c97496be01bf7c44336920d26e9ec9d3d6197b68b4f971495f970e`
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
# Wed, 26 Feb 2025 19:50:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 26 Feb 2025 19:50:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_VERSION=4.0.7
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 26 Feb 2025 19:50:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 26 Feb 2025 19:50:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 19:50:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 26 Feb 2025 19:50:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6489d6eefa5a44b4a7d542b7ec19fc5724c4ac0619c062d4ac8e4f63daa5fc`  
		Last Modified: Wed, 26 Feb 2025 23:33:12 GMT  
		Size: 48.4 MB (48407946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08ae1cc34ed8b98d24f1d97349c611c87992c2f1b470de7b46da7b256e2b293`  
		Last Modified: Wed, 26 Feb 2025 23:33:11 GMT  
		Size: 8.2 MB (8171066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad34ec79cef0eb131eb4b7919ae70cea5f839b0a3c006a0ce5b0bf82e47ddf4f`  
		Last Modified: Wed, 26 Feb 2025 23:33:11 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e366441f3257b2f94b6b7dda5df25ee8c8ab9f4fefd70457b3f278b0400aa5`  
		Last Modified: Wed, 26 Feb 2025 23:33:12 GMT  
		Size: 23.4 MB (23361870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb93e9eafafaad3af593e85b946acc1147c15e2415fa6b8afede7962e636807`  
		Last Modified: Wed, 26 Feb 2025 23:33:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5aa8ae6066540236dff79935dc72b9cc6ab7163a019aa43cebf092a2d472864`  
		Last Modified: Wed, 26 Feb 2025 23:33:12 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9a3f69c34cbd8b1a3ed88e97cf709f6f124386cca954400b0f210d197e1979`  
		Last Modified: Wed, 26 Feb 2025 23:33:12 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e278e39e4b767d68871194fe3e960cf86a7e2ca74db473ff206e601c001bb5`  
		Last Modified: Wed, 26 Feb 2025 23:33:13 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:39717f57ec522ae4c917a36003b3288c7b863a4290cba072ec242ed7b329f839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17925631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d7f73fdcfe2d4c0d3a871b644728ce1f70587554a21bc07b3d99af524d8a34`

```dockerfile
```

-	Layers:
	-	`sha256:29df76530bdee22b751952b46a10b3c231297d07d934ed8f079f8aa3a518365b`  
		Last Modified: Wed, 26 Feb 2025 23:33:11 GMT  
		Size: 2.2 MB (2248505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c689458b1432f1d148d546e71c44ddf184ab1c0c0c3d2ca86308dd08e173cd7`  
		Last Modified: Wed, 26 Feb 2025 23:33:11 GMT  
		Size: 5.2 MB (5202808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:955db88a64c97d799803e9f65d9cf11ec94ea93781e98610fe342ab64a582922`  
		Last Modified: Wed, 26 Feb 2025 23:33:11 GMT  
		Size: 5.2 MB (5210026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530d3a3e6c97b8b585f334735fde12914209f420296adef0c0616281deae8ee4`  
		Last Modified: Wed, 26 Feb 2025 23:33:11 GMT  
		Size: 5.2 MB (5204550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69c31925cc0ac0e9febb55f02fdf3bb12e689df548d63faf100185705dd145cf`  
		Last Modified: Wed, 26 Feb 2025 23:33:12 GMT  
		Size: 59.7 KB (59742 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:83d72e4082bc67c75a2a0e2295405c6481de0d8b515bd1923feaddb2d6d4bdba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89848223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e258902f5959df252dfc37dd03f20a793e7e54de19d26714b039824dca6b512`
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
# Tue, 11 Feb 2025 18:31:38 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 11 Feb 2025 18:31:38 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_VERSION=4.0.6
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Feb 2025 18:31:38 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Mon, 27 Jan 2025 05:10:02 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8abda987357d129b30e39c0898a569ebd84bf1eee386623a7b14e4bc183bada`  
		Last Modified: Wed, 12 Feb 2025 17:52:11 GMT  
		Size: 35.4 MB (35440459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3549d8b54b46c7b0709c88471248fe538023def6a7b64f7b5bd737435f093f8b`  
		Last Modified: Wed, 12 Feb 2025 17:52:10 GMT  
		Size: 6.7 MB (6670889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb4fa1bd7d5d9905ba4d606f347fc99ef3d7cffc10b2cf7db6b085601e3f9c`  
		Last Modified: Wed, 12 Feb 2025 17:52:09 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363f0692a022fcbd942ed9d981ede9af1b94cc44c269f52acae099191d619871`  
		Last Modified: Wed, 12 Feb 2025 18:06:41 GMT  
		Size: 20.9 MB (20850623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5523246aa249e03f72fb68384f54cc103dfd84c69be268dd398d5d6ca31c0d`  
		Last Modified: Wed, 12 Feb 2025 18:06:41 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09eb88032801049df4df8de2b24829fd7d452a9e877e6d12a6737a0139b58707`  
		Last Modified: Wed, 12 Feb 2025 18:06:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f632f38bb69de1a55d3b5b1b4798cf55a1ca3c8bde8a0b2f4d80a6e98be647`  
		Last Modified: Wed, 12 Feb 2025 18:06:41 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af32fa00d0f5701efc4fc27b32bc24769dce6eba53301286dd59e11007fa97`  
		Last Modified: Wed, 12 Feb 2025 18:06:47 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1d2144803921518fad805ef4fb9865b67d71cd244f3ba915eaae799230375af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17657056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38fddb4b1ffb57f7000e850304d818f43cdeaf5661727040340598ce58f919e4`

```dockerfile
```

-	Layers:
	-	`sha256:6f502c5e9ad3158ebd8c8fefa67628043cbcddcad736889c8e8f4a2a5f1b9060`  
		Last Modified: Wed, 12 Feb 2025 18:06:45 GMT  
		Size: 2.4 MB (2368859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9659123aff184b51d2377c83bb5aadb288023b815c371f314d4ef72afc78df17`  
		Last Modified: Wed, 12 Feb 2025 18:06:41 GMT  
		Size: 5.0 MB (5024073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d6105e0e660036f71533ae39ff74b5132b606e600c479d70edf50f50390e1ff`  
		Last Modified: Wed, 12 Feb 2025 18:06:41 GMT  
		Size: 5.2 MB (5178374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe4870ff63f7516249272ec66438e71dcbb710ec48c66fa9473301d4c5258a7`  
		Last Modified: Wed, 12 Feb 2025 18:06:41 GMT  
		Size: 5.0 MB (5025815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ddb3d1edbd1748df75214717e3c09ee15b21493dffd8cf6ed0db65883c6e9e1`  
		Last Modified: Wed, 12 Feb 2025 18:06:42 GMT  
		Size: 59.9 KB (59935 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:073439301d2566768f65f865de47f93110d36a31ca6247e72c71c2486124fb7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107419008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8be097293e43632a25a5d02ec3fe474808907908f8af2cefbdf55f251bbdfa1`
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
# Wed, 26 Feb 2025 19:50:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 26 Feb 2025 19:50:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_VERSION=4.0.7
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 26 Feb 2025 19:50:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 26 Feb 2025 19:50:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 19:50:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 26 Feb 2025 19:50:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57423fa1faf110179a09d3d88c4eb8d484414a0c9419872f5927e0e6b40903b7`  
		Last Modified: Thu, 27 Feb 2025 00:38:03 GMT  
		Size: 46.5 MB (46488373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cf5a33dc3a85cd095f224575195e689ac03e033a6321c14f54a9d916d043c8`  
		Last Modified: Thu, 27 Feb 2025 00:38:02 GMT  
		Size: 8.9 MB (8943201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb65e451698145077814fdc791c016e559d81d3ba9b07175ed25a576dd7223be`  
		Last Modified: Thu, 27 Feb 2025 00:38:02 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bef74b7d71fede61c97b16464402ea3c306e5bea2f90065eb8fd0b033c2dfa`  
		Last Modified: Thu, 27 Feb 2025 00:43:16 GMT  
		Size: 23.1 MB (23082641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38056b31ec92a2f81402a683c1084c707ee998d4bc3a433183c36dadb146cb5f`  
		Last Modified: Thu, 27 Feb 2025 00:43:14 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc95eaa6ed909fe93ac4128cf6f7de7051cc0d900231dc412f989617d50a585`  
		Last Modified: Thu, 27 Feb 2025 00:43:14 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d6752ad9e17456710b509987d886506453e1bc7236faf37dfdbaf7d724dab6`  
		Last Modified: Thu, 27 Feb 2025 00:43:14 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb25aa457e92cbb655ee4eb6672d765de44403b530b550f6b221f80c2a31249e`  
		Last Modified: Thu, 27 Feb 2025 00:43:15 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:48c15e9e0ca5172c373c059d66d7d53b0a37e11fb1a1a997b43559bbb08e4a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18254931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd85499ca25048e47e5ec5e65d08f4c760b79e2cc95162df3e4550a2a65b6aa4`

```dockerfile
```

-	Layers:
	-	`sha256:c70772ec8f0d0fd7dd93968c53404c6340f9cfd215a6f6d870dd0919a57d8810`  
		Last Modified: Thu, 27 Feb 2025 00:43:15 GMT  
		Size: 2.4 MB (2369121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1877180ee4687d65808f68316d74560a84f0617d011042bace6b3aa8162db4e0`  
		Last Modified: Thu, 27 Feb 2025 00:43:15 GMT  
		Size: 5.2 MB (5222405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6216e5fedd3a637cf2707290bfeb205fb1723590769db1c87bb51815d08df50e`  
		Last Modified: Thu, 27 Feb 2025 00:43:15 GMT  
		Size: 5.4 MB (5379277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5005de68497a2d50a843f781eb908961fcc723a94365d40ac130c8228097ea2`  
		Last Modified: Thu, 27 Feb 2025 00:43:15 GMT  
		Size: 5.2 MB (5224147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fd26bb1222eea81c4f42e8569ea422e21a3da34e0b05ceee9cc3260c3a44ccc`  
		Last Modified: Thu, 27 Feb 2025 00:43:16 GMT  
		Size: 60.0 KB (59981 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:6ddc3652c2ec046b14078e227345d945d1395c478c839c8588fa29cd28d7ae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105648098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1029f0a706021a6db3524a672bf74e1843e9f93bbe2fed97dcc2d417358197b5`
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
# Tue, 11 Feb 2025 18:31:38 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 11 Feb 2025 18:31:38 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_VERSION=4.0.6
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Feb 2025 18:31:38 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50259503bc9dc6ddab694e8f9079ff7087d59bea280f556fcb5a578860281177`  
		Last Modified: Wed, 12 Feb 2025 17:51:25 GMT  
		Size: 41.6 MB (41640192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0d4759631349826255d1e56263cb23c7c32e59819592d98451f06c4e826733`  
		Last Modified: Wed, 12 Feb 2025 17:51:24 GMT  
		Size: 8.7 MB (8699441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dae9c33fbee5b9934ca7d98ccd8c574e0dd33a4e0d5869d062ca9872b819075`  
		Last Modified: Wed, 12 Feb 2025 17:51:23 GMT  
		Size: 9.4 KB (9409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00942afab5c9870075aca20e0e7249818167106d9a9096f7d8fcf7ccb46fd68c`  
		Last Modified: Wed, 12 Feb 2025 18:01:43 GMT  
		Size: 20.9 MB (20907481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c99de4dc06ae6d333742bf4576b8d1da8fc90715bc0f28c0b64c4a30f9c6a5`  
		Last Modified: Wed, 12 Feb 2025 18:01:42 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdaa239871cadd2b8dd0ea7a171fb8205a97b8f1b3337ef2e7521bf9f87e378`  
		Last Modified: Wed, 12 Feb 2025 18:01:42 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0799c01397692289d2f5128abd1e279264a5d08c763a1ab6403516b9905c9356`  
		Last Modified: Wed, 12 Feb 2025 18:01:42 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1002caad78009bfcf8be6369fe1c1d6f20e9c540b69955c05313c7e7f94ef6db`  
		Last Modified: Wed, 12 Feb 2025 18:01:43 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0a2ef3e3290a898c8629d2fa76edcf4fc2f345a3d580d371b9ce75d3f0748431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18111391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8547d2ce34cbf4aaa9f11f388fb7bf574c9b781292debceda1bbc1a58f3b9f9`

```dockerfile
```

-	Layers:
	-	`sha256:eb5a16799e7e8bb14844f4d3addbe65336b8012507621e56416baeadb360a38f`  
		Last Modified: Wed, 12 Feb 2025 18:01:42 GMT  
		Size: 2.4 MB (2372410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e7c9f82a811569742668675b6212e7bde001f269b283f4c30ee3108704855eb`  
		Last Modified: Wed, 12 Feb 2025 18:01:42 GMT  
		Size: 5.2 MB (5173519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dae170be1bcaf0d101b85d0c54988fca54d4b64174fdcae493e8c3139222d65`  
		Last Modified: Wed, 12 Feb 2025 18:01:42 GMT  
		Size: 5.3 MB (5330397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b25ebe1b21a1c0f9540ac5a19474953356d200ecd933fbc73e1ed4da07d6d8`  
		Last Modified: Wed, 12 Feb 2025 18:01:42 GMT  
		Size: 5.2 MB (5175261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:280df0758d7293a6d11850bdb013a9719b98f9fa09301816b45b8342d98b0f86`  
		Last Modified: Wed, 12 Feb 2025 18:01:43 GMT  
		Size: 59.8 KB (59804 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:69c12109be39c50fa15d001e61e997d0a851653af2bd3b8e4a2a3f718bc048ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98944953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7d2d0941042570d99f2680dff5a17eaa070eebc061f5f6bd2fd41ffd914a4d`
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
# Tue, 11 Feb 2025 18:31:38 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 11 Feb 2025 18:31:38 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_VERSION=4.0.6
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Feb 2025 18:31:38 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Mon, 27 Jan 2025 05:10:15 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbda3d988f5f88598146968ee3818c7432204a343598556d7c8b67c0aef74a24`  
		Last Modified: Wed, 12 Feb 2025 19:19:15 GMT  
		Size: 37.3 MB (37300925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d84a28cb83f04b9828aa3d3cca26c27e3e38f2cef814aad184165b9233ba6f`  
		Last Modified: Wed, 12 Feb 2025 19:19:10 GMT  
		Size: 9.8 MB (9789671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42ebce46aa7d46baf3c8ea41292f918c17906eb00e448cd382111ddc86aafa0`  
		Last Modified: Wed, 12 Feb 2025 19:19:08 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4f088d84efedf9b862ef713c516208bf688e95c9364d3661b280c33c8aabb7`  
		Last Modified: Wed, 12 Feb 2025 20:53:14 GMT  
		Size: 20.9 MB (20859202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e573da3ba81334517595d5c51f3086ff10581b999934e52b9f661ffd84188ad`  
		Last Modified: Wed, 12 Feb 2025 20:53:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5015ac6ff8e8c3a78e93ef48af7d360b834d44215fa07a471a66edcd1d598fe`  
		Last Modified: Wed, 12 Feb 2025 20:53:11 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9f59e2277d7badb4e7ceb0a3064a7502f930ead11f9db2b5e1c1112cc0807f`  
		Last Modified: Wed, 12 Feb 2025 20:53:11 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f2dc98419dcb95d69a2ef085e8a4f5efa34d4d7cdd76db87753fe1a78b36a4`  
		Last Modified: Wed, 12 Feb 2025 20:53:12 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1ebce22402b26b00b9559c71bf02cf11f2040127cd3938811b40f17590f130e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18099725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5c62d5d734f19277353e6ab61ae7b29d04a2ce25d591e355646822d29a826b`

```dockerfile
```

-	Layers:
	-	`sha256:61cbb151bb47c0efb62c70d5cc760f538bf508d3cdbb994fb6e77c02576ab42d`  
		Last Modified: Wed, 12 Feb 2025 20:53:11 GMT  
		Size: 2.4 MB (2360620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e86fcfcd5d717ea7e5cdc9805eba45c04e83b7482f2cc599f53d34210929df8`  
		Last Modified: Wed, 12 Feb 2025 20:53:12 GMT  
		Size: 5.2 MB (5174420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e0bce097752654cd2bdc334b5edffa7abb3637b027300ee0777a15a05ac394f`  
		Last Modified: Wed, 12 Feb 2025 20:53:12 GMT  
		Size: 5.3 MB (5328719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acbf8ce6fb0802f0419f74410d81739df3de6f1bb1b6229e9ea573e7273e642`  
		Last Modified: Wed, 12 Feb 2025 20:53:12 GMT  
		Size: 5.2 MB (5176162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a1daa97a74e742383f800cef65c6bf91a9984c48ce9455a48444400456a607d`  
		Last Modified: Wed, 12 Feb 2025 20:53:12 GMT  
		Size: 59.8 KB (59804 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:c2df972a8deb815523276595c307804fcb15a3a12a50edd9f938ed3dec18f807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99238838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab5273b7fefe805297d13bb1e174af58f4df4ff9e5f454b4304f8c0dc362bd7`
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
# Tue, 11 Feb 2025 18:31:38 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 11 Feb 2025 18:31:38 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_VERSION=4.0.6
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Feb 2025 18:31:38 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Mon, 27 Jan 2025 05:10:30 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5a8756752fdd12c8717944770b75ef88976bfeb5260dda0d551b1a03b96e5f`  
		Last Modified: Wed, 12 Feb 2025 18:46:44 GMT  
		Size: 40.7 MB (40718834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2056b56335f7ee927e0bbb780c224b510a4bc45b9c40fc1d287df51c98141494`  
		Last Modified: Wed, 12 Feb 2025 18:46:43 GMT  
		Size: 7.6 MB (7551996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a7e3889abaf5307e408cece05cc800aebab52ad9d4258527cecb8e4ff8ea22`  
		Last Modified: Wed, 12 Feb 2025 18:46:43 GMT  
		Size: 9.6 KB (9580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a16a22776f4be4570a31f975009ca4dd483b9041ac9bfb4ba54ba0d995ba995`  
		Last Modified: Wed, 12 Feb 2025 18:46:45 GMT  
		Size: 20.9 MB (20929109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e448675784acaabf97a5de4a00ae7afb4ea81352390a6d3f7da054551fdda44`  
		Last Modified: Wed, 12 Feb 2025 18:46:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6744a1d6ad5fd3bcb96f72666cad67392b0ab6fb22443a90fc3586c92a400a`  
		Last Modified: Wed, 12 Feb 2025 18:46:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438d076d1364f1dd9be99e6922a30dbc2d4fdc47f743607b95ddecd75de87f87`  
		Last Modified: Wed, 12 Feb 2025 18:46:44 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc507c71119589e499f8fb45f7903097d81fa0fa552e33a7454796c3d157afdb`  
		Last Modified: Wed, 12 Feb 2025 18:46:45 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2de26a8d7a34cbd2eae5f8b1da0ef49ba9d78c5b44b66c5632b72857ee13fd13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17741354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91dd956b54560461ea0f63030d6ea7c0a2f565c754adda73807381d77a417ad`

```dockerfile
```

-	Layers:
	-	`sha256:76b79c5ee4a8a3f5f9f7683bc83757ab3fff85ba9f62e0d1184c6d2b3940e4a9`  
		Last Modified: Wed, 12 Feb 2025 18:46:43 GMT  
		Size: 2.4 MB (2370167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2de928f1477d40ff7728e4f4da957662f17931d9d75c40ffe9aae4115b9671d8`  
		Last Modified: Wed, 12 Feb 2025 18:46:43 GMT  
		Size: 5.1 MB (5051385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09c054bd0436ba85bc01146f005966560586f7a854a0083613987a82565e6021`  
		Last Modified: Wed, 12 Feb 2025 18:46:44 GMT  
		Size: 5.2 MB (5206933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2427a0cb483e58f43295fb820b1e2b46502060903b819e8fcad25325b17f52ce`  
		Last Modified: Wed, 12 Feb 2025 18:46:43 GMT  
		Size: 5.1 MB (5053127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8363387ec54f8a279df7b8cb7c1edbbf5678b6019c628c9ddae77571bd2fc5ff`  
		Last Modified: Wed, 12 Feb 2025 18:46:44 GMT  
		Size: 59.7 KB (59742 bytes)  
		MIME: application/vnd.in-toto+json
