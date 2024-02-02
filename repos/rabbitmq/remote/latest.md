## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:c5e8f3b284921b07a20b5f9afa5a5c979ecb24d17cc11be9a883eb8d42396575
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
$ docker pull rabbitmq@sha256:8ceea090e0642d8859b77d3a1b3b104d63c421c8c7edd7038ccc78555ee8f36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102129207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393f6753e973bfe9239bb04268b6fe16bd2b27678a255465e91313ac17ef29e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 30 Jan 2024 18:57:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_VERSION=3.12.12
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jan 2024 18:57:54 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 30 Jan 2024 18:57:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43405e170bf442eff912d966835cc036be398cd9393589a1a2a1e3469b128b14`  
		Last Modified: Fri, 02 Feb 2024 01:01:52 GMT  
		Size: 44.5 MB (44472648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320697912a716636d661f2a9b20d76ddc5b80cc920dd9b2d0e79826766bab34b`  
		Last Modified: Fri, 02 Feb 2024 01:01:51 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11731184dd716e636c9b18ff6fbbe53388d23a149b0700fdb2709b8fb5fdb5cf`  
		Last Modified: Fri, 02 Feb 2024 01:01:51 GMT  
		Size: 7.5 MB (7473475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eaee8120a9e134d973d719e39e6f036fc5bd75256b93fc9d32e4a492a7d8bdf`  
		Last Modified: Fri, 02 Feb 2024 01:01:51 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf3538016476cfabe04829682c7edf04f309ae4ed3d4054eddebafbc01bfc38`  
		Last Modified: Fri, 02 Feb 2024 01:01:52 GMT  
		Size: 10.8 KB (10756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af77ecf0aa6ccd07090a7d0c6b898552212d535d0bf0d61fc7e5d589b79cc18`  
		Last Modified: Fri, 02 Feb 2024 01:01:53 GMT  
		Size: 20.6 MB (20620873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662b8be8e1eb1b2334b20e84b0961a2966f2752719b55eef97e5ddbe9371ab8d`  
		Last Modified: Fri, 02 Feb 2024 01:01:52 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e707813f956c48fe7204b2db99c7140b6dcb4b6ebb77c51522e21c38816c2200`  
		Last Modified: Fri, 02 Feb 2024 01:01:53 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff5f83dc2d0b5bf1e845c5b8285a5c69b805175530c03f8ea1aff535882695c`  
		Last Modified: Fri, 02 Feb 2024 01:01:54 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31513c6556221bbba4d98d48d6170e71945b541a2edffb4ca3d6b9b2c50c4b5e`  
		Last Modified: Fri, 02 Feb 2024 01:01:54 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e3141655839d1ef0f50591219d46cc6c96ea47c7f7eb8e6c2a2ccac65c489b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15791972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5882b5d7317da0cd444fed7851719cb0755f93a430857147eefd100cd3ef125e`

```dockerfile
```

-	Layers:
	-	`sha256:d96b36d618c5b901c6f3fb11285518903f8cc62438b7f9064939afa2fb5d5f9d`  
		Last Modified: Fri, 02 Feb 2024 01:01:51 GMT  
		Size: 2.4 MB (2415633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5901bd49b3fe409a22f0fe5f65d216c15a5727a960fc155c9251ba8e037fa5b`  
		Last Modified: Fri, 02 Feb 2024 01:01:51 GMT  
		Size: 4.4 MB (4434530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49457ce1e5c72a689e17cdda7927ec270865a2b013dbb1f51344536b821ef630`  
		Last Modified: Fri, 02 Feb 2024 01:01:52 GMT  
		Size: 4.4 MB (4436794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9671f648e804701fdf112ee4bdba0005063d2bd9b77564cb83fca01d46939379`  
		Last Modified: Fri, 02 Feb 2024 01:01:51 GMT  
		Size: 4.4 MB (4435904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66e072e8ec86ad0ce36fa1be62cd1d16f295418c97bcdb3af87b43752dd2d35c`  
		Last Modified: Fri, 02 Feb 2024 01:01:53 GMT  
		Size: 69.1 KB (69111 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:422dc2ec731f13e3d9e398a7773d2063d566ef7be9404bfe2e7ad86e347a5eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86002786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0df19833db303545de65f10508430dccb18c9bd00685eb7a6914a3442e1496`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 05 Jan 2024 21:27:24 GMT
ARG RELEASE
# Fri, 05 Jan 2024 21:27:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 05 Jan 2024 21:27:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 05 Jan 2024 21:27:24 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 05 Jan 2024 21:27:24 GMT
ADD file:7c2f93ce47dedf9ba449bf11d41e9930af9fa209725f5772dc09f8c8100b5626 in / 
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["/bin/bash"]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 05 Jan 2024 21:27:24 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 05 Jan 2024 21:27:24 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:781c0280deb7f9bce0fa19ad87a096aa89f97dc84ad63641be966b6c27e33c84`  
		Last Modified: Thu, 11 Jan 2024 17:49:11 GMT  
		Size: 26.6 MB (26634882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7205d04e56f4fdc71befbb0cec3148e2b2dedb28f10c290022960b4cffb993`  
		Last Modified: Sat, 20 Jan 2024 05:34:16 GMT  
		Size: 32.8 MB (32754271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c3fdfa758e8032d8b2de1436fccb736d097a326cbd6e0707ea6437b3bea0e3`  
		Last Modified: Sat, 20 Jan 2024 05:34:15 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987260332e3d37b3e023c4360710585f9b8b94b0d163bdb3bb2aae2bbaa67311`  
		Last Modified: Sat, 20 Jan 2024 05:34:15 GMT  
		Size: 6.1 MB (6060906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e1b0c9cac5e45cd3163e39a9fe7388c2678994d695af7995cfb40c738cb31e`  
		Last Modified: Sat, 20 Jan 2024 05:34:15 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748315eebaf5d7800eeffa321d34028062a42303e9822807135a9c94b3783f3b`  
		Last Modified: Sat, 20 Jan 2024 05:34:16 GMT  
		Size: 10.7 KB (10737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1b9ddb42a2132d53337e63c714780aeffd85fe247dc0530c10bc7bd87e0cb`  
		Last Modified: Sat, 20 Jan 2024 05:34:17 GMT  
		Size: 20.5 MB (20539455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13272302b94e30fea316586a7340b588c082bc8f91b1dcddfa84a658d0678c25`  
		Last Modified: Sat, 20 Jan 2024 05:34:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1bd04781c58452d10a0fabae1b57fa6b98cb489de990361fb61828b8d1331`  
		Last Modified: Sat, 20 Jan 2024 05:34:17 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33e85913e26e0ec15db7735e6fa34bf1b5abeb5d0733c76c4225a9e969f7c5`  
		Last Modified: Sat, 20 Jan 2024 05:34:17 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a7215f2805d2d397c6d88dd8e1c118c25d2cdcac8260a6771e7fca997c1b75`  
		Last Modified: Sat, 20 Jan 2024 05:34:18 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ee14eaa511780c4064ac4f2fce547640e40185920e0d92502886d3a5559d1df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15331994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c65dde14101a28091e818b7b882a022ab81712dd90925259e208108fd4f10c`

```dockerfile
```

-	Layers:
	-	`sha256:0f70852c15fa5faeaff70cb4ac8044dff9c283bcb8542c4c77090c825e4e8641`  
		Last Modified: Sat, 20 Jan 2024 05:34:15 GMT  
		Size: 2.4 MB (2418007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e75b341f277ba13e8cfdf6eb338696a4d98a1e39aa2677f8e424699841abbe0`  
		Last Modified: Sat, 20 Jan 2024 05:34:15 GMT  
		Size: 4.3 MB (4280395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a4c215ad380bbbb01dd2d32e11ba9fc36e464667fae3e61d3634030868e6062`  
		Last Modified: Sat, 20 Jan 2024 05:34:15 GMT  
		Size: 4.3 MB (4282659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8779e3dc7105a51d5cbc6808ca00c4d0b5480ccaa4357cc436f11750ab0d4319`  
		Last Modified: Sat, 20 Jan 2024 05:34:15 GMT  
		Size: 4.3 MB (4281769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:820179dd5be8661c6300f7ed5d15bc2eb6e5daa500baa41185a103537d5b2d74`  
		Last Modified: Sat, 20 Jan 2024 05:34:16 GMT  
		Size: 69.2 KB (69164 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:dec9e0d27390ffd63629220bc160f46594e2ba13b9e404e3a5216ee6fc53287b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97330966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653cb0207a7a6e96098908ca2f28bd3dc7a7e136a2c8c8b1c706e21eac1304ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 05 Jan 2024 21:27:24 GMT
ARG RELEASE
# Fri, 05 Jan 2024 21:27:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 05 Jan 2024 21:27:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 05 Jan 2024 21:27:24 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 05 Jan 2024 21:27:24 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["/bin/bash"]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 05 Jan 2024 21:27:24 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 05 Jan 2024 21:27:24 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:ce9ebea987c26664d067f7e14c93231c6d303e4acb322f15ddbf05b414646d64`  
		Last Modified: Thu, 11 Jan 2024 17:49:04 GMT  
		Size: 27.4 MB (27356849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41903d75b3c754e497f07375c5f0f16ad03631733255e67e343ae901f7890ae1`  
		Last Modified: Thu, 18 Jan 2024 17:31:10 GMT  
		Size: 42.3 MB (42312650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eeb81ccf1ca78d9ceae9ce46cf719da50aeb5403218dd12b5e5448515a6c5eb`  
		Last Modified: Thu, 18 Jan 2024 17:31:08 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aac7534440201d43fc31bfe46b2920e80431c15e0a4c97ae0b6358a7153a628`  
		Last Modified: Thu, 18 Jan 2024 17:31:09 GMT  
		Size: 7.1 MB (7119537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8cfd55c19d72f70a780a55a62dfe9b3cfc08aa9e5f2ca48524358785eb32c0`  
		Last Modified: Thu, 18 Jan 2024 17:31:08 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818ffabf814397a520e740d4428d7610a2b75d0857240ad2df7f05d8168186c4`  
		Last Modified: Thu, 18 Jan 2024 17:31:09 GMT  
		Size: 10.7 KB (10715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e800f83d20fa550a1b2a6a4934bd07066dce06c7e7332e1431fd317bb3653da`  
		Last Modified: Thu, 18 Jan 2024 17:31:11 GMT  
		Size: 20.5 MB (20528692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c816791178937d390ad34f5222ff77c9cc23eee69792ad97918fcc21f113d8`  
		Last Modified: Thu, 18 Jan 2024 17:31:11 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ef90ee051fa07da8a968b9b042a20719bcd0ad7f937a2641d3124e7a058c5e`  
		Last Modified: Thu, 18 Jan 2024 17:31:11 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b216e4c702df6527e370febf17b788bcab22a68629ba607120182d48a86d6c`  
		Last Modified: Thu, 18 Jan 2024 17:31:12 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0279046359d5f38b8c950ed115df7464492af69e036a38dc3d5b203effa07307`  
		Last Modified: Thu, 18 Jan 2024 17:31:12 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ce37eac7bc5f5431b269279fa72af6b52e030be9e03bc6c961eb25d3e6237734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15782783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e14549d3d206568015de8e9ccdd436d8b8243f68bcaec58ce3f826b312e12d1`

```dockerfile
```

-	Layers:
	-	`sha256:60e2978807ac5faa62192ac54eb2340fe9f30c28d7fd2a5bf1d12586842bf04b`  
		Last Modified: Thu, 18 Jan 2024 17:31:09 GMT  
		Size: 2.4 MB (2415966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4279108c6cff387ee4acc9bf5051b54ba23becd963224b0bb7b544dbc819f087`  
		Last Modified: Thu, 18 Jan 2024 17:31:09 GMT  
		Size: 4.4 MB (4431406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6931139d7c74316f888e7d6bf5c0893d3e6b58bd20707929b3abe86d74e0304`  
		Last Modified: Thu, 18 Jan 2024 17:31:09 GMT  
		Size: 4.4 MB (4433670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75c374801a1ec1fc6d2947177ef7652d56de90b5b6c8c2c6ac0788b7a3037284`  
		Last Modified: Thu, 18 Jan 2024 17:31:09 GMT  
		Size: 4.4 MB (4432780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4b52f8df2462656c7acd071e86c0f15577258635723cc13660e9fc22a38cfc`  
		Last Modified: Thu, 18 Jan 2024 17:31:10 GMT  
		Size: 69.0 KB (68961 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:dee61862a5196f2ae255b5ca1853801d565d1291e691ad825bfa36cf92e17a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101715061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe2249a4575a6f644555b4c03de5c6f0c3e555a3a96ad7a33c9ac5a4edd7e57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 05 Jan 2024 21:27:24 GMT
ARG RELEASE
# Fri, 05 Jan 2024 21:27:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 05 Jan 2024 21:27:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 05 Jan 2024 21:27:24 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 05 Jan 2024 21:27:24 GMT
ADD file:4da6fb9ba29da03fa46ed73abfae01fa7c87f2c26044ee297c88359085392aef in / 
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["/bin/bash"]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 05 Jan 2024 21:27:24 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 05 Jan 2024 21:27:24 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:eb06c458f1bcffd534bd10415f36af10d84ad0223c7840a052931ee0238f62ee`  
		Last Modified: Thu, 11 Jan 2024 17:49:17 GMT  
		Size: 34.5 MB (34519608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2c28ea296fc6997dcbfd6e4ee6107c2c59f5ba52366a09d27420dfac03b5db`  
		Last Modified: Wed, 17 Jan 2024 13:28:38 GMT  
		Size: 38.8 MB (38784467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2017b98cffdc242c7ac02ed7fddb2f39c28280ba98d21c502f0fee6e420a7e6`  
		Last Modified: Wed, 17 Jan 2024 13:28:36 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16029874f1a662344f9c1f961cfaee83653ea97153486bfef87b006ed6389679`  
		Last Modified: Wed, 17 Jan 2024 13:28:37 GMT  
		Size: 7.8 MB (7842413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aea30bfd8847493a96ddc8d6eb36ae4adc27f368171300dea08d4e6d6fa305e`  
		Last Modified: Wed, 17 Jan 2024 13:28:36 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e540d0997db324f347fea91ce9f248a74327f2647ff4ec38ede9fe72a2fc7bf1`  
		Last Modified: Wed, 17 Jan 2024 13:28:37 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7dec39eb41bda6860e180d491efecf9be7aec1b7c8850459f1e030f95e2a3a`  
		Last Modified: Wed, 17 Jan 2024 13:28:38 GMT  
		Size: 20.6 MB (20555384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97452c7b6bf4a7f7b5eb9dfd7958b63281f5acf9d90adaeeb0c2508f17df6fa2`  
		Last Modified: Wed, 17 Jan 2024 13:28:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a88028cfa55d99f75c7b257b067081c7a8f57de1766ca4cf2b4bedc381ca395`  
		Last Modified: Wed, 17 Jan 2024 13:28:39 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff1c7a1fd869ff3cf8b775304eb4c7e1e6793c8ce550c38f16cb5c381af3a83`  
		Last Modified: Wed, 17 Jan 2024 13:28:39 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b68b1956ec38da4340ec0a904966df48c0000f4c93698d1177cc41f9c3412a`  
		Last Modified: Wed, 17 Jan 2024 13:28:40 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bc8dea85cc73c8fe36ace89e0d285c1ef679826f7480c94e5d22776777843ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15698628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ab20cb58d0835da0dfb8d7c558dcf505fd387487af5c4dc9e91a0cee3d559f`

```dockerfile
```

-	Layers:
	-	`sha256:f0d6f68581e5e5d882cecdced939f295791662b926b8c4737a1671244e230408`  
		Last Modified: Wed, 17 Jan 2024 13:28:36 GMT  
		Size: 2.4 MB (2419183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d517d14267a881f27d1197fa79fe9e935f723bd9486318f4162ac315fa17d2`  
		Last Modified: Wed, 17 Jan 2024 13:28:36 GMT  
		Size: 4.4 MB (4403121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc58e71f35a337777b5e4c047971936d3b00399a14bd281c16c42d2f42092724`  
		Last Modified: Wed, 17 Jan 2024 13:28:36 GMT  
		Size: 4.4 MB (4404021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3529d35cc4a6d84c56ee72789e2f326644768a2ce199ec6899bb3a8fd647b1c2`  
		Last Modified: Wed, 17 Jan 2024 13:28:37 GMT  
		Size: 4.4 MB (4403131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9236c0e5346e33e7ff2a22d9331229c7bc043b05ca0549d2e06e8e035f0d223b`  
		Last Modified: Wed, 17 Jan 2024 13:28:38 GMT  
		Size: 69.2 KB (69172 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:fc7e1a777c1d06740140608a3633d96206fd873c5e087ac7fb3651e9970e8cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92603863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4951c9662593ca883c31eaa5dd2dd3a40535458160638aaab004066963ae13a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 05 Jan 2024 21:27:24 GMT
ARG RELEASE
# Fri, 05 Jan 2024 21:27:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 05 Jan 2024 21:27:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 05 Jan 2024 21:27:24 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 05 Jan 2024 21:27:24 GMT
ADD file:5ae109128826d2e7660949ed9ff9af4b92bbade5ce06a7011ab7b15bb21d8b75 in / 
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["/bin/bash"]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 05 Jan 2024 21:27:24 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 05 Jan 2024 21:27:24 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c0aadca0a59447759d5cf02c0250d916b74c90d22c4451a011b645d79453f4fa`  
		Last Modified: Thu, 11 Jan 2024 17:49:24 GMT  
		Size: 28.0 MB (28026713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e84aeda759232bcf89c75f2fa4fcb1054b29df11792a44c24f71288063d6df`  
		Last Modified: Sat, 20 Jan 2024 14:03:45 GMT  
		Size: 37.5 MB (37459691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6441bc58fce03c3d39ac02edcfd19d739d3df4530352c63434534bddb968c5`  
		Last Modified: Sat, 20 Jan 2024 14:03:44 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb1a9d8bc73d6bbda26e074147f8c709a937c0484743999a73dfb69de00ceca`  
		Last Modified: Sat, 20 Jan 2024 14:03:45 GMT  
		Size: 6.5 MB (6513963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363540ff6368c2b310efcf0f2fb868dc945ef57cfc4eec0090ea0b6a15c232c5`  
		Last Modified: Sat, 20 Jan 2024 14:03:44 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade41603317364ade94e68242a44e11ee9082e4786ae256a6cb5cf1736f00f06`  
		Last Modified: Sat, 20 Jan 2024 14:03:45 GMT  
		Size: 10.7 KB (10745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aea476331c8351abf39f3d2af55df16e21604e693fb62322354aaa7d167b7c6`  
		Last Modified: Sat, 20 Jan 2024 14:03:46 GMT  
		Size: 20.6 MB (20590223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57eace4150d25c5b0cb870aff4dd9371e52f47ee6181700f6ed81c393502a49`  
		Last Modified: Sat, 20 Jan 2024 14:03:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380abe6b8bf572ec81d887fa93b4ae1090e85187d10e6476acefbcc63f856f9a`  
		Last Modified: Sat, 20 Jan 2024 14:03:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71715bbcf7f78e3a72c031abf54ea87036b21ca93b83ca731c060d9c44bb6fb6`  
		Last Modified: Sat, 20 Jan 2024 14:03:46 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff2df415d799696acc6af17850a6468aeadee6a6afe2745766416d118a808a`  
		Last Modified: Sat, 20 Jan 2024 14:03:46 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e0c9c33dd3ec47ce106ca24f967f393111d75d75690f455bc5fb7bc6a1578811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15387408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3832b969421a8d2f70d0b5f7ceafc4e4bef38ecf65080e0f5574bcf1eed42a`

```dockerfile
```

-	Layers:
	-	`sha256:7df2f007e8e94ec5051a813dea2f2c89cc336b79739cd0cfd3b83ab7885cb57a`  
		Last Modified: Sat, 20 Jan 2024 14:03:44 GMT  
		Size: 2.4 MB (2417448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f84e114877011f7729fcaf797eb371bb1aba8b6b72c6dadf2ccfbf915a8319c9`  
		Last Modified: Sat, 20 Jan 2024 14:03:45 GMT  
		Size: 4.3 MB (4299070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff38ecb88f8261e2dbae897d144f77cc54063cc0839eb2dd18fe42197fe7cc7`  
		Last Modified: Sat, 20 Jan 2024 14:03:44 GMT  
		Size: 4.3 MB (4301334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f525f50b0cd2a375fbc469736cfb1113db46a45f05bd75308c8b4ac5c9f12927`  
		Last Modified: Sat, 20 Jan 2024 14:03:44 GMT  
		Size: 4.3 MB (4300444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13706c990053f26b690d78ee9f3e76e9606a0a3645a1ea5d51b84de2dbdc5cf4`  
		Last Modified: Sat, 20 Jan 2024 14:03:45 GMT  
		Size: 69.1 KB (69112 bytes)  
		MIME: application/vnd.in-toto+json
