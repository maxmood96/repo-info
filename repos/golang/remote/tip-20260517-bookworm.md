## `golang:tip-20260517-bookworm`

```console
$ docker pull golang@sha256:87025993bd4d93adda623b1b077d99812f7425f8c48f8a55272ef3d6b3a6d4f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20260517-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:134997c89af4b7fa3786b40efc7130b35b18186e6f56c2b93010f9058a35cbc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.9 MB (326908517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e56b3c984e7280205fe308a9687284d8ad4b7a580d5aac01bb46e6dd431479c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:18:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:19:52 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 May 2026 02:19:52 GMT
ENV GOPATH=/go
# Wed, 20 May 2026 02:19:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 02:19:52 GMT
COPY /target/ / # buildkit
# Wed, 20 May 2026 02:19:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 20 May 2026 02:19:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e5bd62b551e6aa52d207b2ab8a73ac41d8b02f9f583c11197498b2d38c7ce8`  
		Last Modified: Wed, 20 May 2026 02:20:22 GMT  
		Size: 92.5 MB (92480138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6616f3853b3ecfbe6802f0a5bc39a71a89535589f78590596712ece3ecb87a81`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 97.5 MB (97484964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135e740998e09423ab8ee91092f4b666baa8f9a2ab07073c46c4eef9e8445b9d`  
		Last Modified: Wed, 20 May 2026 02:20:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3a90de799d3cff5510513ef067b18b47e1af1df207ea1421f205dfeff9e19b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b85483503f2a2dbd3a902c89925d228967a9f898c18e3f4098f2473b0221aa9`

```dockerfile
```

-	Layers:
	-	`sha256:92a2abe5d041edc20e4ecadebe1b0e1a11837e2f8a7f65070b1dd00d6d9c08e6`  
		Last Modified: Wed, 20 May 2026 02:20:20 GMT  
		Size: 10.5 MB (10497055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9a3206659ddd01a6f0fe972edeff083605b9682b4a5a6fd1144df23cc38228c`  
		Last Modified: Wed, 20 May 2026 02:20:19 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:45fb4200dd8460ddad351d97501965551bfcc5be11cfe3f70a21a300b644d251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285504086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15133899ef3b9f0219dd3cebd9be2e0f05d2200d3e1e8ecb0d6cfea6bb235bbb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 04:16:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 04:19:05 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 May 2026 04:19:05 GMT
ENV GOPATH=/go
# Wed, 20 May 2026 04:19:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 04:19:05 GMT
COPY /target/ / # buildkit
# Wed, 20 May 2026 04:19:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 20 May 2026 04:19:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61246c0a5a0fe9fe8cdc1bfde0fdfa49ffafcc94cba31f4aecc0c34bc346064`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 22.0 MB (21950133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56a54e4354794da97ac9fe5173f689d775d13afa792e8b390e49425c3caa6b5`  
		Last Modified: Wed, 20 May 2026 01:34:11 GMT  
		Size: 59.7 MB (59661818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3545dc99595d8364091eace8fb1ffb6929321710cc33ee27ea527242c2daf155`  
		Last Modified: Wed, 20 May 2026 04:19:32 GMT  
		Size: 66.3 MB (66339808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5478a8019bc908653f4fe6a66ee439d142c623ca5f9ce8029f0fe1b0d2c74`  
		Last Modified: Tue, 19 May 2026 18:49:27 GMT  
		Size: 93.3 MB (93343015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3980f1a7ccbd3f95a2b44fd294db48d045ff18c0bdbc087b64280a890c7097af`  
		Last Modified: Wed, 20 May 2026 04:19:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f684c00bfeca495de4428cc4db6ba9e016c80166b1e2984a64ae98bd55437a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31766bbb372144fb9c2fea74576bab9e6e8549ef3ab67788e5829b28a69fb279`

```dockerfile
```

-	Layers:
	-	`sha256:90a655fc0ba5db06d61df18343aa8a4a396644a16a33f41de068ad16d6045b61`  
		Last Modified: Wed, 20 May 2026 04:19:31 GMT  
		Size: 10.3 MB (10303751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afdfab61937a6911cb934a6f5359f8239c5292e2b7bef2612839c437e30160ce`  
		Last Modified: Wed, 20 May 2026 04:19:30 GMT  
		Size: 28.5 KB (28497 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1a3706686afe5d14acf6c8095595307210474eb057a40b866d3dcd9786d10563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.3 MB (315255912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2560b7226850ebb8823c04491232936533e4479deed9e407a06200c831fb357`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:17:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:19:37 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 May 2026 02:19:37 GMT
ENV GOPATH=/go
# Wed, 20 May 2026 02:19:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 02:19:37 GMT
COPY /target/ / # buildkit
# Wed, 20 May 2026 02:19:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 20 May 2026 02:19:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb14b640a36236c6c116254b56d6f6dc3bf5a116b2ed02892f75505e68017e40`  
		Last Modified: Wed, 20 May 2026 02:20:05 GMT  
		Size: 86.6 MB (86553863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758ad482d2898f832f866a10e8b2d7cae0b36c78a58ed7da81be2817260f57a4`  
		Last Modified: Tue, 19 May 2026 18:45:10 GMT  
		Size: 92.2 MB (92221410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd922d2d7a3d27fd058cb30752b71947eeea07f4bf278da1a4f8e75fcad8c1ea`  
		Last Modified: Wed, 20 May 2026 02:20:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7ad0abc1df9e019225e42ed4a54bb2fefeffb377f600e3e862fdd50332c8975a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f3b01ac59c45d74839dc13ad58b44726b92c71508fe49a787ef282e03b118f`

```dockerfile
```

-	Layers:
	-	`sha256:df8d8b7d317d4b07156880381501fb2532731a80c6e2328dd2906325cd24510e`  
		Last Modified: Wed, 20 May 2026 02:20:03 GMT  
		Size: 10.5 MB (10524879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece06cf1bf3491512876e65395885e920ad0e8bfe77218dcd6d77771b8a0e894`  
		Last Modified: Wed, 20 May 2026 02:20:03 GMT  
		Size: 28.5 KB (28520 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-bookworm` - linux; 386

```console
$ docker pull golang@sha256:6f363ac73ead21c7165c7317f32d134ccb45e9d5a46c4c456890934f214ce82e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325805484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82f7d65397b3dc015601bda8bdcac39670048456c572a61d1a556d143b178ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:44:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 06:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 06:15:40 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 May 2026 06:15:40 GMT
ENV GOPATH=/go
# Wed, 20 May 2026 06:15:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:15:40 GMT
COPY /target/ / # buildkit
# Wed, 20 May 2026 06:15:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 20 May 2026 06:15:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8bf11fb6e89cfb8d682f511fb7d1b795e747af9c12a192f45f6e50ae7ca54f50`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 49.5 MB (49483120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db105b3a1c2456422c428304ae93436fac4214751cb65053af119fa6d81d85dd`  
		Last Modified: Tue, 19 May 2026 23:24:59 GMT  
		Size: 24.9 MB (24879482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e2a05321daf588afd8b06b380f7ea0a3d7c0de2097ec6f355a74453e7ec6af`  
		Last Modified: Wed, 20 May 2026 02:45:13 GMT  
		Size: 66.2 MB (66243865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0772d2eb7f757a305ce685692df45b08407c33199286addcba722073ac926f62`  
		Last Modified: Wed, 20 May 2026 06:05:19 GMT  
		Size: 89.9 MB (89903350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1c12b1c007dae0ded7a2c5d8a74dfe44bec08363cdf8556a245d7c8b644731`  
		Last Modified: Tue, 19 May 2026 18:46:48 GMT  
		Size: 95.3 MB (95295509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da1653bded4d45f6673f100fa6d83632b723c4b55d22ff37ba73ef198857c3b`  
		Last Modified: Wed, 20 May 2026 06:16:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5f0fa4e7cc667d0eef72ceaec8eeb327f96f8f4afa3abd987438fa7b2770fd6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcec16e3519f379cb3d0dbdea761237e1be770a317dd6a48add658ecbffa476e`

```dockerfile
```

-	Layers:
	-	`sha256:6a0f30c4cbdabe266e296344d44e331a02566529b5c9dc7aac6e23b4d999f73f`  
		Last Modified: Wed, 20 May 2026 06:16:04 GMT  
		Size: 10.5 MB (10476635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f19cea421fb0b1b0757535b15a292f129e982b4d209bac0bf1bbd4e09ba8da8`  
		Last Modified: Wed, 20 May 2026 06:16:03 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:336e067cf52ea726f5abd92da3c9a0719d6cda1e9df833d6b413f0905e62f5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296960875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a37ca699b7c0ebe230aba438675848b5817750d66e7601603334d6418e3c36`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 10:04:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 15:11:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 16:19:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 18:37:44 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 May 2026 18:37:44 GMT
ENV GOPATH=/go
# Wed, 20 May 2026 18:37:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 18:37:44 GMT
COPY /target/ / # buildkit
# Wed, 20 May 2026 18:38:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 20 May 2026 18:38:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:813eaff938e8991b3dd16851af2c46dd2ffc5bb600e30ff866dd5a60502fbffa`  
		Last Modified: Tue, 19 May 2026 22:35:13 GMT  
		Size: 48.8 MB (48786239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2853b2ecd2cc91271c3528597da43fc45c41515894834d1de212a390afbf0ade`  
		Last Modified: Wed, 20 May 2026 10:05:32 GMT  
		Size: 23.6 MB (23621201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bf4bd887b67ee95b1804bd893717310da36bddd5a598cce7e9b621ff52ee05`  
		Last Modified: Wed, 20 May 2026 15:12:43 GMT  
		Size: 63.3 MB (63316337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d8edfd178bcf28b946d64eb3ad538d4ee96dacac854fd44ba3af295e68b368`  
		Last Modified: Wed, 20 May 2026 16:21:18 GMT  
		Size: 70.1 MB (70084514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53f20e8901af388e8277adb933a3ae58abffbc3e51d3a641b11354bd33941f9`  
		Last Modified: Tue, 19 May 2026 19:09:00 GMT  
		Size: 91.2 MB (91152426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518a34dba8b55fbbc932e2e5268754e1b75c86ea972d47d3922bd0e0f7c215d0`  
		Last Modified: Wed, 20 May 2026 18:39:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7ac92507e26b6c8a8e11d5a53613a5109c98cee30d1f6a43890fd49a00e39b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707a72460df4551c96b4fee27c894f5c262006c6dfec62649954baf94150d982`

```dockerfile
```

-	Layers:
	-	`sha256:a1669209545900691d9f4aa54f5ca8fe7070358c0873533c4807543a7dae7f20`  
		Last Modified: Wed, 20 May 2026 18:39:50 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:da266e3e60211ef0684407cfb2b76552a7317eb4ef564bb8ba67b35a119465ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.4 MB (332427649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872d62727452fb5deea333f9e79082a3cf741e90aab7eb16dd0bf8dce0ac62f7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:13:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 06:50:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 09:12:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 18:48:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 19 May 2026 18:48:50 GMT
ENV GOPATH=/go
# Tue, 19 May 2026 18:48:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 18:48:50 GMT
COPY /target/ / # buildkit
# Wed, 20 May 2026 14:17:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 20 May 2026 14:17:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f46c910cb3dd366a8b080c77b15459d7465da54412b3570454cddcaf0cdf40`  
		Last Modified: Wed, 20 May 2026 01:13:39 GMT  
		Size: 25.7 MB (25686466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67cb71cd5984ee53ab56bef57a29d3b0ef6e8939c352146b1efe66402d4c7ff`  
		Last Modified: Wed, 20 May 2026 06:51:27 GMT  
		Size: 69.9 MB (69853485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bae1f9f6144fca8edf5d9d7cc5bb0fe155a272843049769232560831cade6a9`  
		Last Modified: Wed, 20 May 2026 09:13:22 GMT  
		Size: 90.5 MB (90495115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b031549f4a149afd12a0aa62ad2634135f41cb41de30ad0670c5e09695e591f0`  
		Last Modified: Tue, 19 May 2026 18:50:13 GMT  
		Size: 94.1 MB (94052228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c916501412a0f37a791278512b77bcab46ecdf28a6f89d26c2daccb8ee786e69`  
		Last Modified: Wed, 20 May 2026 14:18:24 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:60b4a9bdd8db7466435e5afaf4934f4bce9f90cd3dca86f2300bf70ebaceea2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c9e72f1c1fc7d5a7cdced8b3b2a640fdb1b39d32e957bfcbc5f3c56cd0d254`

```dockerfile
```

-	Layers:
	-	`sha256:12578a43ecc1f811e3caf5ca82fff85016ad882f1ea8af54ede061ec288ced0d`  
		Last Modified: Wed, 20 May 2026 14:18:25 GMT  
		Size: 10.5 MB (10469540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a1d3393c4c13d437fe2c7d7272cb195a46add200af15e2f56d3deb5086a7b33`  
		Last Modified: Wed, 20 May 2026 14:18:24 GMT  
		Size: 28.4 KB (28431 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:5e78848291605e03cac3c77fe3169444582acaeaab47197adefc04c349c602b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299797643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ccb0ea293357f693543402e7e4461902c9080643b940c192cc0d09b68b6dd1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:17:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:46:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 18:46:44 GMT
ENV GOTOOLCHAIN=local
# Tue, 19 May 2026 18:46:44 GMT
ENV GOPATH=/go
# Tue, 19 May 2026 18:46:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 18:46:44 GMT
COPY /target/ / # buildkit
# Wed, 20 May 2026 05:13:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 20 May 2026 05:13:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79feab17202415ba0b431eca0e903b1c895e662e755c4c9f1b5678ad8eb605f`  
		Last Modified: Wed, 20 May 2026 00:18:12 GMT  
		Size: 24.0 MB (24039201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511ade0407a6db3c4a6853a735563e5fb22577aaaa32942a9458cc0c09942583`  
		Last Modified: Wed, 20 May 2026 02:05:37 GMT  
		Size: 63.5 MB (63498321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d6ff3d818fd97aacd81ce6295e3d8da60684c2af3275bbdd42cc1809ea7991`  
		Last Modified: Wed, 20 May 2026 02:46:53 GMT  
		Size: 69.1 MB (69087355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c82cd174659cb53c7768fbc8389b7b3eabb725a4a95e0bd43007eb9eef0a5b`  
		Last Modified: Tue, 19 May 2026 18:47:13 GMT  
		Size: 96.0 MB (96017021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ba2631a4b7b307db2884b779799da6b78dcd228d8ce7e5479e101644414c06`  
		Last Modified: Wed, 20 May 2026 05:14:01 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c276d5d0deb643969f09855038217cf34e599cfba14e0a679b747952612eb5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abe442a090bde0a7a807bc97680ff9c1ef6070a7f18cfc6b9a798ebb66f4bfc`

```dockerfile
```

-	Layers:
	-	`sha256:96672629096d2d6b5f00533621113fc45d0a49b23868a04196abd084d2ed5e71`  
		Last Modified: Wed, 20 May 2026 05:14:01 GMT  
		Size: 10.3 MB (10329561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ea4c5bafe271793fd7ff34f4c23b32db5ba4b35ad5959474207653df3b34f8`  
		Last Modified: Wed, 20 May 2026 05:14:01 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
