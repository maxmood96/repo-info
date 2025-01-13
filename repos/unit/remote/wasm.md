## `unit:wasm`

```console
$ docker pull unit@sha256:99e81c3452c71fffcb3666749a6432d2238d58695301aee8b44a29f288023eb3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:wasm` - linux; amd64

```console
$ docker pull unit@sha256:029478735063632fdccffcf97b80ef49ff2cffb264759972fceb7a43dd6c1daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70419645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374ad229ff6f97a8f6d341e6ec25c76e768f6f545f793471d23488f54cda126e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Fri, 10 Jan 2025 21:01:46 GMT
LABEL org.opencontainers.image.title=Unit (wasm)
# Fri, 10 Jan 2025 21:01:46 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Fri, 10 Jan 2025 21:01:46 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Fri, 10 Jan 2025 21:01:46 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Fri, 10 Jan 2025 21:01:46 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Fri, 10 Jan 2025 21:01:46 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 10 Jan 2025 21:01:46 GMT
LABEL org.opencontainers.image.version=1.34.1
# Fri, 10 Jan 2025 21:01:46 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y          ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config libclang-dev cmake     && export RUST_VERSION=1.83.0     && export RUSTUP_HOME=/usr/src/unit/rustup     && export CARGO_HOME=/usr/src/unit/cargo     && export PATH=/usr/src/unit/cargo/bin:$PATH     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in          amd64) rustArch="x86_64-unknown-linux-gnu"; rustupSha256="6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d" ;;          arm64) rustArch="aarch64-unknown-linux-gnu"; rustupSha256="1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2" ;;          *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;        esac     && url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init"     && curl -L -O "$url"     && echo "${rustupSha256} *rustup-init" | sha256sum -c -     && chmod +x rustup-init     && ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch}     && rm rustup-init     && rustup --version     && cargo --version     && rustc --version     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.34.1-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs                 --otel"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && make -C pkg/contrib .wasmtime     && install -pm 755 pkg/contrib/wasmtime/artifacts/lib/libwasmtime.so /usr/lib/$(dpkg-architecture -q DEB_HOST_MULTIARCH)/     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure wasm --include-path=`pwd`/pkg/contrib/wasmtime/artifacts/include --lib-path=/usr/lib/$(dpkg-architecture -q DEB_HOST_MULTIARCH)/ && ./configure wasm-wasi-component     && make -j $NCPU wasm-install wasm-wasi-component-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure wasm --include-path=`pwd`/pkg/contrib/wasmtime/artifacts/include --lib-path=/usr/lib/$(dpkg-architecture -q DEB_HOST_MULTIARCH)/ && ./configure wasm-wasi-component     && make -j $NCPU wasm-install wasm-wasi-component-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Fri, 10 Jan 2025 21:01:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Jan 2025 21:01:46 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Fri, 10 Jan 2025 21:01:46 GMT
STOPSIGNAL SIGTERM
# Fri, 10 Jan 2025 21:01:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 10 Jan 2025 21:01:46 GMT
EXPOSE map[80/tcp:{}]
# Fri, 10 Jan 2025 21:01:46 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74570b5a71156111b80633eb169786976ad51f20cb69fac8b441919ac41005d5`  
		Last Modified: Mon, 13 Jan 2025 19:37:48 GMT  
		Size: 42.2 MB (42185347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00efaf7cee0375c030c097ccdea60ba76c447721679eee2b3ff91ce5cc2a93e`  
		Last Modified: Mon, 13 Jan 2025 19:37:46 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e303f428c6470833d80ec0947a0ad637a0bb9a4f059ea6206509b445e25c86`  
		Last Modified: Mon, 13 Jan 2025 19:37:46 GMT  
		Size: 1.5 KB (1455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:wasm` - unknown; unknown

```console
$ docker pull unit@sha256:0012c5bfa700188612f2b84eb7932af0d4dbfefd59597abc380fa60cec6db2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e454c04c51f59aa34900d39e6493929d790779ee8bb0855b10117bd69b68b5cd`

```dockerfile
```

-	Layers:
	-	`sha256:a1ef91cbca73a3fab1e9a431f18cfb1b402c8e0456bf16feeae5db4d71f3815e`  
		Last Modified: Mon, 13 Jan 2025 19:37:46 GMT  
		Size: 25.0 KB (25043 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:wasm` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:af2845f2b7b5263027306fa0b001d3084817307e66ce94ecfa5c07fb5d204eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68684814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28dc67e50bb29ffe7ee3cc0f05c0c2a8a2b4417e5c4ca2ac9bb3f41aca00c75f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Thu, 19 Dec 2024 18:23:57 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.title=Unit (wasm)
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.version=1.34.0
# Thu, 19 Dec 2024 18:23:57 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y          ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config libclang-dev cmake     && export RUST_VERSION=1.83.0     && export RUSTUP_HOME=/usr/src/unit/rustup     && export CARGO_HOME=/usr/src/unit/cargo     && export PATH=/usr/src/unit/cargo/bin:$PATH     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in          amd64) rustArch="x86_64-unknown-linux-gnu"; rustupSha256="6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d" ;;          arm64) rustArch="aarch64-unknown-linux-gnu"; rustupSha256="1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2" ;;          *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;        esac     && url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init"     && curl -L -O "$url"     && echo "${rustupSha256} *rustup-init" | sha256sum -c -     && chmod +x rustup-init     && ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch}     && rm rustup-init     && rustup --version     && cargo --version     && rustc --version     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.34.0-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs                 --otel"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && make -C pkg/contrib .wasmtime     && install -pm 755 pkg/contrib/wasmtime/artifacts/lib/libwasmtime.so /usr/lib/$(dpkg-architecture -q DEB_HOST_MULTIARCH)/     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure wasm --include-path=`pwd`/pkg/contrib/wasmtime/artifacts/include --lib-path=/usr/lib/$(dpkg-architecture -q DEB_HOST_MULTIARCH)/ && ./configure wasm-wasi-component     && make -j $NCPU wasm-install wasm-wasi-component-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure wasm --include-path=`pwd`/pkg/contrib/wasmtime/artifacts/include --lib-path=/usr/lib/$(dpkg-architecture -q DEB_HOST_MULTIARCH)/ && ./configure wasm-wasi-component     && make -j $NCPU wasm-install wasm-wasi-component-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
STOPSIGNAL SIGTERM
# Thu, 19 Dec 2024 18:23:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 19 Dec 2024 18:23:57 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:23:57 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4d9d8f5d8ea223fd8250c7c99f51e25828fff207f633b4175d99544d357c03`  
		Last Modified: Sat, 11 Jan 2025 02:49:00 GMT  
		Size: 40.6 MB (40623374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94eed22e0ace04ac77721209c0444790ff3fc59fff7e0a47e8d5bb82d138dd81`  
		Last Modified: Sat, 11 Jan 2025 02:48:58 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed0be957b8aa43e4090f06f63aa2ba623c31d57ba9ad185cc265acbca6dec64`  
		Last Modified: Sat, 11 Jan 2025 02:48:59 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:wasm` - unknown; unknown

```console
$ docker pull unit@sha256:c533809146c689338eadacd8f1295454cdb1a87235ed8add930ca75a525b6eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58928c1d4f15a5acd464562d9cdcd6cfb89bcf9c0db5a4f23244805126d4067f`

```dockerfile
```

-	Layers:
	-	`sha256:6dc0e226fd6ce049f08b559d87a8c60dc43557bafae60dc963d8a464a9383d11`  
		Last Modified: Sat, 11 Jan 2025 02:48:59 GMT  
		Size: 25.1 KB (25123 bytes)  
		MIME: application/vnd.in-toto+json
