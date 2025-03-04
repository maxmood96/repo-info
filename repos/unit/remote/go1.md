## `unit:go1`

```console
$ docker pull unit@sha256:07465be56ec324b38882cd474c469ae10fa90f477fb164cdbc76d280b00c31c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:go1` - linux; amd64

```console
$ docker pull unit@sha256:1ba7eaf299e1e17464d7c25872532bf13a011344183a2a9e15f71086f4a6a23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.5 MB (329511798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7413388de7d730cdf60fa269d58801aa88f3c35ae9b449dbdb86c143031cf062`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.title=Unit (go1.24)
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.version=1.34.2
# Mon, 03 Mar 2025 18:37:38 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y          ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config libclang-dev cmake     && export RUST_VERSION=1.83.0     && export RUSTUP_HOME=/usr/src/unit/rustup     && export CARGO_HOME=/usr/src/unit/cargo     && export PATH=/usr/src/unit/cargo/bin:$PATH     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in          amd64) rustArch="x86_64-unknown-linux-gnu"; rustupSha256="6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d" ;;          arm64) rustArch="aarch64-unknown-linux-gnu"; rustupSha256="1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2" ;;          *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;        esac     && url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init"     && curl -L -O "$url"     && echo "${rustupSha256} *rustup-init" | sha256sum -c -     && chmod +x rustup-init     && ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch}     && rm rustup-init     && rustup --version     && cargo --version     && rustc --version     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.34.2-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs                 --otel"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
STOPSIGNAL SIGTERM
# Mon, 03 Mar 2025 18:37:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:37:38 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Mar 2025 18:37:38 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9760da4e8f07741fae4c26020e61eb395607959e93d79f06d31fc27130f7f938`  
		Last Modified: Tue, 25 Feb 2025 04:17:30 GMT  
		Size: 92.3 MB (92331986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a60326dddc23e8774b39171d6496c16678bd44e52909e9a94763d62f3cbf89`  
		Last Modified: Wed, 12 Feb 2025 10:27:40 GMT  
		Size: 78.8 MB (78805485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8985a99e1ce35674006027d832983346299ede6596587b3c974723c0345c8b81`  
		Last Modified: Tue, 25 Feb 2025 04:17:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cce7e0cc9d86194cf5f2b5c6919f82d9b150615d0c2222fb59a5feb2b2ba02d`  
		Last Modified: Mon, 03 Mar 2025 21:18:23 GMT  
		Size: 21.4 MB (21442602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b348b74dc1c83acec637314d1dc5606e0a9f4a92df36e6d47ebfd7d640c4af9`  
		Last Modified: Mon, 03 Mar 2025 21:18:22 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aebfe515bb11074604470815a0f408ee0063cf02c47387668406c4a04f86eb`  
		Last Modified: Mon, 03 Mar 2025 21:18:22 GMT  
		Size: 1.5 KB (1458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:go1` - unknown; unknown

```console
$ docker pull unit@sha256:41dc581976a52544792f6b9a9e8fa71eb3f5e2c94a0933be97fe51233c8fff6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 KB (28360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ed0b3727ab2c9db982b8b61d06e385121f64234993a66e221a9570a5bce650`

```dockerfile
```

-	Layers:
	-	`sha256:38b9bb28e582a137f1a61347570aff356c1e3b02fc526e73460aba560230f8e4`  
		Last Modified: Mon, 03 Mar 2025 21:18:22 GMT  
		Size: 28.4 KB (28360 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:go1` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:547967a4451e5f009df1e6860cf7246ceab83352bee5d03f2cbdabd86c6e3b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.5 MB (318509036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f6cbfd51f557b9330eab9fa7722b434aac6f5ddc8c83cac2b8dbd3c21b7410`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.title=Unit (go1.24)
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.version=1.34.2
# Mon, 03 Mar 2025 18:37:38 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y          ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config libclang-dev cmake     && export RUST_VERSION=1.83.0     && export RUSTUP_HOME=/usr/src/unit/rustup     && export CARGO_HOME=/usr/src/unit/cargo     && export PATH=/usr/src/unit/cargo/bin:$PATH     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in          amd64) rustArch="x86_64-unknown-linux-gnu"; rustupSha256="6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d" ;;          arm64) rustArch="aarch64-unknown-linux-gnu"; rustupSha256="1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2" ;;          *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;        esac     && url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init"     && curl -L -O "$url"     && echo "${rustupSha256} *rustup-init" | sha256sum -c -     && chmod +x rustup-init     && ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch}     && rm rustup-init     && rustup --version     && cargo --version     && rustc --version     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.34.2-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs                 --otel"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
STOPSIGNAL SIGTERM
# Mon, 03 Mar 2025 18:37:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:37:38 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Mar 2025 18:37:38 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9b8f871d0f3123ba15451c10996dab2d9e3570418f2ca8959fe0f2505e3356`  
		Last Modified: Tue, 25 Feb 2025 15:28:23 GMT  
		Size: 86.4 MB (86383529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18364ce0d2587c74fc30d8602f743c52178d9e6408c64d9091baffbff467af7`  
		Last Modified: Wed, 12 Feb 2025 09:53:13 GMT  
		Size: 75.1 MB (75060222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349146bc915ab644c1732fc873caaf444abef0ba611d35a0d9d3502f076b3094`  
		Last Modified: Tue, 25 Feb 2025 15:28:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4145cd549a6ec5c962b09cfef8f5c106b467fd8369498462bd327a3f54799cf1`  
		Last Modified: Mon, 03 Mar 2025 22:13:00 GMT  
		Size: 20.8 MB (20801741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad33f0cec615f99934ac5679c1f44af4016b0b96bfadac3c93b5fae4f1f3499`  
		Last Modified: Mon, 03 Mar 2025 22:12:59 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c191e78a3b15201b5bfa840a67b0648082eb448d626fea3382dc05c192870c9`  
		Last Modified: Mon, 03 Mar 2025 22:13:00 GMT  
		Size: 1.5 KB (1458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:go1` - unknown; unknown

```console
$ docker pull unit@sha256:dce61fdd35b7ed30aceac4418db2e7f3c551f8706954c4648098fa2edbc776d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 KB (28466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4011912ea7b7d0225dc8529b681d177b1734da50dd1d61d9868472d675aead4`

```dockerfile
```

-	Layers:
	-	`sha256:a358cab0bf4152a6e2af0521794fd65b23f0a62bea4b3ab47ac5ace3c8a6dfd3`  
		Last Modified: Mon, 03 Mar 2025 22:12:59 GMT  
		Size: 28.5 KB (28466 bytes)  
		MIME: application/vnd.in-toto+json
