## `unit:go1.23`

```console
$ docker pull unit@sha256:c517a8f4b9d6a2af25bf25d570a1977750a3f92a1ca09e4e36b65ed530551663
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:go1.23` - linux; amd64

```console
$ docker pull unit@sha256:bd193230987a42e46de3b9ae865ed01b6630a5126ad31ce3d5943d24b15a14cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.7 MB (324749089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63978fdb71f134cfc2543ef0783b28e747c8a038a3c5c4df78161bdb0e2d1cc8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
ENV GOLANG_VERSION=1.23.8
# Mon, 03 Mar 2025 18:37:38 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 18:37:38 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 18:37:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 18:37:38 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
WORKDIR /go
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.title=Unit (go1.23)
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Mon, 28 Apr 2025 22:15:10 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308dc5e793bdeaf7f58d92f66a93b8ca660207ed9d6e632859189d05d6ae5f02`  
		Last Modified: Mon, 28 Apr 2025 23:12:12 GMT  
		Size: 92.3 MB (92349654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eabb1d9476e2a74ca18f982fa2cd1a722047e0ac01f746221f76c65893fe80`  
		Last Modified: Tue, 01 Apr 2025 17:07:22 GMT  
		Size: 74.1 MB (74057106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7c6948724dfc73b5fd1657b7131a4664c411eeac175603d176b39be370d0b0`  
		Last Modified: Mon, 28 Apr 2025 23:12:10 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09e8481c36eacf3626bccaf508d1460a70861484043d5f70d07d3bed1c2d5dd`  
		Last Modified: Tue, 29 Apr 2025 00:23:39 GMT  
		Size: 21.4 MB (21442642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd1223db636a4c4a9d7228bc4dd6b043adf2a8315c23429235e77c727f68bf`  
		Last Modified: Tue, 29 Apr 2025 00:23:39 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb619dbdefafdedb340c279e32c47bf10b6d8b744230b3cc2fdd21134e7012fa`  
		Last Modified: Tue, 29 Apr 2025 00:23:39 GMT  
		Size: 1.5 KB (1459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:go1.23` - unknown; unknown

```console
$ docker pull unit@sha256:439748323535955cd12cc904296102f5fa78a63ecc8be7888cbe9a0666177712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 KB (27787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4e0bac047facf4a87a1911e3e5ad8284619e3d5f8e5667b257004142d35864`

```dockerfile
```

-	Layers:
	-	`sha256:d40831589eaef9b90cc5c1606795f667bd8a9bfca4ada0ccb98d5dc2143d18ba`  
		Last Modified: Tue, 29 Apr 2025 00:23:38 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:go1.23` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:b7bc32dbaefe7054de2f4dd859ad6fdef0fc2b112d2b66521ab05e6a22a0f79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314115898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929de7ff1b9a67b3f460b2001120f6165fad4bcdaebbf3e2879291a766543dc6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
ENV GOLANG_VERSION=1.23.8
# Mon, 03 Mar 2025 18:37:38 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 18:37:38 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 18:37:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 18:37:38 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
WORKDIR /go
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.title=Unit (go1.23)
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9726b91366b288f3bf9f1b85d5cf8b7e50e8f51867ff670418d5b03a1f259c`  
		Last Modified: Tue, 08 Apr 2025 15:59:21 GMT  
		Size: 86.4 MB (86397502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ade281fe97eb70cd41e06b79a8aec5f7db1277a91fb7cdafb8dd984e5d365`  
		Last Modified: Tue, 01 Apr 2025 17:09:49 GMT  
		Size: 70.7 MB (70686122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73bc3ad674689f5ffcdcc1b377b227e13b60e0af7c419256ff1a9793227dbb8`  
		Last Modified: Tue, 08 Apr 2025 16:00:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a948699c063e99b7c11656c21e7a75ba2ded301bcf78e47ca328cb08d0de9b3a`  
		Last Modified: Tue, 08 Apr 2025 21:39:22 GMT  
		Size: 20.8 MB (20801809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30968de1f8b2c913b7b5735d4d7922530bf62574437f23b5ed24c05ad17f91da`  
		Last Modified: Tue, 08 Apr 2025 21:39:21 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3312f9ca463fd00782851439272b13f3a0d1c633bbfd0ab3828735c8abea9e93`  
		Last Modified: Tue, 08 Apr 2025 21:39:21 GMT  
		Size: 1.5 KB (1455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:go1.23` - unknown; unknown

```console
$ docker pull unit@sha256:baf39dece2ab1534d1ff5d4f20c0d8d02981796254ffd2541cb41f28b3a080fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 KB (27868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bf2476b8e2fb354fc2fdf6961602cc9d89358db75378fcea7a11d7dd4fb382`

```dockerfile
```

-	Layers:
	-	`sha256:c26503c9dc52bea2e4d217482c813df9747a90db8d9b0cd078cb5f4b4d8d1a45`  
		Last Modified: Tue, 08 Apr 2025 21:39:21 GMT  
		Size: 27.9 KB (27868 bytes)  
		MIME: application/vnd.in-toto+json
