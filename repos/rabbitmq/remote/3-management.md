## `rabbitmq:3-management`

```console
$ docker pull rabbitmq@sha256:e582c0bc7766f3342496d8485efb5a1df782b5ce3886ad017e2eaae442311f69
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

### `rabbitmq:3-management` - linux; amd64

```console
$ docker pull rabbitmq@sha256:9cfb7e92ae7d296aec4d1ae799e431209f7ed57d55f9c929d95667d0ccf1c920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114458903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de912cbbf07f938bb8aaa5682464a73a00c6a996efdf0880423aeb4eae006c34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 01:21:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 01:21:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 01:21:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 01:21:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 01:21:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:21:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 01:21:23 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 02 Dec 2025 01:21:23 GMT
ENV RABBITMQ_VERSION=3.13.7
# Tue, 02 Dec 2025 01:21:23 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 01:21:23 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 01:21:23 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:21:42 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 01:21:43 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 01:21:43 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 01:21:43 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 01:21:43 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 01:21:43 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 01:21:43 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 01:21:43 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 01:21:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:21:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:21:43 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 01:21:43 GMT
CMD ["rabbitmq-server"]
# Tue, 02 Dec 2025 03:07:49 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Tue, 02 Dec 2025 03:07:49 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fadc669ef1109fe5b0b01d402e7122ac2fe694b09e48f447fb45452965b91ae`  
		Last Modified: Tue, 02 Dec 2025 01:22:35 GMT  
		Size: 43.5 MB (43476479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7084ac8f4ab6e7759662f17795acfa25517fb96c91d711c81f22f967c433d556`  
		Last Modified: Tue, 02 Dec 2025 01:22:31 GMT  
		Size: 7.5 MB (7467932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb0d870d43804b802c0c9de117b0f4559d55a19f8d8ec210ead13790785962a`  
		Last Modified: Tue, 02 Dec 2025 01:22:30 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63c4408fdb7f18d34b259558dd294045a168f0723fa17a785a82ef3eaf73fa4`  
		Last Modified: Tue, 02 Dec 2025 03:07:40 GMT  
		Size: 21.3 MB (21313212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa05c660812131ce38eebdb654a1276825344dcfd19d75013cb9fa7de2a6100`  
		Last Modified: Tue, 02 Dec 2025 02:15:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e7f62f4b80395c0f0da29b68e9e394176c97793e5bcfb974f1024c0dd6c709`  
		Last Modified: Tue, 02 Dec 2025 02:15:27 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1c03b67a7854a75091d07c703298fd41dbf1fa4b3566521c5c438f4b0a986d`  
		Last Modified: Tue, 02 Dec 2025 02:15:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e6209d5fa82fda6b0a2a29e71378dcd4b4528fe5b0824a445dd45ddcbcab6e`  
		Last Modified: Tue, 02 Dec 2025 02:15:28 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d686b50ce172a810f738116ea3ac63fd7edb43569b63de1ae798f047b75b6f18`  
		Last Modified: Tue, 02 Dec 2025 03:08:06 GMT  
		Size: 12.5 MB (12465379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e09d97a495e23988be81d5679fcf51f41452f443c28d0a1d2c02085c467d063a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3099490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ce4ac06e2d8763870937fb048bf1388ef8e27b1a50cd8e007161346fbed569`

```dockerfile
```

-	Layers:
	-	`sha256:16ef6b12768ca883680096237f47c68e77de3c0fdddb674ad339ad9f5c71692d`  
		Last Modified: Tue, 02 Dec 2025 04:53:27 GMT  
		Size: 3.1 MB (3088405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec4c696b8bbd43b17ec72a209e5a9469a0b2e335ad8bd012ae620f11c62d197`  
		Last Modified: Tue, 02 Dec 2025 04:53:28 GMT  
		Size: 11.1 KB (11085 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:171f7b50b4f756589fd5d2ea7eb24527d36f35135bd6e8b3e02e356bcbd6866e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96769693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c8abf63ab2a6c7a83a20cb88d80e95c71cacae80c9fa16c9ca542844d572b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:17 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:17 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:20 GMT
ADD file:dd3740083ecd2e2b1e178f1771ef73043bc7be6c831492453a755b873d8b531b in / 
# Thu, 16 Oct 2025 19:25:21 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 01:27:10 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 01:27:10 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 01:27:10 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 01:27:10 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 01:27:10 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:27:10 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 01:27:11 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 02 Dec 2025 01:27:11 GMT
ENV RABBITMQ_VERSION=3.13.7
# Tue, 02 Dec 2025 01:27:11 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 01:27:11 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 01:27:11 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:27:31 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 01:27:32 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 01:27:32 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 01:27:32 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 01:27:32 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 01:27:32 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 01:27:32 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 01:27:32 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 01:27:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:27:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:27:32 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 01:27:32 GMT
CMD ["rabbitmq-server"]
# Tue, 02 Dec 2025 02:20:03 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Tue, 02 Dec 2025 02:20:03 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:6cdc0abf996c3192bfbda4018d34c282871d4be33fb369176002cb2199673adf`  
		Last Modified: Fri, 17 Oct 2025 08:06:35 GMT  
		Size: 26.9 MB (26852672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb90ea67f714bb72a80fad37b8a870951ed6e640fcc7d01820cb5870c721750c`  
		Last Modified: Tue, 02 Dec 2025 01:28:16 GMT  
		Size: 31.1 MB (31147076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b04251c8ff6ecf3bbbe0091179a6794077a05fe5b3d85e350dc9c58091ef1`  
		Last Modified: Tue, 02 Dec 2025 01:28:14 GMT  
		Size: 6.1 MB (6062754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d299157177dbc81fb0eda3086737039bb4784c67bbd08789432e17827237b`  
		Last Modified: Tue, 02 Dec 2025 01:28:13 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5bff38b4c3be401f780f74d6a78c2db156526561fb0d44eced74885f531e0d`  
		Last Modified: Tue, 02 Dec 2025 01:28:15 GMT  
		Size: 21.2 MB (21214855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164b06e450ae43db9b6ba846b7c7db49193a09299ec8803534c2319315c576e5`  
		Last Modified: Tue, 02 Dec 2025 01:28:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8324915a17bed107031e5425ab086196d502034b2ee487379657daa603fdc146`  
		Last Modified: Tue, 02 Dec 2025 01:28:13 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c4aa76a13f5326c3fce26efd51bb466d5894bb2ccbcc9f6c74b6a04e932ad6`  
		Last Modified: Tue, 02 Dec 2025 01:28:14 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a0da9fae66fb2cc9150bf78e47ad067c63f3672aafc639f1b6e5b9ac544069`  
		Last Modified: Tue, 02 Dec 2025 01:28:14 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f48e3fb9de60134e2e4309ca03408b1c831fd1ed70a8f2e1a83601090394ee7`  
		Last Modified: Tue, 02 Dec 2025 02:20:17 GMT  
		Size: 11.5 MB (11481061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:eb3b4c0e52d85d8aed28885ce60fc17b6d1d52359da76d730aca24b230a35a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3100508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa0fc342b412936531b0d0d6a105749b957ce9501db6dbf7d81a08e337d5f6b`

```dockerfile
```

-	Layers:
	-	`sha256:6461a28c7fd4958c655746d90b0f7bd022505396084a1d21d0a4a55460e69cd8`  
		Last Modified: Tue, 02 Dec 2025 04:53:32 GMT  
		Size: 3.1 MB (3089351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2899ac290c1bb95a4ef33150f1f838e3f93707ee734bcce3ce5e8d0983eec66`  
		Last Modified: Tue, 02 Dec 2025 04:53:33 GMT  
		Size: 11.2 KB (11157 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:8689ddfceca1ff1ecfeaa6619cb9cfc73570cf5fa022d3d904cdb065da1f925d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111084079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2edea6e7a01ca2e4c04f3dd0263d8c521686ef2467f587005747384ae49f2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 02:41:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 02:41:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 02:41:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 02:41:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 02:41:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:41:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 02:41:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 02 Dec 2025 02:41:42 GMT
ENV RABBITMQ_VERSION=3.13.7
# Tue, 02 Dec 2025 02:41:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 02:41:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 02:41:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:42:05 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 02:42:06 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 02:42:06 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 02:42:06 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 02:42:06 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 02:42:06 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 02:42:06 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 02:42:06 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 02:42:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 02:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 02:42:06 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 02:42:06 GMT
CMD ["rabbitmq-server"]
# Tue, 02 Dec 2025 03:27:10 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Tue, 02 Dec 2025 03:27:10 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a669bc3e1dd595cac776afbcb9e1747eff54ec02148a30cbc32d931cf90fdc6`  
		Last Modified: Tue, 02 Dec 2025 02:42:54 GMT  
		Size: 41.5 MB (41509079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908453a3b3f17a4227bdc5f64bb4f189bcccc21710a81539ee1f1b762dae7da7`  
		Last Modified: Tue, 02 Dec 2025 02:42:52 GMT  
		Size: 7.1 MB (7148033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee3d7bda3a274ffec0689a217ea9e5c75b7656c7263b33aa6e48414c5ec8088`  
		Last Modified: Tue, 02 Dec 2025 02:42:51 GMT  
		Size: 9.4 KB (9410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dce9f9a25e21af6fa87597fc88c2b6cfd18699fde7f413a962aa83282d2a1e`  
		Last Modified: Tue, 02 Dec 2025 02:42:54 GMT  
		Size: 21.2 MB (21222009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d707a369044b78c77de976dbcbe5f389e591fcd358c5c6f408740b7d9d58028`  
		Last Modified: Tue, 02 Dec 2025 02:42:51 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba58438a193ece3b6896a2f2ba1e0ff978fc3d2ea6ad09b8f4237b488b4c0f99`  
		Last Modified: Tue, 02 Dec 2025 02:42:51 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6c30257d7d3440b4cca1b0f765536fbd30e3c143d1c1c2322449918c7bf156`  
		Last Modified: Tue, 02 Dec 2025 02:42:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64be2c4c916bd5097029af195c6a2e81d9043fd43d894900ad749dad11663cc`  
		Last Modified: Tue, 02 Dec 2025 02:42:51 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93d97eeeeb848b17c974965d280eb81f72fdb149ca5f689b153228306d19bd1`  
		Last Modified: Tue, 02 Dec 2025 03:27:44 GMT  
		Size: 12.3 MB (12331842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e59cdb598dd26c9eb3f51443151e6100bf0915216b7043febd6a54d3115e4114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3100682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47cb82e66b4c4e96eb3794ad8de8a3287326e26779ae6b59b6ee285a5aa2cfa1`

```dockerfile
```

-	Layers:
	-	`sha256:2b94afbcf0cac89b910067451cf9be28003db09263538c75ee26f086e978fc16`  
		Last Modified: Tue, 02 Dec 2025 04:53:38 GMT  
		Size: 3.1 MB (3089505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efe170664348473cbaf5cb9805476ed1861b786a6b3286327b43bb2a50245b9e`  
		Last Modified: Tue, 02 Dec 2025 04:53:39 GMT  
		Size: 11.2 KB (11177 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:41a7a111dfa8e28550ecf591d83f2ffa920b7fdc290ed60319c74faffddef9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113629858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6780cd51fede33d7e301749884776c531714043d49d303c27e933269b9c269c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 03:25:31 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 03:25:31 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 03:25:31 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 03:25:31 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 03:25:31 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 03:25:31 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 03:25:33 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 02 Dec 2025 03:25:33 GMT
ENV RABBITMQ_VERSION=3.13.7
# Tue, 02 Dec 2025 03:25:33 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 03:25:33 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 03:25:33 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 03:26:11 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 03:26:13 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 03:26:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 03:26:14 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 03:26:14 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 03:26:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 03:26:14 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 03:26:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 03:26:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 03:26:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 03:26:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 03:26:16 GMT
CMD ["rabbitmq-server"]
# Tue, 02 Dec 2025 05:02:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Tue, 02 Dec 2025 05:02:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37979b10277ba7cf53d784c34588c3a848790d169a3d5f191ec60a3d1457384d`  
		Last Modified: Tue, 02 Dec 2025 03:27:39 GMT  
		Size: 37.2 MB (37197304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba04637dd8af3e0615578235400332d9b4e968426b4eee9d9939b8a13fe1b580`  
		Last Modified: Tue, 02 Dec 2025 03:27:35 GMT  
		Size: 7.9 MB (7879347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab90f70dd1d905008df7005a8da6e646014ef99d9d8ad90f2b2e486ecbb9d5`  
		Last Modified: Tue, 02 Dec 2025 03:27:34 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6059cb6c5cd48b345c6f816c084ca363257d3f9a309e6d8321ac90955ddf731c`  
		Last Modified: Tue, 02 Dec 2025 03:27:38 GMT  
		Size: 21.3 MB (21273445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bc01a97d482d2c453615d9b665d2b721ee0334cca80571370e3ccdde0b9c0e`  
		Last Modified: Tue, 02 Dec 2025 03:27:34 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4687f89c334c05cf988d9cf6f6d8aa61372a3c8c959e0baae46822b16e7f63`  
		Last Modified: Tue, 02 Dec 2025 03:27:35 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd66f4ad6c791e97da42ae18f9d5be2ee74b6549d12252784e541f509db8ae1c`  
		Last Modified: Tue, 02 Dec 2025 03:27:35 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8fafe33e4765b37213d07c25f8409173a2b5ff62491a74b55a1d912cfe434f`  
		Last Modified: Tue, 02 Dec 2025 03:27:35 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbe95d5bd6c691a2a138c064669882d601e84fca7cd1737347719253d7269a0`  
		Last Modified: Tue, 02 Dec 2025 05:02:35 GMT  
		Size: 13.0 MB (12964171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2817a7149a375c996cf7e21f5d5f500e903ff90ca2e8536839fef69232c6692d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3104259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d4e91033bcaa1b18c29bb434a207bad88a7423529f92718da92111e97b2b26`

```dockerfile
```

-	Layers:
	-	`sha256:01de75559a504cf891d417c86b5384c4f02f85268c612be8cf60bce4fe69a9ac`  
		Last Modified: Tue, 02 Dec 2025 07:52:31 GMT  
		Size: 3.1 MB (3093136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05d95827cd0d00e0d1ad18f8cc66b1d142f4f474aba3e8707146b9d6b3f78d9`  
		Last Modified: Tue, 02 Dec 2025 07:52:31 GMT  
		Size: 11.1 KB (11123 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:17771b1cf2d231813885def414c768cc3eb394c1aebe125470a075e5865b9fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106198497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a526c95833b2a3a9463cc7bc6cc6bb4f07f5ba9ac9b12f34bbb3e280d98509`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:53:04 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:53:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:53:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:53:05 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:53:45 GMT
ADD file:6c2a12ec42d9e6c7e02041a8483a3a93ab9b91131ca66ecb93506ba161a4909d in / 
# Thu, 16 Oct 2025 19:53:49 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 12:37:58 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 12:37:58 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 12:37:58 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 12:37:59 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 12:37:59 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 12:37:59 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 12:38:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 02 Dec 2025 12:38:02 GMT
ENV RABBITMQ_VERSION=3.13.7
# Tue, 02 Dec 2025 12:38:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 12:38:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 12:38:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 12:40:09 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 12:40:18 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 12:40:19 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 12:40:19 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 12:40:19 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 12:40:19 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 12:40:19 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 12:40:19 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 12:40:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 12:40:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 12:40:19 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 12:40:19 GMT
CMD ["rabbitmq-server"]
# Tue, 02 Dec 2025 16:18:57 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Tue, 02 Dec 2025 16:18:57 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:4f36e1b0a2cc427e5979b49608ef4e52795313f083fdc941cab616d5ab2b861b`  
		Last Modified: Sat, 15 Nov 2025 10:03:37 GMT  
		Size: 31.0 MB (30952148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada861ce59d3d003c5061c1ca4d267644cfe607d7b806bcee3c9cb24e210953d`  
		Last Modified: Tue, 02 Dec 2025 13:14:23 GMT  
		Size: 33.0 MB (32978671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d57dc248029ec39b5745b5ffb6d8e8d33ea36a3f6ef4b5bea559903db5e3c6`  
		Last Modified: Tue, 02 Dec 2025 13:14:34 GMT  
		Size: 8.7 MB (8700782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c6c62c684daf421e064c83e462d25fe2f80952c9a25042857ac95b6713a405`  
		Last Modified: Tue, 02 Dec 2025 13:14:40 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95d9016a507eac9e4d57c1b45f93b42c7f4893af401dddc4a3ebdc0fdfd5ae4`  
		Last Modified: Tue, 02 Dec 2025 13:53:38 GMT  
		Size: 21.2 MB (21225806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c21b9f89fbcaf10eba4599a3a519a12891a64fbf926edf5b473d86c9a80b0`  
		Last Modified: Tue, 02 Dec 2025 13:14:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246bb0c3d9a13d00e79d90272f2e590c92bf6cb1d11b81e31792b2e5a84a86d8`  
		Last Modified: Tue, 02 Dec 2025 13:14:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb70f05088b41ee08d3dd224c249d0ca8daa1150a03b0079c395eecf2e900ebf`  
		Last Modified: Tue, 02 Dec 2025 13:14:50 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bec859b7172fa02e4c4212c6d129b16043cc5a835792ec8e3cf9c368a98bc1a`  
		Last Modified: Tue, 02 Dec 2025 13:14:53 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f44ce1726c503b014a01623fde13c77c60bf90ec7d1e032eda8fac06843f3d`  
		Last Modified: Tue, 02 Dec 2025 16:20:58 GMT  
		Size: 12.3 MB (12329877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:73bf191c0949186ccc87b0625fd24547b9ef1a9c6fde416725e23ea8ec04183c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3091963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062e9715cb897ea5ab9cf4a2c6300bf587e11fd9a29eee20aefaa08b7899f3a1`

```dockerfile
```

-	Layers:
	-	`sha256:9a81182681d8a57de90fd9599f1df83e40c64431ffc16cb90823ddfd2c9c2c3a`  
		Last Modified: Tue, 02 Dec 2025 19:52:34 GMT  
		Size: 3.1 MB (3080840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a317e58ba461fac8fc50b144b974de349a7e9f57cb8c2e96ad931b321c6d71e`  
		Last Modified: Tue, 02 Dec 2025 19:52:35 GMT  
		Size: 11.1 KB (11123 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:0ff0c1aecaad05ea42390addc7cfd0975bef76101d4bbdedd019176e59e1d9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106945914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9851cf99718dbd1a6eae1569baa47bb48d6dd5c985414c0113574017687b54f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:14 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:16 GMT
ADD file:f7335d462150d31c3c91b13ccd3e927bc9a1b9c6664fa8905ccf68bbe3d86cd3 in / 
# Thu, 16 Oct 2025 19:25:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 03:08:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 03:08:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 03:08:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 03:08:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 03:08:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 03:08:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 03:08:23 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 02 Dec 2025 03:08:23 GMT
ENV RABBITMQ_VERSION=3.13.7
# Tue, 02 Dec 2025 03:08:23 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 03:08:23 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 03:08:23 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 03:08:55 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 03:08:56 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 03:08:56 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 03:08:56 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 03:08:56 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 03:08:56 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 03:08:56 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 03:08:57 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 03:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 03:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 03:08:57 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 03:08:57 GMT
CMD ["rabbitmq-server"]
# Tue, 02 Dec 2025 04:10:39 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Tue, 02 Dec 2025 04:10:39 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:7d5b0205a5ff16c2b58f20a113b5eb9a80393a644df077beab5d90635153dc66`  
		Last Modified: Thu, 16 Oct 2025 21:17:39 GMT  
		Size: 29.9 MB (29907597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b1af4a46731b5bf3bed070b13bbbd05648e4e4d8af7e79126403221f6b45bb`  
		Last Modified: Tue, 02 Dec 2025 03:09:57 GMT  
		Size: 36.3 MB (36285922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c6e9079bfe6a4c23d5e05bc8fac50237513857aa7d6b5bcc01be8ab3743328`  
		Last Modified: Tue, 02 Dec 2025 03:09:52 GMT  
		Size: 6.8 MB (6759501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc04c2e37794f4547427d71ab7823ab36df260f7c8fc9f116f4314ea895c81d3`  
		Last Modified: Tue, 02 Dec 2025 03:09:51 GMT  
		Size: 9.6 KB (9638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8533693c7b24f3b65e39551bcaee2ddcf8c413463bbe3a9150788986caf4a02`  
		Last Modified: Tue, 02 Dec 2025 03:09:57 GMT  
		Size: 21.3 MB (21295570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3269541ad072e78b2134a3da6d0bc7ed28225ca0163abe81ffbe42aaef9253a5`  
		Last Modified: Tue, 02 Dec 2025 03:09:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6de292c72312a5204862bba6c0a6b09262b0c881a055197702b9013c73b92e`  
		Last Modified: Tue, 02 Dec 2025 03:09:51 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ab2ce858413c3b27eff55075b2f60b0e40705bb25d914682c32eec1868ec1a`  
		Last Modified: Tue, 02 Dec 2025 03:09:51 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf48c425cff249d9555193a9758d150b726a6616df45d4079f1b451f9144afea`  
		Last Modified: Tue, 02 Dec 2025 03:09:51 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c236055154d475c7c9979955905ef3689c4641afe89b5ed120de9c53dc5d50`  
		Last Modified: Tue, 02 Dec 2025 08:00:29 GMT  
		Size: 12.7 MB (12685934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:aa3b246f9343f953b6554aedcd12ec8ed70fb3349498b674e426a9df23cd4fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3101546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9f661853c2bc3a50de9b5f3035828293b8b58dd3d3bf1edc750fb7fe760e51`

```dockerfile
```

-	Layers:
	-	`sha256:04f07f8e2809db93e918b098a93d5d9c5578d2d37330ec76953d3ddbf956a852`  
		Last Modified: Tue, 02 Dec 2025 07:52:37 GMT  
		Size: 3.1 MB (3090462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d76f886c5fcba8205a37d9283c314c3b586cf8755c171174483947dec3e3e46`  
		Last Modified: Tue, 02 Dec 2025 07:52:38 GMT  
		Size: 11.1 KB (11084 bytes)  
		MIME: application/vnd.in-toto+json
