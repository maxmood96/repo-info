## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:c232ecbdf66d17766eba9cd893967c3424255a8961935525d7f27ce5c7559c46
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
$ docker pull rabbitmq@sha256:92e6c1aa667bac8750dfa2ae28eb9c0cc53f452e6f06ba0eeecc1d39cdb862f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104605723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa53bdfa924d7641b38da7a4777ee9d35ec8c23a931c5337ab23cb5d67972a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Wed, 03 Jul 2024 11:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 03 Jul 2024 11:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 03 Jul 2024 11:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_VERSION=3.13.4
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jul 2024 11:05:20 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 03 Jul 2024 11:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 03 Jul 2024 11:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jul 2024 11:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 03 Jul 2024 11:05:20 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639d5be5ab90943c4b5e110cfcd4d64a6f4306f612ee6a552f1d78eb052bf15e`  
		Last Modified: Wed, 03 Jul 2024 19:05:52 GMT  
		Size: 46.0 MB (46017119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48859dfc02c27e760533589e0ba5f89f994ab5853c340787bdf80c7104f4d27d`  
		Last Modified: Wed, 03 Jul 2024 19:05:52 GMT  
		Size: 7.5 MB (7483801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79520dc43230dbf55a6c68283a80d49377d61685ade6c6b32b47e9faf602112a`  
		Last Modified: Wed, 03 Jul 2024 19:05:52 GMT  
		Size: 10.7 KB (10736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487ca212fb459b7f023032768cce15b506829e325902d5c966f361761549b58`  
		Last Modified: Wed, 03 Jul 2024 19:05:54 GMT  
		Size: 21.6 MB (21558262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552e177e29a11f0ed7f793c05b9cb90fb86d67a1351ff4ce382d6ad18457b96d`  
		Last Modified: Wed, 03 Jul 2024 19:05:53 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce60024c8c453bb85958832fff5495142c3f95e035ffad785778853c8d270ea`  
		Last Modified: Wed, 03 Jul 2024 19:05:53 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b202e8d6521c8e79ce39858635d95011c240697da11b71a7c1824986a20fecb8`  
		Last Modified: Wed, 03 Jul 2024 19:05:53 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d24b6255b08fc1b2c7757f2dbd189b005e38e3a535376adbab4e3f33b7b6f1`  
		Last Modified: Wed, 03 Jul 2024 19:05:54 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b04d66503c20b77db47d0bdd6e2da1c14fc7b70f0babda09e86eb142affc1061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18553926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b650054868ae8a5420fdd5f29782f8e1193c756821a0ab3518250b31ae813119`

```dockerfile
```

-	Layers:
	-	`sha256:802d8c7a3e0622cddea7c44640c02024c6680f3f61bac485298fb31c09d8b118`  
		Last Modified: Wed, 03 Jul 2024 19:05:52 GMT  
		Size: 2.9 MB (2884448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:769cc1f331cdeeb0e5d17c03fb70bf9994336e2fbddb991216f076e954ae82e9`  
		Last Modified: Wed, 03 Jul 2024 19:05:52 GMT  
		Size: 5.2 MB (5160717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98ee0f6549307bb1b0ae07eb8011fdf86c4e2eac1e6bb17a7ab876f1dbf7d23f`  
		Last Modified: Wed, 03 Jul 2024 19:05:52 GMT  
		Size: 5.3 MB (5285294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e6a2dfee2299c49a1b3946c0e8ed9909a9685cf9618a05abe67faa3b8bd75ca`  
		Last Modified: Wed, 03 Jul 2024 19:05:52 GMT  
		Size: 5.2 MB (5162091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68171ec18a1a8eb1d55086115174e15f9bc98d35773e50a44448b3dcfb78dbb9`  
		Last Modified: Wed, 03 Jul 2024 19:05:53 GMT  
		Size: 61.4 KB (61376 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:ab556424bf8fc7d624b6471b26210dfd35acdc0cd7e40b7ee22de0abb9ae0e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87702295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff2427eceebc59f30a79fe224d81f49ba59dc964ed564ab9cf216f6977dcaee7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 27 Jun 2024 19:33:13 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:33:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:33:16 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 19:33:16 GMT
CMD ["/bin/bash"]
# Wed, 03 Jul 2024 11:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 03 Jul 2024 11:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 03 Jul 2024 11:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_VERSION=3.13.4
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jul 2024 11:05:20 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 03 Jul 2024 11:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 03 Jul 2024 11:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jul 2024 11:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 03 Jul 2024 11:05:20 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f6d2cceb710e897ef3b81e28ea21268aa6d28deae90ac1ab9602ff738c88a650`  
		Last Modified: Thu, 27 Jun 2024 20:18:40 GMT  
		Size: 26.6 MB (26638444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43943d8892639acaecade0ac121e17588ef70d441851709ea2ea38583a2e9b02`  
		Last Modified: Wed, 03 Jul 2024 00:13:55 GMT  
		Size: 33.5 MB (33497597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a110c906ee09e45bee4507c444c1d8fd20f15ff19000c4e245ee5a9fe867fd74`  
		Last Modified: Wed, 03 Jul 2024 00:13:55 GMT  
		Size: 6.1 MB (6077355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56672f68b9b4f585cebfcc64518ef69b276b4bd8e98eaf0c6bd7199fd53a140`  
		Last Modified: Wed, 03 Jul 2024 00:13:54 GMT  
		Size: 10.7 KB (10699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73adcdfa5afad09b0764362ce2a90f1103a7a292213db5fc06dbe62446b40cb9`  
		Last Modified: Wed, 03 Jul 2024 20:04:12 GMT  
		Size: 21.5 MB (21476455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84481473c30dc8c7b7356f213b272702ba7ee8e81dabccff5ed996feefdb552c`  
		Last Modified: Wed, 03 Jul 2024 20:04:11 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037f1fc7cfe8b5734ae81efb39a75df2f85b7f669aa1cd4c1d889489028c73ac`  
		Last Modified: Wed, 03 Jul 2024 20:04:11 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b65e034d22a433f31f89e8be330684110a4d7bfd2894fed2ca4f2ecd7216ed2`  
		Last Modified: Wed, 03 Jul 2024 20:04:11 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa3e9e5b3fa68ef6b97b548f8ffd9236ca2b21fbf36fdfb2f07b650bce2741a`  
		Last Modified: Wed, 03 Jul 2024 20:04:12 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:79cf6c16f78281092ad1ec2ae65a09929810228d2fb56c40aafe02a9274f3d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18009733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a286d6d5ffabf3f6b8edc23af70eada5bbf206967a895edb9e38babc2647a8c`

```dockerfile
```

-	Layers:
	-	`sha256:84de4b272d4cf4b5d59b955b21b20a00689f6a1a417e8a7d3f0fa15a4f5719b8`  
		Last Modified: Wed, 03 Jul 2024 20:04:11 GMT  
		Size: 2.9 MB (2885111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad1dc354cd8153c85b40381acba2552e870bb29360c305bb5a7e105d48b5bcdf`  
		Last Modified: Wed, 03 Jul 2024 20:04:11 GMT  
		Size: 5.0 MB (4979870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:260aa2fb5a797571b3c4c2a3562f0d179c82eb17cf44f31da225d8807d953348`  
		Last Modified: Wed, 03 Jul 2024 20:04:11 GMT  
		Size: 5.1 MB (5101943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3ba7f0f06b33fe7357b793a5ddc163917cabf6f8e18c5ba27b6b0e7c97aaa4`  
		Last Modified: Wed, 03 Jul 2024 20:04:11 GMT  
		Size: 5.0 MB (4981244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d587f84f4b0556869c4ca4cd80aecbe1641bcf7332ea9bd44efa0f88bbd9ebec`  
		Last Modified: Wed, 03 Jul 2024 20:04:12 GMT  
		Size: 61.6 KB (61565 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:fe90a049f33ecdab0c0db14969e1ff8abd4113f9f3097befd81ba4e7aff51651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100062883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3b8aabc5f4d4db30756c90efed90d8a5cb7353c2397e9b422bbed58ad834b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Wed, 03 Jul 2024 11:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 03 Jul 2024 11:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 03 Jul 2024 11:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_VERSION=3.13.4
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jul 2024 11:05:20 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 03 Jul 2024 11:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 03 Jul 2024 11:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jul 2024 11:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 03 Jul 2024 11:05:20 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841c7debea38643b1448ee0b0f5a20dd2d352a4798fef5bd53006351144fdd3e`  
		Last Modified: Tue, 02 Jul 2024 22:55:29 GMT  
		Size: 44.1 MB (44089611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbee6e225309433351bfe95f421beb68f17ef039e08669cc4dbaecd3e7a6f6ad`  
		Last Modified: Tue, 02 Jul 2024 22:55:28 GMT  
		Size: 7.1 MB (7133044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f985412444972eec31ba7ee305980d05c4bc6ba6bb5bc315ec4d6ddd9c4119`  
		Last Modified: Tue, 02 Jul 2024 22:55:27 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ad4882e25c2cd253879afa8bc3c1231d89490ff745a9ba4338983f753aa061`  
		Last Modified: Wed, 03 Jul 2024 19:32:10 GMT  
		Size: 21.5 MB (21467760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b883c1aa15941e674f862b1eb93fe509feb27dbdd09fb1789405f64e02ef39d`  
		Last Modified: Wed, 03 Jul 2024 19:32:09 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11d49c0b93edbfb1f74ea9e30f092ef3bb408dc5d1e42371b9ad1ee9b012da8`  
		Last Modified: Wed, 03 Jul 2024 19:32:09 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515cd4f9a6194b903ac35bc03a7d1eaf0add7860341c052afe405327de18a584`  
		Last Modified: Wed, 03 Jul 2024 19:32:09 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dd075a69e9401a733264bd462e0f7ac89121a134860552f392ef329332a9dd`  
		Last Modified: Wed, 03 Jul 2024 19:32:10 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:be9e68ec2dcbc7e3b6f47f61578b9ae20761dc24d0dc61d6cd66156daf859f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18542096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ef9f080f2a860e6f9eb68178dab36fc799171bbdef8a9511d504dbdf48ce09`

```dockerfile
```

-	Layers:
	-	`sha256:916930db7e473b6a9b3de8a551722f7d154644ce7273d754486c1c416926f5a9`  
		Last Modified: Wed, 03 Jul 2024 19:32:15 GMT  
		Size: 2.9 MB (2884720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33cc654b66768efe9e269f1024e51c816afb6d972d51b1b0b100a51ad34396a9`  
		Last Modified: Wed, 03 Jul 2024 19:32:09 GMT  
		Size: 5.2 MB (5156578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3f8f733b985dcba1915173561bf7b88914c25dae02f063d3b1f8c4cbd43f17`  
		Last Modified: Wed, 03 Jul 2024 19:32:09 GMT  
		Size: 5.3 MB (5281167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b42d5fce4695232365f029eec5cf5e928ffff74a1e8361da36ff2a7fd7bdc42`  
		Last Modified: Wed, 03 Jul 2024 19:32:09 GMT  
		Size: 5.2 MB (5157952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d125e05c7bdc76d12854ac5c3eb288709545c6aba74d0eee7bc94cf6efaa9720`  
		Last Modified: Wed, 03 Jul 2024 19:32:10 GMT  
		Size: 61.7 KB (61679 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:b15b1979a679ad337ebbef569670bb58a958b23961812e950119931e7f930d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103464280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d331bd3b937f566b0c6e44046f13b5c3620ae23667b49a460db72ae5f40a512`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 25 Jun 2024 11:05:22 GMT
ARG RELEASE
# Tue, 25 Jun 2024 11:05:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Jun 2024 11:05:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Jun 2024 11:05:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Jun 2024 11:05:22 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Tue, 25 Jun 2024 11:05:22 GMT
CMD ["/bin/bash"]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 25 Jun 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.3
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 25 Jun 2024 11:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 25 Jun 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb761c3b153703b2d6a0cca9b4b1a0893864b79f1f4b437c03fa45fdfd6aa9e`  
		Last Modified: Tue, 02 Jul 2024 19:59:21 GMT  
		Size: 39.6 MB (39598453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2982e1b76065c06482fe58bfa4b9dc7996c59988ac39649b56bb0c5177293700`  
		Last Modified: Tue, 02 Jul 2024 19:59:20 GMT  
		Size: 7.9 MB (7868576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201cc41ce7dbd4038ee1560aeef2a1e196a02cda9b422b06d9ad865f9eee8e8e`  
		Last Modified: Tue, 02 Jul 2024 19:59:19 GMT  
		Size: 10.7 KB (10711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f336d73384cd0e4af395b555203b0526bfa30d4b3042d138952d86804087be`  
		Last Modified: Tue, 02 Jul 2024 19:59:20 GMT  
		Size: 21.5 MB (21523708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9455bd13848079a074fce6c0e44fc682d9d1d311a0ca155462502da016b31221`  
		Last Modified: Tue, 02 Jul 2024 19:59:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a9e44528a206111cc0c73209ddf5e9d8919de5bc5ab313a9bfd748217b2109`  
		Last Modified: Tue, 02 Jul 2024 19:59:21 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eed929c8cb124a8b497a2e0e3a39df0101e76c6166985921584cbf6831a882`  
		Last Modified: Tue, 02 Jul 2024 19:59:21 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada7be030c217b2bbd85ca1b17c9df776dde1263011e6e1fd2ffc9fb5f60954b`  
		Last Modified: Tue, 02 Jul 2024 19:59:21 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7ba6157e2608c6839b663c097fb7fac6d64b28bacb182b27a19fabe7f9d5a6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18440167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59740ff05d077c1c4290c0711b4f7c6a6ad2807660a6a5e63f34159a34c72ecc`

```dockerfile
```

-	Layers:
	-	`sha256:deaefb9568ac0a85f1998a8aba232e51a6cd5b67ae7077ba174947c1c06712e8`  
		Last Modified: Tue, 02 Jul 2024 19:59:19 GMT  
		Size: 2.9 MB (2888202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5e7f0051c42b083457355d3b57699f608c63cceae92a185e4c7d294929e0ce2`  
		Last Modified: Tue, 02 Jul 2024 19:59:19 GMT  
		Size: 5.1 MB (5121888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdf0f02095db5a365d350c81e07a4cb7782ae751ea427e3e986c5362a9e248a9`  
		Last Modified: Tue, 02 Jul 2024 19:59:19 GMT  
		Size: 5.2 MB (5245381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91a5052cfa4ec6043d4958e1424d60cb8a188d5c59eb993f6a3a466cc29724d4`  
		Last Modified: Tue, 02 Jul 2024 19:59:19 GMT  
		Size: 5.1 MB (5123262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:032b6b4a2f3d3be6e283099109a90aef3b2ddca2f157e982038984d1516d8fcc`  
		Last Modified: Tue, 02 Jul 2024 19:59:20 GMT  
		Size: 61.4 KB (61434 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:2ce02349a3b072f85be5eb15225061bd26a1ca35abb4e46eb0249d21f71f13fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94341251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc92ccbe12d7995b3a5ac558bcd33192f204313a4604929a9085c1e1545d1ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 25 Jun 2024 11:05:22 GMT
ARG RELEASE
# Tue, 25 Jun 2024 11:05:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Jun 2024 11:05:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Jun 2024 11:05:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Jun 2024 11:05:22 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Tue, 25 Jun 2024 11:05:22 GMT
CMD ["/bin/bash"]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 25 Jun 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.3
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 25 Jun 2024 11:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 25 Jun 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9414f2a6b9d142f5ee5a4dc404276ed100ddba4dbe1e522174237d9f6d61b3b3`  
		Last Modified: Tue, 02 Jul 2024 10:17:21 GMT  
		Size: 38.2 MB (38235912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830c9e200b9883650cbc2908bf341af1cafb2cad0f4d09a67aa27655eb3e7b7c`  
		Last Modified: Tue, 02 Jul 2024 10:17:20 GMT  
		Size: 6.5 MB (6535437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8b3318f3a4c7f6391b33737e71bab6a3e90842102e39de398d9291c75391b0`  
		Last Modified: Tue, 02 Jul 2024 10:17:19 GMT  
		Size: 10.7 KB (10748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e453040bf8a4abc87da4215b358ab3798cd1356f7a420b153567d4ad5cb381`  
		Last Modified: Tue, 02 Jul 2024 10:17:21 GMT  
		Size: 21.6 MB (21556870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d319a506b1688689e296c5e8984848efdfc7e1653980f01d85c3d201b6f5754f`  
		Last Modified: Tue, 02 Jul 2024 10:17:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e9e0719365679fc94a4af64a0c9bc1fc5046a5705db1c97333ed9fbe7349e`  
		Last Modified: Tue, 02 Jul 2024 10:17:21 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdb178689dd755b7812b73779da3bc66bfa87423b1995147603ea975ed997a2`  
		Last Modified: Tue, 02 Jul 2024 10:17:21 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb9da630d98194d48f0b1f552d68d22e023f398039fd8566a38b083cf91967e`  
		Last Modified: Tue, 02 Jul 2024 10:17:22 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3fd2a30984b4601cd3d76d374799e12cdd42624b8dfd6e7e40290885f4efacd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18081278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b429987dc71f01e5fc995aae833e69c1c2bf281e4b99b914e8cfced22b9366b9`

```dockerfile
```

-	Layers:
	-	`sha256:ac6e2b9b4ff944caf158777ae1bc0a064913a2181e3f85e70df55039ffbef0f7`  
		Last Modified: Tue, 02 Jul 2024 10:17:20 GMT  
		Size: 2.9 MB (2886052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b3e6ffbe42eacb84b05465f4003068754964cf3621f05b6d9230a642808297`  
		Last Modified: Tue, 02 Jul 2024 10:17:20 GMT  
		Size: 5.0 MB (5002997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce2560aadf37022e1ea1488a7fabf880fcf0eed646032a0f8e4ffe51d756965a`  
		Last Modified: Tue, 02 Jul 2024 10:17:20 GMT  
		Size: 5.1 MB (5126480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf05f22ba71e1d606d1c6d80df4a235902c36c32fa37d1be13337fb5de2a2844`  
		Last Modified: Tue, 02 Jul 2024 10:17:20 GMT  
		Size: 5.0 MB (5004371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdfd8e11b525a7b6ff435d4c7c9fe88eaca601a665bf1b59e68a480481b065ab`  
		Last Modified: Tue, 02 Jul 2024 10:17:21 GMT  
		Size: 61.4 KB (61378 bytes)  
		MIME: application/vnd.in-toto+json
