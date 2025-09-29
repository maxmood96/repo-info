## `golang:tip-alpine`

```console
$ docker pull golang@sha256:c1e9e2bce8ef6d154fe6773e75398d377c16990ada565ff2957b32b20f72fa92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-alpine` - linux; amd64

```console
$ docker pull golang@sha256:1c9b83fa43593c44b4c1a0948998d1af73596df54506c18183408564315d5c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87943816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4ab4ccc101151044752bcccb6d267f8713dda2d48fd22361e0c136b21e39d4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b9342bd385b9bd9c1610f76781ee093fcba7c6774800916a4289e62e632ce5`  
		Last Modified: Mon, 29 Sep 2025 17:59:03 GMT  
		Size: 282.4 KB (282441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd392ccd6779e7a888cee1ecce65db01995a1886c75ae75a375deb44486fd071`  
		Last Modified: Mon, 29 Sep 2025 20:26:43 GMT  
		Size: 83.9 MB (83861530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f978a03139e0fb0440efa25ccaa4fe6d2b3cca2be674b4739e2ff46dfc5abba`  
		Last Modified: Mon, 29 Sep 2025 17:58:28 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ead4274061cfb26162c93fd4e35dcab92b266779a8e67ebabbb86ea8b13dcf27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 KB (216665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1846b917c1069b79299702a0ddaed1aed8082f55f7750991aaaf9c24849de202`

```dockerfile
```

-	Layers:
	-	`sha256:0585ced35d5b1c76e8005fa185fa64909db6ab963779fcd2751833250515e07f`  
		Last Modified: Mon, 29 Sep 2025 20:23:58 GMT  
		Size: 191.5 KB (191527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eca1bffe3804f73713c2ccecf5e50d679868f721c679c6ebaa5280fde0920aa8`  
		Last Modified: Mon, 29 Sep 2025 20:23:58 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:ab395d7491ccea6ee142e91c92fe2ed1e0a99577a72e9af0406573bc312c4e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84918780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5e4a08dadc40654cb3ffa193a323e545ae9b15daa29ac5263fca00ffc0c9b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e10eea80913db15dff022e6ead41c1562a1fbe88c47b0e174fb269cb54c212`  
		Last Modified: Mon, 29 Sep 2025 18:01:02 GMT  
		Size: 283.3 KB (283328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892d2bafb7c748b20043b1cea03995c53d72f0418aa848e1ea104b1890116ea7`  
		Last Modified: Mon, 29 Sep 2025 18:01:11 GMT  
		Size: 81.1 MB (81134385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8efc6ec9e982672a355971ab64055f5bcd966f4551ea3ef70a1bc7c33bf9548`  
		Last Modified: Mon, 29 Sep 2025 18:01:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c0c4cc5d2602354710a8a422f0181669badb1621483308ed1d95d271c0da1fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff87769eee3a08fcc57c8f7208b52d178a7705b5b21561dcab84e500305d7f8f`

```dockerfile
```

-	Layers:
	-	`sha256:ecfdb634cb595215d0ed59109ba3bd83087cba210772d4d1921a0b60c430f7ca`  
		Last Modified: Mon, 29 Sep 2025 20:24:02 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:84126e0afffdd29dbd7a5582e120de9ecdd75eb4bf099bd881eb1b50db77af94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84395528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e9f0e41c28ff4e2c21dfc346cbd8be490412cb568273ff256f321d92f9ea90`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d12b51b3b0a3e76c6eceadeceeec9ec4a6c8309e0e056e5904bb5a594a9efb0`  
		Last Modified: Mon, 29 Sep 2025 18:04:19 GMT  
		Size: 282.5 KB (282496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eea36933200b5f141ab18c26e141eacf675fe2778fc8f3cca0727236a934dcf`  
		Last Modified: Mon, 29 Sep 2025 18:04:27 GMT  
		Size: 80.9 MB (80893837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a0ddfdcb9e08ecc7d9164e047bd176c7cdef4f2ecfed7495eccab7b29f242c`  
		Last Modified: Mon, 29 Sep 2025 18:04:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:8373a73b06d89839217edfd3614ae4a984258b317436b32cb9719d81c5e4bb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773fa64daef7ce5598ac0eb34bef94d4ee699e2029282bb4da88a8e62f035fa7`

```dockerfile
```

-	Layers:
	-	`sha256:b24406810efd8cf8e19382c18d345f9aef0a02c496626b3959328d0501576e84`  
		Last Modified: Mon, 29 Sep 2025 20:24:05 GMT  
		Size: 191.5 KB (191549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f2827c9a955549971d8c30c997cc7ca3ddae484f69614b2d67168573d77d1ec`  
		Last Modified: Mon, 29 Sep 2025 20:24:06 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:116bf946772bde0a74009d0cca9cedc45ba57729dc270060b725d806e454e57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84230379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e211fbd4cf07643a830f5cd2a54be5b15e96615e90c2523aaabcdc414860d04`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b550412c4435a604545f894895d65a607a472d0b4de9543f627b4d4f788b2a`  
		Last Modified: Mon, 29 Sep 2025 18:02:07 GMT  
		Size: 284.7 KB (284699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94a779ece8baaa3a2b9ccff68843c683bfb8ad46a4cbd1f1c29fcc7f5e6802e`  
		Last Modified: Mon, 29 Sep 2025 18:02:35 GMT  
		Size: 79.8 MB (79814772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7930c97df107f9554cbc6ea5bab566996cb377ef5e0d4e99aa022090ddb0a7ab`  
		Last Modified: Mon, 29 Sep 2025 18:02:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:046be53ec620861b4d033514f26572a2bc425b3bad74a441c55da4aaaee9b181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ea569684ec218bb8090fc969730f23f81dfacbe3c4226c44af7f5198d8e16d`

```dockerfile
```

-	Layers:
	-	`sha256:f84ed59d84b6ccb54648987c92b7e131e5a4c29a5642e2aff5298424898192ee`  
		Last Modified: Mon, 29 Sep 2025 20:24:09 GMT  
		Size: 191.6 KB (191583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59afd0ec8c68799d1121825b38f82970d7f2b3b09c18d3a93e92765dfcc44ab0`  
		Last Modified: Mon, 29 Sep 2025 20:24:10 GMT  
		Size: 25.3 KB (25298 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:4088b974bb3d2bfa1202a0caaf1fd4ae18b18f07c51998791b84683422f31676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86428774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493cfccf6f245ed77ea241e45be32482075a82495b15e7848904b249a07a9ae8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2a78720363859a00bc952940476e42fb14c7c0558f0f1cdf3f4600bdb7c473`  
		Last Modified: Mon, 29 Sep 2025 17:58:19 GMT  
		Size: 282.9 KB (282922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe29e58b8c06a986ae5ca92831db1a0d8e315d4140a28e6305b3b9513f262ee`  
		Last Modified: Mon, 29 Sep 2025 17:56:00 GMT  
		Size: 82.5 MB (82530689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fbdcfc8072c0f1ee43cb55b3687c3d3b200dffab792575fe5369fd3a4817af`  
		Last Modified: Mon, 29 Sep 2025 17:58:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:400000afd71aaff89aee7b6179dc03704c9cdc10cc098c0da5b223437732998c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 KB (216583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ea29f3586cc3cb5c4264cfef90610e4eb522cb01d5dd2dce989c2a0d0571b1`

```dockerfile
```

-	Layers:
	-	`sha256:3d3b1dd991c0a00d8c27ec2ae63d86edd349757f69961167b9f2ea1bce1d09bf`  
		Last Modified: Mon, 29 Sep 2025 20:24:13 GMT  
		Size: 191.5 KB (191488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e3fe52c5b5bca6a6a27026a3b0143a276b8d7e209479fbab5b8a405c47b295`  
		Last Modified: Mon, 29 Sep 2025 20:24:14 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:0a5a6fe20639ca2cf3d186165dc4c22f65463072cdd41dea92afcb3b3c97b1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85219982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c2863b799fce07ed17aecde2878f99aad5cdbf844947308584c9f366c44317`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a003c52fa58622cf3ddae9c19533da866be514592fe5de16b0ef909e8548ba7e`  
		Last Modified: Mon, 29 Sep 2025 18:30:35 GMT  
		Size: 285.1 KB (285121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4682e6be6673e7aa33301c5b30874cd778044246d060f0fbf3c29475651b8b`  
		Last Modified: Mon, 29 Sep 2025 18:07:23 GMT  
		Size: 81.2 MB (81207592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d243b7d4b6f363295fee98cdad3e62533ef80e745563cf2817c7c8296a85a80`  
		Last Modified: Mon, 29 Sep 2025 18:30:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:cd01fdeafb4ecaee480138601c1f00a96d1404b28736baaf7ea170e8cce60874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f16e7b60595454b0aa092ae1865812d4fd4be73d0e4e26d503d772dfe9fb92d`

```dockerfile
```

-	Layers:
	-	`sha256:e736a6bc52dbd64551da042d2310ee6e3b122f6f6f743275ee069b56c98a6e9c`  
		Last Modified: Mon, 29 Sep 2025 20:24:17 GMT  
		Size: 189.6 KB (189624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37bfb3b57ec6a675e660c1e29f2267711d09a2b00d37a1841723d3cf42b3b75d`  
		Last Modified: Mon, 29 Sep 2025 20:24:18 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:4881680ed63646c658df7787abf03905c69b7cea20971e956b0d1dfb0578dc38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85269828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb911aef8e990b8caebb47cacb31599c147d31959f3218dcf4e1d370602cc21`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 05:23:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e09396f9703679f1457da8ea8533cdf5f2a459c8f9efa4664152e578880b25`  
		Last Modified: Mon, 21 Jul 2025 22:46:21 GMT  
		Size: 282.8 KB (282780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b0814080f4bcc7029d120247499c8b748338b4c710ed5c01c0356e2b757363`  
		Last Modified: Mon, 22 Sep 2025 22:59:29 GMT  
		Size: 81.5 MB (81474090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3019637fdbce8b5a8531a2c41341c03ed7a9556802342266d2d2e437f33c63c1`  
		Last Modified: Mon, 22 Sep 2025 23:36:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f1e79333fea913c1f566c702569e2af0f85eacfc2a1b8d644234a23f8b6d6558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8247869864995ea358fd6d474d5ead9537c2391a2ee910a60f15a868ec5c807c`

```dockerfile
```

-	Layers:
	-	`sha256:3a1fc4d16a600ca790202b45cba1b5616ab6ecfc0b39457269a480aa48144706`  
		Last Modified: Tue, 23 Sep 2025 02:23:33 GMT  
		Size: 189.6 KB (189620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeece5907e605f64ce34d3cafdeec701ea24d3997728bf06a5d0b1549eda2c67`  
		Last Modified: Tue, 23 Sep 2025 02:23:34 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:63bd08cb1a181a22be80edb5a31dca6a437247865a5f97d55909d2421ace9601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86366603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9028f8cd719341c1713f380776228cd320caa2f690dfb30804931db547fc7eea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025c42582583c2dfb029e4963b25762b66e1e377bf0249a918da8af3d551043e`  
		Last Modified: Mon, 29 Sep 2025 18:30:05 GMT  
		Size: 283.5 KB (283472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ed6e6981e4c029c9853a9bbba242bc2c9b41f236141c1f10c1334ce58549f0`  
		Last Modified: Mon, 29 Sep 2025 18:05:39 GMT  
		Size: 82.4 MB (82438002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2281e9b318baf228a230a56ebf7e1026e38e9b6ae22f68ee9ee95fc8025c0d`  
		Last Modified: Mon, 29 Sep 2025 18:30:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:88c3281a0af6c65cd2da7a83e407fd2afe2c55f2151582f9b56c692d98a37685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 KB (214714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd90cc7c21a7b89a07270c05b8df18a52c34dbfadb12fe6a06e343551c353048`

```dockerfile
```

-	Layers:
	-	`sha256:abe7c7621e22314f8e6b65881a1072909f277a3b81a2028c1462b3f2401fe2cb`  
		Last Modified: Mon, 29 Sep 2025 20:24:21 GMT  
		Size: 189.6 KB (189576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0829db64799640191b66c9c63df16ef064d6b759d5f418d21f510d1219d7d7e3`  
		Last Modified: Mon, 29 Sep 2025 20:24:22 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json
