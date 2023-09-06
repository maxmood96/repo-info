## `unit:go1.21`

```console
$ docker pull unit@sha256:33cb01ff89c5bd458df7b8e5f8d36f552c48e45988940697adb43dd30eeecd1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `unit:go1.21` - linux; amd64

```console
$ docker pull unit@sha256:85b56d55eb417ffd9fb7ccb0c1891ad81365f4657ae43b0afed554cdf3101fd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285814131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63bc587ea78fcca4f7e41ca9779ef5497d6f1c8d0b5c3360618490c0ad10f9c3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 06:59:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 06:59:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 00:50:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 00:50:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Sep 2023 18:31:15 GMT
ENV GOLANG_VERSION=1.21.1
# Wed, 06 Sep 2023 18:31:23 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.1.linux-amd64.tar.gz'; 			sha256='b3075ae1ce5dab85f89bc7905d1632de23ca196bd8336afd93fa97434cfa55ae'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.1.linux-arm64.tar.gz'; 			sha256='7da1a3936a928fd0b2602ed4f3ef535b8cd1990f1503b8d3e1acc0fa0759c967'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.1.linux-386.tar.gz'; 			sha256='b93850666cdadbd696a986cf7b03111fe99db8c34a9aaa113d7c96d0081e1901'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.1.linux-mips64le.tar.gz'; 			sha256='3aa007a41f533b50eae2491bbd29926ada09357367a8aa05e7e50ec50c78acf9'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.1.linux-ppc64le.tar.gz'; 			sha256='eddf018206f8a5589bda75252b72716d26611efebabdca5d0083ec15e9e41ab7'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.1.linux-riscv64.tar.gz'; 			sha256='fac64ed26e003f49f1d77f6d2c4cf951422aecbce12232d9ec1bf4585fc44ee1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.1.linux-s390x.tar.gz'; 			sha256='a83b3e8eb4dbf76294e773055eb51397510ff4d612a247bad9903560267bba6d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.1.src.tar.gz'; 		sha256='bfa36bf75e9a1e9cbbdb9abcf9d1707e479bd3a07880a8ae3564caee5711cb99'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 06 Sep 2023 18:31:24 GMT
ENV GOPATH=/go
# Wed, 06 Sep 2023 18:31:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Sep 2023 18:31:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 06 Sep 2023 18:31:25 GMT
WORKDIR /go
# Wed, 06 Sep 2023 18:55:07 GMT
LABEL org.opencontainers.image.title=Unit (go1.21)
# Wed, 06 Sep 2023 18:55:08 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Wed, 06 Sep 2023 18:55:08 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Wed, 06 Sep 2023 18:55:08 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Wed, 06 Sep 2023 18:55:08 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Wed, 06 Sep 2023 18:55:08 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 06 Sep 2023 18:55:08 GMT
LABEL org.opencontainers.image.version=1.31.0
# Wed, 06 Sep 2023 18:55:59 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates mercurial build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && hg clone -u 1.31.0-1 https://hg.nginx.org/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stdout /var/log/unit.log
# Wed, 06 Sep 2023 18:55:59 GMT
COPY file:8b65557c2137d1a3946148e09ddd45af0b855e40210dabb5a9bd6c36fac22006 in /usr/local/bin/ 
# Wed, 06 Sep 2023 18:55:59 GMT
COPY multi:0ef77957b92a7e8997661453cf7256a81db39d0e9f975a137d7e664007d8fcf4 in /usr/share/unit/welcome/ 
# Wed, 06 Sep 2023 18:55:59 GMT
STOPSIGNAL SIGTERM
# Wed, 06 Sep 2023 18:56:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Wed, 06 Sep 2023 18:56:00 GMT
EXPOSE 80
# Wed, 06 Sep 2023 18:56:00 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb4221e2c63c35bb16b63f6d24c104c7ea5d453997636c2244b66884f540537`  
		Last Modified: Wed, 16 Aug 2023 07:13:46 GMT  
		Size: 15.8 MB (15760534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe6e67e69c83952779c1fb8add0b6f81ba6fb03f6290c62225fbdae94c28661`  
		Last Modified: Wed, 16 Aug 2023 07:14:03 GMT  
		Size: 54.6 MB (54584778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4960566fad88b3b3a13610f36e9daf0fb2073f86a8377c10517fbe4bd0742a5`  
		Last Modified: Thu, 17 Aug 2023 00:52:21 GMT  
		Size: 86.0 MB (86031202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b998f18372bda2de2b17cfc0f4c6935e84e44d8f8facefaa699d6098bdba1f`  
		Last Modified: Wed, 06 Sep 2023 18:36:59 GMT  
		Size: 67.0 MB (66989245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef64f5132b197006c43fee798f11def52768169d0cf69c5dd93215e0e1b0baa`  
		Last Modified: Wed, 06 Sep 2023 18:36:48 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d36fc77055e7d94e3ad1e0da2f6414ce69be2404bd8b84ff509b4fd326d493e`  
		Last Modified: Wed, 06 Sep 2023 18:57:49 GMT  
		Size: 7.4 MB (7388859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3194e4f95a32e23e377d9783ee818c9705cc50d3d07f49a58a86308bc023c7d8`  
		Last Modified: Wed, 06 Sep 2023 18:57:48 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f5ad5e3fa51d640cb97a0126e7d09aaf9abc056f19bfe2afe213ad10e3316b`  
		Last Modified: Wed, 06 Sep 2023 18:57:48 GMT  
		Size: 1.5 KB (1467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `unit:go1.21` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:a19de41974ddbfd9321158d3d6d4d27a8ef71a2a3b8007c3853f258881dffdb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276899467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0510ce1f608ba46f010e834ecd2c6abb884ba5d367f46af625c3c72adb38e6db`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 01:23:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 00:00:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 00:00:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Sep 2023 18:31:06 GMT
ENV GOLANG_VERSION=1.21.1
# Wed, 06 Sep 2023 18:31:14 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.1.linux-amd64.tar.gz'; 			sha256='b3075ae1ce5dab85f89bc7905d1632de23ca196bd8336afd93fa97434cfa55ae'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.1.linux-arm64.tar.gz'; 			sha256='7da1a3936a928fd0b2602ed4f3ef535b8cd1990f1503b8d3e1acc0fa0759c967'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.1.linux-386.tar.gz'; 			sha256='b93850666cdadbd696a986cf7b03111fe99db8c34a9aaa113d7c96d0081e1901'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.1.linux-mips64le.tar.gz'; 			sha256='3aa007a41f533b50eae2491bbd29926ada09357367a8aa05e7e50ec50c78acf9'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.1.linux-ppc64le.tar.gz'; 			sha256='eddf018206f8a5589bda75252b72716d26611efebabdca5d0083ec15e9e41ab7'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.1.linux-riscv64.tar.gz'; 			sha256='fac64ed26e003f49f1d77f6d2c4cf951422aecbce12232d9ec1bf4585fc44ee1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.1.linux-s390x.tar.gz'; 			sha256='a83b3e8eb4dbf76294e773055eb51397510ff4d612a247bad9903560267bba6d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.1.src.tar.gz'; 		sha256='bfa36bf75e9a1e9cbbdb9abcf9d1707e479bd3a07880a8ae3564caee5711cb99'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 06 Sep 2023 18:31:15 GMT
ENV GOPATH=/go
# Wed, 06 Sep 2023 18:31:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Sep 2023 18:31:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 06 Sep 2023 18:31:15 GMT
WORKDIR /go
# Wed, 06 Sep 2023 18:54:09 GMT
LABEL org.opencontainers.image.title=Unit (go1.21)
# Wed, 06 Sep 2023 18:54:09 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Wed, 06 Sep 2023 18:54:09 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Wed, 06 Sep 2023 18:54:09 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Wed, 06 Sep 2023 18:54:09 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Wed, 06 Sep 2023 18:54:09 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 06 Sep 2023 18:54:10 GMT
LABEL org.opencontainers.image.version=1.31.0
# Wed, 06 Sep 2023 18:54:49 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates mercurial build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && hg clone -u 1.31.0-1 https://hg.nginx.org/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stdout /var/log/unit.log
# Wed, 06 Sep 2023 18:54:49 GMT
COPY file:8b65557c2137d1a3946148e09ddd45af0b855e40210dabb5a9bd6c36fac22006 in /usr/local/bin/ 
# Wed, 06 Sep 2023 18:54:49 GMT
COPY multi:0ef77957b92a7e8997661453cf7256a81db39d0e9f975a137d7e664007d8fcf4 in /usr/share/unit/welcome/ 
# Wed, 06 Sep 2023 18:54:49 GMT
STOPSIGNAL SIGTERM
# Wed, 06 Sep 2023 18:54:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Wed, 06 Sep 2023 18:54:49 GMT
EXPOSE 80
# Wed, 06 Sep 2023 18:54:49 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abd0588cbb35597a784666f0dc97746829b8b4b730b73e8781fb90678ffef22`  
		Last Modified: Wed, 16 Aug 2023 01:39:26 GMT  
		Size: 15.7 MB (15746520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a8864a846a08e10fbf877e73678d1f0803227b00a1b16d9ba948070c6e58f6`  
		Last Modified: Wed, 16 Aug 2023 01:39:40 GMT  
		Size: 54.7 MB (54676094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3554db3712f687c05665f601b7fbdc22e34adfd69378c3c655439c82370db65c`  
		Last Modified: Thu, 17 Aug 2023 00:01:49 GMT  
		Size: 81.4 MB (81438670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b6caf833252810adcac5a5c4d96d7c5cc687bf36e43d664c608c55634bcc62`  
		Last Modified: Wed, 06 Sep 2023 18:35:46 GMT  
		Size: 64.1 MB (64089237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36962848810295c5233534173b9088b509da58d83ea994eb0fc415957e6e89d3`  
		Last Modified: Wed, 06 Sep 2023 18:35:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44624e1e4a190d3e12326e3319e13176099b7fd22be9e8973a2752ad63493270`  
		Last Modified: Wed, 06 Sep 2023 18:56:25 GMT  
		Size: 7.2 MB (7241282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed9e3502a173f3b1c460bc011bdc4ecab78b87ba8bd8b8dec9c280b7e602156`  
		Last Modified: Wed, 06 Sep 2023 18:56:24 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3aab8b67f5bf89267bca4519d5160e8ae03f9863d7705c0902882e166bd4b2`  
		Last Modified: Wed, 06 Sep 2023 18:56:24 GMT  
		Size: 1.5 KB (1465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
