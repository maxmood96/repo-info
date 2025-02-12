## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:065b468a200263bbf8eddf44cc32bbb5f9cf76e340d6196dc65cd11e4bb77c61
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
$ docker pull rabbitmq@sha256:b1640cc1b5b68e14145252b4154708ca369b3be7eb6e8dda1db61ea14e735b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107294832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea1d003602badddf52204e46fdf87008762e5de0c0d68ddd2fd59d904243811`
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd39c0d937599af7cd538304cc183af9a594d2ecbc5d8c74334397e17e34cbf3`  
		Last Modified: Wed, 12 Feb 2025 17:36:16 GMT  
		Size: 48.4 MB (48410258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbff533017be93de4d0c87a7f0b69598d84b06f2bae69bef550ae1d38eeee978`  
		Last Modified: Wed, 12 Feb 2025 17:36:16 GMT  
		Size: 8.2 MB (8171065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548d91de6f996febf165d1c8c4b2509edfc5aa9e03ebf81da480c4d89f1f9755`  
		Last Modified: Wed, 12 Feb 2025 17:36:16 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e66834e49724de0d22a6b9e4dfb465b5f2af4cc76ed8c4dc43e220d82badc7d`  
		Last Modified: Wed, 12 Feb 2025 17:36:16 GMT  
		Size: 20.9 MB (20948008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8358dec30aab39e22c2ed43ab4d6a69b896881a0d6e48a03721b1a4476ca52ba`  
		Last Modified: Wed, 12 Feb 2025 17:36:16 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680633ae1d4eca5787aa18c9be0302126183e25ee0f5425866d741d5e957c7d6`  
		Last Modified: Wed, 12 Feb 2025 17:36:17 GMT  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63542e0dcf41f72469ea0ce6687ce27d9009ec2945b6c9afd1aff2103716ff96`  
		Last Modified: Wed, 12 Feb 2025 17:36:17 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd30aebf0283c3ed2a169965b9e033a98770095db51de90541cd23a24babc28f`  
		Last Modified: Wed, 12 Feb 2025 17:36:17 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a1afad957a7d2e4e07e79ea87e0b10867b0724c3e3d6c79993ae2c30a12906ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17925631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760f9fa580c44b3ef506fcf0d3f62a014bfb67c00661b988c247ecc0a084e4de`

```dockerfile
```

-	Layers:
	-	`sha256:7384fa41e6096ace6b91151b3763072a8f3287282c385ae00eed69d0ed5f0535`  
		Last Modified: Wed, 12 Feb 2025 17:36:16 GMT  
		Size: 2.2 MB (2248505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f902747b4a257e5638ca92cb5e90582741bf7b254e0662b7d2f57f70347350c`  
		Last Modified: Wed, 12 Feb 2025 17:36:16 GMT  
		Size: 5.2 MB (5202808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e04b68820d019781f822175cffd4a1136a24c9f26eb9270093925f540008cbc4`  
		Last Modified: Wed, 12 Feb 2025 17:36:16 GMT  
		Size: 5.2 MB (5210026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63bfefad591f226dc1806b65fea57c78c4fb10f336ff35ce7c8bfcf1cc416dfd`  
		Last Modified: Wed, 12 Feb 2025 17:36:16 GMT  
		Size: 5.2 MB (5204550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88471b27c24d25ee17c4a6a3ae9c51a2d87b60acecf17684491263086f30b29c`  
		Last Modified: Wed, 12 Feb 2025 17:36:17 GMT  
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
$ docker pull rabbitmq@sha256:8e6f4025bd30c0644afe4d45ff382ca9390da43deb42878187d243625c271cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105197849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4aa7ecc250c50b358f51be6a49d84b25588024fd9de8f2d3342952440bcf7c4`
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8468a8226468d02e6c3e9c0c0b059b7a273735fc37ae01dc37f77edc7c889d42`  
		Last Modified: Wed, 12 Feb 2025 17:49:15 GMT  
		Size: 46.5 MB (46492037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ba871020b9ef3648c0bb8c03454e1f149c45cbf93f199f90a95051e18a3efa`  
		Last Modified: Wed, 12 Feb 2025 17:49:13 GMT  
		Size: 8.9 MB (8943294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb0dbc0fe317586ef43c16173dcd6f7948bbbc08a75f082b9211c2907efe1c2`  
		Last Modified: Wed, 12 Feb 2025 17:49:13 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb29a35a6d1a9da8248e8c12c98421019bbae76416bdfd05c105e443d5a14cd1`  
		Last Modified: Wed, 12 Feb 2025 17:57:17 GMT  
		Size: 20.9 MB (20857723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31c0f62e01f486a64d3a1ee93d22e41a1d1e1ba7b5c0af1d8f17138d365c137`  
		Last Modified: Wed, 12 Feb 2025 17:57:16 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd4ad1116a7e05abda769d3460a7453b061c1cbeaf413792ac27659f9e7a819`  
		Last Modified: Wed, 12 Feb 2025 17:57:17 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bd91c959429fd21ab627847e70661f3418f4993b7a61a0f53d78defd91b817`  
		Last Modified: Wed, 12 Feb 2025 17:57:17 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9edaa14bd5671c1dfa89007c23826ca002dc568e082b9f9de59fcd81b95a06`  
		Last Modified: Wed, 12 Feb 2025 17:57:17 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:12e69f35868b4b3cdbf478265e6779bd04a1f92a3fa3ade7c149d68373e38038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18254919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318601d27a5549849e852365e012c0a94ee4fb8bf9b4e1b4980883fc0357f3db`

```dockerfile
```

-	Layers:
	-	`sha256:2a7ad2216c57110ff961e2316a4c3172b1bbcfef2b7880d3255581619e5f47f3`  
		Last Modified: Wed, 12 Feb 2025 17:57:17 GMT  
		Size: 2.4 MB (2369115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a8ac72d8f3cf9e392fd171db633df994c9ee3ea5f2b4215df6a88cb361becdd`  
		Last Modified: Wed, 12 Feb 2025 17:57:17 GMT  
		Size: 5.2 MB (5222405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a9581a4a2822fdf4e007e18b145fb1f4b489a866fefe7eaa566ad4e4c3b0ef0`  
		Last Modified: Wed, 12 Feb 2025 17:57:17 GMT  
		Size: 5.4 MB (5379271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1a61ebb1553ccdff2b9ab6c7356d9906ddf3481c3543bf4a16820151aebbfbe`  
		Last Modified: Wed, 12 Feb 2025 17:57:17 GMT  
		Size: 5.2 MB (5224147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:593948c013b4ad0e042af96760ecbab41ee3844c1af8bc81fdb9e9b3fabf458a`  
		Last Modified: Wed, 12 Feb 2025 17:57:18 GMT  
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
$ docker pull rabbitmq@sha256:e1589966d7bf43d4475c250e42c5c69033e2295eb14bbe7d67d914809a21ecc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98910445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773e1d2921aec5dba7d943eb5971f5c0157db704b9c9adad1461f220eb034fe7`
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
# Thu, 06 Feb 2025 18:05:23 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 06 Feb 2025 18:05:23 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_VERSION=4.0.5
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 06 Feb 2025 18:05:23 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 06 Feb 2025 18:05:23 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Mon, 27 Jan 2025 05:10:15 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a81086f461c0ba53c83724a5559734d9c283fb91d4a8487192df0095eab7a40`  
		Last Modified: Fri, 07 Feb 2025 02:18:53 GMT  
		Size: 37.3 MB (37301047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfb697dad0874c4698d0d6f2331ceea6a94c70099246d22ccba38f3d4f6e434`  
		Last Modified: Fri, 07 Feb 2025 02:18:49 GMT  
		Size: 9.8 MB (9785134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385854104b2588ac1129436c059a35623ad1ee442df8a4a4e6489bf6a5ca0f05`  
		Last Modified: Fri, 07 Feb 2025 02:18:47 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cc6b4355df3cebfa7e74b048888e2154172ab41ef9cc6344280b7438fe370b`  
		Last Modified: Fri, 07 Feb 2025 03:54:26 GMT  
		Size: 20.8 MB (20829110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a08c5164545b6c42ccbe19d649f42ed8d71444debfd48762b8074df8f491c7`  
		Last Modified: Fri, 07 Feb 2025 03:54:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901adc1339ff753f205e14206d5aa79212ec4baed4ae525448896aec998c638c`  
		Last Modified: Fri, 07 Feb 2025 03:54:23 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4e15f274429f3b7782aaea626b80f65a51a4808c777b014caed7d0ce66ce12`  
		Last Modified: Fri, 07 Feb 2025 03:54:23 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a858e48e1a0bf5a7945a339b644cecdad2e44cbda51eda515917d77c81f906d`  
		Last Modified: Fri, 07 Feb 2025 03:54:24 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d7adb24c5a8f5d972f331898e3e7b5500d25c1abddb7da458817700c72fb7962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18099725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9238aabdfad4846e6c87ad4566b534e75dbd556170c41cc86aac2c7a0dcc19`

```dockerfile
```

-	Layers:
	-	`sha256:86eed8cafcaa74b708d354f3502143ad47eb2f6f3dce7900acb772a0f39ee303`  
		Last Modified: Fri, 07 Feb 2025 03:54:23 GMT  
		Size: 2.4 MB (2360620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03868fc58625890cc55720acb6c79ec0403ec15165a4096b30304d0f296e1672`  
		Last Modified: Fri, 07 Feb 2025 03:54:23 GMT  
		Size: 5.2 MB (5174420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af00e76c163f7201d5c3ef543210f74487ad5d587eaaba37560e7c908d08cc35`  
		Last Modified: Fri, 07 Feb 2025 03:54:23 GMT  
		Size: 5.3 MB (5328719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b6e692b040e0c7debbf47bf54eeb38340c274013d1c1d3ed33a8bd9c784bf4`  
		Last Modified: Fri, 07 Feb 2025 03:54:23 GMT  
		Size: 5.2 MB (5176162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ea0c08bf8bb6ad59a33e43122b8b122fe34da0a2aacf81cee384a4f472b4eb5`  
		Last Modified: Fri, 07 Feb 2025 03:54:24 GMT  
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
