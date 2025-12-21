## `rabbitmq:management-alpine`

```console
$ docker pull rabbitmq@sha256:f10f014d87ff75a34f512eb7e51d0e841021e3888568712ed731032fd8d92d34
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

### `rabbitmq:management-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:bca5611a1b4cf974be29db61b5caf3cc241b228df12785968924767ecce9c22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88441654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928a7167153aa7e958afe7c51a17138892272bd37d62c4e2e6c4b27273241dc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:43:11 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 18 Dec 2025 00:43:11 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 18 Dec 2025 00:43:11 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 18 Dec 2025 00:43:11 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 18 Dec 2025 00:43:11 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:43:11 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 18 Dec 2025 00:43:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 18 Dec 2025 00:43:13 GMT
ENV RABBITMQ_VERSION=4.2.2
# Thu, 18 Dec 2025 00:43:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 18 Dec 2025 00:43:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 18 Dec 2025 00:43:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:43:19 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 18 Dec 2025 00:43:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 18 Dec 2025 00:43:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 18 Dec 2025 00:43:20 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 18 Dec 2025 00:43:20 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 18 Dec 2025 00:43:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 00:43:20 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 18 Dec 2025 00:43:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 18 Dec 2025 00:43:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:43:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:43:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 18 Dec 2025 00:43:20 GMT
CMD ["rabbitmq-server"]
# Thu, 18 Dec 2025 01:21:45 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 18 Dec 2025 01:21:46 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.20.0/rabbitmqadmin-2.20.0-x86_64-unknown-linux-musl'; digest='017747084312a47c38eca52942e6f0dd06f5ab845ac0ce7e744d63de253cd0d6' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.20.0/rabbitmqadmin-2.20.0-aarch64-unknown-linux-musl'; digest='13a9f4f0457c95dbe5739a357663b18bda927b277ebdefe5038f0f9bf2b96570' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 18 Dec 2025 01:21:46 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc878640de49edbec879d5501fd914072b22a27bc988871d8846989cb967d32`  
		Last Modified: Thu, 18 Dec 2025 00:43:49 GMT  
		Size: 42.6 MB (42598832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2b3fb0fc24d3f54fb07b659349be29fa94d1bf5d2f103242c7966f5f901937`  
		Last Modified: Thu, 18 Dec 2025 00:43:44 GMT  
		Size: 9.2 MB (9206830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847a9a6aa2c8b01ca151a25685806b7ff775a4655ffe5f9d05edf4104ebc136b`  
		Last Modified: Thu, 18 Dec 2025 00:43:44 GMT  
		Size: 2.5 MB (2465569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d2b8dd6daa8698583e7bf8570a7f0b6eded142331c1b4d143319be80609c4e`  
		Last Modified: Thu, 18 Dec 2025 00:43:45 GMT  
		Size: 25.3 MB (25317128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d901a09e06dcbf509f04cccecba79c8af1530e0c8a43a4e1a484e1ad7c17d202`  
		Last Modified: Thu, 18 Dec 2025 00:43:43 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2dbf81a9b8bf66535a48484356b0e4760267ff27a981acfa18402a87d4efdb`  
		Last Modified: Thu, 18 Dec 2025 00:43:43 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259d35df5296e2123e4b76e0bd939d026f4444420040704f08148f355bb6d922`  
		Last Modified: Thu, 18 Dec 2025 00:43:43 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554988c62edb19856d5c2a5a966a43bc5817b50bdf9556c6bcba8e463c2cc74d`  
		Last Modified: Thu, 18 Dec 2025 00:43:43 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3069cce1475aff01ca04584bdb2c45f182448bae7faae2744c7cf6dbda5e0787`  
		Last Modified: Thu, 18 Dec 2025 01:21:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0128252320add78fa94b1c1afedd60ae6c43cde2db7d178734f510070b0297`  
		Last Modified: Thu, 18 Dec 2025 01:21:58 GMT  
		Size: 5.0 MB (4991170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:93788741e5d77508d480220f0f6a1a41e36025a13aba202cb6d0ce2309cf05c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.0 KB (691024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211eb60484bb34d7ce2cdadb66f4df659e9ed7b4edbea1b411835a7b282a77d2`

```dockerfile
```

-	Layers:
	-	`sha256:94baff32813ac674bce43b82a2ee512225f462b023cde516c4c70f9cfcdf771d`  
		Last Modified: Thu, 18 Dec 2025 04:52:53 GMT  
		Size: 675.8 KB (675785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca22a0c6edb7fecb0ce95246fed7772f94b91fce1a950ae8ab296f59990b9f1`  
		Last Modified: Thu, 18 Dec 2025 04:52:53 GMT  
		Size: 15.2 KB (15239 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:eb5636536054f9fdeeecd5415125c5094e4d3a83282795b03ceccd91e4250688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71653900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e72ef1ad8baea9b6012d12c29493837f9ff05224649f6d274f4832e645e126c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:02:37 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 18 Dec 2025 01:02:37 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 18 Dec 2025 01:02:37 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 18 Dec 2025 01:02:37 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 18 Dec 2025 01:02:37 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:02:37 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 18 Dec 2025 01:02:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 18 Dec 2025 01:02:40 GMT
ENV RABBITMQ_VERSION=4.2.2
# Thu, 18 Dec 2025 01:02:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 18 Dec 2025 01:02:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 18 Dec 2025 01:02:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:02:49 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 18 Dec 2025 01:02:50 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 18 Dec 2025 01:02:51 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 18 Dec 2025 01:02:51 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 18 Dec 2025 01:02:51 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 18 Dec 2025 01:02:51 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 01:02:51 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 18 Dec 2025 01:02:51 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 18 Dec 2025 01:02:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:02:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:02:51 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 18 Dec 2025 01:02:51 GMT
CMD ["rabbitmq-server"]
# Thu, 18 Dec 2025 01:42:36 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 18 Dec 2025 01:42:37 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.20.0/rabbitmqadmin-2.20.0-x86_64-unknown-linux-musl'; digest='017747084312a47c38eca52942e6f0dd06f5ab845ac0ce7e744d63de253cd0d6' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.20.0/rabbitmqadmin-2.20.0-aarch64-unknown-linux-musl'; digest='13a9f4f0457c95dbe5739a357663b18bda927b277ebdefe5038f0f9bf2b96570' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 18 Dec 2025 01:42:37 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbe4c111a2a0433756d159b026e74fe6186b0bfebff4f505a489535b871d757`  
		Last Modified: Thu, 18 Dec 2025 01:03:07 GMT  
		Size: 33.5 MB (33504388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd995c028c236f6dc09cd69589e6dfee828627b7320aea95438debb978b2491`  
		Last Modified: Thu, 18 Dec 2025 01:03:05 GMT  
		Size: 7.9 MB (7857211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f7ba9ead28cee49fcef78fb534d76d258b951ef25f3c801bc159a306811a3b`  
		Last Modified: Thu, 18 Dec 2025 01:03:04 GMT  
		Size: 1.4 MB (1404613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d3fb7b94b744655403ab4e8bc30f4eaa9a14206b21f6d03ebec7ce595be384`  
		Last Modified: Thu, 18 Dec 2025 01:03:09 GMT  
		Size: 25.3 MB (25317196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4755f9994732bb5ccad4a94b33251e0261f906abea736c87f95d2fc5df4ede`  
		Last Modified: Thu, 18 Dec 2025 01:03:05 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c66dbbb7c619ec636df248257b872b2f9a1f405e3fd12b4c7990c1e2ec046d`  
		Last Modified: Thu, 18 Dec 2025 01:03:05 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d17ef2f1e6d3d704f6c2d4da1408c503e8fe340579fcbde1bbf3cad0f68928`  
		Last Modified: Thu, 18 Dec 2025 01:03:05 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b22d99f86c3c1172f3c0e6c584f457df7cd85db9d3439deffbcf339d4e48ccd`  
		Last Modified: Thu, 18 Dec 2025 01:03:05 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f967c110749fe6aa9b57318c750b8b5d94de94a39706bc30d83ff20edb7b62`  
		Last Modified: Thu, 18 Dec 2025 01:42:47 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:17323cf4303c78222a390cbebee68032960c0544d323f11d3812c2bccf9810f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c8fe3df59eaab0713b6b348c040894da6c7f2919cacb2ffb58ba6eb76cb278`

```dockerfile
```

-	Layers:
	-	`sha256:99d7d9921758ec7d9840cb08a70dd5f6127b9aa590bc71c290b3421317dc0ddb`  
		Last Modified: Thu, 18 Dec 2025 04:52:57 GMT  
		Size: 15.1 KB (15112 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:f5579943363d0f097c15d8f9c706552f7172867539f2ec888c0fabf463b01f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70750397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3081d72dbe792e91a9cac88a856960628da773f11297530517d603cd484e4fe2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:05:18 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 18 Dec 2025 01:05:18 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 18 Dec 2025 01:05:18 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 18 Dec 2025 01:05:19 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 18 Dec 2025 01:05:19 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:05:19 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 18 Dec 2025 01:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 18 Dec 2025 01:05:21 GMT
ENV RABBITMQ_VERSION=4.2.2
# Thu, 18 Dec 2025 01:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 18 Dec 2025 01:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 18 Dec 2025 01:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:05:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 18 Dec 2025 01:05:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 18 Dec 2025 01:05:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 18 Dec 2025 01:05:29 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 18 Dec 2025 01:05:29 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 18 Dec 2025 01:05:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 01:05:29 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 18 Dec 2025 01:05:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 18 Dec 2025 01:05:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:05:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 18 Dec 2025 01:05:29 GMT
CMD ["rabbitmq-server"]
# Thu, 18 Dec 2025 01:43:13 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 18 Dec 2025 01:43:13 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.20.0/rabbitmqadmin-2.20.0-x86_64-unknown-linux-musl'; digest='017747084312a47c38eca52942e6f0dd06f5ab845ac0ce7e744d63de253cd0d6' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.20.0/rabbitmqadmin-2.20.0-aarch64-unknown-linux-musl'; digest='13a9f4f0457c95dbe5739a357663b18bda927b277ebdefe5038f0f9bf2b96570' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 18 Dec 2025 01:43:13 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97b2ecda41c2e368e455d27a478de5faeb0d4c4756985f2349582efca7e62eb`  
		Last Modified: Thu, 18 Dec 2025 01:06:00 GMT  
		Size: 33.4 MB (33409218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5abe74fdd036b9bea8a728aeba74f66161af86867fe4fec4e04279d38fee397`  
		Last Modified: Thu, 18 Dec 2025 01:05:54 GMT  
		Size: 7.4 MB (7447227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a15d44b8a87df525fd0eb9994ad17101ed81eaea739c93e52c7aa3046070136`  
		Last Modified: Thu, 18 Dec 2025 01:05:53 GMT  
		Size: 1.3 MB (1295842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890aa995edbed8658042813a84a480bafe086fed2a7742f191aca7f436baf663`  
		Last Modified: Thu, 18 Dec 2025 01:05:55 GMT  
		Size: 25.3 MB (25316669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a6fdaac027724e74ab7a4b4d414e1e861d59c3ebe30a713bd1c466e6c65475`  
		Last Modified: Thu, 18 Dec 2025 01:05:52 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7932a0d672b810c9f4c3af95f8baee511970ff01295198051e5c2e090527ced5`  
		Last Modified: Thu, 18 Dec 2025 01:05:53 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4161ca153704d43c7c6c8dffed1567aa7746a6429aadbd197b9c914a1629b62c`  
		Last Modified: Thu, 18 Dec 2025 01:05:53 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a673791c7a0bc7aa9998bce6d08a25b8feac96545ea2e975884b6f75fb3bb`  
		Last Modified: Thu, 18 Dec 2025 01:05:53 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fb1501b927e2f55a4927a80694a80bbd8cecd186273f7f3fb7f55e59d88ef4`  
		Last Modified: Thu, 18 Dec 2025 01:43:25 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1bc7bb4d8ada0bd71ef5f165ae93f7b37945ca54f5072735e4e1f2e8c18726c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.3 KB (686255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35458979f28924c73252f57d589351a0dce2ace812db8576d04851dda31689c`

```dockerfile
```

-	Layers:
	-	`sha256:a10c1140ff7df7d10e432b303a2c7c23b21dbddfd38fc4e9d85408b109e1df17`  
		Last Modified: Thu, 18 Dec 2025 04:53:11 GMT  
		Size: 670.9 KB (670928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c0992230eae273fc312bfc623660f5d12a5ce4cceae09f89035ca70b52c2e30`  
		Last Modified: Thu, 18 Dec 2025 04:53:11 GMT  
		Size: 15.3 KB (15327 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:56c3fe9f06ce449d9148f42f998a7fedcd8a119f49f53ebb04e56b9a968c54c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87095208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4da94e7ffd6052ab2a30660b6500ba7b3dfa0fbac74eb58aa0f07583d29f2a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:46:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 18 Dec 2025 00:46:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 18 Dec 2025 00:46:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 18 Dec 2025 00:46:51 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 18 Dec 2025 00:46:51 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:46:51 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 18 Dec 2025 00:46:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 18 Dec 2025 00:46:53 GMT
ENV RABBITMQ_VERSION=4.2.2
# Thu, 18 Dec 2025 00:46:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 18 Dec 2025 00:46:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 18 Dec 2025 00:46:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:46:59 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 18 Dec 2025 00:47:00 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 18 Dec 2025 00:47:00 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 18 Dec 2025 00:47:00 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 18 Dec 2025 00:47:00 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 18 Dec 2025 00:47:00 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 00:47:00 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 18 Dec 2025 00:47:00 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 18 Dec 2025 00:47:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:47:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:47:00 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 18 Dec 2025 00:47:00 GMT
CMD ["rabbitmq-server"]
# Thu, 18 Dec 2025 01:31:24 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 18 Dec 2025 01:31:25 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.20.0/rabbitmqadmin-2.20.0-x86_64-unknown-linux-musl'; digest='017747084312a47c38eca52942e6f0dd06f5ab845ac0ce7e744d63de253cd0d6' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.20.0/rabbitmqadmin-2.20.0-aarch64-unknown-linux-musl'; digest='13a9f4f0457c95dbe5739a357663b18bda927b277ebdefe5038f0f9bf2b96570' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 18 Dec 2025 01:31:25 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b353084ce0e49f3438c5aca9e4e4aceaf099f1867be377c5c34910cc9133e1`  
		Last Modified: Thu, 18 Dec 2025 00:47:31 GMT  
		Size: 40.5 MB (40454885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9947c134b4924a1d46a2403966d38b1795b60e0f1f74e4ddfd8a821255aa562f`  
		Last Modified: Thu, 18 Dec 2025 00:47:25 GMT  
		Size: 10.0 MB (9987910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd256d04ff3d32922e489612b10aa4b36d85a26c5d167ba48c4c3d1f8e5eb081`  
		Last Modified: Thu, 18 Dec 2025 00:47:25 GMT  
		Size: 2.5 MB (2514383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3824e4a7686b5fe6b72dc544830fff8fb348b498fbb4c1a248f44c61b264ab97`  
		Last Modified: Thu, 18 Dec 2025 00:47:27 GMT  
		Size: 25.3 MB (25317281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275a782d8eff888f9e26b08988ad00eefea48cbfa0e749b4b3e3bb6052f74f24`  
		Last Modified: Thu, 18 Dec 2025 00:47:25 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94c3258c54ba3be1bbc67d5b2b8b5bfc9d1065c509ed70dc0b5e8dd30f2e9cb`  
		Last Modified: Thu, 18 Dec 2025 00:47:25 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a4e04aed125148d178a854fc60ad4c25f7cd0b2152990ce6b5e43bfbf86e5b`  
		Last Modified: Thu, 18 Dec 2025 00:47:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6924c2d8b1dcd6984c73ef41ba9dbf2faea78b208e482a0f50f09218c9bd7f85`  
		Last Modified: Thu, 18 Dec 2025 00:47:24 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61fc4478bc91162a923d100061d434ba51ff084d63cbf959f7fb3fab17bf60b`  
		Last Modified: Thu, 18 Dec 2025 01:31:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ad39ecadaafc69ae5e00ab19013d16eb881f1dc0ac48c72a1fbc6b188022e1`  
		Last Modified: Thu, 18 Dec 2025 01:31:38 GMT  
		Size: 4.6 MB (4622989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5570c277e44a5b11556e4c71e32fe7ddd61fb96dd94692278b773c3d090683d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.3 KB (691286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddab6d483bcf8b9f5fc394b8be150c1c0197e297568fcda8c4735ed5360bc1f6`

```dockerfile
```

-	Layers:
	-	`sha256:6f5dcb80cae6a0f2b81ffa6f9ed065f71e70e1abaf34683ca265dc76d1021c41`  
		Last Modified: Thu, 18 Dec 2025 04:53:15 GMT  
		Size: 675.9 KB (675928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6bef05be514fd564987bd84f1ef1882e932a8ac64e66e6fd2eef2dec7b0cc5d`  
		Last Modified: Thu, 18 Dec 2025 04:53:15 GMT  
		Size: 15.4 KB (15358 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:76d5b625620b1f65a01b9d58bde1e8278b0fa5f9abc989ddb3e065419e9e1c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73070206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affc249003e8915cd5e85834a26e66556122add01a39200513e22629a5c199e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:44:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 18 Dec 2025 00:44:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 18 Dec 2025 00:44:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 18 Dec 2025 00:44:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 18 Dec 2025 00:44:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:44:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 18 Dec 2025 00:44:17 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 18 Dec 2025 00:44:17 GMT
ENV RABBITMQ_VERSION=4.2.2
# Thu, 18 Dec 2025 00:44:17 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 18 Dec 2025 00:44:17 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 18 Dec 2025 00:44:17 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:44:22 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 18 Dec 2025 00:44:23 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 18 Dec 2025 00:44:23 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 18 Dec 2025 00:44:23 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 18 Dec 2025 00:44:23 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 18 Dec 2025 00:44:23 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 00:44:23 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 18 Dec 2025 00:44:23 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 18 Dec 2025 00:44:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:44:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:44:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 18 Dec 2025 00:44:23 GMT
CMD ["rabbitmq-server"]
# Thu, 18 Dec 2025 01:19:43 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 18 Dec 2025 01:19:43 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.20.0/rabbitmqadmin-2.20.0-x86_64-unknown-linux-musl'; digest='017747084312a47c38eca52942e6f0dd06f5ab845ac0ce7e744d63de253cd0d6' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.20.0/rabbitmqadmin-2.20.0-aarch64-unknown-linux-musl'; digest='13a9f4f0457c95dbe5739a357663b18bda927b277ebdefe5038f0f9bf2b96570' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 18 Dec 2025 01:19:43 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d46d10e7d721607dbfda20812f27dd3b0dc50998291210732603d3ab1ef397e`  
		Last Modified: Thu, 18 Dec 2025 00:44:48 GMT  
		Size: 33.5 MB (33458989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6324fac6e6681e6e57e11cad647adc94b8b57496355c0bfcb99845a79fdede71`  
		Last Modified: Thu, 18 Dec 2025 00:44:49 GMT  
		Size: 9.2 MB (9197855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0018b436fdb8ae80b83e087b37b29611caa85bcbdab575ecfa8b0213fcffa4`  
		Last Modified: Thu, 18 Dec 2025 00:44:46 GMT  
		Size: 1.4 MB (1408983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440ef39f99d3001c9eae51fbdda7199a7a5fad4082817d9a1e5b5e8a88875036`  
		Last Modified: Thu, 18 Dec 2025 00:44:47 GMT  
		Size: 25.3 MB (25316227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14042a887ad894e0122e23ffe07b0f5a72fa530d1bf77192f2de5f7d6d46759e`  
		Last Modified: Thu, 18 Dec 2025 00:44:44 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd8522d5e5f524da3f5cebec0cd1714779af0f6c6883ebea2ce46a6389cfd1f`  
		Last Modified: Thu, 18 Dec 2025 00:44:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87132d5b08b3de8e63d1c8394a7c6209583af1b2b49153aece757c198efb14c`  
		Last Modified: Thu, 18 Dec 2025 00:44:44 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b89ece089081c30e80f3efcd2b8f67c46278a2057748a6d48a0833503ba9dc`  
		Last Modified: Thu, 18 Dec 2025 00:44:44 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49aa59c5ba7587e2e081d4ff18fd7ca1e8bd11fe87b3d29a794cdb428ab6096`  
		Last Modified: Thu, 18 Dec 2025 01:19:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1479eede3a84f104901627d598e34aad46e669089b1a6707d3067673c3891ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.0 KB (685980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd11f7122e29a51898f582accf27c6f876f1fb7a22eda6dd326a5d443754cd2`

```dockerfile
```

-	Layers:
	-	`sha256:f9fb15c43c4116565c5566e6aa35940d8d472136d3b68256b2059fd84560c2f9`  
		Last Modified: Thu, 18 Dec 2025 04:53:19 GMT  
		Size: 670.8 KB (670780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71f1cbe9b03d96f1b4f37c1a5ffb6333ef1de44ee915303a6522d4a019624d07`  
		Last Modified: Thu, 18 Dec 2025 04:53:19 GMT  
		Size: 15.2 KB (15200 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:7eabe7d22443d61a99f0b214100a232e984d13b8a99594cdebbc736c60645d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74712924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc8498102f4dd5c7405e4d0a2eb170cfe1fe1f8d9763d9ecbdfe65637143139`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 02:13:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 18 Dec 2025 02:13:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 18 Dec 2025 02:13:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 18 Dec 2025 02:13:51 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 18 Dec 2025 02:13:51 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 02:13:51 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 18 Dec 2025 02:13:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 18 Dec 2025 02:13:55 GMT
ENV RABBITMQ_VERSION=4.2.2
# Thu, 18 Dec 2025 02:13:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 18 Dec 2025 02:13:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 18 Dec 2025 02:13:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 02:14:06 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 18 Dec 2025 02:14:08 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 18 Dec 2025 02:14:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 18 Dec 2025 02:14:09 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 18 Dec 2025 02:14:09 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 18 Dec 2025 02:14:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 02:14:09 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 18 Dec 2025 02:14:10 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 18 Dec 2025 02:14:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 02:14:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 02:14:10 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 18 Dec 2025 02:14:10 GMT
CMD ["rabbitmq-server"]
# Thu, 18 Dec 2025 03:41:49 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 18 Dec 2025 03:41:52 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.20.0/rabbitmqadmin-2.20.0-x86_64-unknown-linux-musl'; digest='017747084312a47c38eca52942e6f0dd06f5ab845ac0ce7e744d63de253cd0d6' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.20.0/rabbitmqadmin-2.20.0-aarch64-unknown-linux-musl'; digest='13a9f4f0457c95dbe5739a357663b18bda927b277ebdefe5038f0f9bf2b96570' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 18 Dec 2025 03:41:52 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d162d3b63753d8d295a891a775d5181faa0d31da719ee5b720c1a12648a955e`  
		Last Modified: Thu, 18 Dec 2025 02:14:59 GMT  
		Size: 34.1 MB (34067297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51eb38d1e95e64f0eaf411ad100f93397b95cb10b0d02a4a39c57a64e8d0ccc`  
		Last Modified: Thu, 18 Dec 2025 02:14:56 GMT  
		Size: 10.0 MB (9956656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881ebbc002c6144a03814927d9bacd35c4563b345650b5f49fe968f7872a4fb1`  
		Last Modified: Thu, 18 Dec 2025 02:14:54 GMT  
		Size: 1.5 MB (1542636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0e5700a7b386c993a0f5080dd07617f5106cd0cd70f793068c945015a3e968`  
		Last Modified: Thu, 18 Dec 2025 02:14:56 GMT  
		Size: 25.3 MB (25316520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e66b218be1d46f74370b204e011480a84660403edcb24abba12b15eb4171b5`  
		Last Modified: Thu, 18 Dec 2025 02:14:54 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab58c33eeecf0e155699dcb35ab8ae344921db14cdb043faa5590356f92699ac`  
		Last Modified: Thu, 18 Dec 2025 02:14:54 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d40f5ff035b589767183847b34f228990fc23bab8c439d4d2f5ec062583d97`  
		Last Modified: Thu, 18 Dec 2025 02:14:54 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd26448c3d1263489a02899d424e4705ab12f68381f6b589b48a870edeae088e`  
		Last Modified: Thu, 18 Dec 2025 02:14:54 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ad027c54f9d5763604f03e08876271422b94574ea8a0120143099f2e03af4f`  
		Last Modified: Thu, 18 Dec 2025 03:42:13 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7e2a95ab4bc82d0a7171e93b5be192f2123e5f1c26da2ae7d48ed11cae16e099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.2 KB (686205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fb12dd9f7454822c02812784bc695a9bdbb51f9a17bb3e51f1452c6236b264`

```dockerfile
```

-	Layers:
	-	`sha256:e3ca1ae7f0729884ea8f67ae7b4d151f3e95d9c7677ee708d63177a7f5ddd2f7`  
		Last Modified: Thu, 18 Dec 2025 04:53:23 GMT  
		Size: 670.9 KB (670925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b551c095c24b72348459387c94d96a4f404de611935aee9c54041a919610d65`  
		Last Modified: Thu, 18 Dec 2025 04:53:24 GMT  
		Size: 15.3 KB (15280 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:30488d2e96f38183a5b7b0ebd24c03529e119554bcbdef3b23a447fcf304be97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78639189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a9d71a64cabbe862f72759fed667aa330335de2b167e032134d06d52607f6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 10:52:06 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 19 Dec 2025 10:52:06 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 19 Dec 2025 10:52:06 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 19 Dec 2025 10:52:07 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 19 Dec 2025 10:52:07 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 10:52:07 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 19 Dec 2025 10:52:19 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 19 Dec 2025 10:52:19 GMT
ENV RABBITMQ_VERSION=4.2.2
# Fri, 19 Dec 2025 10:52:19 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 19 Dec 2025 10:52:19 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 19 Dec 2025 10:52:19 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 10:52:56 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 19 Dec 2025 10:53:05 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 19 Dec 2025 10:53:05 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 19 Dec 2025 10:53:05 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 19 Dec 2025 10:53:05 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 19 Dec 2025 10:53:05 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 19 Dec 2025 10:53:05 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 19 Dec 2025 10:53:06 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 19 Dec 2025 10:53:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 10:53:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 10:53:06 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 19 Dec 2025 10:53:06 GMT
CMD ["rabbitmq-server"]
# Sun, 21 Dec 2025 14:44:53 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Sun, 21 Dec 2025 14:44:54 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.20.0/rabbitmqadmin-2.20.0-x86_64-unknown-linux-musl'; digest='017747084312a47c38eca52942e6f0dd06f5ab845ac0ce7e744d63de253cd0d6' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.20.0/rabbitmqadmin-2.20.0-aarch64-unknown-linux-musl'; digest='13a9f4f0457c95dbe5739a357663b18bda927b277ebdefe5038f0f9bf2b96570' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Sun, 21 Dec 2025 14:44:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b16024bea26483c4ecdc60f404c46f57cb84a272c2b594f7f0c40f0b7ca50fb`  
		Last Modified: Fri, 19 Dec 2025 10:57:23 GMT  
		Size: 37.5 MB (37499627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76990ab68bc0fa49949abd7d842d2e3cec338241d21b8d9c5bfb92f2e9746b54`  
		Last Modified: Fri, 19 Dec 2025 10:57:21 GMT  
		Size: 10.8 MB (10786312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff510e29b3470403ce0d3bd1912ea1c8a301f188fadac32a33a5bf6a7940f12f`  
		Last Modified: Fri, 19 Dec 2025 10:57:20 GMT  
		Size: 1.4 MB (1449944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666f4cf3f20e4f9a788134aab3e97c7f6b6824f97c9ae8b231a412121e1b6d08`  
		Last Modified: Fri, 19 Dec 2025 10:57:22 GMT  
		Size: 25.3 MB (25317306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34db82d643b5fb83f1ee2788f9dec1b8d0ce2069d4353f8eec6335713bd0ed9b`  
		Last Modified: Fri, 19 Dec 2025 10:57:20 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b5c0f5d1d4ecba1131ed45747ea34fa1474cb0e4541d511e3c8cc2a4633adf`  
		Last Modified: Fri, 19 Dec 2025 10:57:20 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d9f78729104f576101b211bdac1f9d14473ccc12a8f0bcc0c8e7553f3d99fb`  
		Last Modified: Fri, 19 Dec 2025 10:57:21 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73341f048365011751f92cb6e6342f2ed59b16b60085944724ec8ff41cc58ac1`  
		Last Modified: Fri, 19 Dec 2025 10:57:21 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2eccf5508c63f294eecf2d1f6ddf856767535c63d8156ab072af9c3e44bb4a0`  
		Last Modified: Sun, 21 Dec 2025 14:45:53 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cff0c39a3685046a46dcc5203661b35ad1651e7e41ce805a56eea0fc2e96fdaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.2 KB (689177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad022b4439e57786ce65344d869511844c7d99d7a4541ffb314acf5d3df827a`

```dockerfile
```

-	Layers:
	-	`sha256:4c93829b54a5d9ffcd3375f9ee09a964bbadb1e7270e3ba7f8a0b048814e3e79`  
		Last Modified: Sun, 21 Dec 2025 16:52:36 GMT  
		Size: 673.9 KB (673894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314a9e5a82a9d525a03de942de73e9d9e272afbd3b91d272de75513e697db432`  
		Last Modified: Sun, 21 Dec 2025 16:52:36 GMT  
		Size: 15.3 KB (15283 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:c74abbbd3a65c3ae2a8f21044b5582d4f9b0840b0bfaef6971efe20584cf4fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72825166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37539cb026be5c4a9cf7dae77f65c69826b8b1b5a3d90fe72d9a40fd9ffa5a77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 03:32:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 18 Dec 2025 03:32:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 18 Dec 2025 03:32:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 18 Dec 2025 03:32:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 18 Dec 2025 03:32:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 03:32:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 18 Dec 2025 03:32:56 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 18 Dec 2025 03:32:56 GMT
ENV RABBITMQ_VERSION=4.2.2
# Thu, 18 Dec 2025 03:32:56 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 18 Dec 2025 03:32:56 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 18 Dec 2025 03:32:56 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 03:33:08 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 18 Dec 2025 03:33:10 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 18 Dec 2025 03:33:11 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 18 Dec 2025 03:33:11 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 18 Dec 2025 03:33:11 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 18 Dec 2025 03:33:11 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 03:33:11 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 18 Dec 2025 03:33:12 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 18 Dec 2025 03:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 03:33:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 03:33:12 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 18 Dec 2025 03:33:12 GMT
CMD ["rabbitmq-server"]
# Thu, 18 Dec 2025 04:21:06 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 18 Dec 2025 04:21:06 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.20.0/rabbitmqadmin-2.20.0-x86_64-unknown-linux-musl'; digest='017747084312a47c38eca52942e6f0dd06f5ab845ac0ce7e744d63de253cd0d6' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.20.0/rabbitmqadmin-2.20.0-aarch64-unknown-linux-musl'; digest='13a9f4f0457c95dbe5739a357663b18bda927b277ebdefe5038f0f9bf2b96570' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 18 Dec 2025 04:21:06 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a72ff26a23138cdaa4f0b41bfcc481ade8371719248390c6248e8905289430`  
		Last Modified: Thu, 18 Dec 2025 03:34:02 GMT  
		Size: 33.9 MB (33919488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6924ad8e1ba6e5410a42efe9dcbd3e0096a66790e6ed5f07f6fa89eaf614fd7`  
		Last Modified: Thu, 18 Dec 2025 03:33:58 GMT  
		Size: 8.3 MB (8346912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1210409b7173afd98d184cffda99ceccc0296adf807df7bb7c8066d248a9c0e7`  
		Last Modified: Thu, 18 Dec 2025 03:33:57 GMT  
		Size: 1.5 MB (1515870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28b7694c2744883772a3890c3575001f5611696802768e05cfb8d49a9e8fea6`  
		Last Modified: Thu, 18 Dec 2025 03:34:03 GMT  
		Size: 25.3 MB (25316530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e85f9fe9f47150ba82dba7045fa6911a4f7538e86b809a35497b355185be12`  
		Last Modified: Thu, 18 Dec 2025 03:33:57 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f015b147f83e728ec54cd4540a2dcf3fbbbab8fa86b0d0516bd94b4dd12bdf`  
		Last Modified: Thu, 18 Dec 2025 03:33:57 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4ddabe31ac81772444329627370f3ce7ddeed23b5631f5aef849cdc87a3243`  
		Last Modified: Thu, 18 Dec 2025 03:33:57 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebdd174221fc1d59ab886124ea3124536f2a73653533a642d735e1f76ec9fec`  
		Last Modified: Thu, 18 Dec 2025 03:33:57 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd8b51c110fefa7376720ac0a94307a618ec3df6696d4a0985865e79a1f2d76`  
		Last Modified: Thu, 18 Dec 2025 04:21:18 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0fd19452eef28ffde5c28aaec4ba50f4ecd0e2de6fa55a5eddba982cc88c82bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.1 KB (686125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0235fed5c4e13b724508dedc91cca8e12990dfa0baa9c63154027183b471ec89`

```dockerfile
```

-	Layers:
	-	`sha256:7526c7c77da18a7333f5c8103eacefc8c46a42490fb39a382fc62127f68aab00`  
		Last Modified: Thu, 18 Dec 2025 07:52:38 GMT  
		Size: 670.9 KB (670891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:788140fa2dda83d7af99650b2f8d4265999caf69222b5983a7eff49b03d379a7`  
		Last Modified: Thu, 18 Dec 2025 07:52:39 GMT  
		Size: 15.2 KB (15234 bytes)  
		MIME: application/vnd.in-toto+json
