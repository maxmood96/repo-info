## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:a5faa74a3bef6c5e589d8971ff55d4c825860b92fbc48eeb0141d2535f150e7a
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
$ docker pull rabbitmq@sha256:0707df9f526c8ff49b4484c5ef4c8799e86fe198428d65817dccbac6de74609e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104523502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7bce5d676bec46b959f6c6e610f4438d44eba044f6ed7d67c85533e191aca0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Fri, 29 Mar 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 29 Mar 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 29 Mar 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"26.2.2","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@26.2.2?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 29 Mar 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.1
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 29 Mar 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 11:05:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.13.1","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.13.1?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 29 Mar 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 29 Mar 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 29 Mar 2024 11:05:22 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Mar 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 29 Mar 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:bccd10f490ab0f3fba61b193d1b80af91b17ca9bdca9768a16ed05ce16552fcb`  
		Last Modified: Tue, 27 Feb 2024 19:00:05 GMT  
		Size: 29.5 MB (29538961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeef0afc47425f4ed73ea09ee6effe5b955471b14b3e148a08599e8fbb8e7349`  
		Last Modified: Mon, 01 Apr 2024 23:56:15 GMT  
		Size: 46.0 MB (45972558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befcd9e956c60c228de3578a78e6d2cdda1b0b821e6dd1a33faacefef4a216f1`  
		Last Modified: Mon, 01 Apr 2024 23:56:15 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d522806c2939c574d6fdf843c994a541d9c391878d3b10e284aefde5328d9e`  
		Last Modified: Mon, 01 Apr 2024 23:56:15 GMT  
		Size: 7.5 MB (7473435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d038c4180ec435072ebe49f771405cdd0f6a609d02e530033ae5d605f8db59`  
		Last Modified: Mon, 01 Apr 2024 23:56:15 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a6dc2edc19bd2a5026332359759fdf43c269dd338c78adde61788c7958c9ca`  
		Last Modified: Mon, 01 Apr 2024 23:56:15 GMT  
		Size: 10.7 KB (10707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f1cfd0e1f4e7ed155767d6c7ec8965e446622645ebbfdc532011264dc6f176`  
		Last Modified: Mon, 01 Apr 2024 23:56:16 GMT  
		Size: 21.5 MB (21525318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aa423c36212275cada876e595d3d7ca3aed2d9c8dcef5b39bc41d1bedc8a6b`  
		Last Modified: Mon, 01 Apr 2024 23:56:16 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f77372fb75650f7cab5e3ae17897ac492dc9dc1f70848bc52e7a04c79363ca9`  
		Last Modified: Mon, 01 Apr 2024 23:56:16 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a3b8c697fb72acaea75b4a6c88e5b342a20e95ef9ef88992034d1de5c30a55`  
		Last Modified: Mon, 01 Apr 2024 23:56:17 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a92f86a2717047cd0e2d6dde788b2ed18b941ba934132f38f07d0731cd8bdb7`  
		Last Modified: Mon, 01 Apr 2024 23:56:17 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3baa8865d76b62d01c534bf3f3b5f02ec3c564e829c7e324a61c9768ad1f2958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18351085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a206c2f40ea893ec4ff5e96075ce5395f11e5d481674d8475a18d5503d516e`

```dockerfile
```

-	Layers:
	-	`sha256:933492b833d84c605447d6e17d0db22cc67b708db1abb38a9bd2f4ae1c75294a`  
		Last Modified: Mon, 01 Apr 2024 23:56:15 GMT  
		Size: 2.8 MB (2792777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddc462fe39a06b076019bb77feed98882c91879fa0b0bc8b8f86cfaaf6bed11b`  
		Last Modified: Mon, 01 Apr 2024 23:56:15 GMT  
		Size: 5.2 MB (5161863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c590350ed6c5b38b7a01119206a5ecb3426d79856ccaef9a714e7d8c5605af64`  
		Last Modified: Mon, 01 Apr 2024 23:56:15 GMT  
		Size: 5.2 MB (5164130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9545af1044cc70810aefb9d82214959daaee96788fe8eafb08d273abdcf871d`  
		Last Modified: Mon, 01 Apr 2024 23:56:15 GMT  
		Size: 5.2 MB (5163237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd69cae5d99e9ecc9bfa5bcf1246538779c5501a6af8ae72be42e1df749efc59`  
		Last Modified: Mon, 01 Apr 2024 23:56:16 GMT  
		Size: 69.1 KB (69078 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:66d6486cf03fa6e64926e846bbfa16067263a9c54b02bab1a2e0ceb09e77c20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87637938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5dc11d745e06b08d5b4bab1664d1608d048111d1fadbf5dcf888fc1c748952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
# Fri, 29 Mar 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 29 Mar 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 29 Mar 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"26.2.2","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@26.2.2?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 29 Mar 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.1
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 29 Mar 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 11:05:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.13.1","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.13.1?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 29 Mar 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 29 Mar 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 29 Mar 2024 11:05:22 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Mar 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 29 Mar 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:abb4a589b6575b27b3632780f584416e354f1d3596a2b98cee1cc8dcd76ebe6e`  
		Last Modified: Tue, 27 Feb 2024 19:00:21 GMT  
		Size: 26.6 MB (26637029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf923191c70c814a46a72066b7146b77459be90a74f37a3dc639f6e83af04279`  
		Last Modified: Tue, 02 Apr 2024 04:03:18 GMT  
		Size: 33.5 MB (33475973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bd5cdfb8d7f516d83e5a73c47b3bcd5da03c70f56daf481b7d17539c703bfe`  
		Last Modified: Tue, 02 Apr 2024 04:03:17 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d46b743aba91eef92d87af76384e6e52d63ec6b13567170524eb84c60d6469`  
		Last Modified: Tue, 02 Apr 2024 04:03:17 GMT  
		Size: 6.1 MB (6072560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ae61b71d3cd84993a33f854f21286e8ed914e7401e14f2672021c651794031`  
		Last Modified: Tue, 02 Apr 2024 04:03:17 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6cae0e99eaa6854eba8eec143c0ca499443484885b456d320602c0358fc269`  
		Last Modified: Tue, 02 Apr 2024 04:03:18 GMT  
		Size: 10.7 KB (10698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5379dc402e4a857f3c0cec323aa7745545adbc4ba9b68b89ef73d5015fa338`  
		Last Modified: Tue, 02 Apr 2024 04:03:19 GMT  
		Size: 21.4 MB (21439150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f0ff68945bcf631043f58545f9e0fddecb15304ddfaff6a8e3d06b9124eb43`  
		Last Modified: Tue, 02 Apr 2024 04:03:19 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7611da9f229acc85f7b880ab0ca93233cc8e07ab7f0d3cd5fe4acb39108cf4a1`  
		Last Modified: Tue, 02 Apr 2024 04:03:19 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa83e690d7f74c9f6b112bf5c2583bfc100c7ebde685520692808882e51d8a27`  
		Last Modified: Tue, 02 Apr 2024 04:03:19 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfafe1536c2dd8059f20d4e305bdcc528963ef33a712e8b828c3e466edd7545`  
		Last Modified: Tue, 02 Apr 2024 04:03:20 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bb07cb1775d3f2068d9a0fd66e26c6ad29db478b09004cf143be6b2435f27262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17810865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa267e8302ee3ed49c9fe5d9f9383290eb880855e925b5f19a02c5e6c232d38a`

```dockerfile
```

-	Layers:
	-	`sha256:1cec568ef8d82cf50d2e819255ac5c9497b9e0acdf3082fd68043d3170d22c67`  
		Last Modified: Tue, 02 Apr 2024 04:03:17 GMT  
		Size: 2.8 MB (2795045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29c7f81a3d6a0d003b1e6d1e41d27ca2ec4d48a5b07cb7fc677571b8e1a80fd5`  
		Last Modified: Tue, 02 Apr 2024 04:03:18 GMT  
		Size: 5.0 MB (4981016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a3bb1d4e4b3c68dddbecb0e12f46b752fed9a30a60642dc06521a1405a69ca`  
		Last Modified: Tue, 02 Apr 2024 04:03:17 GMT  
		Size: 5.0 MB (4983283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1cf099c1eca6aa8eef9656411dfef827091b96bf90f7521ef7ebcd3dcdfc6be`  
		Last Modified: Tue, 02 Apr 2024 04:03:17 GMT  
		Size: 5.0 MB (4982390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d2a964a23ec505296f26e4feaddac0726099291b0db804701d68ba86bbb2e3`  
		Last Modified: Tue, 02 Apr 2024 04:03:18 GMT  
		Size: 69.1 KB (69131 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:55235a899af834ba7c12efb81fe80ea8f02fd5e475a0c142134b83215a980722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (99977567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7827876b31d77bb6deb8ffc85a085465a53489113d7cee194b816de47046ea87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Fri, 29 Mar 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 29 Mar 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 29 Mar 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"26.2.2","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@26.2.2?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 29 Mar 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.1
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 29 Mar 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 11:05:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.13.1","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.13.1?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 29 Mar 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 29 Mar 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 29 Mar 2024 11:05:22 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Mar 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 29 Mar 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f4bb4e8dca02be491b4f72d2ef2127a64ce49c48d0d9c0a0fcaffa625067679d`  
		Last Modified: Tue, 27 Feb 2024 19:00:12 GMT  
		Size: 27.4 MB (27358724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088d11a572c9d29849b210a66b50429942520738fc3270a5ae7cfd5799c51f8d`  
		Last Modified: Tue, 02 Apr 2024 03:58:26 GMT  
		Size: 44.0 MB (44040566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58745cd66c2554b97f6516f89273de966673a9c15919c9b8ab5fd8761af5c632`  
		Last Modified: Tue, 02 Apr 2024 03:58:25 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9916cfaca4cd1cbb6b4a8e2298f36d9a54c271cc3b8fea5f4b81f321364216`  
		Last Modified: Tue, 02 Apr 2024 03:58:25 GMT  
		Size: 7.1 MB (7130262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc00dab449b3db5b95395412cbc3a396edba6504811d4776891996a8ad867e4`  
		Last Modified: Tue, 02 Apr 2024 03:58:25 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dce9f55e67b4ac5478ba56daec0b33486aab8c0a35075a4dc982a9b5279bc12`  
		Last Modified: Tue, 02 Apr 2024 03:58:26 GMT  
		Size: 10.7 KB (10715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12cb86a3e61eb1a5fd8e2051ed3becfd79a3120ded01d23d542982a2c406dba`  
		Last Modified: Tue, 02 Apr 2024 03:58:27 GMT  
		Size: 21.4 MB (21434773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6b14fb3ba0b3060e23a3a6fb0208191d81cc3bc15a65e1afa4c899bc58df02`  
		Last Modified: Tue, 02 Apr 2024 03:58:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a00e93bb2fb0170fa3cf8d059823ff2978a3454a4a464c5031a50beec07032`  
		Last Modified: Tue, 02 Apr 2024 03:58:27 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f6e4a2577b49e1b12dcd35aefd1d40fc7ecadbbf8821105fffbaee6684a243`  
		Last Modified: Tue, 02 Apr 2024 03:58:28 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420fbc570146cd9dcc374320aa1f1b81a9f227b1dfc9edbe099b2ca8b3621d8e`  
		Last Modified: Tue, 02 Apr 2024 03:58:28 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7f5b117cc302c5174a95e47bb3825d37f1a17ec444e77cb0d9a9f8d84fc3368b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18338609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01259c3f0650f63d90ab059a30ce0d4187b80eed9b2096d792f73ec9f09b8d5a`

```dockerfile
```

-	Layers:
	-	`sha256:1307833e38266f6fe6d1bc99b023cb657024106b09a3d4c507051a046c2e56a9`  
		Last Modified: Tue, 02 Apr 2024 03:58:25 GMT  
		Size: 2.8 MB (2793004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04e4a1d2a95d00773f331e5e58ffdad927cd145ef7bf873c0cd02954bee6f315`  
		Last Modified: Tue, 02 Apr 2024 03:58:25 GMT  
		Size: 5.2 MB (5157679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d75f35238d44ffe1738630010553f303507a04948e02895236a7deb71de5ce`  
		Last Modified: Tue, 02 Apr 2024 03:58:25 GMT  
		Size: 5.2 MB (5159946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dcc51725d251e06f204664f6ae35ddf31c6843f382ee8c36e7b04bd453c7919`  
		Last Modified: Tue, 02 Apr 2024 03:58:25 GMT  
		Size: 5.2 MB (5159053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70a032833f2d623924bf2672eac3567d07ce1b0ec49915e7a755e888175c7539`  
		Last Modified: Tue, 02 Apr 2024 03:58:26 GMT  
		Size: 68.9 KB (68927 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:88104f1fba6a9ddc5760b155118c381b7ee8a01855f326915229cf41328f9e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103388770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267acf4d8e30884a2a570225914a90a4bd50d1fceed375c45a48ffc2d740bb19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Fri, 29 Mar 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 29 Mar 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 29 Mar 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"26.2.2","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@26.2.2?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 29 Mar 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.1
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 29 Mar 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 11:05:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.13.1","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.13.1?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 29 Mar 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 29 Mar 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 29 Mar 2024 11:05:22 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Mar 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 29 Mar 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:ec9849f84ea05dcddad3aae1dad17f2f49b3b950c39945bf0207824781a4dc58`  
		Last Modified: Tue, 27 Feb 2024 19:00:28 GMT  
		Size: 34.5 MB (34493757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca16aa7689eb171fcfad22a1ef84bc8fbcc3ea2067ca88b76c9360c1231ff721`  
		Last Modified: Tue, 02 Apr 2024 01:49:15 GMT  
		Size: 39.6 MB (39560094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9a07008ff072319a23e78c8f241a1eba7d20c7b0b508814a6d55de44f39d4e`  
		Last Modified: Tue, 02 Apr 2024 01:49:13 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947f5ec2147f390193eb8845045c856b5d3e8d56e7f6c4d91b6b39b77ee0df56`  
		Last Modified: Tue, 02 Apr 2024 01:49:14 GMT  
		Size: 7.9 MB (7857063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596255a162aa31d3fe0b18be402dc5daebde9c6a6f69b17e2678a4c0706acc15`  
		Last Modified: Tue, 02 Apr 2024 01:49:13 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374b475c898f501e3398baf9485dbd9cc706f8711783a5417086c59dd2368bb5`  
		Last Modified: Tue, 02 Apr 2024 01:49:14 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e819eddee9b855dd33bb5d8ce9a240c1b13e3360d67edd913c14b9d16d049e3`  
		Last Modified: Tue, 02 Apr 2024 01:49:16 GMT  
		Size: 21.5 MB (21464664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869ec227598527de28ba2e0b6d71901757d2ccb6bb44e8ba569022553f8a15a6`  
		Last Modified: Tue, 02 Apr 2024 01:49:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721ae1fe1f8483de34bbb2d272c65de8bd7cd289274d079bc7fb20dddbabc3f2`  
		Last Modified: Tue, 02 Apr 2024 01:49:15 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a9e1ac41c02f3c9854c114ed055bf6404ba2b7a5723fbf44b80e78a028ee24`  
		Last Modified: Tue, 02 Apr 2024 01:49:16 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df8769c32c1770387f93559d10db6d6fda9e598aee997693f1fe8b3de5a3eae`  
		Last Modified: Tue, 02 Apr 2024 01:49:16 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4c2a83b864bd369b9776f669c60a1a54d594a8b9f561cb3d2975399553cdfa81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18238886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef2e3e9e8524d8ce5067373b88a0879a4924fe3897a505e6d9e50761daffb88`

```dockerfile
```

-	Layers:
	-	`sha256:84acfbf3442ec92c16c7a540e803733362e640402515e67c1643c11e80ef0fce`  
		Last Modified: Tue, 02 Apr 2024 01:49:14 GMT  
		Size: 2.8 MB (2797166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7df9692007c39dd16ec59fe0581a63f5e31309e27d3e4b781f0aefe3c9d4e549`  
		Last Modified: Tue, 02 Apr 2024 01:49:14 GMT  
		Size: 5.1 MB (5123034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a64ea8c6411281a5a5955236cadf4cb3623ab38d8fc99f5a45ec4a500b86960e`  
		Last Modified: Tue, 02 Apr 2024 01:49:14 GMT  
		Size: 5.1 MB (5125301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41e824a7bcd8bb97fd13544f62c14c257a87c11ce286074767b9f5a7c664e07d`  
		Last Modified: Tue, 02 Apr 2024 01:49:14 GMT  
		Size: 5.1 MB (5124408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04e2e545fac636286778a0ee057d0b485ae437a67380e50e067d5ef5b19fe27c`  
		Last Modified: Tue, 02 Apr 2024 01:49:15 GMT  
		Size: 69.0 KB (68977 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:de7bf3c44bdfe2d72c7b16f5e5ac9610cd89e4baa9d0fece74f80ab241538cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94245469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898b9cf4f6e6fac5ccc341c58b02eb71644a6253bc396f7b0171fd6813cbbc10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Fri, 29 Mar 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 29 Mar 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 29 Mar 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"26.2.2","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@26.2.2?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 29 Mar 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.1
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 29 Mar 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 29 Mar 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 11:05:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.13.1","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.13.1?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 29 Mar 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 29 Mar 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 29 Mar 2024 11:05:22 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 29 Mar 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Mar 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 29 Mar 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:137c4868f69560c0e626198e084a56f05d140f3ac9de35f029d58db50ee2bdd3`  
		Last Modified: Tue, 27 Feb 2024 19:00:35 GMT  
		Size: 28.0 MB (28011097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1391d90d1565340b6ff80f22253474ac7c5b3894e9dd329241c8f70bea882890`  
		Last Modified: Tue, 02 Apr 2024 03:14:47 GMT  
		Size: 38.2 MB (38202947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6b3e83e464510e5b4422ef2b374ce22223c9c6802fccb7cf5c5fe7443b6b7c`  
		Last Modified: Tue, 02 Apr 2024 03:14:46 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b40ce496f8ff2190b0814693b9015ddd102f620dff90d0d1eadf1144b32fe71`  
		Last Modified: Tue, 02 Apr 2024 03:14:46 GMT  
		Size: 6.5 MB (6523608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39871bf60e25fb6d393ea0dd23345f6d65baa55f2830cd635a51a9c7580e18e2`  
		Last Modified: Tue, 02 Apr 2024 03:14:46 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec81e8d57a4cd04a0058141283ef22c1736e8fe6700c6f34c969838145f3864`  
		Last Modified: Tue, 02 Apr 2024 03:14:47 GMT  
		Size: 10.8 KB (10778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6640cd12f0aae67d22210a4e91d637b3657c68419bbf110b95583b3fa46d4c38`  
		Last Modified: Tue, 02 Apr 2024 03:14:48 GMT  
		Size: 21.5 MB (21494510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff180c3b1da557c9625c664d360bcbed04500562a3e093cee3007c06e6162fb8`  
		Last Modified: Tue, 02 Apr 2024 03:14:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47af0f69a3e3e421cae886c283128f0541de6a2b400a5c84f1eb715b1e59a5d6`  
		Last Modified: Tue, 02 Apr 2024 03:14:48 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cc8a0ed8b645562cf80098a65eeac62bdc2810d627512b4de503ef43ea7b9b`  
		Last Modified: Tue, 02 Apr 2024 03:14:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109f3f61566ec632ca36a609aa086ae6015ff3aebc7fcf9a14772a77f9a5dc5b`  
		Last Modified: Tue, 02 Apr 2024 03:14:49 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5e53338550c8fc9162a6a74d00442b2ff6cb499812b4e8f91ed435deece561b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17880004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1006c478ad464547144fecafeffac0bb45a32c1a7804cadd06e99a0c390e2274`

```dockerfile
```

-	Layers:
	-	`sha256:9dba662d635a7cf7d05975eafe33cefd547c4276c74891250900c82ef604e493`  
		Last Modified: Tue, 02 Apr 2024 03:14:46 GMT  
		Size: 2.8 MB (2795016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:119f0cc8ef5d6c0915ea0456ae1ddb10b0093c5d4410ce693fd2421dc5945a53`  
		Last Modified: Tue, 02 Apr 2024 03:14:46 GMT  
		Size: 5.0 MB (5004143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4d6b5609df0afbd32bc541a18938856722f0bed59e3da20a892af81829ef13`  
		Last Modified: Tue, 02 Apr 2024 03:14:46 GMT  
		Size: 5.0 MB (5006410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b300dc97c3bf142265473937e220e71ccd4e1d97efc6f46692e0bc485c02ee7e`  
		Last Modified: Tue, 02 Apr 2024 03:14:46 GMT  
		Size: 5.0 MB (5005517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d638328205f6f18aa128f6bfa47b0578ff3d927b7feaa567434b9e36dee057`  
		Last Modified: Tue, 02 Apr 2024 03:14:47 GMT  
		Size: 68.9 KB (68918 bytes)  
		MIME: application/vnd.in-toto+json
