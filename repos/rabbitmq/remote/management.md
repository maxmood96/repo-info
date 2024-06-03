## `rabbitmq:management`

```console
$ docker pull rabbitmq@sha256:f8540c07a5b814452275446a8a03bafe68d65d6bce1ef4de6f75dd7e09912d46
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

### `rabbitmq:management` - linux; amd64

```console
$ docker pull rabbitmq@sha256:ee1ddc8c2dd06e300e2a94638fa01c084c5cd8cc8d40023a21bd6feb24ca7110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114944820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d267434c554e93b12c28f8567c829652ed7d20707b3ecfb0119a87e99c6edaea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ARG RELEASE
# Thu, 22 Feb 2024 21:58:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.3
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c4850ab6d13165b74f67eb5850acdef906d296ebfb5e9f01b82957412d3f62`  
		Last Modified: Mon, 03 Jun 2024 19:09:49 GMT  
		Size: 46.0 MB (46005305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5274b8dc1c13e3b7fa77f328008122f49096491174862d52aa7362381f62cb8d`  
		Last Modified: Mon, 03 Jun 2024 19:09:47 GMT  
		Size: 7.5 MB (7473450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be19983d7e0a9f1fc8a116977a2a7336e5f0287a1fc0ca95e1a81d5c106e5f`  
		Last Modified: Mon, 03 Jun 2024 19:09:47 GMT  
		Size: 10.7 KB (10741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c834c020bbaf8de42c230690bd270682be02cce8ab1ef9367cb0ab5e62612e42`  
		Last Modified: Mon, 03 Jun 2024 19:09:48 GMT  
		Size: 21.6 MB (21588847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7efec600429ef1a4ed112fa5a9d5080c2864859e36c5ef0a1b28ad0fe9cae4`  
		Last Modified: Mon, 03 Jun 2024 19:09:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a6f5e84439ec03b6894994563bd79557e1b5837ea32fde23a1acf786aed33b`  
		Last Modified: Mon, 03 Jun 2024 19:09:49 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a558d56b6e9c83821c6f086b1812527b10aaa29da478db7391f0cb35a4816f39`  
		Last Modified: Mon, 03 Jun 2024 19:09:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ea4625a409ef931237b2633e74e3f26ae2fc427350931a2332fa8e59d3a2ce`  
		Last Modified: Mon, 03 Jun 2024 19:09:49 GMT  
		Size: 837.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ae99c07ee0bf605451d26e61a06cce18c2094572e95a5a573fc84b91b51991`  
		Last Modified: Mon, 03 Jun 2024 19:55:25 GMT  
		Size: 10.3 MB (10330773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:92ab7730e8b073b5aa7963a68184a4d2d8bc24e99889db02534b757a0033346c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3438090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498f84868c63f1584a4603f2ef2829853d197b97f613a3d1ee7e7b7a5f108560`

```dockerfile
```

-	Layers:
	-	`sha256:3a38ab79c98582b37015764b7f4a72b33001d21ca756687955b0323dcdfc1f09`  
		Last Modified: Mon, 03 Jun 2024 19:55:25 GMT  
		Size: 3.4 MB (3426763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:230659de5edaeac98e39d8e015aaf38719a9adf3fb1702f7bfe887b22ff76cd6`  
		Last Modified: Mon, 03 Jun 2024 19:55:25 GMT  
		Size: 11.3 KB (11327 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:2341d321ca7042bd80e7f1d24495f56e2f4964a6e6abf8cc93878ff04a4dac95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97179810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519abaeb16bf1410130552fc2db49a46d6d3eb0e80d3641188e25cd97dd9bed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ARG RELEASE
# Thu, 22 Feb 2024 21:58:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:ab2e95a123b006ac900aaaf0d1858b88941c8d319f47e41733db6f0f5fe98b87 in / 
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.2
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f5b4213824fc3515b68e6844d3fc289ae00ef8cd07ddcd43856c3ad7faea16d4`  
		Last Modified: Sat, 27 Apr 2024 14:45:43 GMT  
		Size: 26.6 MB (26639789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd36fe06231fa8df4766c2dbc4f75d8354057241ec907ac3436c382e786b22b`  
		Last Modified: Mon, 06 May 2024 17:13:23 GMT  
		Size: 33.5 MB (33495088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe39098462fad2c93e3ff0cea9a498af9261c434caaf5a08168527299b6d409`  
		Last Modified: Mon, 06 May 2024 17:13:23 GMT  
		Size: 6.1 MB (6072556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd16f78a5b9aa96870c7df49ba673712b293a389de08784d0b5339e9261c394`  
		Last Modified: Mon, 06 May 2024 17:13:22 GMT  
		Size: 10.7 KB (10712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f4a9ac0209f034871cf5b6277b86ad1cd3337685536f44b7a18ec537ef962f`  
		Last Modified: Mon, 06 May 2024 17:13:24 GMT  
		Size: 21.5 MB (21488779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf6d1b81adf745f11adf6279d14ecae3158b691831b42f77fd5793bab7d3342`  
		Last Modified: Mon, 06 May 2024 17:13:24 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b595753d328dad00b9fb04e329f8524efcbfbb055bf5d85d8445e49f275dfd`  
		Last Modified: Mon, 06 May 2024 17:13:24 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82aa601f6ebb1c47b1ad235828f9bbd87261b84bcd3175b0b368fb429816cc7`  
		Last Modified: Mon, 06 May 2024 17:13:25 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda5fac3c43517fa538af1ca5fe4329a9e0b249458e81e0ee43ed79e4e2bbdd3`  
		Last Modified: Mon, 06 May 2024 17:13:25 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf495bda965e1826878c127753b62f7474cf0a91d1407cd8c6c1d1223870a0`  
		Last Modified: Mon, 06 May 2024 19:14:21 GMT  
		Size: 9.5 MB (9471140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:67806f0ec88b4f34c2b75c22c90aa4d24dffadfa1f1dac380f91be87be465d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3440407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7348aeb4118c09b2eacbee1b7c04b112bd4f27ed933315ea191ee5acddb0ca96`

```dockerfile
```

-	Layers:
	-	`sha256:68003f2d10cf3fda32c166c7955faa17668b34a36131b7d9a9cc37e22870ba5a`  
		Last Modified: Mon, 06 May 2024 19:14:21 GMT  
		Size: 3.4 MB (3427597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f12ff5a9f7ceecaac02e9ade2d323da0cb79fb0b14539b0ac08612a8aba2b9`  
		Last Modified: Mon, 06 May 2024 19:14:20 GMT  
		Size: 12.8 KB (12810 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:e64a7a840460029cb035607721e0b8116c2843ea2cc7691c4b43c4f7f602aabd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110418775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f111b9a7adc3c9887b1e84c602f39147da0b89a0cf9beb3cc7b1f314295219f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ARG RELEASE
# Thu, 22 Feb 2024 21:58:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.2
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c70932c8e18ce97a296fdb4adb4bcd4fea1c16b52eaffa0612accc0b7170c1`  
		Last Modified: Mon, 06 May 2024 16:51:14 GMT  
		Size: 44.1 MB (44084563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf04a80c4e371b899d5aded5755e4e2d190cc9a1465e9d74c035a334541310c4`  
		Last Modified: Mon, 06 May 2024 16:51:13 GMT  
		Size: 7.1 MB (7130256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8ed72b27a5e7c80213419680f2f514d47198d3baf75a00716aab82936ceaa3`  
		Last Modified: Mon, 06 May 2024 16:51:13 GMT  
		Size: 10.7 KB (10709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a581020418176b676d55a336d4e88afb3e21916dba78ed9d5e4ee0d59775b750`  
		Last Modified: Mon, 06 May 2024 16:51:15 GMT  
		Size: 21.5 MB (21482642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eefca5b6a97535c6d79c43af49229ce651897fded969e9b95559d7a78153a6c`  
		Last Modified: Mon, 06 May 2024 16:51:15 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf657011dd94cdd7014e71940e7b7db9736ee5d7ecd2ea6bf38a5c04957384e`  
		Last Modified: Mon, 06 May 2024 16:51:15 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5323c99aaf82700ee41756b87c829927ad9e911ce690721f78bbd38bfd1c9039`  
		Last Modified: Mon, 06 May 2024 16:51:16 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fc8439759be3c78a464085e837ccab6885a604af42b90d9e5ce0e20adb5934`  
		Last Modified: Mon, 06 May 2024 16:51:16 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4e4c853050721507a03a58abea227429e1b8a8a976b2b664bff59dd011a74b`  
		Last Modified: Mon, 06 May 2024 18:16:20 GMT  
		Size: 10.3 MB (10348326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cbda47d6a52e71f491f84f83479c23b2da17000e603ceca5b0ad6ebe83bfe932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3438200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b7305b9c83dd15061380f95e19121281d2c21f6e444e4577e936d6dd7794af`

```dockerfile
```

-	Layers:
	-	`sha256:2e71b78c27d94c8307e3cf997fe63f856432d38df57594eaef95f7085dac3174`  
		Last Modified: Mon, 06 May 2024 18:16:19 GMT  
		Size: 3.4 MB (3425448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f85755f9716b009d975af8b639bc70ea245e2780a1e7cdf5f7d5578e387ac08`  
		Last Modified: Mon, 06 May 2024 18:16:19 GMT  
		Size: 12.8 KB (12752 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:6f07181f1b1f1d889a68298d9be2d08683cefa4e392157b0fa18e2a9e927b700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 MB (114117108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae360824181e4a32d90c7e9b28945b5836cdd8a97b0af51a7567b62a825b73a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ARG RELEASE
# Thu, 22 Feb 2024 21:58:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.2
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:5b7cf94291ea168ccdc203965a79f54603a4fe2e0738a3acf0f7a8d860e51f32`  
		Last Modified: Sat, 27 Apr 2024 14:45:49 GMT  
		Size: 34.5 MB (34461223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ffd4587aa01be4e8eec017344ea5cc51404ebb09beea24c6acfccfb3500446`  
		Last Modified: Fri, 03 May 2024 00:25:21 GMT  
		Size: 39.6 MB (39587300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4692683c8fdb1668af0d51df1be2caeffbed2616552c2974e456eb4d498649`  
		Last Modified: Fri, 03 May 2024 00:25:20 GMT  
		Size: 7.9 MB (7857067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4dc00dfd0f0bd7c5e9ba8bbcb1454472a234178b43ae70768ce3e9cf241df0`  
		Last Modified: Fri, 03 May 2024 00:25:19 GMT  
		Size: 10.6 KB (10636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c064e5cbbbbc82e6d846f656f965a15497cc602c9a9964c80ecad5f30f4a6f1`  
		Last Modified: Fri, 03 May 2024 00:25:21 GMT  
		Size: 21.5 MB (21510303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c2a08ca258f1df9654d15a73dcf647efff794b318704bedb19da558d7d0217`  
		Last Modified: Fri, 03 May 2024 00:25:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13621a0ddc4030117873633f2c41294119824dee547929991505ab31bf1acc`  
		Last Modified: Fri, 03 May 2024 00:25:21 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d51f171f6cd12421065dc884bf871615c3b9a52f8478bcf06b1303caf9818c`  
		Last Modified: Fri, 03 May 2024 00:25:21 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273e6862d055f768e3f098d5492410f32faee01251f1b9aa3801ab32ffa38cc0`  
		Last Modified: Fri, 03 May 2024 00:25:22 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7b87d0602eb72f4b86c8b120355116ac9b94f1c481b99554b6888853923279`  
		Last Modified: Fri, 03 May 2024 01:17:51 GMT  
		Size: 10.7 MB (10688828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b6e63dfdbc55f7ea39c091819034510d2f12b52a0ab77396754ef891f579f5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3442622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ed27cf9c6d05c4e93eadea23fb6e4958cb7a44cfe64e20ba24bfd562aa143d`

```dockerfile
```

-	Layers:
	-	`sha256:0f9328d984227069f7f647a8b95424229b273e3a62e721fab2a8877a9b550e83`  
		Last Modified: Fri, 03 May 2024 01:17:49 GMT  
		Size: 3.4 MB (3429842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e224dc15a74fc462b74745b948681b95996d837db32132a682c3861df92b146`  
		Last Modified: Fri, 03 May 2024 01:17:49 GMT  
		Size: 12.8 KB (12780 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:bc573ccff28e789bdd2a11a850cf1569f71e611d58d543fe47373c825f79430f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104502674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab42701ba8a4386afe5103429a1072796e378b5322a49cd11285417c37b450b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ARG RELEASE
# Thu, 22 Feb 2024 21:58:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:7d693ab3b1f45d4992a119ec94444efc96c176ad954375f3bc1299ab813a46a0 in / 
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.2
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:01c7fcca5fd930108d469aeb9d86249eb7f2cdc75699dfa8dd132d9b5f55d29f`  
		Last Modified: Sat, 27 Apr 2024 14:45:56 GMT  
		Size: 28.0 MB (28000423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5a26cd838493e5e51399d9af1b5672c7249015174a746d3d3d29f00ffb6483`  
		Last Modified: Fri, 03 May 2024 00:28:04 GMT  
		Size: 38.2 MB (38231091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b54127ad099ab7097620158f6844046e662f5f51db34533f9d2f0a69f37151`  
		Last Modified: Fri, 03 May 2024 00:28:02 GMT  
		Size: 6.5 MB (6523608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76268c287df11d94d0416362ad18c345e6e783a38c7fb00947e9b89b34331eeb`  
		Last Modified: Fri, 03 May 2024 00:28:02 GMT  
		Size: 10.8 KB (10782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45930ed8983565c3fa7f379f63da208addf656a46b54bbf8ec0c2df602e11ac8`  
		Last Modified: Fri, 03 May 2024 00:28:04 GMT  
		Size: 21.5 MB (21540832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1de72f9fc1637acb497f6c658b92072748bd3d91baaf28afd9dde9b2b55104`  
		Last Modified: Fri, 03 May 2024 00:28:03 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f84c533496da9353baa1cb95604e0db23962a98e0564fbe1793d0029ee3c7ad`  
		Last Modified: Fri, 03 May 2024 00:28:03 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b94fb3a3a3be1fb9f1136bdee01489c15ff169669c9f88cb1de4e8819ee976`  
		Last Modified: Fri, 03 May 2024 00:28:05 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937239f963fb97a26e9f2715437800a2a2699fd4b91aa053859084c52e770ab6`  
		Last Modified: Fri, 03 May 2024 00:28:04 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7871c8e5f72fd6e8c44622d88572193cec4fec9c4c288c1411b18909bb1bdf9`  
		Last Modified: Fri, 03 May 2024 01:18:41 GMT  
		Size: 10.2 MB (10194190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:20947f13a5790e93da10c184e722655cd72bb6848379ebe31eab8b141d2ba998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3440088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feab02b546dc238dfc0331ac9bb875350fc5826c72b3530d4629664273fd6b23`

```dockerfile
```

-	Layers:
	-	`sha256:48e447ff6a304977ef238a4bd8d94fea8381e61d888f28fde620b82fa470fb5a`  
		Last Modified: Fri, 03 May 2024 01:18:40 GMT  
		Size: 3.4 MB (3427352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c6ce27f841c064f99e1fde129725bed44d2de41d98266199e595710a72f783f`  
		Last Modified: Fri, 03 May 2024 01:18:40 GMT  
		Size: 12.7 KB (12736 bytes)  
		MIME: application/vnd.in-toto+json
