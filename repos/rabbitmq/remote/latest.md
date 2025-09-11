## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:1066d7aecf893169211df5f292793fde5e414771fd2c647dbb8f2a2df2360f61
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
$ docker pull rabbitmq@sha256:f458282b733b3f4cbc2a8a7c8283e4d7b0dfe739544179c74986eafc3745a62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93949811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cee28338c6818a675d85d18c03836ee2fd7bb9f7ec3cdcbbda2d6805ca3c176`
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
	-	`sha256:4e823e9332188e662391782d0d87ba101759880efca7a17d9a5a20e8906cc8d7`  
		Last Modified: Tue, 19 Aug 2025 17:59:44 GMT  
		Size: 26.9 MB (26851104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fea7d20dbddf6529ca1f35ea447c030222d6be11faa30e3b5a6015aed30650`  
		Last Modified: Thu, 11 Sep 2025 04:47:57 GMT  
		Size: 33.3 MB (33277652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480ca83541230fca30386aaf05ca9ca540ec001ebf157b69a5339bfc54ecfd71`  
		Last Modified: Thu, 11 Sep 2025 04:47:52 GMT  
		Size: 6.7 MB (6670171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f17734ad58d61d344ce75d8c2bd7786c8a30921a45122b877e69643596b267`  
		Last Modified: Thu, 11 Sep 2025 04:47:52 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a357490951387fda87359a5b006f917beda9dc6a13f57a4061429badb28a629`  
		Last Modified: Thu, 11 Sep 2025 04:49:00 GMT  
		Size: 27.1 MB (27139594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4826936d5c900cc93b26eac60bd4192e95f3cc8f1ca6c44a8dc38601188aea`  
		Last Modified: Thu, 11 Sep 2025 04:48:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff97d7ff4212997dfbfca0ec3dae6ba25ede7f90774cccc265427d3edc31b65`  
		Last Modified: Thu, 11 Sep 2025 04:48:57 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad18d3144028a085eb104b8c3cccdee41ac210ce44ae804d40901c04dbd924c`  
		Last Modified: Thu, 11 Sep 2025 04:48:57 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbbefd9d213f51eb9ee2ca288b5102176455fba2c5e5bdee2be470c0daa4b09`  
		Last Modified: Thu, 11 Sep 2025 04:48:57 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8696fd4287b2de105fcebc0c5c09cb04f654985f541178f20ac4d2e6e251e975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18292065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bb6ac5617c04603d3065b0c2dd778c611863c8c21cb090da8e35465ea4a47b`

```dockerfile
```

-	Layers:
	-	`sha256:f70486278a5245d65b4042fec8f84270ac2b5deee846a639383eba7311f27d39`  
		Last Modified: Thu, 11 Sep 2025 06:53:03 GMT  
		Size: 2.5 MB (2484740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:424e511fa6c1f9873687dd34ddae45100d25d9f977b4b11f4e85d597f10e05de`  
		Last Modified: Thu, 11 Sep 2025 06:53:04 GMT  
		Size: 5.2 MB (5197165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b708d2858b7a1ed603d56af47bbae22df36bdb4f95ba3f17af698a1d61a00c`  
		Last Modified: Thu, 11 Sep 2025 06:53:05 GMT  
		Size: 5.4 MB (5351215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de154d98d67dcb3513458a46e0bf7d16f9f8b34dd9c65375b4ab60f1f8cacfb3`  
		Last Modified: Thu, 11 Sep 2025 06:53:09 GMT  
		Size: 5.2 MB (5198907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6100dfc853a952aa2a08d265cb34588b6408af8ead27e2625461972d85b1c50`  
		Last Modified: Thu, 11 Sep 2025 06:53:10 GMT  
		Size: 60.0 KB (60038 bytes)  
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
$ docker pull rabbitmq@sha256:6b092cea76a5318dfc268f764014da4d3a89e3941ded0e38d3d76264da50dddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103289078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3855cd384980f7240d7cb4719a2664146958c370c477db6d98ab2e07c773167`
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
	-	`sha256:80a64b6a7d961af355cc1a24ce954958de51e8bc2fb336684c1fbec689663c29`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 29.9 MB (29933009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2314092146e4a442155946234640fd6fa4963d47d21d0fe9dca444df67b32390`  
		Last Modified: Thu, 11 Sep 2025 00:34:33 GMT  
		Size: 38.6 MB (38569490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646f6346900107a014a1f9ccedcc0aaa711d4b8ba838a0a6083b4ae881b004d9`  
		Last Modified: Thu, 11 Sep 2025 00:34:29 GMT  
		Size: 7.6 MB (7555907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3057b2abe099bab9a6364d4c2e4f505a178f316865f8d6685c6f2b1722f5f7e9`  
		Last Modified: Thu, 11 Sep 2025 00:34:29 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0710cab1839057730912401e95215eff5466fe8cb9832420eb0e7d544ed867a`  
		Last Modified: Thu, 11 Sep 2025 00:45:00 GMT  
		Size: 27.2 MB (27219335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9ea1c2d11c416d33d5eded53759e5715bf2a734b246feb200ad142406d6b63`  
		Last Modified: Thu, 11 Sep 2025 00:44:56 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3e1a39a82b6cc84aeb2eebff66241b97c49834dbe4f2bc3d7e8da47e856763`  
		Last Modified: Thu, 11 Sep 2025 00:44:56 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815f87e14c935f782d35ba6255d96d5770659fa80cad7d3f2390df16842d8766`  
		Last Modified: Thu, 11 Sep 2025 00:44:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29138cc2c5c425fda37aa2533bf945816332c26ed41b768ffeb141fe650b06e1`  
		Last Modified: Thu, 11 Sep 2025 00:44:57 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e4aa5940e8d9b32dd177e38f6f4f73902615e8941144e52865e5b7078cda8d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18377430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe0f196c2b3d373aa2a87b7209dfbaafbca6cc174523b78aa705397ead4d361`

```dockerfile
```

-	Layers:
	-	`sha256:013f32275baf2ac4e2f2be617c2412861ce5a49888edcaeb97730aa393bd8242`  
		Last Modified: Thu, 11 Sep 2025 03:54:14 GMT  
		Size: 2.5 MB (2486050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f99dcc92fd7ae819c08cd9c47ba2c6a53935e0fd3434359f35a491911605b1e`  
		Last Modified: Thu, 11 Sep 2025 03:54:16 GMT  
		Size: 5.2 MB (5224832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50ead28ebaab0f6c44d736c988cf957a7fd999f11cdf146e773c918820da9ee5`  
		Last Modified: Thu, 11 Sep 2025 03:54:17 GMT  
		Size: 5.4 MB (5380133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f75e29b286585b5750feaf05c0a2d27fd9b1f26db206e4c0ca642fe113b686c7`  
		Last Modified: Thu, 11 Sep 2025 03:54:18 GMT  
		Size: 5.2 MB (5226574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3937ce435af30a3de47d7885d6c9d01f47c02b98be12def910e24c5bca2f290a`  
		Last Modified: Thu, 11 Sep 2025 03:54:19 GMT  
		Size: 59.8 KB (59841 bytes)  
		MIME: application/vnd.in-toto+json
