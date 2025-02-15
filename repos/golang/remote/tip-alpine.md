## `golang:tip-alpine`

```console
$ docker pull golang@sha256:c96e03b9853f6066bead754b08260d9b4780dc4778056f4c1dbe67c733fcdc4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-alpine` - linux; amd64

```console
$ docker pull golang@sha256:c37fa528940246a4e1cad5b4e5d34b7c5f63a18777fac16e113d38d86bab7b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133153835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45031175300b28967283d4e7328663f8f60c2e52c2fef1fd3bd03002cd9ae169`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Feb 2025 00:08:35 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 00:08:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289168b4f9dab2dca22882dbf2ff9aa4b5a522094cd6cac7c00fb7bb7eb8e3a3`  
		Last Modified: Sat, 15 Feb 2025 03:39:45 GMT  
		Size: 294.9 KB (294895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f767e601eda3139d3a2c86388748ee052ac66ea4515fdb8e54673dc9e44217`  
		Last Modified: Sat, 15 Feb 2025 03:10:47 GMT  
		Size: 129.2 MB (129216535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fad34f0568e7834028ed9f1277b3f8659ece3a27650e6b7e9acd3563b663b1`  
		Last Modified: Sat, 15 Feb 2025 03:39:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:27fc183ad2306328153705653fce4e5fc2e7aa9e56fc76972473d07095afda85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 KB (239653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34195361fa45d86b5c0db77d6b48ae2e8bcf198f27ac0fcad1bd53c0931ad9a0`

```dockerfile
```

-	Layers:
	-	`sha256:be1034ae7b34da83591a676108b33afaa064bbb20dc8dae27f1fd6b6be4184e7`  
		Last Modified: Sat, 15 Feb 2025 03:23:28 GMT  
		Size: 214.5 KB (214512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d196b89e538d6e4c218bdc85fb5c548ae23324fa28c0a4cbdb6e824d47fbdd1e`  
		Last Modified: Sat, 15 Feb 2025 03:23:28 GMT  
		Size: 25.1 KB (25141 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:8fd3e338d433686fac99643d441ce941e2d7c95261cdabc600a5f6e2a105dd63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126510205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fb3ad9dea5e3f46c2a4cb9a34dfe28c1e8a2ad26aeeca46c551e7c5a5e5f4e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Feb 2025 00:08:35 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 00:08:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:39:12 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f291b9756e2dcaffb7e4bbfc7c8aac860e0029f9218115d59b61d6d6c865b5a5`  
		Last Modified: Sat, 15 Feb 2025 10:10:14 GMT  
		Size: 122.8 MB (122849064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4e47d2a0674c0e34ee5327865a5f55e1e25e5e6331303f4fff747d13825206`  
		Last Modified: Sat, 15 Feb 2025 12:23:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7d1ddcb1123d1433d486a4de1e193202aa4b9f4271268c27cc9fc92851e02410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c4cb24bcdd669eda2485b227c6679db39def8dc1bea1f22de99483b14be51a`

```dockerfile
```

-	Layers:
	-	`sha256:ba4c3019b8d39fa97c51a9125a257aab31aaa2e1c0b2857c20f1ca57918d7152`  
		Last Modified: Sat, 15 Feb 2025 12:23:22 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e5978ae09b50154f2dd7f33e1f646127f4ea057d6e7e9468d60b5283c744ecdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127149944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe68914acbd2b7cfb60832f99b7dc1be427b0acb59dbd3a668660b8db0387e6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Feb 2025 00:08:35 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 00:08:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14aa1d43e92f86dc074668d0ee29a76fd40e91e4c4142a8f0580170417c1a1e6`  
		Last Modified: Sat, 15 Feb 2025 00:23:39 GMT  
		Size: 297.8 KB (297842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905748308911592ab8dd35e81623d80a35a86c1f573f4146926a93bafbba078d`  
		Last Modified: Sat, 15 Feb 2025 09:11:49 GMT  
		Size: 122.9 MB (122858916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94ef8f39a4be074a3348375a5685de8d305ea7c85b7ea6a594f77cdc8e5ffe1`  
		Last Modified: Sat, 15 Feb 2025 11:27:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:cd111522bfb5c3b4e24730c6580625b910df58c5ebcdb2252ca1d02eb71117ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 KB (239870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2be8620f4d2006cae6ff682036cd22a9eb8eb98c8f868c6567572a096d8621f`

```dockerfile
```

-	Layers:
	-	`sha256:ebe68a0ff66cc4efcd7029efd56ec0106f0d9a52b0ebc66f6fcfeaaaa0090df1`  
		Last Modified: Sat, 15 Feb 2025 09:23:25 GMT  
		Size: 214.6 KB (214568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37cee31fc4c881f806ce585bca49ee4a775986dc4dcb2f59926df9b38607027`  
		Last Modified: Sat, 15 Feb 2025 09:23:26 GMT  
		Size: 25.3 KB (25302 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:4dea40c3b9cc773dc567e2e3f52b8cb1c0cc066a62b8fa1eaa83a4d06f8317c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129632185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8b1604c0b4d29e92d5d24d3e4979fdac57e560dac41c64facd8c2cf3802987`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Feb 2025 00:08:35 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 00:08:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768692b15ecb1d86a668a395cd89a2ce7a4fa2eeea3aa4db3247b600602b8654`  
		Last Modified: Sat, 15 Feb 2025 03:44:45 GMT  
		Size: 295.6 KB (295584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b2ede4bc0ff1c223f32b8ba810862b4e27669e273d5c1e6c5993b5698ec335`  
		Last Modified: Sat, 15 Feb 2025 03:10:29 GMT  
		Size: 125.9 MB (125872820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46356f11fda3c4641a4839d39ee9df20c3504259c46a9351bbf37ecb37cc5ec2`  
		Last Modified: Sat, 15 Feb 2025 03:44:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:56e3a32447a47cd4d3ce5b47e37fcbd6e777f56d8f1cba30ef474fac9dcc1bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 KB (239546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8580ec20e2d42b69a72a3bc3bdb0fdc52ed5735ef4a8eda4b68c06df5cf229fc`

```dockerfile
```

-	Layers:
	-	`sha256:1857c277db14b5f1811885189cd7871c72a1231f86939c352fe01d3ef172f08a`  
		Last Modified: Sat, 15 Feb 2025 03:23:29 GMT  
		Size: 214.4 KB (214447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfec0b89b321620ee5048b5934cf1db911ebac3f907b76bc8fad8e4407996c64`  
		Last Modified: Sat, 15 Feb 2025 03:23:30 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:51bed8c5f71b1cb799d3e7671b442b88fbd4298679e70014d85e7a5d911b3e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128252565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7752bcc5349bffcd0bc357817bfad9a6342b0754bce17b3ab0b447ee0f9c408d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Feb 2025 00:08:35 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 00:08:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542036b0f90df8875e93add192346f3bcc8edd586aa34c11a6af80938cb06173`  
		Last Modified: Sat, 15 Feb 2025 00:31:41 GMT  
		Size: 298.3 KB (298267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f05ebd2cfc5d58a8a74d541592f939ce44409deeab829fb1fdead8865b10f81`  
		Last Modified: Sat, 15 Feb 2025 06:09:44 GMT  
		Size: 124.4 MB (124379795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659da44074f6c24f883d02cd2182ef96bcb63032628eff4a49a09518747fd96c`  
		Last Modified: Sat, 15 Feb 2025 09:15:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:b5b409107c8ede16981ca323611d7ea474d7e43a6ac4ad7da17fc9fbc14cd0ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 KB (237835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b65dc9f174cdfd84fecb293200458ea6f3d18a4fb699fdd4e5becd9ddddfd7`

```dockerfile
```

-	Layers:
	-	`sha256:43d2ff04c09d9db47209e65f5961671db77e3aac3ee7c0ca6fb989e083e56bf0`  
		Last Modified: Sat, 15 Feb 2025 06:23:19 GMT  
		Size: 212.6 KB (212635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f04be0c7c7f6552b31ac09bea17f8c3483f8293845a9ad7c6be31e9056b03d53`  
		Last Modified: Sat, 15 Feb 2025 06:23:19 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:e5cb9a583068c87888381937eded5473bc9b44e2f217d7a6345dd27d2446f232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130443865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a28850710272d0a34d5d33d67e420fe52db96574bb07d4f64d09442050df704`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Feb 2025 00:08:35 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 00:08:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45367ec7901486a744e83b8e8c40908894d960175ae2dea51903497a09542717`  
		Last Modified: Sat, 15 Feb 2025 00:31:43 GMT  
		Size: 296.2 KB (296178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f67487422a2fca86e0ab6fdcaa52aa1779b4a197c62c15e515f5ca0841f8f9a`  
		Last Modified: Sat, 15 Feb 2025 08:10:19 GMT  
		Size: 126.7 MB (126679962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5042ee976901cc47affa075ccc293944462bfd654bde471a426f90ebd81db1c9`  
		Last Modified: Sat, 15 Feb 2025 11:27:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:2112f281f8efa056c1050610d5a74cee47b9ceb25f47a988af2ee39467177efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 KB (237703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895a692376c491553af588b8841ee424f46d88d568ab1a571cd973a3d55fb1fa`

```dockerfile
```

-	Layers:
	-	`sha256:007f7445e9d319a40cfecdd14eccd731064be496e34503a408763a1d9b26a07c`  
		Last Modified: Sat, 15 Feb 2025 09:23:29 GMT  
		Size: 212.6 KB (212561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e6bb989840cb79373c87a84fc9e05d45276b5e51071014cbed18fd1d21723a2`  
		Last Modified: Sat, 15 Feb 2025 09:23:29 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json
