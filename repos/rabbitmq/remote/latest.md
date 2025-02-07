## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:82ee1d53d63c646b2fbaacfe4c5fb0e01a447047df585d16836ae236637bb15a
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
$ docker pull rabbitmq@sha256:8196399ba16a67aad44a2eb2cd66d16d72f22bd2d1d55f0e3152df841969cecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107263062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17a8daeb8abbce35039a5aeab6c6d51dbd8edd463a0b45f9b0aced0a83db4f8`
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3184c461034333d3162912fa82f80119b61f31562a1e4dfcb4fd458aef66247f`  
		Last Modified: Fri, 07 Feb 2025 00:37:20 GMT  
		Size: 48.4 MB (48410315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0736e22aa50752aa77ada17c4d316097c8e9f228643c21709d84644ce7888050`  
		Last Modified: Fri, 07 Feb 2025 00:37:19 GMT  
		Size: 8.2 MB (8169273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6043017ac9e6f281cb72b166634b80aff87424e820778497006ae8e237164576`  
		Last Modified: Fri, 07 Feb 2025 00:37:18 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddadda2f4710020eeb3037641201f6cfbcc936b2db37dd9072e64e1f523c1ef`  
		Last Modified: Fri, 07 Feb 2025 00:37:19 GMT  
		Size: 20.9 MB (20917957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fba29582788121ab19ae0098ab2cdb5d992148b7af54a896b7218b14bf7bb27`  
		Last Modified: Fri, 07 Feb 2025 00:37:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7189d2016998eaf635886872a7c7cf5c6c19debbc6304a03265f71670e2fae12`  
		Last Modified: Fri, 07 Feb 2025 00:37:20 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3acd9fa55f31a331a5553e1835fccaecdc6af0c09edd8374a346e5852735c4`  
		Last Modified: Fri, 07 Feb 2025 00:37:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee57700f1f0e7278077f4ebaf4cf98eeaa4b006ad50ad7ca63aa6aa21ff3d88`  
		Last Modified: Fri, 07 Feb 2025 00:37:21 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1a403629963190308be176101f66bee7b3df442bdc2391d8649b6eeb19bb47a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17925631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3ac026cb644a0b58e28a8ffca6ce9f949ec4b8f7f5b3516f1f0f19449af16f`

```dockerfile
```

-	Layers:
	-	`sha256:361add8a1f076926884a5df6b118d77c4988e855dd81ad4034042e926ee181c2`  
		Last Modified: Fri, 07 Feb 2025 00:37:19 GMT  
		Size: 2.2 MB (2248505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:965196f4ae864657735da631264a52232d302ffa645b22233338302ce771eacb`  
		Last Modified: Fri, 07 Feb 2025 00:37:19 GMT  
		Size: 5.2 MB (5202808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3459e495fa8a3d0fa868327ea1bba93e0d60a64e9f8a72e58e4be70028818d9`  
		Last Modified: Fri, 07 Feb 2025 00:37:19 GMT  
		Size: 5.2 MB (5210026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add5b5a34c53d2a4fcfa07fc56b818a96b19607d7197b604fb85faf8e7fd772e`  
		Last Modified: Fri, 07 Feb 2025 00:37:19 GMT  
		Size: 5.2 MB (5204550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d6ebf3dbb72fa20403e9a9524750e945007289f4a1155c455543f83ea14fb8a`  
		Last Modified: Fri, 07 Feb 2025 00:37:20 GMT  
		Size: 59.7 KB (59742 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:77748d43a16cc92a7a5a9a1d81c3d34b69e99631834ebde561813de20e254908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89815804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1393212f56b2336c0c5f5bd1c0e374ad5e829f7b62b5a2ebbec6f8fd1ba0549a`
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
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Mon, 27 Jan 2025 05:10:02 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6daf60e49e177a0a6b6d559a08fbea87e5f2f580d737794ea5b35df9a3d3601`  
		Last Modified: Fri, 07 Feb 2025 03:51:37 GMT  
		Size: 35.4 MB (35440423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4094606c99f3ebee020b13c2766669e19b8834ce9daac18ed691793dcd458cbb`  
		Last Modified: Fri, 07 Feb 2025 03:51:37 GMT  
		Size: 6.7 MB (6668098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2936d128141db2322b2be92f1c31a7348f63ba2f67a0a9e5591d71b0c0f99bbe`  
		Last Modified: Fri, 07 Feb 2025 03:51:36 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4315461189cd46c2da24327805e1077b84e8871de2337bb631c7f3e530b596b6`  
		Last Modified: Fri, 07 Feb 2025 03:57:03 GMT  
		Size: 20.8 MB (20821026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf16568d0a04f35a0f0e180251f4681e379a0b813cc7a9f6d478bc22f83102d`  
		Last Modified: Fri, 07 Feb 2025 03:57:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac6bdd68094e0da0a59be226ea7d0c3b97a0440c469158cd05ed841949307c2`  
		Last Modified: Fri, 07 Feb 2025 03:57:02 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64690047a6281c12e468d3fbb9db3ff938214cbcdbd2610e1b23d4c6ad8ac06e`  
		Last Modified: Fri, 07 Feb 2025 03:57:02 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ab22fe0eb3b49429d2c6b6ffdbaab5add8bc99089d7e13e964aba9bae011ac`  
		Last Modified: Fri, 07 Feb 2025 03:57:03 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f8aaded919cfde9d93ca7a37767e8b84e988e644d3db8bf721830f1d2a709dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17657056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b0c525d7b5921d59c91a21bb04fd8d4fd58335f7cc4b149f5a7f5e669be551`

```dockerfile
```

-	Layers:
	-	`sha256:abfc62db94fe67bfd8efe8949bbffe4a197eef87e9e4713da72f6203df25e83f`  
		Last Modified: Fri, 07 Feb 2025 03:57:02 GMT  
		Size: 2.4 MB (2368859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f06d5124573abb11d5d9b1e3170103dccbc2a2769dabd79de9186eaab2174a6`  
		Last Modified: Fri, 07 Feb 2025 03:57:02 GMT  
		Size: 5.0 MB (5024073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a5da986fb3f346b52ebcc59f126d18a2534fbade55af7013f30f0d135ba2b7e`  
		Last Modified: Fri, 07 Feb 2025 03:57:02 GMT  
		Size: 5.2 MB (5178374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:367f114687a9be5419b2b36ddb4c826aa5aacd28a426ee4b3e209e9b41f487b9`  
		Last Modified: Fri, 07 Feb 2025 03:57:02 GMT  
		Size: 5.0 MB (5025815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d2328f137c70111fd907ef0d2975c2b87862638c58eb41825c330d4fa0bf365`  
		Last Modified: Fri, 07 Feb 2025 03:57:03 GMT  
		Size: 59.9 KB (59935 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:2035087a6e84c144b60af567f2bfad2465e4d47e254e1b2e17449f1889be197e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105159494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b7b0ec91ec675c653b5c673c0d5859fd41b5cc918d35ddf27a870d3523824b`
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabec4e54d75396376496aa43e9a892806cc6e2571f7671ea93b01f5b40ffb23`  
		Last Modified: Fri, 07 Feb 2025 02:53:56 GMT  
		Size: 46.5 MB (46492012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177bca529e19e726fc2de98b50e0b1091d17585e090563b437a31e581269b8a7`  
		Last Modified: Fri, 07 Feb 2025 02:53:54 GMT  
		Size: 8.9 MB (8934918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413c343873e64a512909851d1210de1e50124829f36cb4a5f43fae4196fffa56`  
		Last Modified: Fri, 07 Feb 2025 02:53:53 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c847c0afec247c6d832a0d7a994954f8482f5c34d9e721d0d8d6eff31ed500`  
		Last Modified: Fri, 07 Feb 2025 03:02:06 GMT  
		Size: 20.8 MB (20827769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dbf01d5ba43db7693a36ef4b4162bd212671c1f1ea15d7ac47a1a0dc433d9f`  
		Last Modified: Fri, 07 Feb 2025 03:02:05 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc0e87bf5599b6c9ef53ee48aff120abb3491fd4d2968edc4261a91d6c9e5d9`  
		Last Modified: Fri, 07 Feb 2025 03:02:05 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327ca4109c72ee89abbb73b637667314b2d6d26f359ff653ca2ad89f24e6f879`  
		Last Modified: Fri, 07 Feb 2025 03:02:05 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70750e1e7207dcd6a1439463f909d3ee660fa6088c73dea536f3c74f86da0143`  
		Last Modified: Fri, 07 Feb 2025 03:02:06 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4782f0890a1bc171e363945ba217a5cfff35e0abe5ef31d42a816ebab509e019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18254919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9f1b482c869f9e10e3004893188902369982b63fb140a666582f22143aecb0`

```dockerfile
```

-	Layers:
	-	`sha256:285b0fbdc6506adc88264538b3338a4b2d5bb18943017a7983b9829f30084d36`  
		Last Modified: Fri, 07 Feb 2025 03:02:05 GMT  
		Size: 2.4 MB (2369115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccddec927655afb85b23275c2069414f424e8c0cd80b288ada98de6451ece734`  
		Last Modified: Fri, 07 Feb 2025 03:02:05 GMT  
		Size: 5.2 MB (5222405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6510fdd6994ff3b1e0e484eb7ef768bcb0ad8836d7fd36c084d52e787e15aa31`  
		Last Modified: Fri, 07 Feb 2025 03:02:05 GMT  
		Size: 5.4 MB (5379271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd5efb4219c0f5610602832f733364b61aa0c0ccb0843412d35f39f15514953d`  
		Last Modified: Fri, 07 Feb 2025 03:02:05 GMT  
		Size: 5.2 MB (5224147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2584d3ca77f7489384560cedf8a9cfb5e5c8062455f956774b4a47ce2549bc77`  
		Last Modified: Fri, 07 Feb 2025 03:02:06 GMT  
		Size: 60.0 KB (59981 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:f3339b04b2b5f0badf86967b796ce4b8108e150969e0336b250d3e826fa591dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105607572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f6d4ffcbc61a5f85167d152517215a4f5fff0e4eeaba2bbbeeb5dfcd405420`
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
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee45bbecacce672aaa8c8213e9995873ab948a731acc0dfa9f8deb8052303fb`  
		Last Modified: Fri, 07 Feb 2025 01:55:13 GMT  
		Size: 41.6 MB (41639722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6508f0776d5a22e7f5effd0d6941d6f007a3d3e5344f798d45d7a5a06c2d35`  
		Last Modified: Fri, 07 Feb 2025 01:55:12 GMT  
		Size: 8.7 MB (8689847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f0b649ab9fff0e1f0b5557994e229ff4656fe2ea27928ee4e5a69979fd98cb`  
		Last Modified: Fri, 07 Feb 2025 01:55:11 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1011b0ac667f554cb112244069d6a6d20cfef57c3bbc8fdb3653ecfb48f9fd90`  
		Last Modified: Fri, 07 Feb 2025 02:05:36 GMT  
		Size: 20.9 MB (20877019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218995578acf9a36bd657109d60d010f0bc8d829937edca9465948d1a4f3f095`  
		Last Modified: Fri, 07 Feb 2025 02:05:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd5fe27b80313d07cefd39fee4c2609110e8ec7f0e7fae7f8310dee3a682ae9`  
		Last Modified: Fri, 07 Feb 2025 02:05:36 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d7be8c536d761b9a3ad73f28b21558cde93102f10a5c1f7a9aadb3e489b5d4`  
		Last Modified: Fri, 07 Feb 2025 02:05:36 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328c2f934023175294bfe021040365e3352a6f73305acb49419cdd94bcd06a58`  
		Last Modified: Fri, 07 Feb 2025 02:05:37 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ea6ab1f18623e40098304ca4421030a42077fa72aa40515a2c57427cd570a329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18111391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2bad9989b7df9dee04fbf48199558984e61d6c0f52f5069daf449503418531`

```dockerfile
```

-	Layers:
	-	`sha256:3be8bd819f266ba3cb69602938b04884dee51beed56c47e43fdcbd5faf64d7a3`  
		Last Modified: Fri, 07 Feb 2025 02:05:36 GMT  
		Size: 2.4 MB (2372410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2eb0ebd1e1fa360aea43f97c814d924a4893539e9dad690f8b66a563d244626`  
		Last Modified: Fri, 07 Feb 2025 02:05:36 GMT  
		Size: 5.2 MB (5173519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:799705c3346a9e37d33a30b3f2a932e7cb96ed3726fa002c2391c7eecc1422e8`  
		Last Modified: Fri, 07 Feb 2025 02:05:36 GMT  
		Size: 5.3 MB (5330397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8afa8e24585b3f16f25bfef71802f7a7c7d172511332a2da0253597b302077b`  
		Last Modified: Fri, 07 Feb 2025 02:05:36 GMT  
		Size: 5.2 MB (5175261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ba81091cba6508d814148034b55910f7c8d5435b43b0ac931e211460ad8e3aa`  
		Last Modified: Fri, 07 Feb 2025 02:05:37 GMT  
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
$ docker pull rabbitmq@sha256:aeca77a23469fbe66e819a60bb3ddb52b754e21a7d485f68fe83e4144085ba5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99202984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb2cec5783b4c6547540df35b57ad3d545b918c75db416a3fc27817d671f907`
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
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Mon, 27 Jan 2025 05:10:30 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed283d358608cd98b567b4d1e6b708eb513b1cbec13d1cefbef8e6c7ccfdd4b`  
		Last Modified: Fri, 07 Feb 2025 02:11:32 GMT  
		Size: 40.7 MB (40718669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bcacbbc6e0593cbc745adc4038abe2e57dae2c0ad11ec4510dd77ca067f27c`  
		Last Modified: Fri, 07 Feb 2025 02:11:27 GMT  
		Size: 7.5 MB (7546494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22f0a604f1dd6cf0de18dfb563aed24f3684d6bc0ed834be75e2f98dcc58551`  
		Last Modified: Fri, 07 Feb 2025 02:11:27 GMT  
		Size: 9.6 KB (9586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9c49f061a4659d5e663cb3377de9e6caecdcecddafb804c97c7aceb6ad0aac`  
		Last Modified: Fri, 07 Feb 2025 02:22:34 GMT  
		Size: 20.9 MB (20898931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b18b22148b37659c26f08864020c4c29fc0923921c61ddb9a7696948392bca`  
		Last Modified: Fri, 07 Feb 2025 02:22:34 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadbe32aba1e93d8506bd27ed02bdcb44ee05f1059ad5949a5f6d3be04bf275c`  
		Last Modified: Fri, 07 Feb 2025 02:22:34 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ff4088c9e0de7d319a47561fccf66bff4e82e73decd02f788f3961f69b2712`  
		Last Modified: Fri, 07 Feb 2025 02:22:34 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31022846d433d64f2374b39e5adcf923250f047d33c2e2d6ba56a6452be452e`  
		Last Modified: Fri, 07 Feb 2025 02:22:34 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0b5258256e64ed9b1e06b27c21991325ef6f9fac48f07947044bab918c94d34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17741354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76817ec070972ddb5006ab2c3fc989d7eeb010d04d3a7813d4803e052781ceb6`

```dockerfile
```

-	Layers:
	-	`sha256:91795794fe54760471c0419e6f2dd74ffe7515c0d5f0df18f41e1005f7caf2d7`  
		Last Modified: Fri, 07 Feb 2025 02:22:33 GMT  
		Size: 2.4 MB (2370167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f150aaa963266fb0c38616412b778f27f910008cb0933d4d1029b9fabd78df0`  
		Last Modified: Fri, 07 Feb 2025 02:22:33 GMT  
		Size: 5.1 MB (5051385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb997937ffbbc6d7a70037fccaea22363697d3932070fe243e4d7ef1cc0cff5e`  
		Last Modified: Fri, 07 Feb 2025 02:22:34 GMT  
		Size: 5.2 MB (5206933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46db564896de44abe552e3a2300fc76fbf1e289681d63d08330cf53bc66d0604`  
		Last Modified: Fri, 07 Feb 2025 02:22:33 GMT  
		Size: 5.1 MB (5053127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:402bc967ba6a76995609f9e598e98c139389ed8385ffd2fa22d8cf17f80fced3`  
		Last Modified: Fri, 07 Feb 2025 02:22:34 GMT  
		Size: 59.7 KB (59742 bytes)  
		MIME: application/vnd.in-toto+json
