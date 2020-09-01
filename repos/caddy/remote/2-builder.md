## `caddy:2-builder`

```console
$ docker pull caddy@sha256:92dd94b7abd9868931372f49d1c34ee40a61ab4ec12a828ad42ef1c17675b9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:530d664fc93dca48b1c5aac4041ab8f94db2300c7e301b721578d3aadc9f60d5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305982305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f89e49117b8f842b47277b8ce37f02851dfeb18da89c241f25afe1322ccc517`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:30:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:40:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 19:34:35 GMT
ENV GOLANG_VERSION=1.14.8
# Tue, 01 Sep 2020 19:36:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 19:36:50 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 19:36:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 19:36:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 19:36:51 GMT
WORKDIR /go
# Tue, 01 Sep 2020 19:46:18 GMT
WORKDIR /src
# Tue, 01 Sep 2020 19:46:19 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 01 Sep 2020 19:46:19 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 01 Sep 2020 19:46:21 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 01 Sep 2020 19:46:21 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 01 Sep 2020 19:46:40 GMT
RUN go get -d ./...
# Tue, 01 Sep 2020 19:46:43 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 01 Sep 2020 19:46:43 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8968b2872e472e21554ca58b35a02277634f3e501cc04ab7b0d0963f60f54d`  
		Last Modified: Tue, 02 Jun 2020 01:44:13 GMT  
		Size: 282.6 KB (282603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92cc7c5fd73817407fa0e4de5e1fb262a9c0f34c35c7450a2d01a7cef79c62f`  
		Last Modified: Tue, 02 Jun 2020 01:44:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd28c722f6f6bff33648d1a69362ea09192e6c5b41c0604848f7ea8490ff4db9`  
		Last Modified: Tue, 01 Sep 2020 19:43:02 GMT  
		Size: 107.3 MB (107338308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f4f084ab04cf5f263eaadf7ae8add978a542c095db636287348ff0011b060a`  
		Last Modified: Tue, 01 Sep 2020 19:42:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ebda6c2bf751925c9d28dd3ddf434711b59757ff414e94bc7e95b084490fb3`  
		Last Modified: Tue, 01 Sep 2020 19:46:54 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22004df01bcc06db36622c0faa009585dbdf7419984692ef289bfb30e2df7001`  
		Last Modified: Tue, 01 Sep 2020 19:46:55 GMT  
		Size: 8.3 MB (8310031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95063ecc956a4900df7dbd46015c622c95845c3c82efc7994e13fc83ba0d4d8`  
		Last Modified: Tue, 01 Sep 2020 19:46:54 GMT  
		Size: 3.0 MB (3021529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a5064d0396a56f11b584ef9473239e91b053dc33705d4cb75dc90a4e5db2a7`  
		Last Modified: Tue, 01 Sep 2020 19:47:22 GMT  
		Size: 184.2 MB (184231261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac18da66ebccce66529a8a5c82b6f2f5d98e0284937b2c8b43c204fdd1f09fa5`  
		Last Modified: Tue, 01 Sep 2020 19:46:53 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a6bc59dd3c10a42c3519d7aa483f03e42c0db5ac5e8ccf1c0862cc6e365be1`  
		Last Modified: Tue, 01 Sep 2020 19:46:54 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:982248ee8c889b1765b1481b67ed5d16180a4ff6e82616d8dc82d56484a99742
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301748871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eaed8f6193bdd4f5d28ddfbac079c84ae0260c92d2d9dd4016e87240089423d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 02:02:10 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 02:02:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:51:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Aug 2020 23:55:22 GMT
ENV GOLANG_VERSION=1.14.7
# Tue, 01 Sep 2020 00:03:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.7.src.tar.gz'; 	sha256='064392433563660c73186991c0a315787688e7c38a561e26647686f89b6c30e3'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 00:03:34 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 00:03:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 00:03:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 00:03:40 GMT
WORKDIR /go
# Tue, 01 Sep 2020 05:03:15 GMT
WORKDIR /src
# Tue, 01 Sep 2020 05:03:46 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 01 Sep 2020 05:03:57 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 01 Sep 2020 05:04:40 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 01 Sep 2020 05:04:51 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 01 Sep 2020 05:06:45 GMT
RUN go get -d ./...
# Tue, 01 Sep 2020 05:07:00 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 01 Sep 2020 05:07:07 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c276dc457bae632c9eadd1ac69c1a756a9a67e050b0350a475b19663722191cf`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 282.8 KB (282778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f0819b703e39c232c6d0a8ac0f76d8f3c6856629db16fd6dd7b7ae69368281`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80d870b4111d9793e4a962df54668501236ab71f0b3bd501fe19d8832d95bd2`  
		Last Modified: Tue, 01 Sep 2020 00:33:29 GMT  
		Size: 103.7 MB (103670838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccbe42781b1579f43c5f88783be744d20f9df48567471002d50d7fbbe9a84f2`  
		Last Modified: Tue, 01 Sep 2020 00:32:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd0245d0ee5de14ac31465b43d4761e2c6b5f6554ac131d5c69e9a62b8b7943`  
		Last Modified: Tue, 01 Sep 2020 05:07:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601c9ca872243ac437ea220397f5ade201b20e5178214c4e59bbe24a645c02f2`  
		Last Modified: Tue, 01 Sep 2020 05:07:39 GMT  
		Size: 7.9 MB (7928853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6138db20f867446ba731c89d1a122c6ea3ccf094213787d187d7cbaccb0c7d8`  
		Last Modified: Tue, 01 Sep 2020 05:07:36 GMT  
		Size: 3.0 MB (3023127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f77e821260917b4fa3691d6e4cfda019adea678ca24d055ad067fdc8d95010`  
		Last Modified: Tue, 01 Sep 2020 05:08:25 GMT  
		Size: 184.2 MB (184238858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b673d07c9cd6d327d5134faf2f3b468b126165d6ff3611f980a2149d9b616daf`  
		Last Modified: Tue, 01 Sep 2020 05:07:36 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365b66f8f62ca9ea0f3ec85970e8c4e9c8191604779bbb51b338e322ad549f5a`  
		Last Modified: Tue, 01 Sep 2020 05:07:38 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:01fa1857b3cf6d870b3f80925838fc70f395e3f94905ecb4c4104ef9c51f331d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325308985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ece7e8752b036774e20a6feed00e4ff41063a283273fc0760aead8f655d060`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:10:58 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:11:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 Aug 2020 01:20:45 GMT
ENV GOLANG_VERSION=1.14.7
# Fri, 07 Aug 2020 02:19:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '064392433563660c73186991c0a315787688e7c38a561e26647686f89b6c30e3 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 07 Aug 2020 02:19:26 GMT
ENV GOPATH=/go
# Fri, 07 Aug 2020 02:19:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Aug 2020 02:19:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 07 Aug 2020 02:19:48 GMT
WORKDIR /go
# Fri, 07 Aug 2020 08:25:17 GMT
WORKDIR /src
# Fri, 07 Aug 2020 08:25:19 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 Aug 2020 08:25:20 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Fri, 07 Aug 2020 08:25:23 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 07 Aug 2020 08:25:24 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 07 Aug 2020 08:26:43 GMT
RUN go get -d ./...
# Fri, 07 Aug 2020 08:26:50 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Fri, 07 Aug 2020 08:26:51 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512c25ce227edddad11326504a9bab47e83f8b61c090c9dc95882452984ac62`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 281.9 KB (281892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87928ee7e6c788309b46621e351321410e4dde5374869ffa75f404b19e0e0c12`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da757ec41ca8393023f8db623f117071cb05c07ebf47da0f293c91deca9ebb20`  
		Last Modified: Fri, 07 Aug 2020 05:02:34 GMT  
		Size: 128.2 MB (128213206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692751ab01ad41ed9df38cab0ec15fb400ac55ccebbbac4348dde69682731043`  
		Last Modified: Fri, 07 Aug 2020 05:01:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43c975007342c2ccf0fd2ec1231bbcf2febae5b46c5a18d3261d8066877bdd8`  
		Last Modified: Fri, 07 Aug 2020 08:27:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e900c935258ea5860f9187b513d6fecd815740acc9e33528a9faf0be361d462a`  
		Last Modified: Fri, 07 Aug 2020 08:27:13 GMT  
		Size: 7.1 MB (7144924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8990e9c17542b59ea63a50f939defa16c902442ca269c398725eee23674c1e2a`  
		Last Modified: Fri, 07 Aug 2020 08:27:12 GMT  
		Size: 3.0 MB (3019055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfa76292e48dfea062acf29eee1e371d5d21420ea90a3c7ffffd631e9c9ff18`  
		Last Modified: Fri, 07 Aug 2020 08:28:04 GMT  
		Size: 184.2 MB (184242015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38253d5b437341664ed152f62f4f0ce8ce5ecdea13fbfda26444b1c0e9ed5dab`  
		Last Modified: Fri, 07 Aug 2020 08:27:11 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97293801893b82e8a489a88fef714238eb6fb8b1f07ced09ed6764b4147dc6c5`  
		Last Modified: Fri, 07 Aug 2020 08:27:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:f95c87ceb7a487082901b030b86bc2cde12305df9371ee9d513ee5a0d97c2c17
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301519691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66144a2d6679705e3131c4080b2478ab3cc8108e5d068ee0f156441496d4947c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:57:21 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:58:08 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:59:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 00:04:51 GMT
ENV GOLANG_VERSION=1.14.7
# Tue, 01 Sep 2020 00:09:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.7.src.tar.gz'; 	sha256='064392433563660c73186991c0a315787688e7c38a561e26647686f89b6c30e3'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 00:09:26 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 00:09:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 00:10:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 00:10:34 GMT
WORKDIR /go
# Tue, 01 Sep 2020 16:08:20 GMT
WORKDIR /src
# Tue, 01 Sep 2020 16:08:24 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 01 Sep 2020 16:08:26 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 01 Sep 2020 16:08:30 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 01 Sep 2020 16:08:31 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 01 Sep 2020 16:09:04 GMT
RUN go get -d ./...
# Tue, 01 Sep 2020 16:09:09 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 01 Sep 2020 16:09:10 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f711af9a0d350d42a1cb00f41feb32277e11189d70d84d76fdef5065f78c47`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 283.0 KB (282997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f96fe45779b3ba9e9daededd02c233c5c76715ef1c5e88dd10c7acbea8414f`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d765263503fbbcb5f71d39603a7e297fe40b9b8840f1ce362f8b4046861d71`  
		Last Modified: Tue, 01 Sep 2020 03:15:08 GMT  
		Size: 102.8 MB (102767175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ff95512c1cbdbf84024c707084b2da2d9ddc6fa44026025845b1e81d726ac`  
		Last Modified: Tue, 01 Sep 2020 03:14:40 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c4b867219366f3968b6c4e7558380da29595358cd3db278903547a3a94490e`  
		Last Modified: Tue, 01 Sep 2020 16:09:27 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae610d9c6eb23bdc78114398a242082a77a43e11c3c63dcf7b4de8e97626741`  
		Last Modified: Tue, 01 Sep 2020 16:09:27 GMT  
		Size: 8.5 MB (8499921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a1b1036b0c8808ea0e2862e39fa1c95488b2c6f0c56b11d0c083b830530ac1`  
		Last Modified: Tue, 01 Sep 2020 16:09:26 GMT  
		Size: 3.0 MB (3021595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2df81b6c0caf7e1fefcacb675ece55ddc91f33fa24f456779facf3a2e6a562b`  
		Last Modified: Tue, 01 Sep 2020 16:10:04 GMT  
		Size: 184.2 MB (184238911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814eca1cdd54f7502082ab66bbda2e99ad2b40c0b66ed1972bcb1340df2ddf22`  
		Last Modified: Tue, 01 Sep 2020 16:09:26 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83792c466877bc0a6112531e58cada4801ccaead78c55b3ac73297649cd9e0f7`  
		Last Modified: Tue, 01 Sep 2020 16:09:25 GMT  
		Size: 181.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:8cc99e78dcf94f41180bcee3a629602cdc4ab5764fb71f4b9bc2593dced020a3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300858463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ddd7cd584c9d73c29834a5834f3cda94fdf171cb43a5fde3851d756506d4eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:29:37 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:29:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 01:38:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 01:44:52 GMT
ENV GOLANG_VERSION=1.14.7
# Tue, 01 Sep 2020 01:48:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.7.src.tar.gz'; 	sha256='064392433563660c73186991c0a315787688e7c38a561e26647686f89b6c30e3'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 01:48:55 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 01:49:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 01:49:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 01:49:21 GMT
WORKDIR /go
# Tue, 01 Sep 2020 15:26:51 GMT
WORKDIR /src
# Tue, 01 Sep 2020 15:27:08 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 01 Sep 2020 15:27:14 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 01 Sep 2020 15:27:33 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 01 Sep 2020 15:27:41 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 01 Sep 2020 15:31:50 GMT
RUN go get -d ./...
# Tue, 01 Sep 2020 15:32:03 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 01 Sep 2020 15:32:10 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d800b4e456ea05213bc7310b5d1b1706274430828a3c19a2fa8c6694733dc4`  
		Last Modified: Tue, 02 Jun 2020 01:48:21 GMT  
		Size: 285.0 KB (285034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a45a7c013c1132848fd122dfb4511c34ed884573ddfd7d8ad13d9a8a6157c42`  
		Last Modified: Tue, 02 Jun 2020 01:48:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2027fdcd64944ab1f220602a99a17cd18eeee2c7d59206cb8e9642bbd8c03671`  
		Last Modified: Tue, 01 Sep 2020 02:06:42 GMT  
		Size: 101.6 MB (101582520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c1d330affaa99a19dfa9f39e7990c38015a7b25b19b7801f3095c1d72bbda0`  
		Last Modified: Tue, 01 Sep 2020 02:06:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc4b5e7c3c17fd7432b129997364692b8801a8b6e3790ffa354df15b81f364c`  
		Last Modified: Tue, 01 Sep 2020 15:32:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0adaab1da2a88cfbe917fb16206624914bd5561195fe6101718adcd3cd60104b`  
		Last Modified: Tue, 01 Sep 2020 15:32:46 GMT  
		Size: 8.9 MB (8920028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b963184b73a8b2131be75452e726ce2324bb6f0d7edee7f7191a36ed77c312c6`  
		Last Modified: Tue, 01 Sep 2020 15:32:43 GMT  
		Size: 3.0 MB (3019833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00be76db07f65ba411b5722878c38815096c8f6aca2d673a1ef03482af378186`  
		Last Modified: Tue, 01 Sep 2020 15:33:13 GMT  
		Size: 184.2 MB (184244720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5f8f4bd426981674da8eb439d57c3bb0217d249583fdbd2edb1a67efa4c15f`  
		Last Modified: Tue, 01 Sep 2020 15:32:40 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169a496335ea4c2fae89a7faec825480336ceef1419477a508827799dd046f0b`  
		Last Modified: Tue, 01 Sep 2020 15:32:41 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:7e4c3f3223de987021dc6c2e2dd0171c828b7aa9bb6293181b8cb697e6dab9fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305648613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dac070d5c68f4c2e6cfcc91d843df4050389c9cebe743104c796ea839cdda3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:53:15 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:53:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:53:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 19:44:01 GMT
ENV GOLANG_VERSION=1.14.8
# Tue, 01 Sep 2020 19:45:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 19:45:35 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 19:45:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 19:45:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 19:45:37 GMT
WORKDIR /go
# Tue, 01 Sep 2020 20:04:54 GMT
WORKDIR /src
# Tue, 01 Sep 2020 20:04:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 01 Sep 2020 20:04:56 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 01 Sep 2020 20:04:57 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 01 Sep 2020 20:04:58 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 01 Sep 2020 20:05:14 GMT
RUN go get -d ./...
# Tue, 01 Sep 2020 20:05:22 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 01 Sep 2020 20:05:23 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2094092570892a8483a3fc940b327cccddf0cb7affb2a628ef4c98e40b4830bd`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 283.1 KB (283144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64a1c2f9ba0751e3e55cf33ddc6f0fd325bce1e6d64ef921f6258c5115b3c0`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e232aad579fb98c2f2045f3f7b7ba0fbffcfc8e29b42d0ba5a359837b0c4e1`  
		Last Modified: Tue, 01 Sep 2020 19:49:06 GMT  
		Size: 107.2 MB (107195429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2165b261634b409611a87b9a553177bf635c26b3a0516de364edac85a8d27b27`  
		Last Modified: Tue, 01 Sep 2020 19:48:53 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1062f7882f263f26082444069fc6189191916dc260cbfc4dbe282b15d49a3fbd`  
		Last Modified: Tue, 01 Sep 2020 20:05:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c18eaf417133e1baa67c0e5e908a0d1cc12dbac23d7d930307c5b9973f3b91`  
		Last Modified: Tue, 01 Sep 2020 20:05:38 GMT  
		Size: 8.4 MB (8352245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e16c5f4c29abf40f9273613ac29277c5ee3401f1e69d6e11393d1c5cde4440e`  
		Last Modified: Tue, 01 Sep 2020 20:05:37 GMT  
		Size: 3.0 MB (3019353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae13017144598018fbf639fd94a2cff812baec7a4a31e5eec23d4b12738fa3cd`  
		Last Modified: Tue, 01 Sep 2020 20:05:53 GMT  
		Size: 184.2 MB (184231123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e262f312527240c7ac156ee2650905668e128bd06e381594ab2f18f66d6000e2`  
		Last Modified: Tue, 01 Sep 2020 20:05:37 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb074fabd331ca17a2cb9e7f77792f2e79671375f012ecee518944363de5157`  
		Last Modified: Tue, 01 Sep 2020 20:05:37 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
