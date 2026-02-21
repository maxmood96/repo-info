## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:c8a204d5b0bba833cbff44067b482b40152e8156d811a369e92fa0f1da8cb9c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rabbitmq:4-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:c67ca1e5b7f3ac554911f9e5eb73144975e1e11c73589fc874c06bf290573449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83552172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c18987da5a18e3791d9f84922c279b74b2ae8b7816a492779a5a587f85ce2ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 20 Feb 2026 19:17:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Feb 2026 19:17:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Feb 2026 19:17:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Feb 2026 19:17:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Feb 2026 19:17:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:17:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:17:23 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Feb 2026 19:17:23 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 20 Feb 2026 19:17:23 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Feb 2026 19:17:23 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Feb 2026 19:17:23 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:17:29 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Feb 2026 19:17:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Feb 2026 19:17:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Feb 2026 19:17:29 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:17:29 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Feb 2026 19:17:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Feb 2026 19:17:29 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 20 Feb 2026 19:17:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Feb 2026 19:17:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Feb 2026 19:17:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Feb 2026 19:17:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Feb 2026 19:17:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574b3d74ba697cf20c5699ce646727d4c0fffb4adfc585fe5b801d37870986aa`  
		Last Modified: Fri, 20 Feb 2026 19:17:45 GMT  
		Size: 42.6 MB (42623504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca572afb5bdef21a3d93fcccde1cbc12d61d04ae84bac33e2279269b3fd02c43`  
		Last Modified: Fri, 20 Feb 2026 19:17:44 GMT  
		Size: 9.2 MB (9198209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a0ded005d7f33afcf996826641d37f33eda933e70e48b00c7b6e694645e0ce`  
		Last Modified: Fri, 20 Feb 2026 19:17:44 GMT  
		Size: 2.5 MB (2465561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e416b1ab5bbf0bf221fbfebc255d93515386ebdffaba15229355f981631945a0`  
		Last Modified: Fri, 20 Feb 2026 19:17:45 GMT  
		Size: 25.4 MB (25401329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074029fc6be547461af705573be19fc5833873eb078b59276b716e0212386159`  
		Last Modified: Fri, 20 Feb 2026 19:17:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81c1bf750bd228cd75e3e060f07de954b20baa432b8f56c2b4aaab4e0aed18e`  
		Last Modified: Fri, 20 Feb 2026 19:17:45 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e874ae0330fb23da5ea48731d08b1eacc0934ed2d686016039ffabe7ea1877`  
		Last Modified: Fri, 20 Feb 2026 19:17:46 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53eb36ce69a9417ce4c0c312cec0f998a448eab4ddc6927dd136b3103018b61d`  
		Last Modified: Fri, 20 Feb 2026 19:17:46 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:00bdeb09bb1ea8994f24eec74e7cdc2b0735b6e6b326291e7ae3d9dc1c5fb290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6963104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ba20df0c0a06b5074b0a8746fa74fdfcec7b661baf7f373dc63a94beffb444`

```dockerfile
```

-	Layers:
	-	`sha256:08e1b7d79591b6ebdbcc902ced8c7411ab53111b82ba370cf0d3501e3d8f3eb8`  
		Last Modified: Fri, 20 Feb 2026 19:17:44 GMT  
		Size: 675.7 KB (675709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33da44805702c777b00798eb622c2f4fe52f13e481c5d8c40275d8cc158eabb6`  
		Last Modified: Fri, 20 Feb 2026 19:17:44 GMT  
		Size: 3.2 MB (3190336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e212f5dd498238c61020708b37034f1ba9eb12bb890212dc1da9e5cd68dab1e3`  
		Last Modified: Fri, 20 Feb 2026 19:17:44 GMT  
		Size: 3.0 MB (3036751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff315c9c3e96cb7a610d4afb2cb82f8a4b889d8a325e9ab95fddcc6244872d0`  
		Last Modified: Fri, 20 Feb 2026 19:17:43 GMT  
		Size: 60.3 KB (60308 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:f7ec7c69cb34ce3f8ddef1b0d8e7a07adaabe28c1aa5b0d720eb68db910ed103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71750206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a86ce4e7e62674e244500208afc1d9580e79210f4591bf244ec63414d9a745`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 20 Feb 2026 19:17:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Feb 2026 19:17:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Feb 2026 19:17:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Feb 2026 19:17:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Feb 2026 19:17:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:17:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:17:31 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Feb 2026 19:17:31 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 20 Feb 2026 19:17:31 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Feb 2026 19:17:31 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Feb 2026 19:17:31 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:17:39 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Feb 2026 19:17:41 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Feb 2026 19:17:41 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Feb 2026 19:17:41 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:17:41 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Feb 2026 19:17:41 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Feb 2026 19:17:41 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 20 Feb 2026 19:17:41 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Feb 2026 19:17:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Feb 2026 19:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Feb 2026 19:17:41 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Feb 2026 19:17:41 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880b67f06c795062896744684ec3474908e84d786dafbc23d41a46899d797b5a`  
		Last Modified: Fri, 20 Feb 2026 19:17:49 GMT  
		Size: 33.5 MB (33518391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88238e0903a485d8b59eb7627d81b59cca805828404eeb3ee3005c263ed75bc8`  
		Last Modified: Fri, 20 Feb 2026 19:17:48 GMT  
		Size: 7.9 MB (7854416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25793ae56613a93d7071b2a73b85ba634b97c2071734bfbf4e8c6b2fa5f9bf2`  
		Last Modified: Fri, 20 Feb 2026 19:17:48 GMT  
		Size: 1.4 MB (1404597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92e0a570aa36d0be8dd6924f13ca78ac301b5ce9e9ba193f426a13bd2ee407d`  
		Last Modified: Fri, 20 Feb 2026 19:17:49 GMT  
		Size: 25.4 MB (25401237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42148150c5bd712668d5c7aa3f3a6e05ebdc59b1c14009af61dc329fad890f1e`  
		Last Modified: Fri, 20 Feb 2026 19:17:49 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8ee7934c14504076717727ad9628e4a234c7d04607369285d927b281a94a2a`  
		Last Modified: Fri, 20 Feb 2026 19:17:49 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08c1388332e042d4c5e2dbffd7ec2b5fa607908aa239b64435717387a57efb9`  
		Last Modified: Fri, 20 Feb 2026 19:17:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f0843215fe9912e5ee4001de3899b868ac174c30245c019bd585c8b2340f90`  
		Last Modified: Fri, 20 Feb 2026 19:17:50 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:183de6fad55cf50e67b951b1e5f2cf944222a5d8de4fdbcca6468f7f62362efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 KB (60290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e9ee4b299a29994b3597a656ea9b3d5e47184bc6792a17049035bf661c6ebe`

```dockerfile
```

-	Layers:
	-	`sha256:4ad6675d1d236cdb00a70c0b0f5a42b5a9f321a034d67d279d00becadc9a9f34`  
		Last Modified: Fri, 20 Feb 2026 19:17:47 GMT  
		Size: 60.3 KB (60290 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:da3296410d62d03f35fad92ea5cc8e542788dfadafab5baaed4fc8305d205b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70845189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fdcec4f0e3727886d85782dfdaa1cce2cca4f0a705d1e88bfe97d4565a2174`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Fri, 20 Feb 2026 19:19:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Feb 2026 19:19:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Feb 2026 19:19:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Feb 2026 19:19:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Feb 2026 19:19:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:19:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:19:11 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Feb 2026 19:19:11 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 20 Feb 2026 19:19:11 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Feb 2026 19:19:11 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Feb 2026 19:19:11 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:19:17 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Feb 2026 19:19:18 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Feb 2026 19:19:18 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Feb 2026 19:19:18 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:19:18 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Feb 2026 19:19:18 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Feb 2026 19:19:18 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 20 Feb 2026 19:19:18 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Feb 2026 19:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Feb 2026 19:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Feb 2026 19:19:18 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Feb 2026 19:19:18 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5ccda6b7b82981235d8044d5d5669fa1b97cd7c2d146f105a373feeb628bc0`  
		Last Modified: Fri, 20 Feb 2026 19:19:35 GMT  
		Size: 33.4 MB (33429718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eb3739f6007170841800c04e4dd3d5e7605ae67e4c046c8438e0de1929f7d0`  
		Last Modified: Fri, 20 Feb 2026 19:19:34 GMT  
		Size: 7.4 MB (7435297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4307bc12e214d33d3dd54f4e1ec178eebf729ad47671f5b4a70659e8002c6eb`  
		Last Modified: Fri, 20 Feb 2026 19:19:33 GMT  
		Size: 1.3 MB (1295876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e2a2d5062295bcd024974f4392873f78fac025f2ce99a1769b35a31efba41b`  
		Last Modified: Fri, 20 Feb 2026 19:19:34 GMT  
		Size: 25.4 MB (25400827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047cbbca82bd376bdbad8dacb581712f50137a7401234dca749ce87b94c49f03`  
		Last Modified: Fri, 20 Feb 2026 19:19:35 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fc66011d2b445671f137034d7c4b2ba3a6ad2fa22acf62965db7f25b391498`  
		Last Modified: Fri, 20 Feb 2026 19:19:35 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b6bebfe36a169d79cc5bae0823f5e942495d1dc6df97f67ce9233e3867b89d`  
		Last Modified: Fri, 20 Feb 2026 19:19:36 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb8235ccf7c1530b108a2f9cd671074fc6c870ae4f0fde9122d9c953227ee1f`  
		Last Modified: Fri, 20 Feb 2026 19:19:36 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0c632f2f21e27488d6aca200dfa1df45b3da8d68590768d5242253b507a8aec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7182c7916116f6944a51197b3fc4a440421ff105ee58293b3c6cf0deca2bb64c`

```dockerfile
```

-	Layers:
	-	`sha256:165e46dbefa70f8d5007d8764f662d9059c66817b832be22938739f28fec9018`  
		Last Modified: Fri, 20 Feb 2026 19:19:33 GMT  
		Size: 670.9 KB (670852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df84ccf6d373cb75a0cbb87b7ecd626d0686ba664efdaf4016c2ca8882178c59`  
		Last Modified: Fri, 20 Feb 2026 19:19:33 GMT  
		Size: 3.1 MB (3056827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b2904e1d05107800e5554afb14c4811d806fd329dfb1dfad532a45dc79ae73f`  
		Last Modified: Fri, 20 Feb 2026 19:19:33 GMT  
		Size: 2.9 MB (2901913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a279c2c2dd409b2af2ff50cf59ec2ca3ea47d97fed66aed2bed4f18dc7476935`  
		Last Modified: Fri, 20 Feb 2026 19:19:33 GMT  
		Size: 60.5 KB (60505 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:61c5065d6e0590fb2bac6d16488a261196398b2e788da616a34c98053864417e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82574567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d706fd373db1df545d487863016b92a4669cfba011e629ed4243cbd445898d87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Feb 2026 19:17:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Feb 2026 19:17:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Feb 2026 19:17:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Feb 2026 19:17:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Feb 2026 19:17:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:17:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:17:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Feb 2026 19:17:54 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 20 Feb 2026 19:17:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Feb 2026 19:17:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Feb 2026 19:17:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:18:00 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Feb 2026 19:18:01 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Feb 2026 19:18:01 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Feb 2026 19:18:01 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:18:01 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Feb 2026 19:18:01 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Feb 2026 19:18:01 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 20 Feb 2026 19:18:01 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Feb 2026 19:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Feb 2026 19:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Feb 2026 19:18:01 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Feb 2026 19:18:01 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a52ad2f7b813a6dfa648d5bad99cba347ed8a789338c71dcce7904ee1eb543`  
		Last Modified: Fri, 20 Feb 2026 19:18:19 GMT  
		Size: 40.5 MB (40480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011f88610022079709048f2daf517143c2c7b3a95c5995480998f88c4a24345e`  
		Last Modified: Fri, 20 Feb 2026 19:18:18 GMT  
		Size: 10.0 MB (9979281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00043580deb0e2da9846d4f719d46a48391d6856e1cbdac0a7126f1f72a5242`  
		Last Modified: Fri, 20 Feb 2026 19:18:17 GMT  
		Size: 2.5 MB (2514382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c0aae80508c1ee7f08d2350104110fab3c4879faf495706d57752f3ba9d9a8`  
		Last Modified: Fri, 20 Feb 2026 19:18:18 GMT  
		Size: 25.4 MB (25401334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3f177de1ff6656b87ba9e77d4de72efa4d2836b729bb82c2a3211f7a920250`  
		Last Modified: Fri, 20 Feb 2026 19:18:19 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7fa69f65ce48bf2f1b6db03e93145e27128c7530951ce02d43f954f0844a27`  
		Last Modified: Fri, 20 Feb 2026 19:18:19 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2d41863fbbc1d6aaaa1c22c1ed64b950ceb669e561d08c82d7284811a768f4`  
		Last Modified: Fri, 20 Feb 2026 19:18:20 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59e557422b3268b7c224ae54339541a47f2a3f9ea4ac8ba6909816c27ec9a13`  
		Last Modified: Fri, 20 Feb 2026 19:18:20 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:222819e1c809f67ef08d9195b160c832f70bc272f7420b6cd657b79cffabcba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7036081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9c82214d83eb38d5ff7f6dcf5bbf00a919e87bc7fbb9a21f7c2ae0649977d3`

```dockerfile
```

-	Layers:
	-	`sha256:94ed26e84d9010f8d0743170e9b499fa4b7da6615c429e2233e4027fa79d6df9`  
		Last Modified: Fri, 20 Feb 2026 19:18:17 GMT  
		Size: 675.9 KB (675852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b540f68f4e33633f657fd7bf95cc2cd71afb7d97eb5d977eb7fb9a799a4373b`  
		Last Modified: Fri, 20 Feb 2026 19:18:18 GMT  
		Size: 3.2 MB (3227295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50cb850080173ab850a0495bbfcc6e2c0775a3a828d0c8c6b2f355e828a6dd7b`  
		Last Modified: Fri, 20 Feb 2026 19:18:17 GMT  
		Size: 3.1 MB (3072387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f552e8b78f6c7831ee6c55e0e5a2590b8dd618a03f33c43f66d732545048ebf5`  
		Last Modified: Fri, 20 Feb 2026 19:18:17 GMT  
		Size: 60.5 KB (60547 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:4d8f952e8ecbecbc601c1d10ad955b28148d78e9f30fbab2cfe4caad7c17980c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73168952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95230abbaff0fff9450ae5f0339cc9926946987a43429bc1b97d1fde0ffdba6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Feb 2026 19:12:55 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Feb 2026 19:12:55 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Feb 2026 19:12:55 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Feb 2026 19:12:55 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Feb 2026 19:12:55 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:12:55 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:12:58 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Feb 2026 19:12:58 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 20 Feb 2026 19:12:58 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Feb 2026 19:12:58 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Feb 2026 19:12:58 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:13:03 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Feb 2026 19:13:04 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Feb 2026 19:13:04 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Feb 2026 19:13:04 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:13:04 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Feb 2026 19:13:04 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Feb 2026 19:13:04 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 20 Feb 2026 19:13:04 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Feb 2026 19:13:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Feb 2026 19:13:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Feb 2026 19:13:04 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Feb 2026 19:13:04 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de22a6898763704cebcbd5d40a4b662dcd99f3e7455e4e5a0c9895a6d9c240d0`  
		Last Modified: Fri, 20 Feb 2026 19:13:19 GMT  
		Size: 33.5 MB (33478994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cdb4960c5ce790e45ce6897677fcbb3a48d7a12ee236e50bae3e6293a0b1b1`  
		Last Modified: Fri, 20 Feb 2026 19:13:19 GMT  
		Size: 9.2 MB (9191402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c96f1636aa453cadca01f19c1f388378a8c39b7a878787cd127c2a0f7aba29`  
		Last Modified: Fri, 20 Feb 2026 19:13:18 GMT  
		Size: 1.4 MB (1409002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b421c7cae9bf5ebdc8b11d49f637fbc08f10f451ee5fb752aea9cd66a5f2493a`  
		Last Modified: Fri, 20 Feb 2026 19:13:19 GMT  
		Size: 25.4 MB (25400815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60694aa8816bf54ddd4382a5658c51c011b2f6e065e84f6990c47ce840d3d69`  
		Last Modified: Fri, 20 Feb 2026 19:13:20 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf705000a17f0f73c0c45cbe1fbfc0d8509d4d5e0ae0632499e5e40a07d2e2a`  
		Last Modified: Fri, 20 Feb 2026 19:13:20 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d0c5c7233fed858660ed70d61b3a7b81769a9b4b16fd5bc66ab13a45ded30f`  
		Last Modified: Fri, 20 Feb 2026 19:13:21 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3a104591832f15c3433ad86ce7602a2c09a884e12d2d10731ffa2b319af71a`  
		Last Modified: Fri, 20 Feb 2026 19:13:21 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:02c981d44d73735dbececd52e668d65f947822ea32d63d14a6505db146e6cf82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6914559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114179e57b037b72e6119c963bf4a741b8206a5b1cea6f2c88c43576f4a6fc53`

```dockerfile
```

-	Layers:
	-	`sha256:8f2ee2ebd78a42c909518f36d6d62238493eb0854d7b5f6030d4338c5d0c3c00`  
		Last Modified: Fri, 20 Feb 2026 19:13:18 GMT  
		Size: 670.7 KB (670704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fabe3a68ca99d31bd8f865ee2fd48d45c797ec55cdf48254c03ff55a60c01d23`  
		Last Modified: Fri, 20 Feb 2026 19:13:18 GMT  
		Size: 3.2 MB (3168589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db5d40b2b7cabdb9361ef2053e27fbbc2eac793732dd1e28b536b7f8e7aa61d8`  
		Last Modified: Fri, 20 Feb 2026 19:13:18 GMT  
		Size: 3.0 MB (3015008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa486b86854b4d2561c7fa1c94b2c5196d666612137eed46868d5b1e0af9bc6`  
		Last Modified: Fri, 20 Feb 2026 19:13:18 GMT  
		Size: 60.3 KB (60258 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:ecebdbb1423f0862832a69d7bbd2ae8e1345dbc7ca435473426781658bf98edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74818650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1eca0c2622b20daf331e4016d72fed3f180967cd05be9a112bc0e867c502d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Feb 2026 19:15:01 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Feb 2026 19:15:01 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Feb 2026 19:15:01 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Feb 2026 19:15:02 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Feb 2026 19:15:02 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:15:02 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:15:08 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Feb 2026 19:15:08 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 20 Feb 2026 19:15:08 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Feb 2026 19:15:08 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Feb 2026 19:15:08 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:15:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Feb 2026 19:15:23 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Feb 2026 19:15:24 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Feb 2026 19:15:24 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:15:24 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Feb 2026 19:15:24 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Feb 2026 19:15:24 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 20 Feb 2026 19:15:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Feb 2026 19:15:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Feb 2026 19:15:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Feb 2026 19:15:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Feb 2026 19:15:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc7cb17c54ac50cf1a89344f5a34389dc40b624e9361960d6d48167c3c0f748`  
		Last Modified: Fri, 20 Feb 2026 19:16:01 GMT  
		Size: 34.1 MB (34091198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631d19e2aa427472a21704eaae3d98f712f877b4ccd595005bf079a0e60b7b3c`  
		Last Modified: Fri, 20 Feb 2026 19:16:01 GMT  
		Size: 10.0 MB (9952632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755299ed22a42193da38c2e59d10d76b7da098de6a997a3763a8e6119de78244`  
		Last Modified: Fri, 20 Feb 2026 19:16:00 GMT  
		Size: 1.5 MB (1542643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd77480b6a1f06b9ef9c977321d3c414ef8680eb037d860fba98ed68e57a01d`  
		Last Modified: Fri, 20 Feb 2026 19:16:01 GMT  
		Size: 25.4 MB (25400782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90037a42fb4fbc2258873f6ba59336ab20f4ecadbdbd62f1f64720b12048e3f`  
		Last Modified: Fri, 20 Feb 2026 19:16:01 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6feb57b5d18e982b6e0b3c9e66c3032f61bf63ba428a689eb14c890faa63af2`  
		Last Modified: Fri, 20 Feb 2026 19:16:02 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61939138d53d218b7c285b288211d6a10bb713bd81d6cac9b07c5618d1407cca`  
		Last Modified: Fri, 20 Feb 2026 19:16:02 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ddf69fc0b6d8d98e5bfc14bda6be0e005d38592f5cd53765fdf25033ea3f75`  
		Last Modified: Fri, 20 Feb 2026 19:16:03 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:db8ab3f64ace0da13d0fa5502ecb8f2c73880ab31fd44461a31e9effd90a001a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6937756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cab824fd479a5fa84a33d26e503a91d84e1eb3cd19ca5a49504088ebe73201a`

```dockerfile
```

-	Layers:
	-	`sha256:5295083974cfd20588a6287a926f67ae9755acaa2c4e26279e6b7fbc6047abba`  
		Last Modified: Fri, 20 Feb 2026 19:16:00 GMT  
		Size: 670.8 KB (670849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2fa1ad4937e9dd42b12b0a1d4cfb004bf62f0d302eb563de46153ef61cacf45`  
		Last Modified: Fri, 20 Feb 2026 19:16:00 GMT  
		Size: 3.2 MB (3180730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83d7c7a39bb43e2712aca0c599e3b555f78f62c65fb1f74b4381eca76bf3f511`  
		Last Modified: Fri, 20 Feb 2026 19:16:00 GMT  
		Size: 3.0 MB (3025810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88f9a0dd50f898ab2331ea6fdd8ff921aaee1b8320620c6b24bf22fb73619465`  
		Last Modified: Fri, 20 Feb 2026 19:15:59 GMT  
		Size: 60.4 KB (60367 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:e702938754cfaa2a6fc05d842c3684fcad22580bf113219b287ab44591ee10d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78739224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6eec7517364853c8f5108b88571febf99751e4b9ae9c8f87fc979ff9b7d0cd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Fri, 20 Feb 2026 21:32:57 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Feb 2026 21:32:57 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Feb 2026 21:32:57 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Feb 2026 21:32:58 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Feb 2026 21:32:58 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 21:32:58 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Feb 2026 21:33:11 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Feb 2026 21:33:11 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 20 Feb 2026 21:33:11 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Feb 2026 21:33:11 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Feb 2026 21:33:11 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 21:33:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Feb 2026 21:34:03 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Feb 2026 21:34:03 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Feb 2026 21:34:03 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Feb 2026 21:34:03 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Feb 2026 21:34:03 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Feb 2026 21:34:03 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 20 Feb 2026 21:34:04 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Feb 2026 21:34:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Feb 2026 21:34:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Feb 2026 21:34:04 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Feb 2026 21:34:04 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb0d8589bf1d1582f0d4cf17446d285159e523deeb0a4c6c5bd3defe2fd5f27`  
		Last Modified: Fri, 20 Feb 2026 21:39:39 GMT  
		Size: 37.5 MB (37520770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1588ea5a3816ab1bff706167c39047d145f960df1f81f8fcb1db26ee79aeb763`  
		Last Modified: Fri, 20 Feb 2026 21:39:33 GMT  
		Size: 10.8 MB (10780483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440ce7659295697c061ef36b1ce413a25c3712878f22501e4ab66c59ed8949f1`  
		Last Modified: Fri, 20 Feb 2026 21:39:29 GMT  
		Size: 1.4 MB (1449907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e6c3c41487fd1bb899b322323d077c5d78deedbfae214280a0cfe339fc02fb`  
		Last Modified: Fri, 20 Feb 2026 21:39:38 GMT  
		Size: 25.4 MB (25401024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc4b5a4dfe3d1e7888fce7a950a5334a12577e807dc891680a5e1c4f0fe2e7c`  
		Last Modified: Fri, 20 Feb 2026 21:39:32 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e2d2c76ddb49b7d4e8fd22994c2f2738f5158e096032a8b66f01a6baeb5e3f`  
		Last Modified: Fri, 20 Feb 2026 21:39:34 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4034504d3c45795e6b7b393e828e3ef51cf0782feb76dd8218191f7f9f36af37`  
		Last Modified: Fri, 20 Feb 2026 21:39:35 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23af59f78f39dcf673ac7bf7c86fee8d6577fab3d64368d23d5e10db5234385`  
		Last Modified: Fri, 20 Feb 2026 21:39:36 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:dc6fcd4abe821202872fe28b3323b9e70b8dcb7583bb0728bdb5dc54499e682b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec822b570b254f54f6cdaee8584c935167678328653c538427ff7ab52017f1c0`

```dockerfile
```

-	Layers:
	-	`sha256:9830e43652da92d77853f410d12a277b45a154f50b887cd77fa4ce6dc8ece58c`  
		Last Modified: Fri, 20 Feb 2026 21:39:29 GMT  
		Size: 673.8 KB (673818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01aa2ca5ca9301d8745b0b0557b3a7bc8117e989cdf640b87d7df4a22604aac5`  
		Last Modified: Fri, 20 Feb 2026 21:39:29 GMT  
		Size: 3.2 MB (3218845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b46de9b8ce485b77f680e2d735f4522fa0c46e8a1e9a82786b3c2062ed248ed`  
		Last Modified: Fri, 20 Feb 2026 21:39:30 GMT  
		Size: 3.1 MB (3063937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaae7100c815af2ba113eb059f4a1f85a9ee2368417fc587c9f62264ba195068`  
		Last Modified: Fri, 20 Feb 2026 21:39:29 GMT  
		Size: 60.4 KB (60377 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:09186f49bdddc1d04ec0a39b9e55fa9182ffde756bfd5fbb38fc76bff2c3e851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72913056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a45ff73ff65bec6003aa843b24edd71788ebdaf5ae37e35cb95281f8590414a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 20 Feb 2026 19:17:59 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Feb 2026 19:17:59 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Feb 2026 19:17:59 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Feb 2026 19:18:00 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Feb 2026 19:18:00 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:18:00 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:18:08 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Feb 2026 19:18:08 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 20 Feb 2026 19:18:08 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Feb 2026 19:18:08 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Feb 2026 19:18:08 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:18:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Feb 2026 19:18:22 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Feb 2026 19:18:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Feb 2026 19:18:22 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:18:22 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Feb 2026 19:18:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Feb 2026 19:18:22 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 20 Feb 2026 19:18:24 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Feb 2026 19:18:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Feb 2026 19:18:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Feb 2026 19:18:24 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Feb 2026 19:18:24 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e97c8c8c4a68253e472e0c4aab85a9d4ae52c996df4223f15d2b1ec59557d5`  
		Last Modified: Fri, 20 Feb 2026 19:19:00 GMT  
		Size: 33.9 MB (33929378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b24ff1eb84e7426bc97faa273ed09079fff68765db70c518cdf4107741ee2a7`  
		Last Modified: Fri, 20 Feb 2026 19:18:59 GMT  
		Size: 8.3 MB (8339888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd99a96f3128870b2e3d8a48c61b73846cd00bfba1f465beddcc8888df31432c`  
		Last Modified: Fri, 20 Feb 2026 19:18:59 GMT  
		Size: 1.5 MB (1515896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2c1f4747c21378c0979d3db54dd91de3347f99e39a2d26f24444d080fba466`  
		Last Modified: Fri, 20 Feb 2026 19:18:59 GMT  
		Size: 25.4 MB (25400804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ed2bceca41f7cda3736cbce5662dba7df3803b329d28500cd0a005c7b43d17`  
		Last Modified: Fri, 20 Feb 2026 19:19:00 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2857f442707ddd5e03a441b5080a9ce100ba257dbb4e3b1281471d8918c382ca`  
		Last Modified: Fri, 20 Feb 2026 19:19:00 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c1495456d57634e059724d97cacad6046c2bf08261388f800c481807ce57bd`  
		Last Modified: Fri, 20 Feb 2026 19:19:01 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a489c22c5de1cb81ecf55f6c10f5dd6d275e348fd62149a5e1c0a857d31f56a`  
		Last Modified: Fri, 20 Feb 2026 19:19:01 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9af63a9979b506e01021a33721d62dead537ffef5b9ede45fcf1eebd7a8a688b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6714140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea1cdea641b0bc040045ef4c9da0633de1295440e116bb3a5df223e76988b1c`

```dockerfile
```

-	Layers:
	-	`sha256:5d07a9f2cce38022b61cb4ff922797b9a0e614fb45e6562e474fc7242c328f3e`  
		Last Modified: Fri, 20 Feb 2026 19:18:59 GMT  
		Size: 670.8 KB (670815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d28f70c47dea2beae70e148b3553ee5dc8a36f1796bdc7ad9b48d04ed5a6a00`  
		Last Modified: Fri, 20 Feb 2026 19:18:59 GMT  
		Size: 3.1 MB (3068954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e47f615c002e814f50729c1f892ba6f7a3a1538d56e0ed48897a6eb7ae9741fa`  
		Last Modified: Fri, 20 Feb 2026 19:18:59 GMT  
		Size: 2.9 MB (2914064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cdf700d0107ab66bd9289189ed0749764260c0a74ed017fe7323dcaa816f205`  
		Last Modified: Fri, 20 Feb 2026 19:18:59 GMT  
		Size: 60.3 KB (60307 bytes)  
		MIME: application/vnd.in-toto+json
