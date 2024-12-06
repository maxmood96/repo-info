## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:bc58ab4267ede4af04bb36aac04512ea8615189334083c96101f4272d26cf644
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
$ docker pull rabbitmq@sha256:4f49e203fd8b733d1919c3f0c077ae013c5e29fc931e0bdf633155c316902c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107206771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05393889addde0efef8bde33f2f0c8cb6d15daf79a9838a48852f1d9076addaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Dec 2024 18:32:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_VERSION=4.0.4
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Dec 2024 18:32:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Dec 2024 18:32:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d127cefdcf70d9f8322bed0f3b7dbf33d6f959f5e895aa789adc52e3f6f26cbf`  
		Last Modified: Fri, 06 Dec 2024 01:35:41 GMT  
		Size: 48.4 MB (48375494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a48246b5e14ac7b9fee3aa8c6fe4f3a740ca5f2b95e3e0b2f41cd61e453233`  
		Last Modified: Fri, 06 Dec 2024 01:35:40 GMT  
		Size: 8.2 MB (8169250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8492123cbec944bce5ff92e55d7ae92da8b91cee642ab181fb004791ec05dcd9`  
		Last Modified: Fri, 06 Dec 2024 01:35:40 GMT  
		Size: 9.5 KB (9457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3117fdf1fd65a1bb1807f25e8cd431fa64dbcf78b560c81dc58708a19b819fc`  
		Last Modified: Fri, 06 Dec 2024 01:35:40 GMT  
		Size: 20.9 MB (20898853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f511652c5633b8608c43fac00accc05c2bc82379985688d0b38a07986f4ff`  
		Last Modified: Fri, 06 Dec 2024 01:35:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed77df65cf139fa4ee16485c4db249698b05d379cca3d5dc7c89647a82bb1f`  
		Last Modified: Fri, 06 Dec 2024 01:35:41 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93be3017f04ced38d4550444174fbce366e5d0b1cb0eff79c59cffb636dad980`  
		Last Modified: Fri, 06 Dec 2024 01:35:42 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99431079685f95b1289194083caa3d02e429d2f3aa92995b6f89c6f4adac01c8`  
		Last Modified: Fri, 06 Dec 2024 01:35:42 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:12ff2c3a099afd30d4d93e459f62c2819bbaa8afcf18add543df150b7576caa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18215276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df05791859a189cb6493f041ee177c399e3c193d272065ffa4549d68b918590`

```dockerfile
```

-	Layers:
	-	`sha256:56ff25d0d45793514c58d65abdb340b70ff01a7a3a5b2f2ebdc3daff80a8f4e6`  
		Last Modified: Fri, 06 Dec 2024 01:35:40 GMT  
		Size: 2.4 MB (2364996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eed5afd46fdb6194a8854285026ed3f522533001a4cbd494c7ab2039bf84f3b`  
		Last Modified: Fri, 06 Dec 2024 01:35:40 GMT  
		Size: 5.2 MB (5210935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb2bde9083a7a635c8637344ccba72981df3b7cdab9fca4586bb7f6ec525c68`  
		Last Modified: Fri, 06 Dec 2024 01:35:40 GMT  
		Size: 5.4 MB (5366934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3472500d7705e391788e2c385fd43535daaa7facad16379bac6de84fc951c097`  
		Last Modified: Fri, 06 Dec 2024 01:35:40 GMT  
		Size: 5.2 MB (5212669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59f7231b5d77989b224e6697b29ba60232ac5557f53d4e455c6421a0bc007a54`  
		Last Modified: Fri, 06 Dec 2024 01:35:41 GMT  
		Size: 59.7 KB (59742 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:2b6d0021a445f855d6e2c5ef14290f53686ef51ebf40e67ca12cc4f67a23b401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89754396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2555ba1dee0ae2f23f27717a74a7fee1ac9a3c4ceec394e541a77dda430e115b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:50 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:53 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Tue, 19 Nov 2024 16:18:53 GMT
CMD ["/bin/bash"]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Dec 2024 18:32:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_VERSION=4.0.4
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Dec 2024 18:32:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Dec 2024 18:32:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e8c2e8e27e2bb3c5d9361f48e5fe32e3edf8c259b6a6e1d18166066ff31b67`  
		Last Modified: Fri, 06 Dec 2024 02:20:23 GMT  
		Size: 35.4 MB (35405738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124e70c4ba80ad1cb800343eeeb799ad4a28443e37391464e2db23601ed0bb6d`  
		Last Modified: Fri, 06 Dec 2024 02:20:22 GMT  
		Size: 6.7 MB (6667937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583da24a66aa6268a5db06eb39785fb5f38c70254a3d949a03050e758f96c935`  
		Last Modified: Fri, 06 Dec 2024 02:20:22 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c448962540f2b242573569df4814f0ff5c0011379935b494f1239b4e02bcb5`  
		Last Modified: Fri, 06 Dec 2024 02:40:56 GMT  
		Size: 20.8 MB (20799799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391412fcb129f71c914722b9f76ee1092aba7386014922a5699381f08d7354f9`  
		Last Modified: Fri, 06 Dec 2024 02:40:55 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677dad2a39166e2905dd963443981f6a9976e53c0695e3a25c4350e2915db2d3`  
		Last Modified: Fri, 06 Dec 2024 02:40:55 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69abaa7173020e7c552552ae146aff7cc80fb71ea69f52c05f8993e90b8b459b`  
		Last Modified: Fri, 06 Dec 2024 02:40:55 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aceacba98dfbe2de0174641992338e48d2df93361dbbe1944cd62436ef799821`  
		Last Modified: Fri, 06 Dec 2024 02:40:56 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:dece755188ed0cc0f6e8341535ad363577565c1c6924d8526b245e761da85c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17676617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e846035d84e7d00da5fdd640c178029fc6ad7e2bbad3e1df585abb5c12cc21b`

```dockerfile
```

-	Layers:
	-	`sha256:945c335cd6a370b8aa399f63723d11065ad755c11bef1fc54984bdcaba6b4f95`  
		Last Modified: Fri, 06 Dec 2024 02:40:55 GMT  
		Size: 2.4 MB (2365797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3f5e17bf8cde2014b1b483ea508bbd4349d4fa8844673ea808df15d30d08b6f`  
		Last Modified: Fri, 06 Dec 2024 02:40:55 GMT  
		Size: 5.0 MB (5031901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c3a866c7b5c049e8a652a0d8ca6f44d499f374ff570fbb0533fbe40955665f`  
		Last Modified: Fri, 06 Dec 2024 02:40:55 GMT  
		Size: 5.2 MB (5185349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c6f500fa3c0dafa2c2edfcd1ab8cfe1e670be9d24dd28b44f9aa6b1e8469b54`  
		Last Modified: Fri, 06 Dec 2024 02:40:55 GMT  
		Size: 5.0 MB (5033635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c68b666cd1a5a6dcee20c8701296605e425ab9c3f0de1dedc063ad89f2ed7eea`  
		Last Modified: Fri, 06 Dec 2024 02:40:56 GMT  
		Size: 59.9 KB (59935 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:a79382319986506d1f6ecda9876e44b0766bae743fbbd9a24be6df01f872a312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105109594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9959269bddaf6467aa9ffd69df50c3ccaebb59b2d78ecce0e5143f714c10bbc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Dec 2024 18:32:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_VERSION=4.0.4
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Dec 2024 18:32:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Dec 2024 18:32:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740597fc6a68c4ee729191e34f2ebf5a05d885ec4b2f912408bed9b1211a5ea4`  
		Last Modified: Fri, 06 Dec 2024 02:25:04 GMT  
		Size: 46.5 MB (46462665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9150778600e5598e469c51f561b032f35fe78c17b15d1c012381424e258b4a50`  
		Last Modified: Fri, 06 Dec 2024 02:25:02 GMT  
		Size: 8.9 MB (8934206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8968a460661900aa75eabec4d574621f140e74bdf9361c3235738aa3b19cd8aa`  
		Last Modified: Fri, 06 Dec 2024 02:25:01 GMT  
		Size: 9.4 KB (9433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a963e7741e4fd9d0700df46e32a58df453e60104e340c0a62cf0789d3581aa5`  
		Last Modified: Fri, 06 Dec 2024 02:33:28 GMT  
		Size: 20.8 MB (20808878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe14e7e8c1022ef2a5149704ea03356b2833d8e7568d862e1c4d1d748d45bb1`  
		Last Modified: Fri, 06 Dec 2024 02:33:27 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076635c168659af47a1883552879e03b8cb1305e3df6b591822a55f7478f44c3`  
		Last Modified: Fri, 06 Dec 2024 02:33:27 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4e5dfc84f96631f77b404aa70e3c1fa6896f3726d8c9c701cda2065d387b0c`  
		Last Modified: Fri, 06 Dec 2024 02:33:27 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45b99a965c23969055a5caf7f8c35d83435f456ab84c4a533835e0d9884befb`  
		Last Modified: Fri, 06 Dec 2024 02:33:28 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2b0d74065e6172304126458cbfda608b7c66d9e20ccdc65a0086da8ceb05534f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18275450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489828fba0f0224eec3af41490e1730bd843f4a581230dd232f6b1e8d834d115`

```dockerfile
```

-	Layers:
	-	`sha256:b53b2c45e9749e8a67aa609c16992b6f8b36d56a379678cbd3e4441b4eabd548`  
		Last Modified: Fri, 06 Dec 2024 02:33:27 GMT  
		Size: 2.4 MB (2366056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa54d89082ca96be8e393180536c9c8f191389f55d1f3370599e23e5d97bb343`  
		Last Modified: Fri, 06 Dec 2024 02:33:27 GMT  
		Size: 5.2 MB (5230554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b20314e63e3f21bb9189a15448593feff400a172aa0d9647268c9a1d37d6a7`  
		Last Modified: Fri, 06 Dec 2024 02:33:27 GMT  
		Size: 5.4 MB (5386571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9ce840a8f7b04f6dc5b73de00434fe54260e41fc2d445d82bb860bc7463bbcd`  
		Last Modified: Fri, 06 Dec 2024 02:33:27 GMT  
		Size: 5.2 MB (5232288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a9565287df4d3d73661c10871edccaba7cb418be6d7c862ae92b4788aa3293f`  
		Last Modified: Fri, 06 Dec 2024 02:33:28 GMT  
		Size: 60.0 KB (59981 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:196ff721ae74be652516414d75422aec01385b4fad9a6e6610ae6773ef883b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105556078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c4fa88042564fd8b7f641fc2974b4fca0a9e3a9b973543c5d347a1469e5b58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Dec 2024 18:32:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_VERSION=4.0.4
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Dec 2024 18:32:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Dec 2024 18:32:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e7f01e011ebfa2050f5dd304ed8e94a609fc1884948a74d8a58c4cbe550da8`  
		Last Modified: Fri, 06 Dec 2024 02:29:21 GMT  
		Size: 41.6 MB (41606764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c010a6323c76ffe986f86f11f9448ceb936176d0c7d3872e9c54f626d87a09`  
		Last Modified: Fri, 06 Dec 2024 02:29:19 GMT  
		Size: 8.7 MB (8689223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aee11cc06f45fc540a5da743a42a20fa2b39ad1744ba3b588625dd8f9dbbf1`  
		Last Modified: Fri, 06 Dec 2024 02:29:18 GMT  
		Size: 9.4 KB (9436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0fd606452981b5d4f2df3dd50cb47f202222898406f68b1d62791245afee1c`  
		Last Modified: Fri, 06 Dec 2024 02:39:03 GMT  
		Size: 20.9 MB (20860088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29fa99ba4bef7d5da4729e359a535ea366eec4296552631337788c557708308`  
		Last Modified: Fri, 06 Dec 2024 02:39:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9c013d01314ee93079f4e980063b65410dbdff7f56cb5cded8b115339d90d2`  
		Last Modified: Fri, 06 Dec 2024 02:39:02 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7352a6cf0e3340282f4eb3d2eab6de3e27ef4fc0746f9b196bcc978bc43f6f0b`  
		Last Modified: Fri, 06 Dec 2024 02:39:03 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2e7e8ed5f27a9588f68a54350e3e7758789df84be093cba14a32da2370acef`  
		Last Modified: Fri, 06 Dec 2024 02:39:03 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:17a6aff1e8495f5c88a1f67062d840b72c6cce4872a4c699c61f53e496752c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18131608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df315c516dd16ff54932cee764faf5bf8908672c2ac3258275072b16131b945a`

```dockerfile
```

-	Layers:
	-	`sha256:d4b5faae2879cf62d9d0a2ff3cb8dfd98f3a3fde80dd006f28d3c5924dc46978`  
		Last Modified: Fri, 06 Dec 2024 02:39:02 GMT  
		Size: 2.4 MB (2369350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd4a404141501ad157f4b3cd6be014c42f01a15028832b7671bc727beb57d716`  
		Last Modified: Fri, 06 Dec 2024 02:39:02 GMT  
		Size: 5.2 MB (5181564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:699679b38f2e758c6511a49bb001ecef892ea5633a0628a48973e232b0455a6e`  
		Last Modified: Fri, 06 Dec 2024 02:39:02 GMT  
		Size: 5.3 MB (5337593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5c741a95703006c2f4e3de51ad9d93a5ca6ad0cf8c3cd95033c2cd2609f5049`  
		Last Modified: Fri, 06 Dec 2024 02:39:02 GMT  
		Size: 5.2 MB (5183298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23259b218a90aa19fa947b8ae4ce2c10d627610d4b05273c721777178a56a056`  
		Last Modified: Fri, 06 Dec 2024 02:39:03 GMT  
		Size: 59.8 KB (59803 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:b20018eb8383c7d90f4443277fe41614e2f52fa85aa09be0e9ba280189439f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98840543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e895de8a94b84498c6c7813d2c6a2d2bddfe6f96ef5f0daee82338ec462d8230`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 16:33:48 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:33:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:33:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:33:49 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:34:25 GMT
ADD file:23c2e341d6cf3572f2762ef1304c406cf6d4f5ee8ee8719ef289a3b75a8323aa in / 
# Tue, 19 Nov 2024 16:34:27 GMT
CMD ["/bin/bash"]
# Fri, 22 Nov 2024 21:01:04 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Nov 2024 21:01:04 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Nov 2024 21:01:04 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Nov 2024 21:01:04 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Nov 2024 21:01:04 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 21:01:04 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Nov 2024 21:01:04 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 22 Nov 2024 21:01:04 GMT
ENV RABBITMQ_VERSION=4.0.4
# Fri, 22 Nov 2024 21:01:04 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Nov 2024 21:01:04 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Nov 2024 21:01:04 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 21:01:04 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Nov 2024 21:01:04 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Nov 2024 21:01:04 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Nov 2024 21:01:04 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Nov 2024 21:01:04 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Nov 2024 21:01:04 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Nov 2024 21:01:04 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Nov 2024 21:01:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 21:01:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Nov 2024 21:01:04 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Nov 2024 21:01:04 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:0dcc8c973ba119a0fb5275114fd0456179bba1132bdc69f2afa4e1c4a235c540`  
		Last Modified: Tue, 19 Nov 2024 17:38:52 GMT  
		Size: 31.0 MB (30980838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75404d683300b91e8aab96e1252dd1849402996128448a7cdc2dd951f9365b12`  
		Last Modified: Tue, 03 Dec 2024 08:36:43 GMT  
		Size: 37.3 MB (37252990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdc9d1a47cbf76cd0fbf8186f478257776fd834d8fa883f704a97502dfc77db`  
		Last Modified: Tue, 03 Dec 2024 08:36:39 GMT  
		Size: 9.8 MB (9783398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32ac3d43ae011e477292914aa44bc52000d679c962d69b1bb3f770bd7bc741d`  
		Last Modified: Tue, 03 Dec 2024 08:36:36 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01ba0243d423782c540a92fcbba64e9bca1d06f3cd73363825945faf844bb38`  
		Last Modified: Tue, 03 Dec 2024 08:46:14 GMT  
		Size: 20.8 MB (20812067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a981a68baafea19f0e6a9598b14c26b7006dce00acd9d66e1e349b35828626`  
		Last Modified: Tue, 03 Dec 2024 08:46:11 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb33642c53c1c3846b218092d52975dcced7f142c9ce431e936c42c9905a67f`  
		Last Modified: Tue, 03 Dec 2024 08:46:11 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ab0bbb951028572e580543554aba9a6a39983d94f930568d2585a87be9e392`  
		Last Modified: Tue, 03 Dec 2024 08:46:11 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c45a64251e115dfc7238c1d70679aa1d1987c8dc618003237615093ec706b0`  
		Last Modified: Tue, 03 Dec 2024 08:46:12 GMT  
		Size: 836.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:122cb1b74a3bd95babd097580ab7883670b1ada0cc74bc752325797c8264ec3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18090128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4517c91341343edabf2558228ef964ed4fb82270904f5177e2e2ef6b47be39`

```dockerfile
```

-	Layers:
	-	`sha256:02046ea30d2e5c1d99d582de21f2a73b423eae4466600108c9452f691dea677a`  
		Last Modified: Tue, 03 Dec 2024 08:46:11 GMT  
		Size: 2.4 MB (2357584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39c0624de10572bad554db1339d9798efd7135aa3bc0935a71985f31ec270ba7`  
		Last Modified: Tue, 03 Dec 2024 08:46:12 GMT  
		Size: 5.2 MB (5172520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22392cc275e0ccde9ee1d780cbbda10f19de6fff8abf804d3bd38cd4061563e`  
		Last Modified: Tue, 03 Dec 2024 08:46:12 GMT  
		Size: 5.3 MB (5325966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12b25bd3c0f8bdd6e036ab06a483c04c75e7e928f332f2affd68c8ef951d75e7`  
		Last Modified: Tue, 03 Dec 2024 08:46:12 GMT  
		Size: 5.2 MB (5174254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:690517e34b87e759db4c34b0817fdfff96b8518b8c8bf591bd235e925832a6d4`  
		Last Modified: Tue, 03 Dec 2024 08:46:12 GMT  
		Size: 59.8 KB (59804 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:596e3b54be05c8c618341f574caf00cca4f53e2b6d13faa31ebb9d6255b6aaad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99160647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a10ba8390d7ef8390632dbfd90f043203373dacbfe9bc4910cab865a7db7762`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:14 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:16 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Tue, 19 Nov 2024 16:18:16 GMT
CMD ["/bin/bash"]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Dec 2024 18:32:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_VERSION=4.0.4
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Dec 2024 18:32:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Dec 2024 18:32:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7299cedc00fbf6a9b0fa09b2e6cf4427569320893465272dfea2271e194be9b`  
		Last Modified: Fri, 06 Dec 2024 02:21:31 GMT  
		Size: 40.7 MB (40698916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d819b79daad17252ee433d840bcbe14223ef09c10b704b373a54067b6a7b5857`  
		Last Modified: Fri, 06 Dec 2024 02:21:30 GMT  
		Size: 7.5 MB (7546317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00c8a1753fcca9bc1d56db39dfe13c447cef5a31547d0038dd8316e993981e0`  
		Last Modified: Fri, 06 Dec 2024 02:21:30 GMT  
		Size: 9.6 KB (9582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e75011b922c775cadf9db0170997b30ef19187e5c8e72436c823aa3355edda2`  
		Last Modified: Fri, 06 Dec 2024 02:32:30 GMT  
		Size: 20.9 MB (20883261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d0fab7ab421f6d0802344cc0ef92241dc92949f459e90db189fc061f2aeef6`  
		Last Modified: Fri, 06 Dec 2024 02:32:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93b908db5a6e337912e4a06f0de2aa176cb2c2507603127d93c84cf6f42a7f0`  
		Last Modified: Fri, 06 Dec 2024 02:32:30 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ee754c9e17413c0c7510be13784e5e634fe91507712f5981a494af2e89aba9`  
		Last Modified: Fri, 06 Dec 2024 02:32:30 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b431e5ebb651147495dfeb5a92a7cfd624f57764006e04e3afc0594e9a7a5d`  
		Last Modified: Fri, 06 Dec 2024 02:32:31 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fdd40bea8e8525027fe9bd06a2ac56eb5ed6997b9db00360e6902e5a0bdb45e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17763111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39533950cd5c004141b89fdc701b27c5674ec5968ffe821ff12d04bea22510b9`

```dockerfile
```

-	Layers:
	-	`sha256:9cf03474757fb40a56b1d709dbbaf44421c3ff6b86bb50cc2adc7f9caafc1a73`  
		Last Modified: Fri, 06 Dec 2024 02:32:30 GMT  
		Size: 2.4 MB (2367848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d06b13fe55bfd5b969bd19e70a2c230e611e54571d791bea26b77aa9992a187`  
		Last Modified: Fri, 06 Dec 2024 02:32:30 GMT  
		Size: 5.1 MB (5059263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7445e906c6612d2ce24d5616f6f596c83b08244714a620a186edd7862e1f6ebe`  
		Last Modified: Fri, 06 Dec 2024 02:32:30 GMT  
		Size: 5.2 MB (5215262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0d048db21f7e4c7e55dc9da9bad04781a27e9ba2541447847a324dde9db926e`  
		Last Modified: Fri, 06 Dec 2024 02:32:30 GMT  
		Size: 5.1 MB (5060997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e5e7892bdf2f2df4d8a53f459f856994b162fb71bac6bb5659359b125b96f5`  
		Last Modified: Fri, 06 Dec 2024 02:32:31 GMT  
		Size: 59.7 KB (59741 bytes)  
		MIME: application/vnd.in-toto+json
