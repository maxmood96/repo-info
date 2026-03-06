## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:fd1e631d06bcf264896debacf16929ff8cd6d5a3502c361ea36fb87ed850299b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:0848a6229c266184878f437e8e9f26289972e0155922d57010733f078e1aca79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79797159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea6bc2cb002fd78b4e5210dc03d1f0b539f3a6ef48388c50c599a018d2e0b34`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:11:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:12:05 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:12:05 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:12:05 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:12:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:12:05 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:12:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:12:07 GMT
WORKDIR /go
# Fri, 06 Mar 2026 02:01:59 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Fri, 06 Mar 2026 02:02:00 GMT
ENV XCADDY_VERSION=v0.4.5
# Fri, 06 Mar 2026 02:02:00 GMT
ENV CADDY_VERSION=v2.11.1
# Fri, 06 Mar 2026 02:02:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Mar 2026 02:02:00 GMT
ENV XCADDY_SETCAP=1
# Fri, 06 Mar 2026 02:02:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 06 Mar 2026 02:02:00 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 06 Mar 2026 02:02:00 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644a983862e3898a5575fef5c81590cbc92d1c1e1bf5f61112c0cd35e6b7be98`  
		Last Modified: Fri, 06 Mar 2026 01:12:20 GMT  
		Size: 296.1 KB (296074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbff1d4eb7eece408734c05c8c63a49bb181871bc1280cff3f0e28d25a4ea28`  
		Last Modified: Fri, 06 Mar 2026 01:12:19 GMT  
		Size: 67.2 MB (67216879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ee208a3600503f47e9ec1ced0e8abb825a045473b092f1fe872b81d9873706`  
		Last Modified: Fri, 06 Mar 2026 01:12:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7536c32ffb9d0750ab8231670250f1ec3d91766d9d9bc395405fa1288dbba14a`  
		Last Modified: Fri, 06 Mar 2026 02:02:07 GMT  
		Size: 6.6 MB (6575295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2ed686c6a0542f92f81d59c764c369b3cad39aab2300bce968479eecb8a961`  
		Last Modified: Fri, 06 Mar 2026 02:02:07 GMT  
		Size: 1.8 MB (1846498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d154dde61d0cef3b37f3ecb5bd09f8eef4b639936e75a90ce2202fb422934cef`  
		Last Modified: Fri, 06 Mar 2026 02:02:07 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3e3a7c260ca655632015ac348f420257a65e50213ee94beb28e6194bfebdc81d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 KB (304454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf94860227b93feff4e246719bbe1fe4fdb43b6b02e5f64be3a5ba8a9825d396`

```dockerfile
```

-	Layers:
	-	`sha256:d25c27a525b856ffba173f19ea11d90fb065a057d09a7bdbc631080ccb5aadcf`  
		Last Modified: Fri, 06 Mar 2026 02:02:07 GMT  
		Size: 284.3 KB (284325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:583669327988b4736a032d66a180f1746a8efbbe7a32c954bb8dabe7062bfef8`  
		Last Modified: Fri, 06 Mar 2026 02:02:07 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:b68e351f465c71af270b5c3c37626586f891ff484b97728728f611cebaac9fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77854461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd9cd11ada7abb332c6ff64aedf895836ccbd60fcae325b1264190c401871eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:12:48 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:13:12 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:13:12 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:13:12 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:13:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:13:12 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:13:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:13:15 GMT
WORKDIR /go
# Fri, 06 Mar 2026 01:59:23 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Fri, 06 Mar 2026 01:59:23 GMT
ENV XCADDY_VERSION=v0.4.5
# Fri, 06 Mar 2026 01:59:23 GMT
ENV CADDY_VERSION=v2.11.1
# Fri, 06 Mar 2026 01:59:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Mar 2026 01:59:23 GMT
ENV XCADDY_SETCAP=1
# Fri, 06 Mar 2026 01:59:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 06 Mar 2026 01:59:23 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 06 Mar 2026 01:59:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1109a5071b02b1044612a78906bb866947d31adddc34582210c9b1df0d6c2d`  
		Last Modified: Fri, 06 Mar 2026 01:13:26 GMT  
		Size: 297.3 KB (297262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96dfc026f620d0674c1a89536cf39d64e74602dba70d199d21c90c7b01bd9ba2`  
		Last Modified: Fri, 06 Mar 2026 01:13:28 GMT  
		Size: 65.8 MB (65757141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bf8dd9810462b9c3cf1794258fb5fb3448a3b8ff5e6eee0b1449b61acbdab2`  
		Last Modified: Fri, 06 Mar 2026 01:13:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb961baed51b0dfc2504f17360672a62bf0ef8694cb664cb5696e752b0b1621`  
		Last Modified: Fri, 06 Mar 2026 01:59:28 GMT  
		Size: 6.5 MB (6484645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e936ba61abccb588545490dffe8c48a3111537972adf0037bc5ad62d232070`  
		Last Modified: Fri, 06 Mar 2026 01:59:28 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906d3254d53454158dc8259477654e15f2c477e46e3d9dd518119becf0352527`  
		Last Modified: Fri, 06 Mar 2026 01:59:28 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:b4f000f78e0bde861628638b69a95839d3eec164ffa8b64b7729cbed26684652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6aef0d9b5ba74e8d10e6caff27319d2d79d1728176fae3af639e54f94efa98`

```dockerfile
```

-	Layers:
	-	`sha256:64cc2470ec058c121a985e2a9f0169c963231016f7e5349975d64d463e73c4f6`  
		Last Modified: Fri, 06 Mar 2026 01:59:28 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ef2c2a68153a2815b415dd5026a2db9b814ced8bf1d3783018c346738e9e67ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77008742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2e3ef8349150789db0678c05b7fe5362f8eda742491a96def460508891cf02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:11:40 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:11:52 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:11:52 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:11:52 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:11:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:11:52 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:11:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:11:55 GMT
WORKDIR /go
# Fri, 06 Mar 2026 02:01:41 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Fri, 06 Mar 2026 02:01:42 GMT
ENV XCADDY_VERSION=v0.4.5
# Fri, 06 Mar 2026 02:01:42 GMT
ENV CADDY_VERSION=v2.11.1
# Fri, 06 Mar 2026 02:01:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Mar 2026 02:01:42 GMT
ENV XCADDY_SETCAP=1
# Fri, 06 Mar 2026 02:01:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 06 Mar 2026 02:01:42 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 06 Mar 2026 02:01:42 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8528f8fd0be7185e5fdd156634e845361ee385919d5f74f4dcdcdb37ceb8ff5`  
		Last Modified: Fri, 06 Mar 2026 01:12:09 GMT  
		Size: 296.2 KB (296202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c71a08a325c7d5f7b73bc8da93a0980d5401206ec7c3b40584ca8d21ca82f77`  
		Last Modified: Fri, 06 Mar 2026 01:11:53 GMT  
		Size: 65.8 MB (65757104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffb5ff6c2a264c2b3f1d07eb347799ecf4b393d1b4bfabb7c4d26a87c7354ae`  
		Last Modified: Fri, 06 Mar 2026 01:12:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8c7fb5130bf6ec425e9c894e0883a924efa2f25800d3048a979fb9f6c7cc42`  
		Last Modified: Fri, 06 Mar 2026 02:01:49 GMT  
		Size: 5.9 MB (5934362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9991bf00fb1597e9101f4997fe4d4160c2cb5bb1f058d5d04023997dd62ff3`  
		Last Modified: Fri, 06 Mar 2026 02:01:49 GMT  
		Size: 1.7 MB (1738758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdee45358057d0489329c53381bb82ee6499a3c0c1344c932b7f7cedc15d5c4e`  
		Last Modified: Fri, 06 Mar 2026 02:01:49 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:eb9999edac04c78634266961dc64892ad9b84cf9ad851c4d2c9fd8a6b2cbfa56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 KB (306971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ae3ac6ed4a10079014b04436973b215cbcf89845cfdf1b3ce452b73c15dfaf`

```dockerfile
```

-	Layers:
	-	`sha256:ee8a55d1f2c386daab7e977fc56015a1e77850f8491eb817410dcd23d77e2426`  
		Last Modified: Fri, 06 Mar 2026 02:01:49 GMT  
		Size: 286.7 KB (286717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17964f10ecec074220bf4099087551f076adb720bbd1161a922606466d41f455`  
		Last Modified: Fri, 06 Mar 2026 02:01:49 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9bb77fa8353dda97b47ab9bc04da155e32cb60a7326e189b0ddf547414c2960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76977276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c99768a4fa1ec535c4ee641e818ef10f1859bba1a221fa3684cbcbbdc8b574b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:11:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:11:46 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:11:46 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:11:46 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:11:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:11:46 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:11:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:11:48 GMT
WORKDIR /go
# Fri, 06 Mar 2026 02:04:50 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Fri, 06 Mar 2026 02:04:51 GMT
ENV XCADDY_VERSION=v0.4.5
# Fri, 06 Mar 2026 02:04:51 GMT
ENV CADDY_VERSION=v2.11.1
# Fri, 06 Mar 2026 02:04:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Mar 2026 02:04:51 GMT
ENV XCADDY_SETCAP=1
# Fri, 06 Mar 2026 02:04:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 06 Mar 2026 02:04:51 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 06 Mar 2026 02:04:51 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62764d53541d11f63129956ccd8b52d20597aca289f431759deb77ea2275f569`  
		Last Modified: Fri, 06 Mar 2026 01:12:03 GMT  
		Size: 298.8 KB (298849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49db9bb2f958b7444a4f28145af7a815dd0a47fec1608d03e2f1c673b3aa858b`  
		Last Modified: Fri, 06 Mar 2026 01:12:04 GMT  
		Size: 64.1 MB (64106129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4901bef231fb8a6d26e9c2ceb808c5c0ed8319bb7a5f6b5a284cac28d8f72b8e`  
		Last Modified: Fri, 06 Mar 2026 01:12:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccadc75e815a97cc240bc05b5338bae684e885e662215e7cffb3a42d510b9745`  
		Last Modified: Fri, 06 Mar 2026 02:04:59 GMT  
		Size: 6.7 MB (6658228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e378394d67d383f1fe7bec84f7250ced453e685b31c8ce3b6a3d635c9c4188b`  
		Last Modified: Fri, 06 Mar 2026 02:04:59 GMT  
		Size: 1.7 MB (1716386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d377e8d345b7e0251f776585f9b72ca53c8c417f56301e8daf606dde2a39d153`  
		Last Modified: Fri, 06 Mar 2026 02:04:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ba137697faf456e4102b43be07770990becfea7c7f9f4462ea5facb3e94dfec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 KB (304075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1ef2aba94fc1a4949c1c3badd38eaa86c753fba8a9b5380ed9b5fd11664496`

```dockerfile
```

-	Layers:
	-	`sha256:2ef870a0c52ad0a26d0dd7d02aa2ff41d7c1c5748dc13e0d605489f03fc7db0f`  
		Last Modified: Fri, 06 Mar 2026 02:04:59 GMT  
		Size: 283.8 KB (283779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac9eb4ec79538f6b5c5a8b74cac22052c3128279d66d47ffc12b2f6635f8887`  
		Last Modified: Fri, 06 Mar 2026 02:04:59 GMT  
		Size: 20.3 KB (20296 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:e16387084e794ad1a215d4862bac1be924483f54bfd0db93c7e08df95c8f9895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77594654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee018b6e9143aa7d3013fdb784e9ae8ff55307d5e3a9938a7456296d2df46b18`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:12:22 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:10:37 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:10:37 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:10:37 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:10:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:10:37 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:12:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:12:41 GMT
WORKDIR /go
# Fri, 06 Mar 2026 02:07:35 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Fri, 06 Mar 2026 02:07:36 GMT
ENV XCADDY_VERSION=v0.4.5
# Fri, 06 Mar 2026 02:07:36 GMT
ENV CADDY_VERSION=v2.11.1
# Fri, 06 Mar 2026 02:07:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Mar 2026 02:07:36 GMT
ENV XCADDY_SETCAP=1
# Fri, 06 Mar 2026 02:07:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 06 Mar 2026 02:07:37 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 06 Mar 2026 02:07:37 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e662a4a3a7cbf153b23a38a961b2078122cec8354bbb9cc27381fb9fd6abd628`  
		Last Modified: Fri, 06 Mar 2026 01:12:55 GMT  
		Size: 299.3 KB (299266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace710cfb3bb4da72d185d83d05e86cb22a686c0abd5be3e83cdf74e34b68d02`  
		Last Modified: Fri, 06 Mar 2026 01:12:05 GMT  
		Size: 64.8 MB (64765980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3645e9a27139f1a82b884568a2ebeca4b84caad36f011c206583bab85d758e73`  
		Last Modified: Fri, 06 Mar 2026 01:12:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1a66af16688cd52acc6e44bd18a39dba777cd311ad70462741a2ad39c4dbf3`  
		Last Modified: Fri, 06 Mar 2026 02:07:57 GMT  
		Size: 7.0 MB (6993179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9ba7ac4817dae141315f9b20cf0a15a9cb87bd733600c84a5ff4753ea99388`  
		Last Modified: Fri, 06 Mar 2026 02:07:57 GMT  
		Size: 1.7 MB (1705994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d7566760304b45ea889aef434c12d1bd9934ef449375d59288394393589e67`  
		Last Modified: Fri, 06 Mar 2026 02:07:57 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:afd3b47b9c7c39787a0e6ee1e93e9e5780c0de830fc5a1429368f643f5bd1350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 KB (303946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998edb93fca775c95d7b1be7fdcbdce769f28a04a21ab90ab2537620e14d2fba`

```dockerfile
```

-	Layers:
	-	`sha256:a50cedb20463473c8234a42d61738e209ad6a29f795d0673bbefd9dd4596d821`  
		Last Modified: Fri, 06 Mar 2026 02:07:57 GMT  
		Size: 283.7 KB (283748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:227a496d204aca8164b9888e3ed4b1529f5519e0efa3450a2e879a8230f05f92`  
		Last Modified: Fri, 06 Mar 2026 02:07:56 GMT  
		Size: 20.2 KB (20198 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:d507461699fd89c3aacb5030fdc31f34e0b4c2f4945f48476d1abe6c509bdc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77435272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547a2e079a6e0c6a0366ea8db305e02d9affda17ffa80fb4cae0323248c40945`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:12:00 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:12:00 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:12:00 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:12:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:12:00 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:20:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:20:33 GMT
WORKDIR /go
# Fri, 06 Mar 2026 03:23:18 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Fri, 06 Mar 2026 03:23:20 GMT
ENV XCADDY_VERSION=v0.4.5
# Fri, 06 Mar 2026 03:23:20 GMT
ENV CADDY_VERSION=v2.11.1
# Fri, 06 Mar 2026 03:23:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Mar 2026 03:23:20 GMT
ENV XCADDY_SETCAP=1
# Fri, 06 Mar 2026 03:23:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 06 Mar 2026 03:23:20 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 06 Mar 2026 03:23:20 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f6a28a44ff91c18ab295ffef6822bbaccafe002bd1f4a117c179d363e86328`  
		Last Modified: Thu, 29 Jan 2026 19:14:45 GMT  
		Size: 296.5 KB (296505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7741c0adede1d2e9597a871420fa82f196151039c468eac7755d531cfe50922`  
		Last Modified: Fri, 06 Mar 2026 01:18:47 GMT  
		Size: 65.1 MB (65077505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15647ffd280dd6c01380ff7053031d8b9c620450567c4be60c59090f35528445`  
		Last Modified: Fri, 06 Mar 2026 01:21:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87114ce9ff5981d8be6f900576f8ea469d86991e6cdf84ceddb9c9f8c48f3e57`  
		Last Modified: Fri, 06 Mar 2026 03:24:37 GMT  
		Size: 6.8 MB (6751171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfe7643713b692a4ea718e8114ee24ed4e57833833aa97a233dd5f0c907d4c2`  
		Last Modified: Fri, 06 Mar 2026 03:24:36 GMT  
		Size: 1.7 MB (1724211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b56db1cb6001293793778f495357fe5899f6c9491a9f0e810522f934fee930`  
		Last Modified: Fri, 06 Mar 2026 03:24:36 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:7a499e1612b59ac0a5c01bcc3c066261a427176bf7443d4374381c371facc47a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 KB (303942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2d2ae1bba6f7ab06e1e0fa7017bf0393bfb1816d1043cda984d3b4cb04db88`

```dockerfile
```

-	Layers:
	-	`sha256:0c63cf4e01ca4221644399f768c35da49d8c450163e32e0606e03918de2c1ada`  
		Last Modified: Fri, 06 Mar 2026 03:24:35 GMT  
		Size: 283.7 KB (283744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f99522bdac15eb9f4afb354a219491cc8979353a460f36850dbf3f742732b721`  
		Last Modified: Fri, 06 Mar 2026 03:24:35 GMT  
		Size: 20.2 KB (20198 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:26251e426c426c4786c8a44c3c0f8bd08e83556454d961b78b6f7c2bc4a6014d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79100336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b78fa6892e5021602ee80a83026499c3b95c016705ddcf0bc960b86e896e9f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:10:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:10:52 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:10:52 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:10:52 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:10:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:10:52 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:10:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:10:56 GMT
WORKDIR /go
# Fri, 06 Mar 2026 02:02:40 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Fri, 06 Mar 2026 02:02:41 GMT
ENV XCADDY_VERSION=v0.4.5
# Fri, 06 Mar 2026 02:02:41 GMT
ENV CADDY_VERSION=v2.11.1
# Fri, 06 Mar 2026 02:02:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Mar 2026 02:02:41 GMT
ENV XCADDY_SETCAP=1
# Fri, 06 Mar 2026 02:02:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 06 Mar 2026 02:02:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 06 Mar 2026 02:02:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79449d8f37ca627569c53e700d0b5ae9b25ebeef0a08dac074cc719821e22ba7`  
		Last Modified: Fri, 06 Mar 2026 01:11:18 GMT  
		Size: 297.2 KB (297183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ac4fc296175935efd55931d7d181f8e7c85d38405c6fdcb1a96bcb9115d7eb`  
		Last Modified: Fri, 06 Mar 2026 01:11:11 GMT  
		Size: 66.4 MB (66432747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d729dd9fe0b725e8d914a70685a29638ee35da82ebe402e075a4ca4768e879b3`  
		Last Modified: Fri, 06 Mar 2026 01:11:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3449d85ed8aaeef608816df7eb2c8d8f2f1a79dcbe1301433445a6794befdb8d`  
		Last Modified: Fri, 06 Mar 2026 02:02:54 GMT  
		Size: 6.9 MB (6861639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f99a76a20775f3544286e2296a4fc09f896a468d4bff8d9d36a7916fb85b47`  
		Last Modified: Fri, 06 Mar 2026 02:02:54 GMT  
		Size: 1.8 MB (1782842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d99d4783a126b42d3c2d7304949e4ab0269d147ee5fa8d6b0bbe318e5cacd7e`  
		Last Modified: Fri, 06 Mar 2026 02:02:54 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:d99ae40d43c1b51bc237ea4b999dacf5fbd77749c200493a0a46fa51cc31a307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 KB (303803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f965e9bbf9ee9a62a09448ff44d7ead1579cb072fa3aa248446524cc696a87ba`

```dockerfile
```

-	Layers:
	-	`sha256:239ae9d691526852e6ed6431e47be2be2bafd30e737c8b073a60126b9b388393`  
		Last Modified: Fri, 06 Mar 2026 02:02:54 GMT  
		Size: 283.7 KB (283674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:972ae0fc627f1b60a177a994fa1373cfb55ab80e191b70241bbfcabe907159e4`  
		Last Modified: Fri, 06 Mar 2026 02:02:54 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json
