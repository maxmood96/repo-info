## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:6e6076af22e6c48f378505a2cc653990d69e3b2efb4198e48a387bde750fdc5c
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

### `rabbitmq:latest` - linux; amd64

```console
$ docker pull rabbitmq@sha256:a9d813e3c19aceec72f54817708f3d32a0313901ea8eeb96ee4acc6634766414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104624144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb179b9f4315d7fdb8a337cc84b2edec5c7ac3ffa0746fb59e3113998de7099b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 17:41:23 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 04 Jun 2024 17:41:23 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 04 Jun 2024 17:41:23 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 04 Jun 2024 17:41:23 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 04 Jun 2024 17:41:23 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 17:41:23 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 04 Jun 2024 17:41:23 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 04 Jun 2024 17:41:23 GMT
ENV RABBITMQ_VERSION=3.13.3
# Tue, 04 Jun 2024 17:41:23 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 04 Jun 2024 17:41:23 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 04 Jun 2024 17:41:23 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 17:41:23 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 04 Jun 2024 17:41:23 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 04 Jun 2024 17:41:23 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 04 Jun 2024 17:41:23 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 04 Jun 2024 17:41:23 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 04 Jun 2024 17:41:23 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 04 Jun 2024 17:41:23 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 04 Jun 2024 17:41:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 17:41:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 17:41:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 04 Jun 2024 17:41:23 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04462dba3f374444bae3b4ef2ef8d62c392d5a9d9f4d6ffac5f937f6f53ad2c5`  
		Last Modified: Wed, 05 Jun 2024 02:27:12 GMT  
		Size: 46.0 MB (46005262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4510fcf79f234d5682a0453cf73802194877073b51ede4475b21b777468cc6`  
		Last Modified: Wed, 05 Jun 2024 02:27:12 GMT  
		Size: 7.5 MB (7483797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5281fd20b9570a8d14a58d9f615f36a32d3d05f8615de845de552caffe74815b`  
		Last Modified: Wed, 05 Jun 2024 02:27:11 GMT  
		Size: 10.7 KB (10734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742d698ad83e872519d25d4210e66a8656ebd5da36af6c21b294effd50ec325d`  
		Last Modified: Wed, 05 Jun 2024 02:27:12 GMT  
		Size: 21.6 MB (21588848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2ed69a577bc4add9440a9a6b2bd51f7d74d21350056b90849454ef71aef1a7`  
		Last Modified: Wed, 05 Jun 2024 02:27:13 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13fdbb3584232407f6085ba70e1883a19f9327814c26e4102286a79314ee84`  
		Last Modified: Wed, 05 Jun 2024 02:27:12 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df16e38d24277964a3011db13e0114cbe403ecb01b0ce4d72a9e1b7cc3852cb`  
		Last Modified: Wed, 05 Jun 2024 02:27:13 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee882b7bc039999f9385b6b6c395a81e88755247d09602cf584520264e3ebb6`  
		Last Modified: Wed, 05 Jun 2024 02:27:13 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:899cc945ba580362ab5779ae06b15fe65616fdfe2be3661c5355aa7b4d71b143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18553510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4110e9caaabbcbe3a507626057cf9444d4f8a54d70b44face80169476497cb`

```dockerfile
```

-	Layers:
	-	`sha256:0265ec3dbae18daffdf711d9357cd9d14b5ca257f145d203d99ae3728bed93bf`  
		Last Modified: Wed, 05 Jun 2024 02:27:11 GMT  
		Size: 2.9 MB (2884412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3d53ea2c9bce52760d871d5bffe8f23e5d75410f217abde7b9ccb98f1a6894`  
		Last Modified: Wed, 05 Jun 2024 02:27:12 GMT  
		Size: 5.2 MB (5160712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9736a2309092b4d98cf008ae4c32fb9cb8c16be7e1fce5456c8859530e92d98a`  
		Last Modified: Wed, 05 Jun 2024 02:27:11 GMT  
		Size: 5.3 MB (5284981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62bad355e3cc6cccbe79110cad3dd09bd1b68dd54bfdbad281f82cb8ff4d7072`  
		Last Modified: Wed, 05 Jun 2024 02:27:11 GMT  
		Size: 5.2 MB (5162086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d05d97b3921c283db02c4dc8180ac757dde3ba77f165389ca039de56ada7e1b`  
		Last Modified: Wed, 05 Jun 2024 02:27:12 GMT  
		Size: 61.3 KB (61319 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:97d68b4fc7be06987f26bbe8976fd939a799450004d8fe9e282613e3a87c351f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87730897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7232ff88388b27ef9dad2ce3bc0dbb997ef828f069d3084160af75f8f567f907`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:35:06 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:35:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:35:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:35:06 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:35:17 GMT
ADD file:ab2e95a123b006ac900aaaf0d1858b88941c8d319f47e41733db6f0f5fe98b87 in / 
# Sat, 27 Apr 2024 14:35:18 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 17:41:23 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 04 Jun 2024 17:41:23 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 04 Jun 2024 17:41:23 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 04 Jun 2024 17:41:23 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 04 Jun 2024 17:41:23 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 17:41:23 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 04 Jun 2024 17:41:23 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 04 Jun 2024 17:41:23 GMT
ENV RABBITMQ_VERSION=3.13.3
# Tue, 04 Jun 2024 17:41:23 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 04 Jun 2024 17:41:23 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 04 Jun 2024 17:41:23 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 17:41:23 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 04 Jun 2024 17:41:23 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 04 Jun 2024 17:41:23 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 04 Jun 2024 17:41:23 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 04 Jun 2024 17:41:23 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 04 Jun 2024 17:41:23 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 04 Jun 2024 17:41:23 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 04 Jun 2024 17:41:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 17:41:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 17:41:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 04 Jun 2024 17:41:23 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f5b4213824fc3515b68e6844d3fc289ae00ef8cd07ddcd43856c3ad7faea16d4`  
		Last Modified: Sat, 27 Apr 2024 14:45:43 GMT  
		Size: 26.6 MB (26639789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbd5a39c627ce56075acfe44aef1097acffe8b376cfd129483d6aebe2575d63`  
		Last Modified: Wed, 05 Jun 2024 02:48:23 GMT  
		Size: 33.5 MB (33495154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e5142d4fa6ec0c14b08a52954a3c5bc803de9b797f0d3f6baa6a6cd1e48515`  
		Last Modified: Wed, 05 Jun 2024 02:48:22 GMT  
		Size: 6.1 MB (6077363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a362a74b260290d3976e73621a0da264792984e3f64541d65aa51debbd0a1b`  
		Last Modified: Wed, 05 Jun 2024 02:48:22 GMT  
		Size: 10.7 KB (10730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da6b9f59c3af494b11938dbe788df8c6425234137ca355eb083e04a3b2d4bc5`  
		Last Modified: Wed, 05 Jun 2024 02:48:23 GMT  
		Size: 21.5 MB (21506112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b8b076091f2484eb9f58a8004409e450007ae9b2fc823a91db37701ed43c99`  
		Last Modified: Wed, 05 Jun 2024 02:48:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64196afa56b2500a24a85ee657cc0c2e9a8ef193a260b11208e5c20243c9e43`  
		Last Modified: Wed, 05 Jun 2024 02:48:23 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449fd40be2b4a79192705bb1c87babb34850c0c8b4f7385f4d5ca58f800fa0ab`  
		Last Modified: Wed, 05 Jun 2024 02:48:24 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5fa414eb1068b8a679cb756bebab84c232cb2d7021fa8c37a2fc827bfd2748`  
		Last Modified: Wed, 05 Jun 2024 02:48:24 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c424fdd1989fa2a8b8276f4549e1f261281050845fa7a7a90836e8f078f605ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18012604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a368feb109055a309a592b3c432a47dbe7326b7aef0f207dd095e7e44074026`

```dockerfile
```

-	Layers:
	-	`sha256:865d0093ad1fecc2244d1d08a7b4904f4170fe2a91a0279b293af2f350820427`  
		Last Modified: Wed, 05 Jun 2024 02:48:22 GMT  
		Size: 2.9 MB (2885083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82ec92ae7eb2e03ada8c432af4d5b86309371e7aa90735b802197bb10faefa8c`  
		Last Modified: Wed, 05 Jun 2024 02:48:22 GMT  
		Size: 5.0 MB (4980955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88a785dc209c7ce67913022348ab3ec83b611a910904415bd6bf5c152676e39f`  
		Last Modified: Wed, 05 Jun 2024 02:48:23 GMT  
		Size: 5.1 MB (5102732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d507df8ecc67f6f076df98136f49c31352cea1d0286b8e1a7c56d10d021526e4`  
		Last Modified: Wed, 05 Jun 2024 02:48:22 GMT  
		Size: 5.0 MB (4982329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915c0dd3d785e1074188a4010bace63ccda66e4ed6ed43c7ad21d6dedb5adeb7`  
		Last Modified: Wed, 05 Jun 2024 02:48:23 GMT  
		Size: 61.5 KB (61505 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:c19c03d7e1b9cb4ee30e2656e6df8647258db651747ea87fc8e9fd6296939757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100084150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2893b14a4dfd9d4408dbeec389dcbb604578ad9fea51f78d99ca572bdeac73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Fri, 31 May 2024 23:16:53 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 May 2024 23:16:53 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 May 2024 23:16:53 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 May 2024 23:16:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_VERSION=3.13.3
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 23:16:53 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 May 2024 23:16:53 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 May 2024 23:16:53 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 May 2024 23:16:53 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 May 2024 23:16:53 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 May 2024 23:16:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 23:16:53 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 May 2024 23:16:53 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fc274e21d0b7eb2be9dd980a12b31e81da0622afdb25bb7b414d5b866e4905`  
		Last Modified: Tue, 04 Jun 2024 17:25:32 GMT  
		Size: 44.1 MB (44084489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3d02e5a234c45d42c17df478c5ed854093f7650539c7371569a4250c07f3e0`  
		Last Modified: Tue, 04 Jun 2024 17:25:32 GMT  
		Size: 7.1 MB (7130266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7064aa2c140b7a7d0b6336a813519910c94cba0259a6d28e41c283825c0e5f0f`  
		Last Modified: Tue, 04 Jun 2024 17:25:31 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f3ea75963fee9a25e5c18a059f9630523a77bedec028c50a01d12516b046b7`  
		Last Modified: Tue, 04 Jun 2024 17:25:32 GMT  
		Size: 21.5 MB (21496395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239910e9e133fa374b8633b7225ef9d988498cb2336e8151f821bbfbb2b2fd65`  
		Last Modified: Tue, 04 Jun 2024 17:25:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b08bbe8d19a6450247542dcaa8eccaf9ceb142b85b5ba9d243c2b74e1605380`  
		Last Modified: Tue, 04 Jun 2024 17:25:33 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5940e7bcc9cfd0289a6d23ba362cae2c7883c605dc77632d66e3eed853e40b1`  
		Last Modified: Tue, 04 Jun 2024 17:25:33 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19563ccc03b78257ce3920633393f3777b10d087403ffc7e6f0ce3877c40de97`  
		Last Modified: Tue, 04 Jun 2024 17:25:34 GMT  
		Size: 836.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5206edbac8eed561a9e5f2ee39399561ca0b3162536cec3b2a9cafc073b3d4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18544948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1813c0b2ce01f159d0a2dd2e81fbb048e0412eab75f2b2090276787cffbf52fb`

```dockerfile
```

-	Layers:
	-	`sha256:df5a15b5f725970025d907f7f742e4ed62dff2b09c823f54799d9335910fcb5d`  
		Last Modified: Tue, 04 Jun 2024 17:25:31 GMT  
		Size: 2.9 MB (2884684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a8a01b565e96b50d50a39c51b7ddbfdd7d25dda07d1dfe455b0db41d6c8d329`  
		Last Modified: Tue, 04 Jun 2024 17:25:31 GMT  
		Size: 5.2 MB (5157663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:163c1debe9edeaf56474151b9764147965b5d67954387584b9d1d4bd755be137`  
		Last Modified: Tue, 04 Jun 2024 17:25:31 GMT  
		Size: 5.3 MB (5281944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e108bb6151787f2d40616c40d40e7470ff3c566941b3290a0019acb655ebc8e0`  
		Last Modified: Tue, 04 Jun 2024 17:25:31 GMT  
		Size: 5.2 MB (5159037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a64e8635bc8d2ed370033f3b096a207c64547741480849c0e2f54ef868332c4`  
		Last Modified: Tue, 04 Jun 2024 17:25:32 GMT  
		Size: 61.6 KB (61620 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:adcd9cb07007a2642153775de237c506a2e60c1798a37697e73c3b7c4e47b8fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103442334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdff1572b1cefb08259355994851ff048af1c1145aa9b49bc3f4a6a97e96d34c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Fri, 31 May 2024 23:16:53 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 May 2024 23:16:53 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 May 2024 23:16:53 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 May 2024 23:16:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_VERSION=3.13.3
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 23:16:53 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 May 2024 23:16:53 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 May 2024 23:16:53 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 May 2024 23:16:53 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 May 2024 23:16:53 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 May 2024 23:16:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 23:16:53 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 May 2024 23:16:53 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:5b7cf94291ea168ccdc203965a79f54603a4fe2e0738a3acf0f7a8d860e51f32`  
		Last Modified: Sat, 27 Apr 2024 14:45:49 GMT  
		Size: 34.5 MB (34461223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad8e0fdc1bd0d1fff0ae032166f4d36c2833fd6700229c09eb41895e2ba3adc`  
		Last Modified: Tue, 04 Jun 2024 01:43:23 GMT  
		Size: 39.6 MB (39587767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8765c79ffc656de682115e9201aea7885cd38a52f145a09b6ddb9a06a323f41`  
		Last Modified: Tue, 04 Jun 2024 01:43:22 GMT  
		Size: 7.9 MB (7857078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac74cac4dce65486e8c77b443f0b002a4aa98fca072a7da226ddd154c62b8398`  
		Last Modified: Tue, 04 Jun 2024 01:43:21 GMT  
		Size: 10.7 KB (10678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1591c747b08908ec7d847ff339104eda597f2af552c34ebddc37d2009d4f857`  
		Last Modified: Tue, 04 Jun 2024 01:43:23 GMT  
		Size: 21.5 MB (21523829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ed8c72b2c83a82299681a9edf1850c6c59d63a64d3f20a0c382eb96b3f554e`  
		Last Modified: Tue, 04 Jun 2024 01:43:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb4cedb81e9f17cccd4caa0f928e12b9f9fffca8f56e915ff9d77f1a9742a02`  
		Last Modified: Tue, 04 Jun 2024 01:43:23 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d4e3344060f8fc80115ee7112beb8e1b9847037466ac7b80af72376e2620fc`  
		Last Modified: Tue, 04 Jun 2024 01:43:24 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2584c1229e866e05bf968cc683fbf386a29eb33adbc1f0a3c23be4a89b46fe`  
		Last Modified: Tue, 04 Jun 2024 01:43:25 GMT  
		Size: 837.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f85297063f7ed23a947cd8c93171737c67b8cd36a371ed229e163947b42dc1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18443028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099c6ad62f5c28937be5b41c43b70d0cfbe1978542026e81e5fd7d088adfefcd`

```dockerfile
```

-	Layers:
	-	`sha256:8a8702dc25c2fc03089c84bfc136183009414e970ff6d920ed0e2151b4e79ffc`  
		Last Modified: Tue, 04 Jun 2024 01:43:22 GMT  
		Size: 2.9 MB (2888171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd3b726dac3f708b1f64f3983f0b93a546430738dbac19865d7e79e8672b3754`  
		Last Modified: Tue, 04 Jun 2024 01:43:22 GMT  
		Size: 5.1 MB (5122973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29fdd99397721e92cd972865fd709ce06a71d48aae67331edfc277d7eba84635`  
		Last Modified: Tue, 04 Jun 2024 01:43:22 GMT  
		Size: 5.2 MB (5246162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaaa90cee2f0a6d315dee1c1101b7866540fa7df2ba274d3ffc5c001f52677a9`  
		Last Modified: Tue, 04 Jun 2024 01:43:22 GMT  
		Size: 5.1 MB (5124347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a658f6c7a2727eaf7c8ea20bfe357414b1ccf0f1ee8adea992f56aa26c7063d`  
		Last Modified: Tue, 04 Jun 2024 01:43:23 GMT  
		Size: 61.4 KB (61375 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:ec7cda3d0f539d31a662ba5760929f218aa5776e151211c34430ddf6a42aa066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94324515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1d99698ce43e00c1bb78879f64e3232002c6134ba89f4850204030827844d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Apr 2024 13:52:56 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:52:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:52:58 GMT
ADD file:7d693ab3b1f45d4992a119ec94444efc96c176ad954375f3bc1299ab813a46a0 in / 
# Sat, 27 Apr 2024 13:52:58 GMT
CMD ["/bin/bash"]
# Fri, 31 May 2024 23:16:53 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 May 2024 23:16:53 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 May 2024 23:16:53 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 May 2024 23:16:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_VERSION=3.13.3
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 23:16:53 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 May 2024 23:16:53 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 May 2024 23:16:53 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 May 2024 23:16:53 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 May 2024 23:16:53 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 May 2024 23:16:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 23:16:53 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 May 2024 23:16:53 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:01c7fcca5fd930108d469aeb9d86249eb7f2cdc75699dfa8dd132d9b5f55d29f`  
		Last Modified: Sat, 27 Apr 2024 14:45:56 GMT  
		Size: 28.0 MB (28000423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eacc927a9819a5bd440c54b7d9ad65664aa200bb56d990babf251c3ce88c42e`  
		Last Modified: Mon, 03 Jun 2024 21:24:40 GMT  
		Size: 38.2 MB (38231057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03f52155973e5c87b801d2804e9bc1b05a439362a7525271b19e0658500b7cc`  
		Last Modified: Mon, 03 Jun 2024 21:24:39 GMT  
		Size: 6.5 MB (6523578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbd2e1fbb8b3e99372c3a7178e7afb2036114864cee41a8300429c65b7f1827`  
		Last Modified: Mon, 03 Jun 2024 21:24:39 GMT  
		Size: 10.8 KB (10773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4157505b1b95f6458da9bf39761ae227372eeb6cefc776275a7461f3ef591882`  
		Last Modified: Mon, 03 Jun 2024 21:24:40 GMT  
		Size: 21.6 MB (21556936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1be020d5ec912460e8738bb9d36ab938d235c6817d8b07605ac5bddd1d32686`  
		Last Modified: Mon, 03 Jun 2024 21:24:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418d89094b14a46749d8d2c92b125129ce104425fa192c22ecdec780d1619664`  
		Last Modified: Mon, 03 Jun 2024 21:24:40 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1841c9f0cd63a7a4e5d9834a9fda4179064c7a453a4bc0a30ae370458b6a4889`  
		Last Modified: Mon, 03 Jun 2024 21:24:40 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086c6633eccb831e21bfacfabac8dae018a34ee3393d3b1a1cd6a6288ee540df`  
		Last Modified: Mon, 03 Jun 2024 21:24:41 GMT  
		Size: 835.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:399c3a46feee7ad598f4076f6daef1141a97e58fcab7612e8a6a6ca386bf0395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18084139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f435f03bb39e2186882247161936410f16ae34eba9fac54cda81032d65fd5df1`

```dockerfile
```

-	Layers:
	-	`sha256:66fce578f8282ceb0a66bd19aa18d2a806a16af80957df75d5bb75e20939e1ba`  
		Last Modified: Mon, 03 Jun 2024 21:24:39 GMT  
		Size: 2.9 MB (2886021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58aa6675b4de3e5e36894ef8816cf4425c5702637dc2fc16df8e0b84abdf273e`  
		Last Modified: Mon, 03 Jun 2024 21:24:39 GMT  
		Size: 5.0 MB (5004082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d86f079354dd9218f9a22c28172b60e81282804d8fe63491ef100c9248fc10`  
		Last Modified: Mon, 03 Jun 2024 21:24:40 GMT  
		Size: 5.1 MB (5127261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edc0e137ab01dd56e168e21a8632aab585eca7cec4d40f2e0735e9ee13fbdac1`  
		Last Modified: Mon, 03 Jun 2024 21:24:39 GMT  
		Size: 5.0 MB (5005456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:286e476e9369ae984edc4b5970b39c3813e7b6e0f1b31e24bd557b99a080ac32`  
		Last Modified: Mon, 03 Jun 2024 21:24:40 GMT  
		Size: 61.3 KB (61319 bytes)  
		MIME: application/vnd.in-toto+json
