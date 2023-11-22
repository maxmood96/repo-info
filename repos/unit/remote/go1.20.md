## `unit:go1.20`

```console
$ docker pull unit@sha256:eae66a385d309db6476e1014b8bccbcfb816d18fed9d88a2d812df76c85b0eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `unit:go1.20` - linux; amd64

```console
$ docker pull unit@sha256:0d81a62c4be5ff96852848efe6cb42f49ccda77a3d425b20dc26aa366de329e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.3 MB (319333014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fed1ebc1d2f0de7acfa325032fd074dd7af1f81059e170a90d288f99af3730`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:54:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:54:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 23:53:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 23:53:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 23:53:43 GMT
ENV GOLANG_VERSION=1.20.11
# Tue, 21 Nov 2023 23:53:52 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.11.linux-amd64.tar.gz'; 			sha256='ef79a11aa095a08772d2a69e4f152f897c4e96ee297b0dc20264b7dec2961abe'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.11.linux-armv6l.tar.gz'; 			sha256='636a1b4d75c739f4d6373b36d7d278e25523141d4d69eb1bde5526ed56a49635'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.11.linux-arm64.tar.gz'; 			sha256='7908a49c6ce9d48af9b5ba76ccaa0769da45d8b635259a01065b3739acef4ada'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.11.linux-386.tar.gz'; 			sha256='168b11bbc30f5a18671412fb9535ede76b3d98389be01ba37319635eea76de24'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.11.linux-ppc64le.tar.gz'; 			sha256='e04676e1aeafe7c415176f330322d43a4be5ea6deb14aca49905bd1449dc7072'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.11.linux-s390x.tar.gz'; 			sha256='6112113758b7994249db5d33c34723cd2b2f96d0d80ece07c0e59a91e45912db'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.11.src.tar.gz'; 		sha256='d355c5ae3a8f7763c9ec9dc25153aae373958cbcb60dd09e91a8b56c7621b2fc'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 21 Nov 2023 23:53:53 GMT
ENV GOPATH=/go
# Tue, 21 Nov 2023 23:53:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 23:53:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 21 Nov 2023 23:53:54 GMT
WORKDIR /go
# Wed, 22 Nov 2023 05:07:18 GMT
LABEL org.opencontainers.image.title=Unit (go1.20)
# Wed, 22 Nov 2023 05:07:18 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Wed, 22 Nov 2023 05:07:18 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Wed, 22 Nov 2023 05:07:18 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Wed, 22 Nov 2023 05:07:18 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Wed, 22 Nov 2023 05:07:18 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 22 Nov 2023 05:07:18 GMT
LABEL org.opencontainers.image.version=1.31.1
# Wed, 22 Nov 2023 05:08:06 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates mercurial build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && hg clone -u 1.31.1-1 https://hg.nginx.org/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stdout /var/log/unit.log
# Wed, 22 Nov 2023 05:08:07 GMT
COPY file:8b65557c2137d1a3946148e09ddd45af0b855e40210dabb5a9bd6c36fac22006 in /usr/local/bin/ 
# Wed, 22 Nov 2023 05:08:07 GMT
COPY multi:44b909b4ee0b15a0820a0f95f866a48ec9fbcb6e3c46d6d937842c09126ebe93 in /usr/share/unit/welcome/ 
# Wed, 22 Nov 2023 05:08:07 GMT
STOPSIGNAL SIGTERM
# Wed, 22 Nov 2023 05:08:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Wed, 22 Nov 2023 05:08:07 GMT
EXPOSE 80
# Wed, 22 Nov 2023 05:08:07 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577ff23cfe55ac8872bc433ce99971a34011e7a15f7c8afa3d6492c78d6d23e5`  
		Last Modified: Tue, 21 Nov 2023 10:02:30 GMT  
		Size: 15.8 MB (15764247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b1e60e9d5a0f16eb1f998245666f7a64a44f8b1f2317bd31e8a658150c23d3`  
		Last Modified: Tue, 21 Nov 2023 10:02:45 GMT  
		Size: 54.6 MB (54595728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714cd879eb99cfb743b3a75412becbafa1675d3fcaab91e6174ae2b7a1ca8677`  
		Last Modified: Tue, 21 Nov 2023 23:54:57 GMT  
		Size: 86.1 MB (86085928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09597daca66436345239f9cdf2103dac242c4c7309a99178609ae6e24326429`  
		Last Modified: Tue, 21 Nov 2023 23:55:44 GMT  
		Size: 100.4 MB (100434776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d04a1b63013e9f48faf7e68ce7030423f01f61b84104996fde413778dad3bcf`  
		Last Modified: Tue, 21 Nov 2023 23:55:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3363852310af5d817e3f569806b65073aa8114b7c9f13676a241c4de81c3006d`  
		Last Modified: Wed, 22 Nov 2023 05:14:23 GMT  
		Size: 7.4 MB (7391523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b3f9e52d93652c987357ccee74f99ce07c68aa04e11d7d4286f770d7fad06c`  
		Last Modified: Wed, 22 Nov 2023 05:14:21 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb04ecf1ca61c082815a375f34af94f11570197a129299d7b823ffa04643d6a`  
		Last Modified: Wed, 22 Nov 2023 05:14:21 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `unit:go1.20` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:f18bc981ab3f9e13285d07afd82d9f2acb880668be3b4007a55073f500c54295
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308629044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d9ffb9c6441c9521a1e5b312d64efd93507b83828a21298978318d991802d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:59:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 21:43:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 21:43:41 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 21:44:10 GMT
ENV GOLANG_VERSION=1.20.11
# Tue, 21 Nov 2023 21:44:18 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.11.linux-amd64.tar.gz'; 			sha256='ef79a11aa095a08772d2a69e4f152f897c4e96ee297b0dc20264b7dec2961abe'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.11.linux-armv6l.tar.gz'; 			sha256='636a1b4d75c739f4d6373b36d7d278e25523141d4d69eb1bde5526ed56a49635'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.11.linux-arm64.tar.gz'; 			sha256='7908a49c6ce9d48af9b5ba76ccaa0769da45d8b635259a01065b3739acef4ada'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.11.linux-386.tar.gz'; 			sha256='168b11bbc30f5a18671412fb9535ede76b3d98389be01ba37319635eea76de24'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.11.linux-ppc64le.tar.gz'; 			sha256='e04676e1aeafe7c415176f330322d43a4be5ea6deb14aca49905bd1449dc7072'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.11.linux-s390x.tar.gz'; 			sha256='6112113758b7994249db5d33c34723cd2b2f96d0d80ece07c0e59a91e45912db'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.11.src.tar.gz'; 		sha256='d355c5ae3a8f7763c9ec9dc25153aae373958cbcb60dd09e91a8b56c7621b2fc'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 21 Nov 2023 21:44:19 GMT
ENV GOPATH=/go
# Tue, 21 Nov 2023 21:44:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 21:44:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 21 Nov 2023 21:44:20 GMT
WORKDIR /go
# Wed, 22 Nov 2023 04:38:41 GMT
LABEL org.opencontainers.image.title=Unit (go1.20)
# Wed, 22 Nov 2023 04:38:41 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Wed, 22 Nov 2023 04:38:41 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Wed, 22 Nov 2023 04:38:41 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Wed, 22 Nov 2023 04:38:41 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Wed, 22 Nov 2023 04:38:41 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 22 Nov 2023 04:38:41 GMT
LABEL org.opencontainers.image.version=1.31.1
# Wed, 22 Nov 2023 04:39:20 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates mercurial build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && hg clone -u 1.31.1-1 https://hg.nginx.org/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stdout /var/log/unit.log
# Wed, 22 Nov 2023 04:39:20 GMT
COPY file:8b65557c2137d1a3946148e09ddd45af0b855e40210dabb5a9bd6c36fac22006 in /usr/local/bin/ 
# Wed, 22 Nov 2023 04:39:20 GMT
COPY multi:44b909b4ee0b15a0820a0f95f866a48ec9fbcb6e3c46d6d937842c09126ebe93 in /usr/share/unit/welcome/ 
# Wed, 22 Nov 2023 04:39:20 GMT
STOPSIGNAL SIGTERM
# Wed, 22 Nov 2023 04:39:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Wed, 22 Nov 2023 04:39:20 GMT
EXPOSE 80
# Wed, 22 Nov 2023 04:39:20 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e860a4a6ca9e583881322c2e78baef1911e4d61bc607563e8ad9891e2d91f9`  
		Last Modified: Tue, 21 Nov 2023 08:07:01 GMT  
		Size: 15.8 MB (15750113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a9d2006a8ea812285a7be34dfc82465b2a592d6217f4d385d373c298de4642`  
		Last Modified: Tue, 21 Nov 2023 08:07:16 GMT  
		Size: 54.7 MB (54700129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c9170f58813b7ec5830efa8a508543393dbbe58fe8ef1897feaba3c06929a9`  
		Last Modified: Tue, 21 Nov 2023 21:45:17 GMT  
		Size: 81.5 MB (81486798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c29ca2f9a338e55d09a846dbab5a71d4d9a1efd9d3ec3b4bac09c4ec8942ba2`  
		Last Modified: Tue, 21 Nov 2023 21:46:00 GMT  
		Size: 95.7 MB (95734694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadaf750ba30fc72cf37aba9e0f1e2cb5e678496db6465400f424238b73e938f`  
		Last Modified: Tue, 21 Nov 2023 21:45:50 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15da1013b38dfb770636e07fb4f01f3bf363e6d53715990ec4d6575673436ed0`  
		Last Modified: Wed, 22 Nov 2023 04:40:17 GMT  
		Size: 7.2 MB (7246538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6802093556775e31b2c22c100f9fc2c8dff853b8cfbb53d1e0f003d77d1729`  
		Last Modified: Wed, 22 Nov 2023 04:40:16 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e0b5ac814faedbbf1c123aa79dd5beb43155fe3b7853b0173483beef88e13`  
		Last Modified: Wed, 22 Nov 2023 04:40:16 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
