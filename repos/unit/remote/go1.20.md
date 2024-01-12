## `unit:go1.20`

```console
$ docker pull unit@sha256:90be4e1ee30e23d71b1cf79e78360ec5558f8e49c56654bc047028aff51107c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:go1.20` - linux; amd64

```console
$ docker pull unit@sha256:7aea5fbd866277faf4d3749b6147a8fa2ef065ba1ea6dfa1a5e0a16aa23e9117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.2 MB (319219395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb324557afd591d5585264cd20c16bf8ef9e2d2087048dc4b790ed89e3783fd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Thu, 19 Oct 2023 10:47:22 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 19 Oct 2023 10:47:22 GMT
CMD ["bash"]
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Oct 2023 10:47:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Oct 2023 10:47:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Oct 2023 10:47:22 GMT
ENV GOLANG_VERSION=1.20.13
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.13.linux-amd64.tar.gz'; 			sha256='9a9d3dcae2b6a638b1f2e9bd4db08ffb39c10e55d9696914002742d90f0047b5'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.13.linux-armv6l.tar.gz'; 			sha256='d4c6c671423ce6eef3f240bf014115b2673ad6a89e12429b5a331b95952c7279'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.13.linux-arm64.tar.gz'; 			sha256='a2d811cef3c4fc77c01195622e637af0c2cf8b3814a95a0920cf2f83b6061d38'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.13.linux-386.tar.gz'; 			sha256='4da6f08510a21b829a065d3f99914bfbe1d8b212664cea230485a64e7e6d00d8'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.13.linux-ppc64le.tar.gz'; 			sha256='5f632b83323e16f8c6ceb676cd570b3f13f1826e06a81d92985d1301b643a7d3'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.13.linux-s390x.tar.gz'; 			sha256='ae6c8f75df9b15c92374cfeae86e97d2744d4d4cdafcb999fea5b63e20c22651'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.13.src.tar.gz'; 		sha256='0fe745c530f2f1d67193af3c5ea25246be077989ec5178df266e975f3532449e'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Thu, 19 Oct 2023 10:47:22 GMT
ENV GOPATH=/go
# Thu, 19 Oct 2023 10:47:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Oct 2023 10:47:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 19 Oct 2023 10:47:22 GMT
WORKDIR /go
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.title=Unit (go1.20)
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.version=1.31.1
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates mercurial build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && hg clone -u 1.31.1-1 https://hg.nginx.org/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stdout /var/log/unit.log # buildkit
# Thu, 19 Oct 2023 10:47:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Oct 2023 10:47:22 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Thu, 19 Oct 2023 10:47:22 GMT
STOPSIGNAL SIGTERM
# Thu, 19 Oct 2023 10:47:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 19 Oct 2023 10:47:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Oct 2023 10:47:22 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c23b7d6528239a16f11d6e650e9a9fdb7039721df42b6ca01777fe34c2b116`  
		Last Modified: Thu, 11 Jan 2024 04:45:57 GMT  
		Size: 54.6 MB (54601205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de87067350268be51f2c816aad697b479a7e9d2499dedbfaa1c8ed04fa48a774`  
		Last Modified: Thu, 11 Jan 2024 15:31:22 GMT  
		Size: 86.1 MB (86106422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25820bd180daa00295e895b01d2cf3fe093295b81f650ee59556ea62492215d2`  
		Last Modified: Thu, 11 Jan 2024 15:32:58 GMT  
		Size: 100.5 MB (100518985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acefcfe285eda5e3817fb60b3814e479da6da79f3d9150e83e5d697ad85f00c4`  
		Last Modified: Thu, 11 Jan 2024 15:32:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82516ba7ed4a0432aed212a66057c87e7a6d3735b3a2602b01fc6053712e8593`  
		Last Modified: Fri, 12 Jan 2024 00:25:46 GMT  
		Size: 7.2 MB (7167069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97d5f592753af1cf88339189a20d0601c583b687a899c8bf3bc8c95adc935be`  
		Last Modified: Fri, 12 Jan 2024 00:25:46 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb04d774630bedcaca713227afdd069998dcb4b99c0a337d63b70c998f68cbf`  
		Last Modified: Fri, 12 Jan 2024 00:25:47 GMT  
		Size: 1.5 KB (1453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:go1.20` - unknown; unknown

```console
$ docker pull unit@sha256:22a84b5327c6c3f4acf671a7bd32b15d9ceb76b98dced683d891610ab93f719f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8809773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f366b02ca81149f9c2b4672fba0888d0f34881dedb9f71b09dfc4ead636c65`

```dockerfile
```

-	Layers:
	-	`sha256:d51540cfa2343bfb379d633804393a869b184688d789779ec53e5b9e9b432077`  
		Last Modified: Fri, 12 Jan 2024 00:25:46 GMT  
		Size: 8.8 MB (8785168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc45001943a70aea025ff0a59a5f7d6ef4be2459ed25b45c7deb7984ea90e4be`  
		Last Modified: Fri, 12 Jan 2024 00:25:46 GMT  
		Size: 24.6 KB (24605 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:go1.20` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:b23ff072d07bffe5cb3f7bf3eb8a7a6032e8e876f1ff995b89d8877bb19813b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.0 MB (309028596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78497b6a624a0fd1fa0ba80bd543fe7b9bb1e6c4d84cc34242eee8d1308c334d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Thu, 19 Oct 2023 10:47:22 GMT
ADD file:06ba7e39a2f8e1a7bcbb929fa9d1e6fb1f8bdcf5096dc903576af8f7014e353b in / 
# Thu, 19 Oct 2023 10:47:22 GMT
CMD ["bash"]
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Oct 2023 10:47:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Oct 2023 10:47:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Oct 2023 10:47:22 GMT
ENV GOLANG_VERSION=1.20.13
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.13.linux-amd64.tar.gz'; 			sha256='9a9d3dcae2b6a638b1f2e9bd4db08ffb39c10e55d9696914002742d90f0047b5'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.13.linux-armv6l.tar.gz'; 			sha256='d4c6c671423ce6eef3f240bf014115b2673ad6a89e12429b5a331b95952c7279'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.13.linux-arm64.tar.gz'; 			sha256='a2d811cef3c4fc77c01195622e637af0c2cf8b3814a95a0920cf2f83b6061d38'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.13.linux-386.tar.gz'; 			sha256='4da6f08510a21b829a065d3f99914bfbe1d8b212664cea230485a64e7e6d00d8'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.13.linux-ppc64le.tar.gz'; 			sha256='5f632b83323e16f8c6ceb676cd570b3f13f1826e06a81d92985d1301b643a7d3'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.13.linux-s390x.tar.gz'; 			sha256='ae6c8f75df9b15c92374cfeae86e97d2744d4d4cdafcb999fea5b63e20c22651'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.13.src.tar.gz'; 		sha256='0fe745c530f2f1d67193af3c5ea25246be077989ec5178df266e975f3532449e'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Thu, 19 Oct 2023 10:47:22 GMT
ENV GOPATH=/go
# Thu, 19 Oct 2023 10:47:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Oct 2023 10:47:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 19 Oct 2023 10:47:22 GMT
WORKDIR /go
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.title=Unit (go1.20)
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.version=1.31.1
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates mercurial build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && hg clone -u 1.31.1-1 https://hg.nginx.org/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stdout /var/log/unit.log # buildkit
# Thu, 19 Oct 2023 10:47:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Oct 2023 10:47:22 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Thu, 19 Oct 2023 10:47:22 GMT
STOPSIGNAL SIGTERM
# Thu, 19 Oct 2023 10:47:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 19 Oct 2023 10:47:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Oct 2023 10:47:22 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:396a672fee8bade1a7c9f228d919717447f110f39046d8b5ed21ad45ae13ab61`  
		Last Modified: Tue, 19 Dec 2023 01:44:57 GMT  
		Size: 53.7 MB (53708091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010797996cc86cf2cf7495aebc22e5be7d18a10bde1e11562dbe5283c226c0e9`  
		Last Modified: Tue, 19 Dec 2023 11:43:17 GMT  
		Size: 15.8 MB (15750308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70092c2a6b382a0cc0bd2adeb187b94d74c8bcf2ceb6f33bb8e4e4e9c6561141`  
		Last Modified: Tue, 19 Dec 2023 11:43:31 GMT  
		Size: 54.7 MB (54699871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aea5ee0f94d038f071199297175350bfa92e575e220b1f772fbf67b942202c9`  
		Last Modified: Tue, 19 Dec 2023 20:03:39 GMT  
		Size: 81.5 MB (81486689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c025792a1f0a68df403143fe73b3f27ecea1763433846b0f8ee1c2103ee1b13`  
		Last Modified: Tue, 09 Jan 2024 22:45:57 GMT  
		Size: 95.8 MB (95818978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61089c5c8cc433a24c19973bd3195fb702f129eecb385501a7b510858f6fa6d`  
		Last Modified: Tue, 09 Jan 2024 22:45:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e36e6ea23e8904e58cf17ae01d8d19c9d2490b66a10c8c0f0ce82506cc087e`  
		Last Modified: Wed, 10 Jan 2024 01:04:47 GMT  
		Size: 7.6 MB (7561772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c60d4f361ce1926a1084d80110f9c3aab6502b9b761fc05a8160771bb62d973`  
		Last Modified: Wed, 10 Jan 2024 01:04:46 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f19ba41ffb0022bfb57ee7421c0ea23c7b99377415105227eb4237186828c7c`  
		Last Modified: Wed, 10 Jan 2024 01:04:47 GMT  
		Size: 1.5 KB (1457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:go1.20` - unknown; unknown

```console
$ docker pull unit@sha256:b0e52e3e2a94e5face87aa82e687fe75e2a0b3e22b3d8ed8aeee28ae1f6f4eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8813131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40828b070fda1dec8e75ff3e4dece1da09f188b0701470a2c5963cf8a7792ec1`

```dockerfile
```

-	Layers:
	-	`sha256:ed2f312148faa2d87a5bb617eea5aa3bbee8ddce602669cfc8242dfc8c36487c`  
		Last Modified: Wed, 10 Jan 2024 01:04:46 GMT  
		Size: 8.8 MB (8788525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a81cdbbc7090bd311f19c653d4d482022806d082ef113cc8d3db27dcd708b95c`  
		Last Modified: Wed, 10 Jan 2024 01:04:45 GMT  
		Size: 24.6 KB (24606 bytes)  
		MIME: application/vnd.in-toto+json
