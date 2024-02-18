## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:556d69518f4fb4d457645f1ba7b6bf74e0661c26cf9a6f538da6cca1572f1c28
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
$ docker pull rabbitmq@sha256:39b5b95ec9b8e65590c9b4b575c2d66ea97d43ccd77d9a7f1f3a4a8d2d40b1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102129572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80099828f6f4ea9fa40bc7ef9370c7df3608fab4aac6d05fde874e4abe4c654`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:05:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 16 Feb 2024 06:05:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 16 Feb 2024 06:05:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.9","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.9?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 16 Feb 2024 06:05:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_VERSION=3.12.13
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Feb 2024 06:05:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 06:05:28 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.13","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.13?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 16 Feb 2024 06:05:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 16 Feb 2024 06:05:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 06:05:28 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 06:05:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 16 Feb 2024 06:05:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:01007420e9b005dc14a8c8b0f996a2ad8e0d4af6c3d01e62f123be14fe48eec7`  
		Last Modified: Tue, 13 Feb 2024 10:22:22 GMT  
		Size: 29.5 MB (29536188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36f9c24dfac1f00d88e372952b880682f5e4b17f3da67c2f97cb4cf987d3ee3`  
		Last Modified: Fri, 16 Feb 2024 19:57:25 GMT  
		Size: 44.5 MB (44469457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9e77bbd5ae0d1c8ebd10fc7195764dfaa4ac83175d236b2d7666e402d92de2`  
		Last Modified: Fri, 16 Feb 2024 19:57:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57791f73483d8ca74414ee0058d31c557287e20db9403e08d7bf3f5afbaf644b`  
		Last Modified: Fri, 16 Feb 2024 19:57:24 GMT  
		Size: 7.5 MB (7473467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6747ece6f2256a656c79fbcdfc84617b9e0be13c9c30b81753ff45113671f23f`  
		Last Modified: Fri, 16 Feb 2024 19:57:24 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2058f40ddfd77858df42603d6118dcec2cee62c3f35dccfb9354e4171b5b44a`  
		Last Modified: Fri, 16 Feb 2024 19:57:25 GMT  
		Size: 10.7 KB (10717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e7700ef02b19e7c26d2a502847c0904faf39cb8ef04cadbe7e32380d5da284`  
		Last Modified: Fri, 16 Feb 2024 19:57:25 GMT  
		Size: 20.6 MB (20637210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3513f51346f7a4bf6a395cd67ec179816c5ec634606aa49be9c616f25b12b9d8`  
		Last Modified: Fri, 16 Feb 2024 19:57:25 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e213fb40f853e51e979ee1baa15e52a065bb05fd5e561075b3812135731f3060`  
		Last Modified: Fri, 16 Feb 2024 19:57:26 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae48820b29ec14ad6dbfb9025fa123cc108d20c949b21aacd278418f247ca0ad`  
		Last Modified: Fri, 16 Feb 2024 19:57:26 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14842ccb66bacb0a7661c45e0ffc825d81671e2fcae373454ac1bc2cdfdf3cee`  
		Last Modified: Fri, 16 Feb 2024 19:57:26 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ac8c23ebab4747eba9d00bf8daa67053e704c62f1dbd996386c2e5a929733b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18573748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4e072828ad0ff1d3a730b354c3e38a8ebf653139033e3a75793e6f07515eb3`

```dockerfile
```

-	Layers:
	-	`sha256:680a95fcca522242a3b21cc58dc6a5b7f888ef7dbba22f97653e358a5b94e25f`  
		Last Modified: Fri, 16 Feb 2024 19:57:24 GMT  
		Size: 2.9 MB (2880004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2fb3e86dc23ba45a7e0bd8e38c034e20d5804aff0a3ed556277ef7506906ce5`  
		Last Modified: Fri, 16 Feb 2024 19:57:24 GMT  
		Size: 5.2 MB (5160634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3b4c04fa875cdbb6c8766633e0037ebdc2738ac8f736858143a93277ebf2622`  
		Last Modified: Fri, 16 Feb 2024 19:57:24 GMT  
		Size: 5.3 MB (5301990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e41e49a63ee1b77a897426830e7bfa3fea088fe20b9029c196dd65b79cc35027`  
		Last Modified: Fri, 16 Feb 2024 19:57:24 GMT  
		Size: 5.2 MB (5162008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfac446b94adc1c6d3a0968be2be66297c956663c24565e0b72358f90b99cb82`  
		Last Modified: Fri, 16 Feb 2024 19:57:25 GMT  
		Size: 69.1 KB (69112 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:d5e3d0fe6430de5bc70aad1e4e2976674aa723721051e7bc166563488c4ad507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86034898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7e44666643bdd494250de35c679307a1d5c6757bac954f7b1533e551dff9ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:00 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:20 GMT
ADD file:6767efafdb51cef2acde13d723fa618ffb3cd2155983115496c43ae730e762e6 in / 
# Tue, 13 Feb 2024 10:08:21 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:05:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 16 Feb 2024 06:05:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 16 Feb 2024 06:05:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.9","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.9?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 16 Feb 2024 06:05:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_VERSION=3.12.13
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Feb 2024 06:05:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 06:05:28 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.13","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.13?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 16 Feb 2024 06:05:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 16 Feb 2024 06:05:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 06:05:28 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 06:05:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 16 Feb 2024 06:05:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c600ef85012d74e6f7cd7bd4158f722dfa9c8e13439ef794a365d3147011453f`  
		Last Modified: Tue, 13 Feb 2024 10:22:34 GMT  
		Size: 26.6 MB (26638123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba343c138b8d3194a2daabb2a26d07eae08e0aa951c1635db4e5eb6d9714dda`  
		Last Modified: Sat, 17 Feb 2024 07:44:22 GMT  
		Size: 32.8 MB (32754806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed936f0c0a1d1036d0c01007c63fbe72e562e1211b53c7f13741a97677c9c89`  
		Last Modified: Sat, 17 Feb 2024 07:44:21 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288dcadb5aa2484c4441bffe0da678be69522b326de895b33f147fc496ba460f`  
		Last Modified: Sat, 17 Feb 2024 07:44:22 GMT  
		Size: 6.1 MB (6072554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7438324c3e5d67653fbbea71957a292c1a8c745e2e39c5ff607ebf06c85db171`  
		Last Modified: Sat, 17 Feb 2024 07:44:21 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0f9d4762a1c6f91830f3db6a8d4e31317f948663c3d6d7ba3458719d553114`  
		Last Modified: Sat, 17 Feb 2024 07:44:22 GMT  
		Size: 10.7 KB (10740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecfe45a9c97d9022307399565c43822319e3ebb3874efabcd5e3135c4ceec5a`  
		Last Modified: Sat, 17 Feb 2024 07:44:24 GMT  
		Size: 20.6 MB (20556148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bd06d081a31dd5c80c3964dfcb99ca6f27faaa00240912f33482e2f981191d`  
		Last Modified: Sat, 17 Feb 2024 07:44:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5691a5dc8853306cf88d3dd9f1ce984b426c763c17036703435fce46e998a96`  
		Last Modified: Sat, 17 Feb 2024 07:44:23 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd23d4dc6bb7ce1c8e5b1ababa40011ec7f059ab16dd610a2cd50684674d8f86`  
		Last Modified: Sat, 17 Feb 2024 07:44:24 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84aca0025983776466464be81ac6a5c9ba49e567ca01b3d6862403e292b1cab3`  
		Last Modified: Sat, 17 Feb 2024 07:44:24 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5bc25f75b2cd589634ca2047b349e1865bf9ce53943e03292f82da6d6e8291ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18031305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e735bc45d8dabe4c85126b4c8b381f40bc5359b756f4ad3753725240fcf8b7`

```dockerfile
```

-	Layers:
	-	`sha256:4d9091e467f8259a3b5632c0da3255d0fcffbacde0ac052616737b1d90f8580b`  
		Last Modified: Sat, 17 Feb 2024 07:44:22 GMT  
		Size: 2.9 MB (2881299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aba4739c51fbdb2b0658c21db8abae4ad3ba1a0c7e83c36ac54474c12f6b55c2`  
		Last Modified: Sat, 17 Feb 2024 07:44:22 GMT  
		Size: 5.0 MB (4979787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9c4c2e6c1c32113d1c1ce94883cc6771c0f4b92ff557764bc0d7c91c9fe23d7`  
		Last Modified: Sat, 17 Feb 2024 07:44:22 GMT  
		Size: 5.1 MB (5119733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b8daf025fa160af492c2361724d67799c5b8cd360ae9be495f262ef6bbf47b`  
		Last Modified: Sat, 17 Feb 2024 07:44:22 GMT  
		Size: 5.0 MB (4981161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14fb871160756a6412489304edf4cbb22c59b7d56295700cc729774278a9ad0e`  
		Last Modified: Sat, 17 Feb 2024 07:44:23 GMT  
		Size: 69.3 KB (69325 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:9be8d9bb4fab3063ac612ccc4fafe57873e7976ea1bc62efe790a89bdf13999d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97366473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9499f7c60eebf71aaadcb8806009ce9801f147bcc856445a1f5e8eeeb67828`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:05:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 16 Feb 2024 06:05:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 16 Feb 2024 06:05:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.9","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.9?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 16 Feb 2024 06:05:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_VERSION=3.12.13
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Feb 2024 06:05:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 06:05:28 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.13","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.13?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 16 Feb 2024 06:05:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 16 Feb 2024 06:05:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 06:05:28 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 06:05:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 16 Feb 2024 06:05:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:a4a2c7a57ed8b997579870d0927433b03cfd94f5dba2153bdbcd885b5d620035`  
		Last Modified: Tue, 13 Feb 2024 10:22:28 GMT  
		Size: 27.4 MB (27356877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e166cb5d21fa9bb70e05e3f481245439473df2a5c94e5f118f0300e5f8bf0192`  
		Last Modified: Fri, 16 Feb 2024 19:02:45 GMT  
		Size: 42.3 MB (42317548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5835e405dcddf2b6160f3a317ae38295aa8f7e62623efd9bc3792990cf0e5ef9`  
		Last Modified: Fri, 16 Feb 2024 19:02:44 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a382aac7117ea6faa65c80e7f19d3881febeeacf4819468f152bf3e5923443`  
		Last Modified: Fri, 16 Feb 2024 19:02:44 GMT  
		Size: 7.1 MB (7130275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ad4a542db0f14af882fa1fe5d773469e5bed195bb6d0bee47f9c95f9f8d794`  
		Last Modified: Fri, 16 Feb 2024 19:02:43 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76af14eead852a9d5d0c6eedf31df8dd69cd7dab18af4d8af7469340ae39e57c`  
		Last Modified: Fri, 16 Feb 2024 19:02:45 GMT  
		Size: 10.7 KB (10705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec38e2087c84a9b0d3631cadd80bd0916dbd1ba0be6ed2d265f9a7a1df60a1f5`  
		Last Modified: Fri, 16 Feb 2024 21:08:46 GMT  
		Size: 20.5 MB (20548537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e199ff8101e3067795d4eb921896a115b92c6b9fdb1a8e9a7b66d4902de5c00`  
		Last Modified: Fri, 16 Feb 2024 21:08:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8328254f46c574b88469a5bf9df3eed6d80871789c8e36f4c02ca605b35cc369`  
		Last Modified: Fri, 16 Feb 2024 21:08:43 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483e0b1189684fe080fa4332c30bd65bfe60a73b71c361c71ec7957443dc3fa4`  
		Last Modified: Fri, 16 Feb 2024 21:08:43 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4ffc3adefa582139785d177459ad0f5aae21c7623dc2bafd8d7da7f1a186d9`  
		Last Modified: Fri, 16 Feb 2024 21:08:44 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:aaf58293e402e8e2a039ad956d75626c15dbf51dce561579ca94e32e6677401b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18561277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24fe36cffb9c154894770afb5ba558c9a6eb391073edc847f9c6c666db878a5`

```dockerfile
```

-	Layers:
	-	`sha256:1196bdd06179e7bb5f295d262388bb20c84628c5eda6bc302e20b46a726b274e`  
		Last Modified: Fri, 16 Feb 2024 21:08:44 GMT  
		Size: 2.9 MB (2880231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a43596d4d2175587127967958d2ec4096e3ce3b1fe8335c4a6c1a99350e86ed`  
		Last Modified: Fri, 16 Feb 2024 21:08:44 GMT  
		Size: 5.2 MB (5156450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1fb5e4cd99c6333a02f8038cf0d1c67b4bb59f85db5fc572bac651f202c3da4`  
		Last Modified: Fri, 16 Feb 2024 21:08:44 GMT  
		Size: 5.3 MB (5297812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9128a8808ba4994a6c0d3aaf9c18f41b22a5dd5185a7b9ed1fac681ab3a50aad`  
		Last Modified: Fri, 16 Feb 2024 21:08:44 GMT  
		Size: 5.2 MB (5157824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2389f7a0496c4480f6607c19ff3dd210e4d2a02b6cecc01d6532774f96e61b22`  
		Last Modified: Fri, 16 Feb 2024 21:08:45 GMT  
		Size: 69.0 KB (68960 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:070032d7717590a5e0f0a564792eab347754250e57de8bf481d6ebedfd5849bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101734855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98645bcd314ed4e63e8d35b893ed1b1b1aeb174d6e68620dcb0f87927d2320b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:05:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 16 Feb 2024 06:05:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 16 Feb 2024 06:05:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.9","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.9?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 16 Feb 2024 06:05:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_VERSION=3.12.13
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Feb 2024 06:05:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 06:05:28 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.13","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.13?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 16 Feb 2024 06:05:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 16 Feb 2024 06:05:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 06:05:28 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 06:05:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 16 Feb 2024 06:05:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4aad68167a35c53ced5a1c04f1766357ff1b620dec9d272c01720d4fb0d9558c`  
		Last Modified: Tue, 13 Feb 2024 10:22:40 GMT  
		Size: 34.5 MB (34503224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa7adced8c83ec488f8cfb31362bc60bd0c5a7c929926ee0c9dc32e3bda880b`  
		Last Modified: Fri, 16 Feb 2024 18:52:45 GMT  
		Size: 38.8 MB (38786258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff48afe96b236f97ebff251f4e60df3dc95a23d23d918ec98f858fb137a861cd`  
		Last Modified: Fri, 16 Feb 2024 18:52:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c730c61af476d045832640ddc0e61322861146d06d62918141950e069a1e011`  
		Last Modified: Fri, 16 Feb 2024 18:52:45 GMT  
		Size: 7.9 MB (7857073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994fb40d2f950f12becbe58213cdb0a084684b35614a004ccf13c8f912ca5ebc`  
		Last Modified: Fri, 16 Feb 2024 18:52:44 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b908ae4a36dd2692598c84ec541e2ce0de67c03184a75883e17c13a725e72`  
		Last Modified: Fri, 16 Feb 2024 18:52:45 GMT  
		Size: 10.6 KB (10616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d069a51dde9a4b20aac0332b9c0eb466f1f9c4bb7ffe4ed40820c12e42e64d73`  
		Last Modified: Fri, 16 Feb 2024 20:17:22 GMT  
		Size: 20.6 MB (20575149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e160367a336ad536f06483b22bcfa38a0518a575b0e9950993f04d338b2c0e48`  
		Last Modified: Fri, 16 Feb 2024 20:17:21 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc310f1ad9ae16bc3477bba773a90ed9ea8e5350939307022ef74d338699abb5`  
		Last Modified: Fri, 16 Feb 2024 20:17:22 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6278249c42bf7e62ee9e99fd53a84588d44e2c6565e7b3c895346eab378ff3e2`  
		Last Modified: Fri, 16 Feb 2024 20:17:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ccf6a367bbff6d065620ee0df7f3839d65ff89f8c5a286f81996f77aec04e`  
		Last Modified: Fri, 16 Feb 2024 20:17:27 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cdcab2b68c0fe976c1edb3b3b19fa0ed81ee90d4de3eb6c68db41e9b4db22eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18461559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf79c71853f93eea9ab2803cd84089b31dfce082a9f57f28183bc7c6096c3177`

```dockerfile
```

-	Layers:
	-	`sha256:b952d70c61e5d460ebac29c6f30bc4d2a1172190095240e99a19c876656b579f`  
		Last Modified: Fri, 16 Feb 2024 20:17:21 GMT  
		Size: 2.9 MB (2884393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b47d84d71034ab112787db4feefe1b9efc1427ca75e125f897251489e39f32a`  
		Last Modified: Fri, 16 Feb 2024 20:17:22 GMT  
		Size: 5.1 MB (5121805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4047bd049366e85ff724f830ba496b30baab0004942319c11ea7f5e629cbe80c`  
		Last Modified: Fri, 16 Feb 2024 20:17:21 GMT  
		Size: 5.3 MB (5263171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:978416a2264d70b6116838d69690485b90b8adf00e822302a96641545083dafd`  
		Last Modified: Fri, 16 Feb 2024 20:17:22 GMT  
		Size: 5.1 MB (5123179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a628cc19e074cd9bc7d73eeb4e2ffb90c487ccb5e4b02088454fe111b4f5d7e`  
		Last Modified: Fri, 16 Feb 2024 20:17:23 GMT  
		Size: 69.0 KB (69011 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:296724fea54c91365db1d78d89a284df8437f90e21ffd3bbb2c67be2f2d71731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92612498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df7cda765e4ebb1c2743f9ef837d83e6ec5f751501ae6b5dff9bae5764d60b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Feb 2024 10:05:41 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:05:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:05:43 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 13 Feb 2024 10:05:43 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:05:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 16 Feb 2024 06:05:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 16 Feb 2024 06:05:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.9","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.9?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 16 Feb 2024 06:05:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_VERSION=3.12.13
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Feb 2024 06:05:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Feb 2024 06:05:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 06:05:28 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.13","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.13?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 16 Feb 2024 06:05:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 16 Feb 2024 06:05:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 06:05:28 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Feb 2024 06:05:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 06:05:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 16 Feb 2024 06:05:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8c305036370ece07999393ab52726bcdf8fc6cfdfaecfb9cb60f40ebaecec9e9`  
		Last Modified: Tue, 13 Feb 2024 10:22:46 GMT  
		Size: 28.0 MB (28008375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7fa2b5b2440e7950c578d2d7cb9c55dbdecb799af08c39f99e8c03ee4d8162`  
		Last Modified: Sat, 17 Feb 2024 07:29:43 GMT  
		Size: 37.5 MB (37461398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7f303b18b7f27ed94e036500363371ac36e1aa8e8008ba75781bce3ce7a1ae`  
		Last Modified: Sat, 17 Feb 2024 07:29:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c44951e1e56d79836bbd4698a276d8a60e357fe31625d5ff746d96e149ecd71`  
		Last Modified: Sat, 17 Feb 2024 07:29:43 GMT  
		Size: 6.5 MB (6523618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c2440c0e4a0f3db2cae7ff1c1d7c0b914eb5e1fe87fa1e758a967f27fca84e`  
		Last Modified: Sat, 17 Feb 2024 07:29:42 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8af653d16ecc467cccbb8ed307a293b526e8ef0686c2e05cd6175897176be2`  
		Last Modified: Sat, 17 Feb 2024 07:29:43 GMT  
		Size: 10.8 KB (10776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb5c8af50423d3f67f44de88fcc97a6a8057caa77b42d4aeabf218217e3eb15`  
		Last Modified: Sat, 17 Feb 2024 07:29:43 GMT  
		Size: 20.6 MB (20605792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac2a34ed82f7f614f306a0465873481a709d2aa4d09e4676c3af75106b52c76`  
		Last Modified: Sat, 17 Feb 2024 07:29:44 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c177c477184eecd6cd70a3de9e0dde285d0f35edd62b41ee2124d6daa532b452`  
		Last Modified: Sat, 17 Feb 2024 07:29:44 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e6af1c8a782fee92962984bcbda5ed2213920230cf6b8e5f39076d27c896fe`  
		Last Modified: Sat, 17 Feb 2024 07:29:45 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a74e441914559e8c235a6709b26bcd6048fb895a9e161c8ea8893612fa3fc0c`  
		Last Modified: Sat, 17 Feb 2024 07:29:45 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1355d06c5c9865d7c73758c88eb22c25f15fc1b83846dfec54682ba2c44adb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18102827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13321f8aa769a5236a7dfafbf8675afa949caa1b2ea2742ebe7f5d3be9ffafef`

```dockerfile
```

-	Layers:
	-	`sha256:6686744fca0955f96e2bee2fce62c7aeabb1d6a4fe6889c7245bcd9acf29754d`  
		Last Modified: Sat, 17 Feb 2024 07:29:43 GMT  
		Size: 2.9 MB (2882243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebaa5d080f3e71e968dafb38bd23e1f2737305c13e827153d890b955f95dc944`  
		Last Modified: Sat, 17 Feb 2024 07:29:43 GMT  
		Size: 5.0 MB (5002914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c79ebde14957ac068163339b45dbeda8139cb9d62745452affa69928c551a04`  
		Last Modified: Sat, 17 Feb 2024 07:29:43 GMT  
		Size: 5.1 MB (5144270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:256cea6f6f51a6de577ac97331148cf22f85930761e80db5e025a79332f7d423`  
		Last Modified: Sat, 17 Feb 2024 07:29:42 GMT  
		Size: 5.0 MB (5004288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25464d2e22f84e8d529d3c312b9253ecbf3dff3cdfcb362f1f2dcc54f24b7eae`  
		Last Modified: Sat, 17 Feb 2024 07:29:43 GMT  
		Size: 69.1 KB (69112 bytes)  
		MIME: application/vnd.in-toto+json
