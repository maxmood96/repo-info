## `golang:1-alpine3.18`

```console
$ docker pull golang@sha256:3c8959be72c0de050d3ce6fb5512d80ac1419fba9009a5cc2c662e0cd1764024
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:1-alpine3.18` - linux; amd64

```console
$ docker pull golang@sha256:ddf1daf6f09b678205fc3b066bbd39245358122f3df2a7fb5696469738b2046f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73038789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4e5330a687b123a20d059fde890535e3982c352dd646e48db30f868b73437b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0593119ece12d950009e49bc9887d4a51a7223e91a6f8877965ce77d967d710`  
		Last Modified: Tue, 14 May 2024 22:57:18 GMT  
		Size: 293.4 KB (293395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a37d9fbc90eb12205f6e84f34311e4f9927672926a872e755905662f13c950`  
		Last Modified: Tue, 14 May 2024 22:57:19 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b48a043c8955b2ddf24e0856c3b40103897ae67a1a40b934b8f22f51a8983a3`  
		Last Modified: Tue, 14 May 2024 22:57:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.18` - unknown; unknown

```console
$ docker pull golang@sha256:ca5ed4743cf5b36224fea5155f5156ff076e1adb650a074037187701b03f31e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 KB (226011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087cd4533d88d242283052831dd468586bdf8a8af898945f0904fbe65c382b17`

```dockerfile
```

-	Layers:
	-	`sha256:43edf4d1ed03423b9f64765d08d631c53f6c4fcec58960d25ed0fcb32c98e6ac`  
		Last Modified: Tue, 14 May 2024 22:57:18 GMT  
		Size: 203.2 KB (203167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:317d64bd15ef7305a95b2a712548be19ed6eb779d66bf35a900b65edd48092ac`  
		Last Modified: Tue, 14 May 2024 22:57:18 GMT  
		Size: 22.8 KB (22844 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.18` - linux; arm variant v6

```console
$ docker pull golang@sha256:d40b8b46d73768c7a3741927a8a8e45861569a53fd5b5d65734a88420c1aa4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71156485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130c9719eb87d83b98f391f31020b7b726b8b5def0b263a5e2f9c37023750b90`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27c253e1ccd740370512ac16dc1198d4cc7e5f79502d830e914be781d2a53ef`  
		Last Modified: Tue, 14 May 2024 23:02:34 GMT  
		Size: 294.1 KB (294052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f87622d8ade59df0daad35a20a0a1b816a8c25ed474cf6048473d6bbd0d46f2`  
		Last Modified: Tue, 14 May 2024 23:01:52 GMT  
		Size: 67.7 MB (67715217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ae0b3b7b9c42c241fed3097122bff9c34f28ea0429903cecbafaad003176e0`  
		Last Modified: Tue, 14 May 2024 23:02:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.18` - unknown; unknown

```console
$ docker pull golang@sha256:9decaa4c0907918c410bab46a842666a01ee4cc5e069849a477ca493dd8a5153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 KB (22721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06ca667a0cb2646bf2bce39cf7a472359f0dcacdf2ff3c8b0f7dfcebcdecc39`

```dockerfile
```

-	Layers:
	-	`sha256:09c0037386ee9fd9789048ab019a43d09d257ae25cf4b73b937abb1cf5ecfc20`  
		Last Modified: Tue, 14 May 2024 23:02:34 GMT  
		Size: 22.7 KB (22721 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.18` - linux; arm variant v7

```console
$ docker pull golang@sha256:2e57541bf401b95bb81bf87459ac80d5e0875339aa877543d865c543bb8963e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70900714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40410a0646662330c22bc56628defa06f6e37f7a322f4f810de6c32de3358b55`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de95814623b83a4328b4db2e23b14214f57c18389a27379988469d9b6bbccc`  
		Last Modified: Sat, 16 Mar 2024 00:51:49 GMT  
		Size: 284.1 KB (284082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6b4809d7be867dc48eeaceb719e94f544b1169dce59a9a9c08766e4243de04`  
		Last Modified: Tue, 07 May 2024 18:30:43 GMT  
		Size: 67.7 MB (67715033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f78d50d16ddc626b592984bfd646d75740a6eebf44e6f37e92b808547aea395`  
		Last Modified: Tue, 07 May 2024 18:30:30 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:64cf4de143277bb4a62dca75e283a956d15da7950b2719fa505b7d9941a49b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69891979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15764b60211e4ed4dd88e24a5be66d933a068343e01ebd53785a8e166c83c49d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c4102457739613c6fcb205a5a8e7dbc8383d57dade0a4502b1bca7b100a4d`  
		Last Modified: Sat, 16 Mar 2024 02:38:03 GMT  
		Size: 286.3 KB (286314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baeaa103b63dd745d677f7cb9d35c5d6e22d449042087f38a5451c5175341412`  
		Last Modified: Tue, 07 May 2024 17:43:15 GMT  
		Size: 66.3 MB (66272097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa4b0ff524f9482b91f8b30048629a4d585b1a760aad57f8941ab53e9c21c33`  
		Last Modified: Tue, 07 May 2024 17:43:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.18` - linux; 386

```console
$ docker pull golang@sha256:f1ae898d09826c33d69b954aac8417ab38ca0c4f5a55a733596ba44339d2a753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70875870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca086291259e1ae05076549d9c348ed87a499e8e290ddd195c7698879578aed8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18573c70dbf50549b7a206e67787eed0020fed8185714414ecad526c9936a5b7`  
		Last Modified: Tue, 14 May 2024 22:57:17 GMT  
		Size: 293.3 KB (293319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae2df63a1850a53fbbc0c4553334c47e00fa2d0dd54cb30a3f0f2e2169353eb`  
		Last Modified: Tue, 14 May 2024 22:57:19 GMT  
		Size: 67.3 MB (67343329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbc6a27de39625a7c2078bbfb8e4b19358690bd91293e09f291352fefb64455`  
		Last Modified: Tue, 14 May 2024 22:57:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.18` - unknown; unknown

```console
$ docker pull golang@sha256:184bde2bdd303e4ff3b5691b9a8f5ab1bbe99807bfff1ee843e966fe6ee51aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 KB (225919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eaa144d4e67d9bde8eba5ba76b1cf6d04ec62c3eefc1a338f3cfd039bd9a5c6`

```dockerfile
```

-	Layers:
	-	`sha256:14da7d05caf8a89f8672ca38c6d730174439f93f77d3c28bdaf2f0dd20006e5c`  
		Last Modified: Tue, 14 May 2024 22:57:17 GMT  
		Size: 203.1 KB (203108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d592bafc59bd631154cb6e84ca285f1338fb90a9721bc453c42cdee6b2b68e`  
		Last Modified: Tue, 14 May 2024 22:57:17 GMT  
		Size: 22.8 KB (22811 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.18` - linux; ppc64le

```console
$ docker pull golang@sha256:f1e7e4da2e7fad01007e1d5963acbf916e51675edc6506d7d486b2724b16f352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70074971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8595addb91705404da5f641e309acfa1ae58128b0cb22e94fcba8716eee3a254`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b2216e014970a83beea11c197a24ccf7f0027acc0d35a08b3a3b2c976b5eff`  
		Last Modified: Wed, 15 May 2024 04:47:32 GMT  
		Size: 296.3 KB (296270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a09e6cada02540e54f2e6e8c59f80c9960dc5c4559a3d96a1cc4bcca469ff9e`  
		Last Modified: Wed, 15 May 2024 04:44:01 GMT  
		Size: 66.4 MB (66430056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd39fad9340cb137aa235308cd7c89a3c56def5c2794e0a45ce6739fb1496852`  
		Last Modified: Wed, 15 May 2024 04:47:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.18` - unknown; unknown

```console
$ docker pull golang@sha256:9500c71b0de1b68edeccc885e8fcf504f946342cb2126bb337f8fa969e2094d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 KB (224000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc82df34c40293633920985f1c4af657d4431b3e353526d1a384fbeddeb0051`

```dockerfile
```

-	Layers:
	-	`sha256:0d2b8403c2d168c7633cb936c96c9f88cffdb066716b0a0d45fa16a96b2db7a3`  
		Last Modified: Wed, 15 May 2024 04:47:32 GMT  
		Size: 201.3 KB (201281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e5224fa46f40afc4cb7579054d90542b4fa58a561e80c0c8fc0b73766ffaab`  
		Last Modified: Wed, 15 May 2024 04:47:31 GMT  
		Size: 22.7 KB (22719 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.18` - linux; s390x

```console
$ docker pull golang@sha256:1dd89ed4c61daf6100f5f50a20d28a1f2ff73949ef877c4a9cd3be3e94b4dc56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71910693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8327478eb9263542094498786ebc5943bf73b8042a540043277cb346873af72d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1a1d4bba7fb363f0ef2f025a4c6c441c7026445c4b9c955c509893576ea917`  
		Last Modified: Wed, 15 May 2024 02:47:56 GMT  
		Size: 293.9 KB (293929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b913ee17a483cc427f632db9240a13b45ee66ca5d56d622dcfedef41eaa6cd`  
		Last Modified: Wed, 15 May 2024 02:44:08 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd84da77a7134a684827315d8ec6701962d13f19fe2d540d01f7886e407e071`  
		Last Modified: Wed, 15 May 2024 02:47:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.18` - unknown; unknown

```console
$ docker pull golang@sha256:d9444f94431309bb7ba725101b7fb7e627fa8f79e27477f677479a52365a7bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 KB (223888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52360fa6babaf91ab9253186f63313e230ac06ba602bfc73f6d648b4fb4f84a8`

```dockerfile
```

-	Layers:
	-	`sha256:54992673c44c7999eb64190384eaf3aa5815651e86b219f2b686bcc6b3d5a6a6`  
		Last Modified: Wed, 15 May 2024 02:47:56 GMT  
		Size: 201.2 KB (201211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da044f6f1bf9c7bad048d20a709259daf1d2c3bb2d92ed0598de7afef7155439`  
		Last Modified: Wed, 15 May 2024 02:47:56 GMT  
		Size: 22.7 KB (22677 bytes)  
		MIME: application/vnd.in-toto+json
