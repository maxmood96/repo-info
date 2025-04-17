## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:54ea5cdf57a21e3c38f4f943d0683abdc5997e7cc1af2a90fd4e8d0a69a68854
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
$ docker pull rabbitmq@sha256:42ecb6d18fbd64ce9c0e4067f7b7f7015c1f73b7dac7f8aeaca588e2a22c1817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115155058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9efcaf2871c0b9d005e3861ed9f9d6b1a322d6b7c4a00146d01580153d2ba35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 17:58:56 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 16 Apr 2025 17:58:56 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 16 Apr 2025 17:58:56 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 16 Apr 2025 17:58:56 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_VERSION=4.1.0
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 16 Apr 2025 17:58:56 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Apr 2025 17:58:56 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 16 Apr 2025 17:58:56 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 16 Apr 2025 17:58:56 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 16 Apr 2025 17:58:56 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Apr 2025 17:58:56 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 16 Apr 2025 17:58:56 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1080edc4726286af12067263e97ba78513754790003232cc94386151113c413`  
		Last Modified: Thu, 17 Apr 2025 18:33:25 GMT  
		Size: 46.2 MB (46238596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f18cb54bfd09ed34472ae24ec5e858481188546ec098298076b54cffe1b6ed`  
		Last Modified: Thu, 17 Apr 2025 18:33:24 GMT  
		Size: 8.2 MB (8171046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9542485d6a6155f2fadf4b017e90638a8c38c70e20a7d3a950c42be71c4bccdc`  
		Last Modified: Thu, 17 Apr 2025 18:33:23 GMT  
		Size: 9.5 KB (9467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2021e674e22b463660b1bc22cc344f3f7b549a7a6d3c17a41e905141a82cf`  
		Last Modified: Thu, 17 Apr 2025 18:33:25 GMT  
		Size: 31.0 MB (31016542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b058adf20de918c699c5d03c94da595bfa8aadd3f5d42fa8d46d900af1b329`  
		Last Modified: Thu, 17 Apr 2025 18:33:24 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d03cd9ff351c1c44904c0d6d3626fa5b9f3ef1464d914445b3b84ba69ab9ab6`  
		Last Modified: Thu, 17 Apr 2025 18:33:25 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eb49d2191df8850a98ea510d15adeaa38cdfa7f888e07a200a4bfc086ebae6`  
		Last Modified: Thu, 17 Apr 2025 18:33:25 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2371181ab69ac667be97336a981f5d2ba05c1aca81fc3bd00bb23b5d69ece566`  
		Last Modified: Thu, 17 Apr 2025 18:33:26 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9414d23b891ebdd73c15938a6f7dc1c99a57bbbde99c8addce9fe3bac2ffe778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18193684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b56cdd5cdc57fa2d0589bfde144113d061c1f928dd3cc75ed0502025a63473`

```dockerfile
```

-	Layers:
	-	`sha256:800de7bb0936e21d4593a61273a8441542395fbe7c9edadf6ef90af3975a8e67`  
		Last Modified: Thu, 17 Apr 2025 18:33:24 GMT  
		Size: 2.4 MB (2366876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff79fa381049f1938b5ef0e043591890655f67a2eac955bf680d8f2c9ed47c7`  
		Last Modified: Thu, 17 Apr 2025 18:33:24 GMT  
		Size: 5.2 MB (5202998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb336db1762bc2d8907c06875a69bf505430c2669b3483b39d56c97c2c6b11e`  
		Last Modified: Thu, 17 Apr 2025 18:33:24 GMT  
		Size: 5.4 MB (5359243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08de8dd99b0b821437ddb8ccf2919905546807a6c77e20ffba0e46157c9573bf`  
		Last Modified: Thu, 17 Apr 2025 18:33:24 GMT  
		Size: 5.2 MB (5204740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e8c4579dce3932ef4c73f3b0ee396cf7a61f1e1a7f767dae4701bbad069d9a`  
		Last Modified: Thu, 17 Apr 2025 18:33:25 GMT  
		Size: 59.8 KB (59827 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:d6799a12a90d147ee84f9cac1fc643418f85f19ba890ac71aba934459198b9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97717987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243ab8102aca1fc5ea161e85a321abfcb4e8636e91692677c284eb667c2984af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:57 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:47:00 GMT
ADD file:0c96eee5fced5e61820b5d18bd668a362ad0e5b3fc04c115f9023e8c295e7000 in / 
# Tue, 08 Apr 2025 10:47:00 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 17:58:56 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 16 Apr 2025 17:58:56 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 16 Apr 2025 17:58:56 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 16 Apr 2025 17:58:56 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_VERSION=4.1.0
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 16 Apr 2025 17:58:56 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Apr 2025 17:58:56 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 16 Apr 2025 17:58:56 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 16 Apr 2025 17:58:56 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 16 Apr 2025 17:58:56 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Apr 2025 17:58:56 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 16 Apr 2025 17:58:56 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:34560582cc6246fb88c88648a1db5ef09d8b65d143991211ba2abe7378aee811`  
		Last Modified: Tue, 08 Apr 2025 11:53:53 GMT  
		Size: 26.8 MB (26837532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ae971573d856036122f6022328e6e93cd599c8ce3ffa442babc1cacd91ffae`  
		Last Modified: Thu, 17 Apr 2025 18:32:06 GMT  
		Size: 33.3 MB (33279601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0cb2c9936b092c383409e18fbb8e623733b8de6a582e549a4822b3b607460b`  
		Last Modified: Thu, 17 Apr 2025 18:32:05 GMT  
		Size: 6.7 MB (6670891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3104fac498baae3b8bfc305a40f853ad7ee1f3b6bd101456a5cacf8e04bee7d2`  
		Last Modified: Thu, 17 Apr 2025 18:32:04 GMT  
		Size: 9.5 KB (9546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973e9446c21f4dd3c1e554542ee3ddb69c52bc0ec53f55d049f83fb663ac7a5c`  
		Last Modified: Thu, 17 Apr 2025 18:32:06 GMT  
		Size: 30.9 MB (30918669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538fe72604399207a1ff161670c07387fc5db6e5a10e740eb520b1228f563dd1`  
		Last Modified: Thu, 17 Apr 2025 18:32:05 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c478b363828fe64a685cfb1ed6b849ff2ca6cd61df54eefb6993a19547ab5632`  
		Last Modified: Thu, 17 Apr 2025 18:32:06 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d840e5b6616d0f6e44288c5cb147ef4376fe7a4fb367cfab8ac5b207cec469`  
		Last Modified: Thu, 17 Apr 2025 18:32:07 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b69d204efb5e799202abef5c9dd4bcaae0fb3ea3a28bee79ee4925296305cdc`  
		Last Modified: Thu, 17 Apr 2025 18:32:07 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4eb1834536b2d930ee7d30ba5d60275cb6566c310823c87c8e0f8540f22eac83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17655929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9def251fd4d598e8a2eb73b8bfee09e53ae49dc450f01e027d3c17341f503fce`

```dockerfile
```

-	Layers:
	-	`sha256:5a3082a87ee24dfa7dd7105d2abc59c486aa984b099c847871141d82d35e49bc`  
		Last Modified: Thu, 17 Apr 2025 18:32:04 GMT  
		Size: 2.4 MB (2367680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06f49a8bda0994821aa38a0714f063ef163629edde14a81675655564edf5a525`  
		Last Modified: Thu, 17 Apr 2025 18:32:05 GMT  
		Size: 5.0 MB (5024263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4d7b67d5b2cfc0a8359a531d6a7ff100027f01b28e06243761aac71bdbbe537`  
		Last Modified: Thu, 17 Apr 2025 18:32:05 GMT  
		Size: 5.2 MB (5177961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dcc27140a3ed81abf1e76ed19f732f2ff62cd6dd9dc04464cc4d67c187f6b97`  
		Last Modified: Thu, 17 Apr 2025 18:32:05 GMT  
		Size: 5.0 MB (5026005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:823e7667d490a3a412236f7b75cf72173007db196741588f9b8fb1c6ec9c7db0`  
		Last Modified: Thu, 17 Apr 2025 18:32:06 GMT  
		Size: 60.0 KB (60020 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:dbb509f2b2b119733046aeef4a313581728df8257c6f8506d35632234ffcd7d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113058495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1149daa162050a312a0f883ec6018f3481d1ba62ab0dd3642330f34344551e33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 17:58:56 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 16 Apr 2025 17:58:56 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 16 Apr 2025 17:58:56 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 16 Apr 2025 17:58:56 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_VERSION=4.1.0
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 16 Apr 2025 17:58:56 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Apr 2025 17:58:56 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 16 Apr 2025 17:58:56 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 16 Apr 2025 17:58:56 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 16 Apr 2025 17:58:56 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Apr 2025 17:58:56 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 16 Apr 2025 17:58:56 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10838f41ce74181f3dff58782e2f752271df01cebc0e1da76adc921e47a6aea7`  
		Last Modified: Thu, 17 Apr 2025 18:30:40 GMT  
		Size: 44.3 MB (44332051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4e20e47be92e51ea9d218c9f45aee6b6eca6594903924c212c66cda91e6ad`  
		Last Modified: Thu, 17 Apr 2025 18:30:39 GMT  
		Size: 8.9 MB (8943267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34784bf8e462c67fbde36da4ebc50bdfa7510803e2bb1dbe4e001e8c710a4e10`  
		Last Modified: Thu, 17 Apr 2025 18:30:38 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d05a3fed0467ea1ba59411bb22b65dc5c4d3cb03a2937dc8fc14f25c74054e6`  
		Last Modified: Thu, 17 Apr 2025 18:30:40 GMT  
		Size: 30.9 MB (30925046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d28712c126112e29d855d652d35367436567aa30a0e49affd2426cdf1df80d0`  
		Last Modified: Thu, 17 Apr 2025 18:30:39 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea81af84b74c6bab7f96396c35af1d139465a647948ff54379a6026c8644c8`  
		Last Modified: Thu, 17 Apr 2025 18:30:41 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128dde520023ab435e3dc5c9544bafdc6f8c62af97f797916339738bdd590777`  
		Last Modified: Thu, 17 Apr 2025 18:30:41 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc377e32dbeea8cc183340c7ff3947cb8978b7da989dc53987d167383413a687`  
		Last Modified: Thu, 17 Apr 2025 18:30:42 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:69a88d38c4a2743e2cc22e9013a20dd0a69b4e520944262145477e94a7b58619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18253792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f5fc3555536b758e6375fb3193ce751421a89f0d23a2085921e3bb9e4194dd`

```dockerfile
```

-	Layers:
	-	`sha256:b0deacf467f9dd4144a9d21e421688552f6266952892f3eb3060dcebaab5a557`  
		Last Modified: Thu, 17 Apr 2025 18:30:39 GMT  
		Size: 2.4 MB (2367936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f06a839dbac583d681ed32ff9972762136b5f03f29a6c73e996e8804ff90758`  
		Last Modified: Thu, 17 Apr 2025 18:30:39 GMT  
		Size: 5.2 MB (5222595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1097cc89fd322c9768800cf3b8dd9266b9a7f68109fdbda1f4a99d99277430d2`  
		Last Modified: Thu, 17 Apr 2025 18:30:39 GMT  
		Size: 5.4 MB (5378858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:878260efb07e21e231120a4eee96c5c37dbdbb754aa476b4753ef9b84fa80924`  
		Last Modified: Thu, 17 Apr 2025 18:30:39 GMT  
		Size: 5.2 MB (5224337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d004a6d8423a1be2b573322435ec20826f0742d30c08ee124c71ef71a0044524`  
		Last Modified: Thu, 17 Apr 2025 18:30:40 GMT  
		Size: 60.1 KB (60066 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:d4afbd54cc99ccbf5b21746ce7bc8a30c50ae546e49efe8d772a8d234e08c262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113505458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5faee4ba74dc3655e68144007aab4f13246f543abe0f44d5ef3723b398a690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 17:58:56 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 16 Apr 2025 17:58:56 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 16 Apr 2025 17:58:56 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 16 Apr 2025 17:58:56 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_VERSION=4.1.0
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 16 Apr 2025 17:58:56 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Apr 2025 17:58:56 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 16 Apr 2025 17:58:56 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 16 Apr 2025 17:58:56 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 16 Apr 2025 17:58:56 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Apr 2025 17:58:56 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 16 Apr 2025 17:58:56 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f1f1051afcd1a357a56e2a2e680c53620c77f88f01d0929a193a71cf8ce6f2`  
		Last Modified: Thu, 17 Apr 2025 18:32:15 GMT  
		Size: 39.5 MB (39479724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a094d73c6f681d80bbc27e35f9801ae35c9a5bdd8bdbc70c0484481205ec6c3a`  
		Last Modified: Thu, 17 Apr 2025 18:32:14 GMT  
		Size: 8.7 MB (8699391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4a56edb9b52814caebce0ae90716f0c557d47d090e4a47e49644e745be301b`  
		Last Modified: Thu, 17 Apr 2025 18:32:13 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a653adc940b6fc361d89b8ef669f660dd6fc784ac9b385cf2e62c9bb41f0f3`  
		Last Modified: Thu, 17 Apr 2025 18:32:15 GMT  
		Size: 31.0 MB (30974325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d30a0b1a5764c3b70e77a0c9ef7fa55e0d483082547067eefe14f9ed3d9f8d`  
		Last Modified: Thu, 17 Apr 2025 18:32:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4029afb8fdd565313e65915cf0b562fadb0ad78e6db30b01f4e47ef40873ae8e`  
		Last Modified: Thu, 17 Apr 2025 18:32:17 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a5e259af6f3c1488ce89bf4b5381d176c81e8f2bbcf958f4aba5423a336646`  
		Last Modified: Thu, 17 Apr 2025 18:32:16 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6598256bd23670e8bb632c46afa505451bf886b87d10d6c5cd95ada70e0f11d4`  
		Last Modified: Thu, 17 Apr 2025 18:32:17 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ca629cc2a7a94e3d1b77af47b4dec41c77f07814bf3a599d9c4d6f1b1a8b3997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18110264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475b3638d3c40f5b2e03d05522a7815bee110db8c7d0a377cbdcd59627829709`

```dockerfile
```

-	Layers:
	-	`sha256:9290a5a9967ff5be37bc1e41f826671b2c323993f48ba3db405184e9a60cff35`  
		Last Modified: Thu, 17 Apr 2025 18:32:13 GMT  
		Size: 2.4 MB (2371231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ae73052ee464b8cab58503b331dd406adbf107f06dc1446cfae37d9f4a4e488`  
		Last Modified: Thu, 17 Apr 2025 18:32:17 GMT  
		Size: 5.2 MB (5173709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7891835fe3bf4b755a14dabd825bcba19cc154366a08f1a05d8e21237cf65944`  
		Last Modified: Thu, 17 Apr 2025 18:32:14 GMT  
		Size: 5.3 MB (5329984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dba00e515382ad80bae524d993964e54f9fd9b349c6bf25f65284f5a3bc1dff4`  
		Last Modified: Thu, 17 Apr 2025 18:32:14 GMT  
		Size: 5.2 MB (5175451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f9601dea4979f2cd1f7fe82d677cc83101fad199e6c2d59406751609377e65e`  
		Last Modified: Thu, 17 Apr 2025 18:32:16 GMT  
		Size: 59.9 KB (59889 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:f18370fc6757b2c94788c2b8b0be974872920c7fb5ccbd38616c655ce07174df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106800849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde5b16a5a43c10c13f022a0eef0a8424a58318251eb45544ac1f0be371aa189`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 08 Apr 2025 11:16:50 GMT
ARG RELEASE
# Tue, 08 Apr 2025 11:16:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 11:16:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 11:16:51 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 11:17:29 GMT
ADD file:ef7c97f5dd8d665aae899afe52c54f7acaf71fa51e9d7f26e13ed6073141c666 in / 
# Tue, 08 Apr 2025 11:17:31 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 15 Apr 2025 17:26:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_VERSION=4.1.0
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 15 Apr 2025 17:26:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 15 Apr 2025 17:26:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:ba2f284f7444fb0b78fa804d74c44dee4b397610267539e4a6e9c41ae41e06a1`  
		Last Modified: Tue, 08 Apr 2025 11:54:06 GMT  
		Size: 30.9 MB (30943202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cdbd868cc1adc61328d67614839fa18450a921df3252989bd14ec77ec87008`  
		Last Modified: Wed, 09 Apr 2025 07:14:19 GMT  
		Size: 35.1 MB (35128410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8c6de69198d0d40e4ba20190ce9009e900d7e1eb1af51c0d3a540a62a207bf`  
		Last Modified: Wed, 09 Apr 2025 07:14:15 GMT  
		Size: 9.8 MB (9789666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cb4ca09dc366fa63314e988f583aaf21a9b21db831297d8186593ff9595d29`  
		Last Modified: Wed, 09 Apr 2025 07:14:12 GMT  
		Size: 9.5 KB (9473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006bc319611428e7a11bfd0a0b9348e561666ec950fad039b820ef10ee14da33`  
		Last Modified: Tue, 15 Apr 2025 22:09:30 GMT  
		Size: 30.9 MB (30928350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0f625112680bb993a8cc6659c38e207774c086222d1c82b9b6e32d9ae11ca9`  
		Last Modified: Tue, 15 Apr 2025 22:09:25 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68d5ab49bcaf3302dc8edf02b7c4703b9fb960f613daa05ffeeb8debe41673`  
		Last Modified: Tue, 15 Apr 2025 22:09:25 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6adf6baf052188b321b4b6ab6ba0d5af8ca5875d979ef1910dcc2c930f0231`  
		Last Modified: Tue, 15 Apr 2025 22:09:25 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6deb30df57639abb0d80bd23a7e92a1a9d02e34e3c1a44fe09cb468a4262ac8d`  
		Last Modified: Tue, 15 Apr 2025 22:09:26 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:698147c675d83d4f16bcce7681a08378c81cf70ce993aef567dff8d851e649da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18083874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35741052d8103174714bd39025d0f4743578da318db202e7fe879373d9e26506`

```dockerfile
```

-	Layers:
	-	`sha256:5df5b32ca73dde09f7b5a4acc49c32ddd21d91f8e6b22874fddf7f1cfbc4330e`  
		Last Modified: Tue, 15 Apr 2025 22:09:25 GMT  
		Size: 2.4 MB (2359441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:856590e32f4c843e50dae8c9d07ce685e9aa1bf9c1a7c9c0b0b4800131b4994a`  
		Last Modified: Tue, 15 Apr 2025 22:09:26 GMT  
		Size: 5.2 MB (5169702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89cb5d3e8d1215cc96c43463976481a9a265ee01a20ee7217a6f668ce75df078`  
		Last Modified: Tue, 15 Apr 2025 22:09:26 GMT  
		Size: 5.3 MB (5323398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66fc720accc6d2441dce3c3f391790e79b26d20447a63bea3de7739d1c8bd4c3`  
		Last Modified: Tue, 15 Apr 2025 22:09:26 GMT  
		Size: 5.2 MB (5171444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db888d36e456b246c6ad28d351db5ae39a33b10230c22b07a67af266157f198`  
		Last Modified: Tue, 15 Apr 2025 22:09:26 GMT  
		Size: 59.9 KB (59889 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:6363cfab16043c2c73b046639d2a605752d5c4fe8fc1a825145a31f97b886a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107079616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d1b48d79921a7215f54d254356ab129e2bb0e9c60fec8c7496d077b02125b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:29 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:29 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:30 GMT
ADD file:8f287f40ca940c9bd87c8706751f5f1c5bbd0a83fd75f7d938832b226fdb936d in / 
# Tue, 08 Apr 2025 10:46:30 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 17:58:56 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 16 Apr 2025 17:58:56 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 16 Apr 2025 17:58:56 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 16 Apr 2025 17:58:56 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_VERSION=4.1.0
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 16 Apr 2025 17:58:56 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 16 Apr 2025 17:58:56 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Apr 2025 17:58:56 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 16 Apr 2025 17:58:56 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 16 Apr 2025 17:58:56 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 16 Apr 2025 17:58:56 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Apr 2025 17:58:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Apr 2025 17:58:56 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 16 Apr 2025 17:58:56 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:e5722f32c6281fa87f1e5f7ebe307864b50aa95a116496a205ce47478bc9b52c`  
		Last Modified: Tue, 08 Apr 2025 11:54:12 GMT  
		Size: 30.0 MB (29956206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589d5d235db0796b353cb3e951e47530ba8664be14919370f8503c4c5da8ba60`  
		Last Modified: Thu, 17 Apr 2025 18:35:21 GMT  
		Size: 38.6 MB (38560963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6318ad2990e6afa6e2bd1eb89e0c7cb5598bad7ba48fe3580ae7552e5c0d465`  
		Last Modified: Thu, 17 Apr 2025 18:35:21 GMT  
		Size: 7.6 MB (7552002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7852eedca1a3ddf569b964f4a9386ab0bf0f8a4fd8dda081f52be9df72b76a`  
		Last Modified: Thu, 17 Apr 2025 18:35:20 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47392f0e2db5bb880624b345459fdf9e26d8503e6d814ac48568d02c55860d8c`  
		Last Modified: Thu, 17 Apr 2025 18:35:23 GMT  
		Size: 31.0 MB (30999073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169a78c09cab9345967d8c2259d485df4dffbfec95fd956895deea91614e7c85`  
		Last Modified: Thu, 17 Apr 2025 18:35:21 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3e01b5a9b82ba7eb39a694680ce2418d9d91ff1f2f9944ac2f67ae422d3982`  
		Last Modified: Thu, 17 Apr 2025 18:35:22 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064d539dfe9bea920aece586e6f01f2f68d658d2ec05488a2a8d0229f9904fe9`  
		Last Modified: Thu, 17 Apr 2025 18:35:23 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fac6873e5605395cdfeba4c348afdd5086d803ea1f5b3d8e14b26630b5edfad`  
		Last Modified: Thu, 17 Apr 2025 18:35:23 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a388abf5e8b0d517b46b8fb0556c246e4f0cabe8730adc4550eb785cb9964f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17740227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de74c41d8b5541a2134f35c2e8d54ffe8a67fed879d9431cff25186af02ab2e`

```dockerfile
```

-	Layers:
	-	`sha256:21a3ed265181bd98c005f8208f3ed446c1c380318838cd8329c568600af00b53`  
		Last Modified: Thu, 17 Apr 2025 18:35:20 GMT  
		Size: 2.4 MB (2368988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7415ed573eb7c92a37d23d60e7daf91493cdc7cc02d60df5770531ddf4d31bf2`  
		Last Modified: Thu, 17 Apr 2025 18:35:21 GMT  
		Size: 5.1 MB (5051575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7a8207ff11859a4faaa7e6729bb36e729d1b99d7cf5b80ac0f4127816a96260`  
		Last Modified: Thu, 17 Apr 2025 18:35:21 GMT  
		Size: 5.2 MB (5206520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7be3ea58e74f2abdd3f312bf56024cbc0dbccab302996a574ac46198acc7360e`  
		Last Modified: Thu, 17 Apr 2025 18:35:21 GMT  
		Size: 5.1 MB (5053317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8778629d725317fca31f80c500cffddc6e1a15733c27f0deb9ae2b7d8024c58`  
		Last Modified: Thu, 17 Apr 2025 18:35:22 GMT  
		Size: 59.8 KB (59827 bytes)  
		MIME: application/vnd.in-toto+json
