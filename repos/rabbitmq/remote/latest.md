## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:1f5970642b6ecce21c6a875069ab6796f86cdecc65f2651ede3b23b6b2f8616b
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
$ docker pull rabbitmq@sha256:a7337176ee2da6cd45bf0f1fe38a5b9f06fd32c58e838be458389490b5f08e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106650298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd22d53bb61de6563237d3e112f907130873a93c3860da8fc4b1b97260cd749a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 00:38:01 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 19 Sep 2024 00:38:01 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 19 Sep 2024 00:38:01 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_VERSION=4.0.1
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 00:38:01 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 19 Sep 2024 00:38:01 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 19 Sep 2024 00:38:01 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 00:38:01 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 19 Sep 2024 00:38:01 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba57eb073d4f2fc914506854b1cf9f9592525a2c8ee5785c54cfc1f0c9d3022`  
		Last Modified: Thu, 19 Sep 2024 19:04:34 GMT  
		Size: 45.4 MB (45447870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a23a82ef0dc06b2f13dd36916cfdf9bc78a04391b73654609fc7b9be035b47`  
		Last Modified: Thu, 19 Sep 2024 19:04:33 GMT  
		Size: 8.2 MB (8169252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236ec1c441f08abd6ebb3be39dd2ab463bc8d9689407be7758abe32545fa06e2`  
		Last Modified: Thu, 19 Sep 2024 19:04:33 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2147aa0ab326bde867e900abfeb77e64f8ce51463a133ce8cb6de5f5ba4077`  
		Last Modified: Thu, 19 Sep 2024 19:04:34 GMT  
		Size: 23.3 MB (23272153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5dc71dca897dbaf7d50feb431f1c366d6c48c24f53681ff9dc67c1dc4523fd`  
		Last Modified: Thu, 19 Sep 2024 19:04:34 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76fef37674d06f6a52380be09734de7d60c8efa098815438c3bea497e058d2a`  
		Last Modified: Thu, 19 Sep 2024 19:04:34 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7ea9bb53f563d7a75a9ee1e9fde906cd935ec0ca146042ebbb8be45104d4ac`  
		Last Modified: Thu, 19 Sep 2024 19:04:35 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a61e1737481d01a7be243face43b40bb5dd1a12d0a91da4dd62674ef6e67c7`  
		Last Modified: Thu, 19 Sep 2024 19:04:35 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a7724702d9a5fbc9cc90fd17fc2c14d8db8bfb6f4411fcfdd00fb6d9bf78a4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15774683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6575d755229eac61552e7fabdb4cd2febbab26dd8f909fb0579f50276360fbea`

```dockerfile
```

-	Layers:
	-	`sha256:fe62d5f8708fe604c77f86a89c18a69a325aa5a9a2e1196066683bb8e3c7e899`  
		Last Modified: Thu, 19 Sep 2024 19:04:33 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f7e0c3edd11d642ad18ce050ff2a8b86f83b5344710f05fb50fe21f7890d45`  
		Last Modified: Thu, 19 Sep 2024 19:04:33 GMT  
		Size: 5.2 MB (5189949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cfb93759cf1c303d53e58714d4622a50154abba057216a776ae84596387acd6`  
		Last Modified: Thu, 19 Sep 2024 19:04:33 GMT  
		Size: 5.3 MB (5330046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05609b1c0453f07b70c4c340e2eb5821defab5087c59247b52bae23d23b9568f`  
		Last Modified: Thu, 19 Sep 2024 19:04:33 GMT  
		Size: 5.2 MB (5191471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9643fcdf3b29dc29b2d05a8f1f805f9f91abc7de2e2599cc56429e1dfcad126`  
		Last Modified: Thu, 19 Sep 2024 19:04:34 GMT  
		Size: 61.0 KB (60984 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:51f5f3c4c281f48d6641f34dff83542673262d871e0ab5420420e4f4c6ebbe7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89222315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248eec3854017ec54d59cb45e0bad9e97c50984a7684b28c45d7d25b92c09284`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:10 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:14 GMT
ADD file:0efc83f80e5e3a9125a702063e487f836d2e0ff9a88f4d0330897d15e445d415 in / 
# Tue, 27 Aug 2024 15:55:14 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 00:38:01 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 19 Sep 2024 00:38:01 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 19 Sep 2024 00:38:01 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_VERSION=4.0.1
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 00:38:01 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 19 Sep 2024 00:38:01 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 19 Sep 2024 00:38:01 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 00:38:01 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 19 Sep 2024 00:38:01 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:eb7e9efa9f9d063fec8aeb787b87620ae79d524925cdea2e8c267bdd96cac928`  
		Last Modified: Tue, 27 Aug 2024 17:08:17 GMT  
		Size: 26.9 MB (26865525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4eb81e19e008def654bc092bd0d34a7142120758f6c1873d7331d0b0208501c`  
		Last Modified: Tue, 17 Sep 2024 02:20:37 GMT  
		Size: 33.1 MB (33120962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2502431ef7910f292e4a9d0f7bafe973a91014cb350260b862949a61079181c1`  
		Last Modified: Tue, 17 Sep 2024 02:20:36 GMT  
		Size: 6.7 MB (6667920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cfd9a54b206afb355157305e502e6219ef454b804062b9fc26eb99f2c73d72`  
		Last Modified: Tue, 17 Sep 2024 02:20:35 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42159aec2f7490fdf00115648ef3164570405d9f6e377f8f95e309b87b2cd74`  
		Last Modified: Thu, 19 Sep 2024 19:09:58 GMT  
		Size: 22.6 MB (22556635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286a5eedfde9cb8dabd8417b511d7e909b30c856661cb74d70749e4e0351f684`  
		Last Modified: Thu, 19 Sep 2024 19:09:57 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaad7d27c9e88bf2e7645cb9ca4eead103fbf39ed4864bcd68605921a8f52031`  
		Last Modified: Thu, 19 Sep 2024 19:09:56 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297b34bd5e7cbc7c715ee6beb98d3312638ba0edf28ea8de21747b2c1e47790e`  
		Last Modified: Thu, 19 Sep 2024 19:09:56 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fac3c593d7f11293b09acf646bf49d0d4ef6daa0dbaae4fc8e161cb0dd81f6`  
		Last Modified: Thu, 19 Sep 2024 19:09:57 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:44f29ac830b276e1cc7c1c5ce13e72464dc097f618a699b36b5ed4de6607e562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17579704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c67200053298e21eb1e2c532dea4ce5d187fc201a64bea49b04cbc4e3b7d332`

```dockerfile
```

-	Layers:
	-	`sha256:b3d98949a20f3dd662e69165ffefcfb65e55982e0b13b4d9386678fd6552b842`  
		Last Modified: Thu, 19 Sep 2024 19:09:57 GMT  
		Size: 2.3 MB (2344036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4deee5ed65c10bfaed67d30b3ea268892edd24638a392098c0256cd239227245`  
		Last Modified: Thu, 19 Sep 2024 19:09:57 GMT  
		Size: 5.0 MB (5011671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4fe12781ce44eeb392cdda469a05d537e89b4c2f01e29548b69ed53d195ccb`  
		Last Modified: Thu, 19 Sep 2024 19:09:57 GMT  
		Size: 5.1 MB (5149633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5adafc4f9df37ecef63daa0aba92d194c5e3fc72248e18345b31cdcf90ec53b`  
		Last Modified: Thu, 19 Sep 2024 19:09:57 GMT  
		Size: 5.0 MB (5013193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56512789d1388801db59fac24c23a73bb371d9925813cf71ec7ef8ddc7f9db3d`  
		Last Modified: Thu, 19 Sep 2024 19:09:58 GMT  
		Size: 61.2 KB (61171 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:cd2342e7d3bdaaef79a0fbb75c82c52c61c07ba8254c20ebed6ed43b330cf693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104304715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284ed050092333846089ede4389151e37742f32b8b7b0f5ed48f45b6b8422a88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 00:38:01 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 19 Sep 2024 00:38:01 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 19 Sep 2024 00:38:01 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_VERSION=4.0.1
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 00:38:01 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 19 Sep 2024 00:38:01 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 19 Sep 2024 00:38:01 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 00:38:01 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 19 Sep 2024 00:38:01 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547eca683c77aeb4ceebef69bb98a6942657d60ae733bcacdaae0cdbad28807b`  
		Last Modified: Tue, 17 Sep 2024 02:49:01 GMT  
		Size: 43.5 MB (43478555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f39ec5e5d2461e710e856c8c1d09a2a7319d3853b0a46b176fb4442c790cc6`  
		Last Modified: Tue, 17 Sep 2024 02:49:00 GMT  
		Size: 8.9 MB (8934211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e0bc84bde268a3664b171f86ac3f88246c88ab0b7b8929bfea1302fcca833`  
		Last Modified: Tue, 17 Sep 2024 02:48:59 GMT  
		Size: 9.5 KB (9465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bd47ca1467474a982046c967be23f42c0ba20b5f5a9e0428caa000f352baa6`  
		Last Modified: Thu, 19 Sep 2024 19:11:15 GMT  
		Size: 23.0 MB (22995138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68e9704dbd766a0b52dcea547e279f9f09f386344d954024edfb68a27a30ea5`  
		Last Modified: Thu, 19 Sep 2024 19:11:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544e672b91a332622e1162b0278090369bfa3080662459b589cdb227a8482434`  
		Last Modified: Thu, 19 Sep 2024 19:11:14 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d2350997680fdea61bb59b6c87d20f6b6a1e34fb2f3a07d7aaeb71c44335ba`  
		Last Modified: Thu, 19 Sep 2024 19:11:14 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455ca336a3f9c5f1c1725658d4ef5468cdd097151cdbb7131d2a6c330c4ac5ea`  
		Last Modified: Thu, 19 Sep 2024 19:11:15 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cd5fdd02c974abfd6473677081989cec64eb66778896e84419e075ac4ba846a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18176037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f382d5d8d54d4ff8b725687b4ab55e3bbf0e192226488acf0efcf0ac184520`

```dockerfile
```

-	Layers:
	-	`sha256:a63ba561826b470d6cbf6b309cd1c92e9595eca98783ef10f806e235cb2831df`  
		Last Modified: Thu, 19 Sep 2024 19:11:14 GMT  
		Size: 2.3 MB (2344087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e1efe4135415087734886f364bb3bdbc0574c63f579371924a28d96ba3c4d9`  
		Last Modified: Thu, 19 Sep 2024 19:11:14 GMT  
		Size: 5.2 MB (5209676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73137069a329dbddc617f34fffc1058fe80f15371fabbc714af8811c56b5080`  
		Last Modified: Thu, 19 Sep 2024 19:11:14 GMT  
		Size: 5.3 MB (5349791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:435cc2e19a95e7694186406d038276413de9a274b0c34c49d84f069da5e17960`  
		Last Modified: Thu, 19 Sep 2024 19:11:14 GMT  
		Size: 5.2 MB (5211198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf2b62103e371fe52cdb6e30db3e48cd681591d88a16822b3b19c72b2b9df03`  
		Last Modified: Thu, 19 Sep 2024 19:11:15 GMT  
		Size: 61.3 KB (61285 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:7770f4a8f7fd3feb57c5c11b7907bdc85a5fac66d31f175a8173c53afb9d1acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105700775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e107424e6f67963457b47f2446212f1df1b3066f5be75a05c56a3447082fc4cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 00:38:01 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 19 Sep 2024 00:38:01 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 19 Sep 2024 00:38:01 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_VERSION=4.0.1
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 00:38:01 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 19 Sep 2024 00:38:01 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 19 Sep 2024 00:38:01 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 00:38:01 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 19 Sep 2024 00:38:01 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c526398e5e771684dae49961d5a74cd9606dcbcf7ddafb1fcc1433293927dca4`  
		Last Modified: Tue, 27 Aug 2024 17:08:24 GMT  
		Size: 34.4 MB (34392345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae12c93b42b1f5880b2b7fdac9201786e362f11134a3011163fbf779bc63a0c`  
		Last Modified: Tue, 17 Sep 2024 01:59:54 GMT  
		Size: 39.2 MB (39155450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df1a7bb15f08cf4f1e98ca99d7b0cfce8bc13361fc57368b06d089d4089f948`  
		Last Modified: Tue, 17 Sep 2024 01:59:53 GMT  
		Size: 8.7 MB (8689238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39128545dcc5b74866a4c37ac73cd13dc7bdeb526be46bbcbfd80816da7eee3`  
		Last Modified: Tue, 17 Sep 2024 01:59:52 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973eb3be9b603da528c2de92b7372f20181d4909ea923eb0421af65a42acbe80`  
		Last Modified: Thu, 19 Sep 2024 19:17:22 GMT  
		Size: 23.5 MB (23452607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd005688363b2a40542e76d0b3883cb01d5cf231e99ffa026091a2653d8166f9`  
		Last Modified: Thu, 19 Sep 2024 19:17:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6068349ec027da91a3a181e4bbf2347064c84fd50e59ca806390221ecadaa4fd`  
		Last Modified: Thu, 19 Sep 2024 19:17:21 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5497cd998f530d761c42fb70abf2151337d1c577cd66efaa8d734d3267f291b5`  
		Last Modified: Thu, 19 Sep 2024 19:17:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28e66bb8131aa067363ce6bbfb7b36e9033ab13956972d58ef58d8aa151cb97`  
		Last Modified: Thu, 19 Sep 2024 19:17:22 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6a54d839dac78fc081dd522718c7c3a7f17f38aae533fd5e2b964c98988f4ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18032776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe0d575d28a13257e1921c9722ed3dca046e7a3c4e067e47dcb2a871fa7be04`

```dockerfile
```

-	Layers:
	-	`sha256:fe93567404e68fd0f988f7df15afbfc9fe3ad95cbb938b7aca50d3c98fdcbe05`  
		Last Modified: Thu, 19 Sep 2024 19:17:21 GMT  
		Size: 2.3 MB (2347381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6233549e8d02486a822d6bc0b1abd182e0a030377ac5122a16309657b5b5d1fa`  
		Last Modified: Thu, 19 Sep 2024 19:17:21 GMT  
		Size: 5.2 MB (5160902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:272b0d6de882bb581f8055cf06b42112b9d9b2da693ebef7258938f87841947b`  
		Last Modified: Thu, 19 Sep 2024 19:17:21 GMT  
		Size: 5.3 MB (5301029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84430f033e5735999b708b3946f5b3a07912fa3906dc24882769cf5ffb6e4149`  
		Last Modified: Thu, 19 Sep 2024 19:17:21 GMT  
		Size: 5.2 MB (5162424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea4486328bdd73930662ece1ddad2932d7ff67991b63dadf1279931526b5bd7`  
		Last Modified: Thu, 19 Sep 2024 19:17:22 GMT  
		Size: 61.0 KB (61040 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:1c4e2160af4162bdecd5dab6d84c12178f38842028d271fd564a53ff317da3a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98575815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6bbd942a0701693607c580a8d89e45eda04b886f742c68989fbbbe161c71cc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Aug 2024 16:13:45 GMT
ARG RELEASE
# Tue, 27 Aug 2024 16:13:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 16:14:17 GMT
ADD file:93d9ee7cf8a421a6d4ab56202ff743dbe7e87beb3d3c9bc1cebb49cf8e1ae4a7 in / 
# Tue, 27 Aug 2024 16:14:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 00:38:01 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 19 Sep 2024 00:38:01 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 19 Sep 2024 00:38:01 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_VERSION=4.0.1
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 00:38:01 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 19 Sep 2024 00:38:01 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 19 Sep 2024 00:38:01 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 00:38:01 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 19 Sep 2024 00:38:01 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:651d7149a766bf9e12f26204ac9f977fa21fa3adbb24c0d2746c0b1cb99c8924`  
		Last Modified: Tue, 27 Aug 2024 17:08:30 GMT  
		Size: 30.9 MB (30949308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d857a6a002e9fecd6c4fed15dd85c6c7febaf7a9149e5bfadbaf083cdb1e07`  
		Last Modified: Tue, 17 Sep 2024 04:04:36 GMT  
		Size: 34.9 MB (34941624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3d855f63fbc2dd7c0b7c0fd227bc9b480c4c82882cc5851ccb86f32a8d8b28`  
		Last Modified: Tue, 17 Sep 2024 04:04:32 GMT  
		Size: 9.8 MB (9783464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d0a2d7021dda83a82ae4161fb70a188abe40d0fedf8146ec44e3a74d59a944`  
		Last Modified: Tue, 17 Sep 2024 04:04:28 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397efe14ce001a29631e867e6fa05a8d9d807abf6a54082effb00d17e9909738`  
		Last Modified: Thu, 19 Sep 2024 20:12:06 GMT  
		Size: 22.9 MB (22890173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0683d549330124c3bae85dc7038331b84825344033ca36a3522c9ee353054d3`  
		Last Modified: Thu, 19 Sep 2024 20:12:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5029ccf57d81e2b9ce390a65fb0053e81866a2c9314500c39d853d060273ddf5`  
		Last Modified: Thu, 19 Sep 2024 20:12:02 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9695b1e75f0ac3107fc99079bc78aaff22bc2c8ec28f31cb9e213754ef1371`  
		Last Modified: Thu, 19 Sep 2024 20:12:03 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66433cc12bc8be8817a56576211ee51c17b4c6739f732ca286867d40d63f8af`  
		Last Modified: Thu, 19 Sep 2024 20:12:03 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e4a04dc2749c53652c2e2f5c2d94ede4128843f04589608ba331c3b8356e7670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17993639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010b7d2c5c8a81c7e5c72e44948ce80ab7243aaff1f0fd852ef0d03c3c56eeb4`

```dockerfile
```

-	Layers:
	-	`sha256:f314e51e539f49179b138ab32bed192677a6825f362142e8291f1339922eeb98`  
		Last Modified: Thu, 19 Sep 2024 20:12:03 GMT  
		Size: 2.3 MB (2335929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb5ede51555d5ae995881735dc89b7f3f0c5da421b61a3cec28d6d5753a6f39`  
		Last Modified: Thu, 19 Sep 2024 20:12:06 GMT  
		Size: 5.2 MB (5152396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea6c585052a6524be99398d2452aa94f1205ca8a967522a3f06ff61cd6f528e3`  
		Last Modified: Thu, 19 Sep 2024 20:12:03 GMT  
		Size: 5.3 MB (5290356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a000b0a9e2b80df385a9423274a9a689e7ee730888deaa4b56ed7d38e1d54c5b`  
		Last Modified: Thu, 19 Sep 2024 20:12:03 GMT  
		Size: 5.2 MB (5153918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37a85a46a7c8f844b8f8743a73ae4380e0921c929edf30609d6f26a7c62fedbd`  
		Last Modified: Thu, 19 Sep 2024 20:12:04 GMT  
		Size: 61.0 KB (61040 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:40dc946b9aa6b51df155d50585daf6c16521b4a558ef62f2fd0cea34868aa85c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98784944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c867a3b36b3942e58baa7ab2ac94acc5c31f0f1e88a927da3d8913f99b8b8ef1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 00:38:01 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 19 Sep 2024 00:38:01 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 19 Sep 2024 00:38:01 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_VERSION=4.0.1
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 19 Sep 2024 00:38:01 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 00:38:01 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 19 Sep 2024 00:38:01 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 19 Sep 2024 00:38:01 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 19 Sep 2024 00:38:01 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 00:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 00:38:01 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 19 Sep 2024 00:38:01 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:43b981c5954bdfa7626a4bec06cf075f7bb2df6698b5c0b42b5b5770109637c6`  
		Last Modified: Tue, 27 Aug 2024 17:08:36 GMT  
		Size: 30.0 MB (30024629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa05ab9b97b42f7997fce79630852028f7ebfed588e2b3e2e897b95b89bec18`  
		Last Modified: Tue, 17 Sep 2024 02:28:57 GMT  
		Size: 38.3 MB (38260472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab857053fa6d133ee8ab1aa5a40a857754dbe098c5ff8315c408be8efc5ff1`  
		Last Modified: Tue, 17 Sep 2024 02:28:57 GMT  
		Size: 7.5 MB (7546297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d969711d8f29a6599306abfdc526f3327653341c04ee4d5ba5637d3863c866d1`  
		Last Modified: Tue, 17 Sep 2024 02:28:56 GMT  
		Size: 9.6 KB (9607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7088df409a10af47eaa0c4363a50c3f895bddb033705894f52ff1a4a09599`  
		Last Modified: Thu, 19 Sep 2024 19:16:43 GMT  
		Size: 22.9 MB (22942192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fc007853258aef2ae6dd3dc376982a0e751c33e0993df16c60e96f5abc22c3`  
		Last Modified: Thu, 19 Sep 2024 19:16:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3da74691c3a55792d31c6c4a25224a5df67241bbdacb210aa0eba9c0eb8e026`  
		Last Modified: Thu, 19 Sep 2024 19:16:42 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98e8d163beedebe0fa343f7964d8872b7ac41dae31fbe862e7e189ea35d1eeb`  
		Last Modified: Thu, 19 Sep 2024 19:16:42 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bef02b7a1cea04ae3c21fb2915f4a99cf389e67165e3697ff6216fda1cbd78f`  
		Last Modified: Thu, 19 Sep 2024 19:16:43 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d8bc75e675f5e6c4b8878bfa57f002a6a8817f0e4f4da2c4f86289a792cc62ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17663531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d0a5cc64d2ac56f946c7efca5e412092032a78986f2fe92cb0c4670fa9983a`

```dockerfile
```

-	Layers:
	-	`sha256:dbc18de5e840ebfc62dc41dfddeb9ffdf42e4bdfcd89d4d23f0a01f5eaee63f3`  
		Last Modified: Thu, 19 Sep 2024 19:16:42 GMT  
		Size: 2.3 MB (2345247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e1733caaa024fbe4f73e6b51b4cc1583cb31a327e174a81f9aa51b82ca1b2c`  
		Last Modified: Thu, 19 Sep 2024 19:16:43 GMT  
		Size: 5.0 MB (5038925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31541a690c90bfad5c88adbacc2d0f122da10eceb8cba80b7a0a5ad31d935f6a`  
		Last Modified: Thu, 19 Sep 2024 19:16:42 GMT  
		Size: 5.2 MB (5177928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:251ad7f615cf4f43f013358770327991489a100930c98436556ecaf03443c12b`  
		Last Modified: Thu, 19 Sep 2024 19:16:42 GMT  
		Size: 5.0 MB (5040447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb0306ac15b5418ae287a5c9c863d7ebe2b90d1655bf0112509858f554d65a6`  
		Last Modified: Thu, 19 Sep 2024 19:16:43 GMT  
		Size: 61.0 KB (60984 bytes)  
		MIME: application/vnd.in-toto+json
