## `golang:tip-20251017-trixie`

```console
$ docker pull golang@sha256:12a6a84b3a1e8e46f3b377e41f36324c655a4d2d2d1a8b426a3cc2e3bc1d8264
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-20251017-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:81fafae640198a4331beaffa2155c84fed945f72c73da358979472451a794a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292617845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7becaa88d3495ecdd83d12d203862305f014553476658ff066ca420f72117356`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 20 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb493dcf3b69e9a1db697812a3fc5bfe7fcb242df4acefdbc52c83061a17b0`  
		Last Modified: Tue, 21 Oct 2025 18:15:32 GMT  
		Size: 72.7 MB (72733669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e37a565b466ff673d6eaad95f7f918df4a47f13ea7ff94f9312bc4a254253fc`  
		Last Modified: Tue, 21 Oct 2025 18:15:25 GMT  
		Size: 87.8 MB (87837459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a856dfd500b2aa8241f23d4669787e93188d793c824341ec59103ce815f2e6cd`  
		Last Modified: Tue, 21 Oct 2025 18:15:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251017-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:371e9e28dd2efc8fd1bdc5dd63a865e31e93d647025ad9e02085f57e2542f8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbad00bc52e3733c59982fdf4904cc813ed4aecda26975610e2915ec9eec649`

```dockerfile
```

-	Layers:
	-	`sha256:d52001bc3ad5f4b4c578a5d2b3fbed554197b08cd9d0f2387f5451f54af513fd`  
		Last Modified: Tue, 21 Oct 2025 20:23:21 GMT  
		Size: 10.6 MB (10580347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82be58608af11df0966bd94327550281a5e4aae9a4d90fb18b2fc0cdb633d879`  
		Last Modified: Tue, 21 Oct 2025 20:23:22 GMT  
		Size: 29.1 KB (29135 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251017-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e2525ded3c602b9a736006ad95be6ddb8e0a5b924ea232f773d570ffff220100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327273357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b856be8164e60d280650f21d5a0d0ff45391505d377b5583de62f55bac9e4926`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 20 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3a2979d3d2873337872b28636ebe83674827dca73806746af98a4a1108b939`  
		Last Modified: Tue, 21 Oct 2025 18:13:55 GMT  
		Size: 98.2 MB (98234205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c596fe60daead99d920e71d2cefb1c0329c841dbd8772728b90e497e3f4f21b`  
		Last Modified: Tue, 21 Oct 2025 18:14:12 GMT  
		Size: 86.8 MB (86788679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98c7592f4866fe7dd69a089d41d99689231559236c387e2a7cdfae60c70663f`  
		Last Modified: Tue, 21 Oct 2025 18:13:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251017-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8b2912e70d9b43faa08841ebfcd084980cd5ad74a0e9b907f5234a33cb86ef81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40301f124d2cd3e43066f35f1535b09fe3956942051cb4d6c99f7aca0190563`

```dockerfile
```

-	Layers:
	-	`sha256:22f49855aae0cb8fbf66e8c16aa23c8e720fcf517154ec8c45bd1efd89d86bde`  
		Last Modified: Tue, 21 Oct 2025 20:23:30 GMT  
		Size: 10.9 MB (10904915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6527259ce91a601728b92a1fd301be5392eda55f261a09a8e6d04724e1c5ea81`  
		Last Modified: Tue, 21 Oct 2025 20:23:31 GMT  
		Size: 29.2 KB (29166 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251017-trixie` - linux; 386

```console
$ docker pull golang@sha256:8e6af2ac9a6abf4088c422b6ed5975ea36b64e25a872ee90c91c394caec218e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.6 MB (337567965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba876d81e88cf9fd65d99c700ab6a18f9d60400635b0aaf0ef39aa630f2b69f3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 20 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e11ad5a4fd5be41f07ac93311f8ae1f7dfd6455edf9f5cf950e26d70ee4c6`  
		Last Modified: Tue, 21 Oct 2025 01:53:30 GMT  
		Size: 26.8 MB (26775679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e99453a1ea6755d1a3a58fe6632281db5820c733291dbefe645ffd8397c7e4`  
		Last Modified: Tue, 21 Oct 2025 02:36:27 GMT  
		Size: 69.8 MB (69795039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedac785dced647bf1c5e3bebc7774ba100dbbbe98decc8a71b09a04910d1f2a`  
		Last Modified: Tue, 21 Oct 2025 18:13:43 GMT  
		Size: 100.5 MB (100533198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f21a8159428f1559d656875bfece2dbae3e195e6c40dc6a160e07432d96a1ef`  
		Last Modified: Tue, 21 Oct 2025 18:13:42 GMT  
		Size: 89.7 MB (89663317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2ae2e87e35026c7590fc9e60523518ec8ba6f329c01ea2f61f3fcf2fd87edb`  
		Last Modified: Tue, 21 Oct 2025 18:13:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251017-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:ee36a3fdb2643e91230e18dd26530325fac8b2275e74f3dc4f76fc4021bde289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fc1f06b8d686ebd23fc862bcaee23759023fee2ba959f452d62ed6ed5b8b20`

```dockerfile
```

-	Layers:
	-	`sha256:6f95392db2d725bc8faac36093fb78a71061714a34c5836eee459814eb20507c`  
		Last Modified: Tue, 21 Oct 2025 20:23:37 GMT  
		Size: 10.8 MB (10755724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2997047cabc8076ff203b172e7c57e20555c046dac743aa8a99cf9abe5e8ab37`  
		Last Modified: Tue, 21 Oct 2025 20:23:38 GMT  
		Size: 29.0 KB (28968 bytes)  
		MIME: application/vnd.in-toto+json
