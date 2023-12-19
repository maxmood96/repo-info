## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:b90f2abfacd58424d5417edaf46444f12bba8553080d4383a264c057a9f33ffa
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
$ docker pull rabbitmq@sha256:04cbdbc468127ad0309a1b150ad03a2639046b5de80d5b904e217b18644297dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102095799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2112372129ef8c01c8aa056f25c77c7ec3ee2aa6e92082ffdaf79ef46dc8b796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 19:34:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 18 Dec 2023 19:34:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 18 Dec 2023 19:34:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_VERSION=3.12.10
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 19:34:09 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 18 Dec 2023 19:34:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 18 Dec 2023 19:34:09 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 19:34:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 18 Dec 2023 19:34:09 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:a486411936734b0d1d201c8a0ed8e9d449a64d5033fdc33411ec95bc26460efb`  
		Last Modified: Tue, 12 Dec 2023 11:55:25 GMT  
		Size: 29.5 MB (29547485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f562238a268839db3897b877f024b4705238db8541cb53eef49ffebd71bb7d2`  
		Last Modified: Tue, 19 Dec 2023 00:59:30 GMT  
		Size: 44.5 MB (44472656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6b3af08868e1e491acdca92578f96801a6b347f0c229268d35fcca7154cd60`  
		Last Modified: Tue, 19 Dec 2023 00:59:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036bd5cfee94191c3cb291e8fe49b9297c78bab86bfc8107d31c8b7e5639795a`  
		Last Modified: Tue, 19 Dec 2023 00:59:29 GMT  
		Size: 7.5 MB (7463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ee8422a66f86515a63920cd47550b689110444d9f78f5abfd4059501986951`  
		Last Modified: Tue, 19 Dec 2023 00:59:29 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e076a0359c4f5f372af77a9a04100f198fb53838fba5754766badf5feb3f1c9`  
		Last Modified: Tue, 19 Dec 2023 00:59:30 GMT  
		Size: 10.8 KB (10756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a570163442d56cbacc20154b3a62bc3cbb038de4979ce3e8c9b2e76dafc5b50`  
		Last Modified: Tue, 19 Dec 2023 00:59:31 GMT  
		Size: 20.6 MB (20598853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2959158cb58bd0db14697b05f1e82fb40ee75d9da4bac9ce43aee030d2462f70`  
		Last Modified: Tue, 19 Dec 2023 00:59:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e640bc39f060eca64b54b22d1e33fd4c0ff770e0ac419405b08afac8aea5e3c`  
		Last Modified: Tue, 19 Dec 2023 00:59:31 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0375dfc623e39348433655af637c24da4cee2f374457e0ca4c1b60e865fb24`  
		Last Modified: Tue, 19 Dec 2023 00:59:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf5534f9e249be932b36e2c9eb280b69761ac8c4a41844b5f9cf909107393c6`  
		Last Modified: Tue, 19 Dec 2023 00:59:31 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:83b882ffc21a0488a57e2a9875bee15dc1890d6a72bd6d013bff8c08d6d57ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15787791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687f5e7cec6b2d499d5efa96d75f0599f04b7e128de16b2e4788efe74ac0db21`

```dockerfile
```

-	Layers:
	-	`sha256:865a4f4bb27025b3880cd0abf2186c949a1fd0c16dc922af81746815c84e01e3`  
		Last Modified: Tue, 19 Dec 2023 00:59:29 GMT  
		Size: 2.4 MB (2414181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a8d729d325a4648fd885980f559f07231cc1c3b3eb360a30a2a422e8c9617f`  
		Last Modified: Tue, 19 Dec 2023 00:59:29 GMT  
		Size: 4.4 MB (4434530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b797cfe015124cadefffa9f339a73125213a4da1ced9cbd3fef8c02b032e7781`  
		Last Modified: Tue, 19 Dec 2023 00:59:29 GMT  
		Size: 4.4 MB (4435430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c6c167b019ab80586b28d866e4324e48ae9b23c649f976f4ccca7438443e65a`  
		Last Modified: Tue, 19 Dec 2023 00:59:29 GMT  
		Size: 4.4 MB (4434540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fa65c7bcd13ac659e76ed2acba8c47e5d03d44e41aa83626b8813d6c8e14edf`  
		Last Modified: Tue, 19 Dec 2023 00:59:32 GMT  
		Size: 69.1 KB (69110 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:451a6f77dbbaa86a94f08882480f76ff946408e1c3ab5d2543deb3567335650c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85979683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f990eb8901bb578c8fea1dbd6dfbde75b40f6246d31ac4cfd198d568090ec2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:01 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:06 GMT
ADD file:62316c1da591602d5f15e0cda8787ce54cb80cd63ee53391aad6e4ea9cc97f06 in / 
# Tue, 12 Dec 2023 11:41:06 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 19:34:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 18 Dec 2023 19:34:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 18 Dec 2023 19:34:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_VERSION=3.12.10
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 19:34:09 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 18 Dec 2023 19:34:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 18 Dec 2023 19:34:09 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 19:34:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 18 Dec 2023 19:34:09 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d33cdf8c116214cd1f23278abc2741878af19658bf65c210a48280807622d871`  
		Last Modified: Tue, 12 Dec 2023 11:55:37 GMT  
		Size: 26.6 MB (26635272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1756f39a9ef8a560e4c0b48b70e5aeb72a03b5e713e94c9cf09abd42954b214b`  
		Last Modified: Tue, 19 Dec 2023 01:22:49 GMT  
		Size: 32.8 MB (32754309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ccaf4cdbb319047e2c8f8132f05326e2a5197597b7a5fe258eb6b00b8f7d75`  
		Last Modified: Tue, 19 Dec 2023 01:22:48 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b24075e7378f595997a84b844cd308391de81c9fbd8443a77fb0682eb356def`  
		Last Modified: Tue, 19 Dec 2023 01:22:48 GMT  
		Size: 6.1 MB (6060890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cddb009e87e76b0ad4428214040d8fcb46318ed1b31e1bd311c9ce6d48460b`  
		Last Modified: Tue, 19 Dec 2023 01:22:48 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494c8b6418d6347e6c3da77ba3694765b1cf59164fb3da685117d89f49c27e3`  
		Last Modified: Tue, 19 Dec 2023 01:22:49 GMT  
		Size: 10.7 KB (10705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e2e88a01b040289868ebf9a9f53bd95d52b2d9bb5a7d54fc916ee218a8c5df`  
		Last Modified: Tue, 19 Dec 2023 01:22:50 GMT  
		Size: 20.5 MB (20515978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b1bbfb0fe923de187df369ebf25b283c869fa3faabfd4d54a99309aced24eb`  
		Last Modified: Tue, 19 Dec 2023 01:22:50 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bca15d90a931ac672735fb0e2ed06666a08cf05297304773f74d8cde643c9db`  
		Last Modified: Tue, 19 Dec 2023 01:22:50 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcce7a2513b7ca56540e43994fc744aa74e87f7509f22ecd499d4751c1053f16`  
		Last Modified: Tue, 19 Dec 2023 01:22:51 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351908c06ee7f4735cc5a1b49019573fa63515eb20ebd4fd61aa43ffdd8d69d4`  
		Last Modified: Tue, 19 Dec 2023 01:22:51 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5dbaeb55ce38d4ba7b9aaba4867a1962c0517ee1ea8eb54f6be38dfaf18f2f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15327975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffc1e891574fa3dd1b24a02645072754a57c5588290ea90f9d7144b98f7de5f`

```dockerfile
```

-	Layers:
	-	`sha256:a8cc9828a2d4798545b0d89aa4659747b3219835f9bc5a81123586acaefc6723`  
		Last Modified: Tue, 19 Dec 2023 01:22:48 GMT  
		Size: 2.4 MB (2416555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b8820a01e39ae214f1a550e9627b51915d8ca6ccbc69097f10bc9d5e2e1547d`  
		Last Modified: Tue, 19 Dec 2023 01:22:48 GMT  
		Size: 4.3 MB (4280395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b00e3d22f74fc1038658fdd964be0c4147076ea0d1dd99b957fbea9802f10c`  
		Last Modified: Tue, 19 Dec 2023 01:22:48 GMT  
		Size: 4.3 MB (4281295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72cd44928db41122cf2e9fda3b0003b0426d66cfa7e0f813b43298ee9f3606ce`  
		Last Modified: Tue, 19 Dec 2023 01:22:48 GMT  
		Size: 4.3 MB (4280405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eda066794ceb0f15088fa8c62b8950c26707ab406994104f24957eb5f0a1ede`  
		Last Modified: Tue, 19 Dec 2023 01:22:49 GMT  
		Size: 69.3 KB (69325 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:946888ce0db6413f903657f68f06545ba920176eb4c79ae9520a31afc205b720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97311306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98daea36bdab3e136d32319e62d26ec3c1174c1e06d6af03dcfbb6eab6fb82bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 19:34:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 18 Dec 2023 19:34:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 18 Dec 2023 19:34:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_VERSION=3.12.10
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 19:34:09 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 18 Dec 2023 19:34:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 18 Dec 2023 19:34:09 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 19:34:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 18 Dec 2023 19:34:09 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:005e2837585d0b391170fd9faf2e0c279d64ba0eb011cda8dedf28cb5839861e`  
		Last Modified: Tue, 12 Dec 2023 11:55:31 GMT  
		Size: 27.4 MB (27358237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e85db1016b634d153f353777affefa4d34a523b4265a7d9d21cb2544552c5e`  
		Last Modified: Tue, 19 Dec 2023 01:16:47 GMT  
		Size: 42.3 MB (42312671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e462478bb2ad5fa4e7acea7f30406537631f1a5aada00f70e13efc45788bbaa`  
		Last Modified: Tue, 19 Dec 2023 01:16:45 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377e761341665a06b9e9ec0158ed2c3d55c90e376fa77b8bc570157aebec3c2`  
		Last Modified: Tue, 19 Dec 2023 01:16:47 GMT  
		Size: 7.1 MB (7119550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562e0516451f0e9fc44f5f2c1c71439eed058dc2498e9a0a1806c0793bb84db0`  
		Last Modified: Tue, 19 Dec 2023 01:16:45 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b27d4b02ed15bec80ca96f3a5fe53cf3edf5384f89964be56ac361c94e23d6`  
		Last Modified: Tue, 19 Dec 2023 01:16:46 GMT  
		Size: 10.7 KB (10731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994dd4e3a32c7bfc32a31d3bfa592d5ed1bbc132de167f727f629d2698afd757`  
		Last Modified: Tue, 19 Dec 2023 01:16:47 GMT  
		Size: 20.5 MB (20507587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928076d4f5bf9d828f7aa361d08c186c4b4c6bc89b66be44738a0b6071e71d04`  
		Last Modified: Tue, 19 Dec 2023 01:16:47 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5205acce36287b5757449a724e2114581b3df401de9c37c4a4040dbeeb3c568c`  
		Last Modified: Tue, 19 Dec 2023 01:16:48 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c7e761eeec1099a2abec42eb0ab226a881d787aaea49fbfa66252775f3efa9`  
		Last Modified: Tue, 19 Dec 2023 01:16:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c971639e4e74dfd6143de1c407ca316e776622460330c38432ada81f0d2aa66`  
		Last Modified: Tue, 19 Dec 2023 01:16:49 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:82ecf2ff32a612a7f3a1944f607bd89e87f3d6144f2e009c7586f0a3fb4ece64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15778764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d5b28ae08c402941ee21b1a6d2e0ae119e6f06971224dbdacc295631ef746b`

```dockerfile
```

-	Layers:
	-	`sha256:8da4430997a644549a2c0794fb94bb5894dab9519c20e0a5c225c0c3f0a4933f`  
		Last Modified: Tue, 19 Dec 2023 01:16:45 GMT  
		Size: 2.4 MB (2414514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a95ce7a6d36e0f80d46331da49a7c2a19245abeb6e8dc7253d4e0539ab41fc45`  
		Last Modified: Tue, 19 Dec 2023 01:16:45 GMT  
		Size: 4.4 MB (4431406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df08e8a52c04d01479f04241125176dfaea235b1cfb1bc59404b247a964d89b6`  
		Last Modified: Tue, 19 Dec 2023 01:16:45 GMT  
		Size: 4.4 MB (4432306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7aaf9bd7e73c51c66fac02c6f06900abcd3b5999a613fa72f78beaa9e9a079`  
		Last Modified: Tue, 19 Dec 2023 01:16:46 GMT  
		Size: 4.4 MB (4431416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40477b3b078f76859d41df883b26736436dca7ef188fbe4a6b548fc1c99c491`  
		Last Modified: Tue, 19 Dec 2023 01:16:46 GMT  
		Size: 69.1 KB (69122 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:fa58539794873bf457742293edf56b1e58050c1b54070ac37eae4120678b8471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101677289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cd9ca20de269eaba84488527158f23f525e1ec6686fa7850e94b6b0a8ba0e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 22 Nov 2023 06:55:25 GMT
ARG RELEASE
# Wed, 22 Nov 2023 06:55:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 Nov 2023 06:55:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 Nov 2023 06:55:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 22 Nov 2023 06:55:25 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Wed, 22 Nov 2023 06:55:25 GMT
CMD ["/bin/bash"]
# Wed, 22 Nov 2023 06:55:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 22 Nov 2023 06:55:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_VERSION=3.12.10
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 22 Nov 2023 06:55:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 22 Nov 2023 06:55:25 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Nov 2023 06:55:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 22 Nov 2023 06:55:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6d5f22cb7a5ae76d71ff8d8d5254febad219eb4adbf9b849b5e1d5bd967691cd`  
		Last Modified: Tue, 12 Dec 2023 11:55:44 GMT  
		Size: 34.5 MB (34521615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5e4abbdd519aa024a98d0c599e2b3b90b0d65282448a023e5525213e542730`  
		Last Modified: Sat, 16 Dec 2023 16:18:38 GMT  
		Size: 38.8 MB (38768421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad33c553e39c7250c53b66583e4bf329022ee0a5108b0db4e14c1130f6bb0be5`  
		Last Modified: Sat, 16 Dec 2023 16:18:36 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee508e1e6fd909797f0563a1ee1f54bb4f1f4d891cf9657b8c2a3e5757ae931`  
		Last Modified: Sat, 16 Dec 2023 16:18:37 GMT  
		Size: 7.8 MB (7842361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a31422aa3bb4d79cae086a100449c441e622fb7880aedd0b0bcd282ed64d67`  
		Last Modified: Sat, 16 Dec 2023 16:18:36 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9310a1d5e0901c4f0abcb6dc053f92846dbb0e60d349f01112399857ac584bdf`  
		Last Modified: Sat, 16 Dec 2023 16:18:38 GMT  
		Size: 10.7 KB (10665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71417cf8478bc73bc920ba512abd627c6d1f4628d37c25a742c1d2126df0113c`  
		Last Modified: Sat, 16 Dec 2023 16:18:38 GMT  
		Size: 20.5 MB (20531691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935e37780cf26358a01341ce6a03c59f8d4bb1ae7caf2029943896f12ff061bf`  
		Last Modified: Sat, 16 Dec 2023 16:18:38 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083342f3d8e105eeeef9f881d0f2971b4e783549eb2d7916f9f27f0183a1b459`  
		Last Modified: Sat, 16 Dec 2023 16:18:39 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd998e840d42a96bbcfc35dfd958cbb8ace88f6789b25c8bd1f2fd81b7e51a20`  
		Last Modified: Sat, 16 Dec 2023 16:18:39 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba2634a4df744c2e957af37758ea0ed8b35e61281cd9f782d44fcc47b6a4e67`  
		Last Modified: Sat, 16 Dec 2023 16:18:40 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:64cbd10618985f25ebed4d477047e7e131c0c52cc2f978963d32b3d73157be4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15698120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c38b7f2b85d00d445ee63df5433ee2f35fc796fb2c5d43bd5def7e31cb029bb`

```dockerfile
```

-	Layers:
	-	`sha256:59f9ac04a7784bea2f3b078d5918965c64c9ac08f553400252e4dfed7c54a583`  
		Last Modified: Sat, 16 Dec 2023 16:18:36 GMT  
		Size: 2.4 MB (2418676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:383eaaca6569270f00336716b6d6402ffdbdcfe4032c5c7046df595bf0a948a3`  
		Last Modified: Sat, 16 Dec 2023 16:18:37 GMT  
		Size: 4.4 MB (4403121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:037a24551b7ea306776d328cf1bd1892950793db605965f8d6c861b7726de59c`  
		Last Modified: Sat, 16 Dec 2023 16:18:37 GMT  
		Size: 4.4 MB (4404021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e7a856a773875d33389e998878e22ef13909963d9f33f5f31a2fb0a6be853f9`  
		Last Modified: Sat, 16 Dec 2023 16:18:37 GMT  
		Size: 4.4 MB (4403131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ba0c290959ff5be8943b426d9a05341e981ae16187d4a68b0381405e180bea7`  
		Last Modified: Sat, 16 Dec 2023 16:18:38 GMT  
		Size: 69.2 KB (69171 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:627f413908bff37c5928b0c03de5b6121c5a5014bc3cc8b4827b355112de266b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92580753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fbf38558c3f0afd8455b6c8632f48af0db6fbd86a7211327a82cb00e184bb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 12 Dec 2023 11:44:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:44:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:44:59 GMT
ADD file:1729e720d10023da7d783040cefa8f30d3c61772a5e1ae577182a1fcba69aff1 in / 
# Tue, 12 Dec 2023 11:44:59 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 19:34:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 18 Dec 2023 19:34:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 18 Dec 2023 19:34:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_VERSION=3.12.10
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 19:34:09 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 18 Dec 2023 19:34:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 18 Dec 2023 19:34:09 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 19:34:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 18 Dec 2023 19:34:09 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8cf433553d1d6625c1509159e9502639154da459bba2d5aadeb708dbe9637230`  
		Last Modified: Tue, 12 Dec 2023 11:55:50 GMT  
		Size: 28.0 MB (28027192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24705ecb58928b5b875c6f44de91814cc92dde0d6459a5f67614a4cb0d2d820`  
		Last Modified: Tue, 19 Dec 2023 01:13:42 GMT  
		Size: 37.5 MB (37459595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad4cf0d240f3c042835896fb5b87b4806fd75d59c864f11d2104f86a3d679d`  
		Last Modified: Tue, 19 Dec 2023 01:13:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fbc65a2cfa5a3126d80ec95cf37b38351f72a98cdad94eeb5d277d43077004`  
		Last Modified: Tue, 19 Dec 2023 01:13:41 GMT  
		Size: 6.5 MB (6513978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56f6b06f3484a79de340517cdba026b7ebddeda686c4893287ead3993a0ae12`  
		Last Modified: Tue, 19 Dec 2023 01:13:41 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418d5cd32805390aefb24d08b345ab293fae61e2571c3d89b4e66d9f81b7a07e`  
		Last Modified: Tue, 19 Dec 2023 01:13:42 GMT  
		Size: 10.8 KB (10752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff7d20d625175ba39398393eba9ec0b20b01cec8b399a175e4a8cf39b4ac8c2`  
		Last Modified: Tue, 19 Dec 2023 01:13:42 GMT  
		Size: 20.6 MB (20566696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c53b623814dac2a3df918fa0204456f1b11a4b06cfa9233b44e1cb6616f16fd`  
		Last Modified: Tue, 19 Dec 2023 01:13:42 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa7b718d3abe374ca0ae4815e17197c4690df494b713001542e9b8c34b1f1cb`  
		Last Modified: Tue, 19 Dec 2023 01:13:43 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c97b6edec92382111d74b3c42fc0ff03ee95a5fb7430307b89d87371fe729f`  
		Last Modified: Tue, 19 Dec 2023 01:13:43 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f1624a49fbf5d6bfc182b83ed077f53c3c5ef56be265456dac7d89de9b7199`  
		Last Modified: Tue, 19 Dec 2023 01:13:43 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f555c41dd0ad4eab4e79f0c63a107c99bc44b4d78471bd1f33ed4d9f6fff6328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eae11707c2728ca657496640184a5b94930bd5778a808186392affb828e4cbe`

```dockerfile
```

-	Layers:
	-	`sha256:b311783288cf5bb98990e0c7b8484bbf8c3e273b7022a05de922fd9aed95fcb6`  
		Last Modified: Tue, 19 Dec 2023 01:13:41 GMT  
		Size: 2.4 MB (2415996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e8004fdc3a198ae17c295c04d37e1c1f1754d42e974db22090fdd4ce105b89`  
		Last Modified: Tue, 19 Dec 2023 01:13:41 GMT  
		Size: 4.3 MB (4299070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6295c21a037e771e1569e8b5b3e7a287765d277a1354fd4fad0e0f239f4534b0`  
		Last Modified: Tue, 19 Dec 2023 01:13:41 GMT  
		Size: 4.3 MB (4299970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2deafb4559b2142362159646c3f0a7ebf76b5f0cdb4bf0bec051eb57ec1c12`  
		Last Modified: Tue, 19 Dec 2023 01:13:42 GMT  
		Size: 4.3 MB (4299080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:220ba8619eacba5ae4f773d7f244c6dca1ae8d5d2e31f658c7786422688bb4d3`  
		Last Modified: Tue, 19 Dec 2023 01:13:42 GMT  
		Size: 69.1 KB (69112 bytes)  
		MIME: application/vnd.in-toto+json
