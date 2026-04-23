## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:2dc4037ea53605965db6ed45af9dce9e17ceb8976098029e27d814666a3f596a
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
$ docker pull rabbitmq@sha256:92108e18c4196aac52c119966a1335dc2616414b6221318fd3721420849641b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113497011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14da33ef3efc40ba0f3af28cb3e6673337fb7fcdd3df177a087e747e3939ed03`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 17:22:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 23 Apr 2026 17:22:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 23 Apr 2026 17:22:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 23 Apr 2026 17:22:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 23 Apr 2026 17:22:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:22:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:22:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 23 Apr 2026 17:22:28 GMT
ENV RABBITMQ_VERSION=4.3.0
# Thu, 23 Apr 2026 17:22:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 23 Apr 2026 17:22:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 23 Apr 2026 17:22:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:22:47 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 23 Apr 2026 17:22:47 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 23 Apr 2026 17:22:47 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 23 Apr 2026 17:22:47 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:22:47 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 23 Apr 2026 17:22:47 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 23 Apr 2026 17:22:47 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 23 Apr 2026 17:22:47 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 23 Apr 2026 17:22:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 17:22:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 17:22:48 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 23 Apr 2026 17:22:48 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c208cbccbf21e80693cb020440d2f786d8efe34214685945c299a50cb829af70`  
		Last Modified: Thu, 23 Apr 2026 17:23:10 GMT  
		Size: 46.3 MB (46301245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627108982610ca559cf235c41744080990bcbcb75421866ef374ba8ff8cd8ec7`  
		Last Modified: Thu, 23 Apr 2026 17:23:08 GMT  
		Size: 9.0 MB (8990279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3d47650f6e44709fc5627a8f100e5646d98da1de1c48dcb72fb3c5942ce960`  
		Last Modified: Thu, 23 Apr 2026 17:23:08 GMT  
		Size: 9.7 KB (9693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd73412fc5151f8dd2a8e0e728db07d7986094dc5734c4256e9a7b40e858031`  
		Last Modified: Thu, 23 Apr 2026 17:23:10 GMT  
		Size: 28.5 MB (28461070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad5b0b4812013a323e97c8e10ff139dccb63df2dc7b7ff26386b4643caad90b`  
		Last Modified: Thu, 23 Apr 2026 17:23:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231b6f1e098f583b06a5dbd91ec2adcad815a157e204df9ad927aa3f2cdcd429`  
		Last Modified: Thu, 23 Apr 2026 17:23:10 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55494f80ea956f01225d4a716b73ea8a7810d4bd75e5ab5668a318ca70683098`  
		Last Modified: Thu, 23 Apr 2026 17:23:10 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1d9bd603a6f51f21300310930c62601f7949b37af776dc7e2f5ae3a0157323`  
		Last Modified: Thu, 23 Apr 2026 17:23:11 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a6334a601843399143c725b92f62c8db99fc042f91b61b7eb27709010ed19435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18840944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e57173fb27fda0e4e3fdad3295a17f394c4c9f2e7018f657542436748717be`

```dockerfile
```

-	Layers:
	-	`sha256:e924f050a65aa6477c757c54fc85776e413a102964617e972299d19944be1fd8`  
		Last Modified: Thu, 23 Apr 2026 17:23:08 GMT  
		Size: 2.5 MB (2486687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa11b682731e0510db9170ef64994a29ad6194236b8b304c3414ecb1a00cc85b`  
		Last Modified: Thu, 23 Apr 2026 17:23:09 GMT  
		Size: 5.4 MB (5378513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d57abc887d878b3d5c347efd68f58cb09bca0ecf547cf82a7005a523a471189`  
		Last Modified: Thu, 23 Apr 2026 17:23:08 GMT  
		Size: 5.5 MB (5535288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b760c73b373eb90edc16d6996789a4f974f83a7d071227d71cd049fbcd84859`  
		Last Modified: Thu, 23 Apr 2026 17:23:08 GMT  
		Size: 5.4 MB (5380255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea4011c97bacae82ba58a0b7fd1e4deffafa39462c51ee3a4b243fd04b873ace`  
		Last Modified: Thu, 23 Apr 2026 17:23:09 GMT  
		Size: 60.2 KB (60201 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:ac75308f9e45df3451441b50683016b80ce31cc82f6ab6c95e35f9dcbf8158a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95865127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cf07f1617a6b571a8dab86026eb691618bfbc491dae4715d19bc4742d7fe0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:30 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:33 GMT
ADD file:341ecc672c4413d50e9543a8a38e44f8686dbdcc696b241b06e6b5b3a3ad57f6 in / 
# Fri, 10 Apr 2026 06:56:33 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 17:20:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 23 Apr 2026 17:20:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 23 Apr 2026 17:20:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 23 Apr 2026 17:20:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 23 Apr 2026 17:20:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:20:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:20:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 23 Apr 2026 17:20:15 GMT
ENV RABBITMQ_VERSION=4.3.0
# Thu, 23 Apr 2026 17:20:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 23 Apr 2026 17:20:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 23 Apr 2026 17:20:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:20:38 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 23 Apr 2026 17:20:39 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 23 Apr 2026 17:20:39 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 23 Apr 2026 17:20:39 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:20:39 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 23 Apr 2026 17:20:39 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 23 Apr 2026 17:20:39 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 23 Apr 2026 17:20:39 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 23 Apr 2026 17:20:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 17:20:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 17:20:39 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 23 Apr 2026 17:20:39 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a8bfdbb3919a487508e22db18853909d3934222b024972d78871f6649076c8`  
		Last Modified: Thu, 23 Apr 2026 17:21:04 GMT  
		Size: 33.3 MB (33324871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380ce2372007b00d42e8c236679beac408b52fe92044c2d446eb9347d97a430e`  
		Last Modified: Thu, 23 Apr 2026 17:21:03 GMT  
		Size: 7.3 MB (7306732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ddd77f62e4a145f3030e7e5cd49a6992a37947addec1012e177ac5cad8536c`  
		Last Modified: Thu, 23 Apr 2026 17:21:02 GMT  
		Size: 9.7 KB (9727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f87b1adebcf5479c5b89e1a4c4e4e216edf71a6c5d0a8bf4b04f826b2bfe60`  
		Last Modified: Thu, 23 Apr 2026 17:21:04 GMT  
		Size: 28.4 MB (28362357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d963bdd69af597e26a8be4c67acf0695e61c70450817ed4686166a9144c28e`  
		Last Modified: Thu, 23 Apr 2026 17:21:04 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0fb8db134f3b616b682577bb70bfcb5563e80d22296e5a86e4b5545a6beb12`  
		Last Modified: Thu, 23 Apr 2026 17:21:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648de947879b6f2d673ce6d3cc00c7e52769522b8f175f544f473cff46a96e78`  
		Last Modified: Thu, 23 Apr 2026 17:21:05 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629e74b8bc567438183cd7019eb4aa3becc8f034dd23327f2a2c04dc68e97870`  
		Last Modified: Thu, 23 Apr 2026 17:21:05 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ffb4d73e22996f8fa93724b53c3dd3e90de1e3a89730ce42abe0ed0c54817e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18295657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2863c8ed21c49fd3db635e92a948408fa03419d90e8bddf0068d7711cd86cd3f`

```dockerfile
```

-	Layers:
	-	`sha256:0790bdffc8a6a70247b29e2e06cb4d7f95f2dda77ded9d2bc11853077e77679a`  
		Last Modified: Thu, 23 Apr 2026 17:21:02 GMT  
		Size: 2.5 MB (2487487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7bed45c058dc5536f08b20ac9542646dd08c1e641711529429748239e8b8f91`  
		Last Modified: Thu, 23 Apr 2026 17:21:03 GMT  
		Size: 5.2 MB (5197271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89cf86af8817ad524c5a22d3347e9841e4d921c4917a7760cb9f8de89bf6aac8`  
		Last Modified: Thu, 23 Apr 2026 17:21:03 GMT  
		Size: 5.4 MB (5351489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce7a4bbc4b9de921712a42e89f1d11d2ed96e8fb763754c19d3a80faad5578d`  
		Last Modified: Thu, 23 Apr 2026 17:21:03 GMT  
		Size: 5.2 MB (5199013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9741947bfc15140be10c41dc68b38ba16787965cf3bf21bd948b729fcdc9640a`  
		Last Modified: Thu, 23 Apr 2026 17:21:04 GMT  
		Size: 60.4 KB (60397 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:e6a6b4fbbb458ac53ba9c5430e58762cef81d53bbfc3415cd94728648a42930f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111360465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a71b73f29fb2195129a03c78c846801bebf2095e9e814656aa42fad1873247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 17:21:53 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 23 Apr 2026 17:21:53 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 23 Apr 2026 17:21:53 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 23 Apr 2026 17:21:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 23 Apr 2026 17:21:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:21:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:21:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 23 Apr 2026 17:21:55 GMT
ENV RABBITMQ_VERSION=4.3.0
# Thu, 23 Apr 2026 17:21:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 23 Apr 2026 17:21:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 23 Apr 2026 17:21:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:22:17 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 23 Apr 2026 17:22:18 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 23 Apr 2026 17:22:18 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 23 Apr 2026 17:22:18 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:22:18 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 23 Apr 2026 17:22:18 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 23 Apr 2026 17:22:18 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 23 Apr 2026 17:22:18 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 23 Apr 2026 17:22:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 17:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 17:22:18 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 23 Apr 2026 17:22:18 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea41eadcb6769c17e6969c4ee0b9c50068dc0ed947d735ae1b9616cd0568147`  
		Last Modified: Thu, 23 Apr 2026 17:22:45 GMT  
		Size: 44.4 MB (44387264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79f5f2661e359f5a4525e43a03a7b2d3643711f78463068a908af92d38961f5`  
		Last Modified: Thu, 23 Apr 2026 17:22:44 GMT  
		Size: 9.7 MB (9714852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd2d060d5ff3f8631421b1719d6e966369427929444fa10347111ec3300aa0a`  
		Last Modified: Thu, 23 Apr 2026 17:22:43 GMT  
		Size: 9.6 KB (9631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafac8a5c75c931409b667a00881df423c7f7d9aeaa7815c3694843e6989ce1d`  
		Last Modified: Thu, 23 Apr 2026 17:22:45 GMT  
		Size: 28.4 MB (28371187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d9d682d4fe79651bfa2559b6fdab5f9ea7247c1e6e07d2a9c652232bc4ba66`  
		Last Modified: Thu, 23 Apr 2026 17:22:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18227997aa9fbd2a1fc72c48347554ff2abeedd42e665a73faaf185c57174a36`  
		Last Modified: Thu, 23 Apr 2026 17:22:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a756c0a16251d8b3c4ecb7e9f38cd53d09923b45a3a15f6a8264a0d5cc9de9`  
		Last Modified: Thu, 23 Apr 2026 17:22:46 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3c8017b2a25adc46af8df4f93e600d038b352a381ba25899c4df0fc7ee2c03`  
		Last Modified: Thu, 23 Apr 2026 17:22:47 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3bf39d5809ce4bdb39c2fd064460acac58df94b9411725bc5d514dbcff8fd29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18899911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a3f5c038b93fc4d1bb5ab91d4dc8a59f2313c81bea202bcc5560bf072648d4`

```dockerfile
```

-	Layers:
	-	`sha256:ff491a40020431061ef84678217560c7edc7f53f06fe406c4e2e02ca43f248c5`  
		Last Modified: Thu, 23 Apr 2026 17:22:44 GMT  
		Size: 2.5 MB (2487747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:835461b54cb6816db11b8db9c9bf55b0544101512794155610311a93c798f9cb`  
		Last Modified: Thu, 23 Apr 2026 17:22:44 GMT  
		Size: 5.4 MB (5397730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a91caa092d66eab6c38c933b6a05cf113bb8d656e947d346815bf461b639e0e7`  
		Last Modified: Thu, 23 Apr 2026 17:22:44 GMT  
		Size: 5.6 MB (5554523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:284e065173712411832e7dc9c72f31d72132a8a27bad8a3ee890a91997ac7b5d`  
		Last Modified: Thu, 23 Apr 2026 17:22:44 GMT  
		Size: 5.4 MB (5399472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b00e9cf1adf18f4cb77840fc986f86c60ab5ab4e5ed58aa751a58b95111a074d`  
		Last Modified: Thu, 23 Apr 2026 17:22:45 GMT  
		Size: 60.4 KB (60439 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:14fa9b7fe4d8cb2716e3adbf8f03d46c77200b1c2cc29e1134b0e51438408bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111885686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830158a889e80c1328c0d65aa81250a942f4afebf432238bbbf3c3f50410335a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 22:29:58 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 21 Apr 2026 22:29:58 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 21 Apr 2026 22:29:58 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 21 Apr 2026 22:29:59 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 21 Apr 2026 22:29:59 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:29:59 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:30:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 21 Apr 2026 22:30:02 GMT
ENV RABBITMQ_VERSION=4.3.0
# Tue, 21 Apr 2026 22:30:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 21 Apr 2026 22:30:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 21 Apr 2026 22:30:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:17:43 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 23 Apr 2026 17:17:45 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 23 Apr 2026 17:17:45 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 23 Apr 2026 17:17:45 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:17:45 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 23 Apr 2026 17:17:45 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 23 Apr 2026 17:17:45 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 23 Apr 2026 17:17:46 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 23 Apr 2026 17:17:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 17:17:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 17:17:46 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 23 Apr 2026 17:17:46 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc816157179a8bfcdae99f55c6f2d26139173bfb43af906ce2614c5cb69d7af`  
		Last Modified: Tue, 21 Apr 2026 22:31:38 GMT  
		Size: 39.5 MB (39538683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be564f6d9c95fc723dd0c54ad71feb32c81b5fbdb3a23cdffb66f66f7f1e364`  
		Last Modified: Tue, 21 Apr 2026 22:31:36 GMT  
		Size: 9.6 MB (9599875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966a412fe6a56a14ba7ab222c6bd45dba446e6968f80fe31dbad889db191ac4`  
		Last Modified: Tue, 21 Apr 2026 22:31:35 GMT  
		Size: 9.7 KB (9668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fb77f30625e120586b570e6212f51d742e456e1b12a61ec93eded443053517`  
		Last Modified: Thu, 23 Apr 2026 17:24:57 GMT  
		Size: 28.4 MB (28421528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf3782fcd1d7efa737148a2161305e2ac87c05059c43a9bbfd906202eaf957c`  
		Last Modified: Thu, 23 Apr 2026 17:24:56 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80edf7a30899ab1b77bbe8f39c5272041f4bc3859846f5a1830dc917c791a0ba`  
		Last Modified: Thu, 23 Apr 2026 17:24:56 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a51e2609582337d6a1829393a3d5a042f923bf0df8d6a10e56d6026d664614`  
		Last Modified: Thu, 23 Apr 2026 17:24:56 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5052252cf74dcbb5f2848b1f88e927e4b84a90e21b896b0584e2f22f6c9b17e3`  
		Last Modified: Thu, 23 Apr 2026 17:24:58 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:379eec4e274ea27de5b68246a8fe1958cfb48830543d6c692662dcde66a222a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18755297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4966778c8ba1c479c1d930b31077abfff04672a82a21260439af473724330e`

```dockerfile
```

-	Layers:
	-	`sha256:15b6e85dde5f08a18c700dd76fe2b223b742c6a26b35567e73e44a122bc92049`  
		Last Modified: Thu, 23 Apr 2026 17:24:56 GMT  
		Size: 2.5 MB (2491140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5444fa8319ed8c48c8e0a3da003267d993ebf6c61fe5609ea841b80620d55d51`  
		Last Modified: Thu, 23 Apr 2026 17:24:56 GMT  
		Size: 5.3 MB (5348449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31b9d2eab7e6e80f964e76ee9373cf13dbe39c554810ab09f0b1f609f17e80f8`  
		Last Modified: Thu, 23 Apr 2026 17:24:57 GMT  
		Size: 5.5 MB (5505254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa8f9d7bad41123aebde6881b3c740285f11e12baf7afa9dd95c45152a0b6851`  
		Last Modified: Thu, 23 Apr 2026 17:24:56 GMT  
		Size: 5.4 MB (5350191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f6cd291b9baf491e37971fa19d553cb262c686e584a095fc0e98038dac72a66`  
		Last Modified: Thu, 23 Apr 2026 17:24:58 GMT  
		Size: 60.3 KB (60263 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:c92abf72c9863175b5c10cd9d5e777b139d942d075f28524996778e8bd3c661d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104881397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51121df4a1e67f28a154d398f4e691078450c908629b5875c200ee35e7dab42d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 10 Apr 2026 09:24:05 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:24:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:24:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 09:24:43 GMT
ADD file:a9a4679e3df2846468311b83a8f6ab86f5a205bab966d3f236c9f30151010c5b in / 
# Fri, 10 Apr 2026 09:24:47 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 03:52:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 22 Apr 2026 03:52:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 22 Apr 2026 03:52:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 22 Apr 2026 03:52:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 22 Apr 2026 03:52:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:52:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 22 Apr 2026 03:52:34 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 22 Apr 2026 03:52:34 GMT
ENV RABBITMQ_VERSION=4.2.5
# Wed, 22 Apr 2026 03:52:34 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 22 Apr 2026 03:52:34 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 22 Apr 2026 03:52:34 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 05:23:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 22 Apr 2026 05:23:30 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 22 Apr 2026 05:23:31 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 22 Apr 2026 05:23:31 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 22 Apr 2026 05:23:31 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 22 Apr 2026 05:23:31 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 22 Apr 2026 05:23:31 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 22 Apr 2026 05:23:31 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 22 Apr 2026 05:23:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 05:23:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 05:23:31 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 22 Apr 2026 05:23:31 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:a7f0c74374451005259fe6b1b7ef3185055f2b6c419b5ba0ae8e4f55b1e1c31d`  
		Last Modified: Fri, 10 Apr 2026 09:34:45 GMT  
		Size: 31.0 MB (30965327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c960ea9e328ab3ee58c30b09ea3a95d1f30dea9d977bfb27e1aabaf0dba39aa`  
		Last Modified: Wed, 22 Apr 2026 04:01:18 GMT  
		Size: 35.2 MB (35179488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e98760d3d077246d6e1c6d8b7d5ace39954b7d7fc75b716fae346432ec72772`  
		Last Modified: Wed, 22 Apr 2026 04:01:11 GMT  
		Size: 10.8 MB (10836870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33eb29b1bda2d247b07c6d6d675bb9780b9b8fa42ed028b8ff4cc75687e1a6f`  
		Last Modified: Wed, 22 Apr 2026 04:01:05 GMT  
		Size: 9.7 KB (9683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76da0348dfbaa0fd3d2ab97503e96ff1df4a09a73b2a29a718a2559ec1eca44b`  
		Last Modified: Wed, 22 Apr 2026 05:31:10 GMT  
		Size: 27.9 MB (27888283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4b0ca35f78e15079cc041196818b0731b44a0b4d04b216b18557781f812f68`  
		Last Modified: Wed, 22 Apr 2026 05:31:04 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3595a5374c0dfddbee40b6d99d4fb889d92e058d64affb328e30c3a3f7dedb`  
		Last Modified: Wed, 22 Apr 2026 05:31:03 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a3f295dac546276d43eb86f2072d7ec0a41bd1e261c9a53055c2af36e0435`  
		Last Modified: Wed, 22 Apr 2026 05:31:03 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44388665c6d55a862cc5c243524a87d8ffc859422f9298ccfde6aa92bf6b7836`  
		Last Modified: Wed, 22 Apr 2026 05:31:06 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3835da92a35c226ecc286b801ae4ec019a7888cc9b34bd6221de1338268e1505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18723828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ecf1f9b3f686c951fdb1214499d64722abb18aa3367f63c4a5b6b99aa989b5`

```dockerfile
```

-	Layers:
	-	`sha256:a6c58d56361563fb78b7b78199728a3be8f525437a13fdcf1406eb7e30d07ae0`  
		Last Modified: Wed, 22 Apr 2026 05:31:04 GMT  
		Size: 2.5 MB (2478990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cb8d7045957afd9518fcfbabd15f0c1ccdf9ce47b07ad7a8432e561a4ea797e`  
		Last Modified: Wed, 22 Apr 2026 05:31:05 GMT  
		Size: 5.3 MB (5342870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ce8a33c53c198cd1438839c4bd408d623b3807bcec121d562172d5aa060862b`  
		Last Modified: Wed, 22 Apr 2026 05:31:06 GMT  
		Size: 5.5 MB (5497086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0dabdeb1db31ccaa4c077ea2ffe79ccab1c3a01865bb1993a8005bb771cbd5`  
		Last Modified: Wed, 22 Apr 2026 05:31:06 GMT  
		Size: 5.3 MB (5344612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a696933cdd0ed9b9a4756c80298b47e9cd0932b48b4ced9bade6b359d952e87`  
		Last Modified: Wed, 22 Apr 2026 05:31:06 GMT  
		Size: 60.3 KB (60270 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:25d3ebd17f2f7bec6aba486f2780e2652f4edc3e5ee3652bc4a40e72a02756d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105613204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433000bd01f7e63b63583621a1ba295c399dde6aa02c699ebbbe56484ba64f9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 22:30:05 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 21 Apr 2026 22:30:05 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 21 Apr 2026 22:30:05 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 21 Apr 2026 22:30:05 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 21 Apr 2026 22:30:05 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:30:05 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:30:07 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 21 Apr 2026 22:30:07 GMT
ENV RABBITMQ_VERSION=4.3.0
# Tue, 21 Apr 2026 22:30:07 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 21 Apr 2026 22:30:07 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 21 Apr 2026 22:30:07 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:26:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 23 Apr 2026 17:26:38 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 23 Apr 2026 17:26:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 23 Apr 2026 17:26:50 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:26:50 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 23 Apr 2026 17:26:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 23 Apr 2026 17:26:50 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 23 Apr 2026 17:26:57 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 23 Apr 2026 17:27:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 17:27:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 17:27:02 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 23 Apr 2026 17:27:02 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480091d9e2fc287cc53a0907fc8da9bf8e7fb0040f22c9b53c8cf5bd3669c45a`  
		Last Modified: Tue, 21 Apr 2026 22:31:05 GMT  
		Size: 38.6 MB (38623058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64681a4de2d2ca5809f14e54ab31b57a25d86328e52ab11d41b2cdf21c729b61`  
		Last Modified: Tue, 21 Apr 2026 22:31:05 GMT  
		Size: 8.6 MB (8621410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf74ab9d858bc9e67ad748808d0a1a1a09dd3fcaff12acf4e6ae5743bd3b6aa`  
		Last Modified: Tue, 21 Apr 2026 22:31:05 GMT  
		Size: 9.8 KB (9827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9783a79d444bf4388aabd221a430195d2096f4e26c696384fb00612ff84a5b6`  
		Last Modified: Thu, 23 Apr 2026 17:45:47 GMT  
		Size: 28.4 MB (28445011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548585cd93bd296f199a01d1d4617ea701a37b96cc81cad63a8abf4afc57f3ce`  
		Last Modified: Thu, 23 Apr 2026 17:45:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511977212bfa95531e132e47a88412bcb8974b756cc1f7084792f1724b7535d9`  
		Last Modified: Thu, 23 Apr 2026 17:45:39 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac98f69fb435b90ef70bd5d4165b914c2cbb67336f1e64ebafae2c4b84d8a5b`  
		Last Modified: Thu, 23 Apr 2026 17:45:43 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa913bdca7afeba79dee9da3f9a09e96d7ee7d3f216467f82e54111b9fbb9a3`  
		Last Modified: Thu, 23 Apr 2026 17:45:46 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b43e6891c1fc459dcb5f1e2df1e7c0765c81106f0ff8679da9fa42d2c5fef0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18381035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c4163b874650a04748f6df2872b245f7ca2c6077f5068830e083b9cac18f23`

```dockerfile
```

-	Layers:
	-	`sha256:7c7586e82ca4e33cfe95bd74dbf9ce2147a4c70325db7a5620583ed83f580f27`  
		Last Modified: Thu, 23 Apr 2026 17:45:44 GMT  
		Size: 2.5 MB (2488797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3584634c2b7a3214b99d7fbdf61bdc178b974731ba98aa3d8fe4221189165273`  
		Last Modified: Thu, 23 Apr 2026 17:45:43 GMT  
		Size: 5.2 MB (5224942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfa465be28a6c96fc2cb87701aaf0e0e27e4633beee1724b776ba1660278f03e`  
		Last Modified: Thu, 23 Apr 2026 17:45:45 GMT  
		Size: 5.4 MB (5380412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d1c30204cd88be58f30a2dba22031525f3e42f57f558d59245760d63468d57`  
		Last Modified: Thu, 23 Apr 2026 17:45:45 GMT  
		Size: 5.2 MB (5226684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:654e54c1711018875ddf636f437ed8be9ca5cb53a10996d923f3433167814750`  
		Last Modified: Thu, 23 Apr 2026 17:45:46 GMT  
		Size: 60.2 KB (60200 bytes)  
		MIME: application/vnd.in-toto+json
