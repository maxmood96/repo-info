## `golang:tip-alpine`

```console
$ docker pull golang@sha256:7ffe86a8ccd53e73efc6c8f05b0a1a1e2e3558cafe559ecfd3c00cc052606945
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
$ docker pull golang@sha256:c2c043d8bb38a3bcb14f4ce78c8421a66f6708e4bb5af84dfb9aba34d6e77807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130794636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6a8d5797723fc5a6fd89e9f8c24c950fe3a459a86da9963af87fd87a0be65a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5713e045d5831de7a40a4e278b2d55c5d4d18e2caf4c3e8bb5b79c205bbe119`  
		Last Modified: Mon, 21 Apr 2025 22:37:12 GMT  
		Size: 294.9 KB (294908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25d4babeaf90344f4555f59166692dee6d066349b1a2f5cb41fc36591cc0aa6`  
		Last Modified: Mon, 21 Apr 2025 22:37:14 GMT  
		Size: 126.9 MB (126857323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cc2396e1bc194eaee5244a7b164c71f1ece7c47623e4d148a7e72bae0a6305`  
		Last Modified: Mon, 21 Apr 2025 22:37:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c292cb6070793a4553968bbe380a8e068f13d1ea6d51894677ca0d9bee90fe1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 KB (236941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12db9d343f607812d57811382066c496747152312292c4cf82d0c90c3e80814e`

```dockerfile
```

-	Layers:
	-	`sha256:01f8e4b90ad44996779a71066c2c89062aa7b67e5d3b8b54888e3c23175dcfed`  
		Last Modified: Mon, 21 Apr 2025 22:37:12 GMT  
		Size: 211.8 KB (211799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cfd34c7e78a7bd145feb06ac9c770abbac0cffa3781ea45eebb2fcdf884ebec`  
		Last Modified: Mon, 21 Apr 2025 22:37:11 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:39ec63943e7b8e5e776a5951a61b84c248082d1bbaa0f8fd881a11d9ef27dc6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125903098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddded95fca02d2038ae06409dd024787d7fa9d9c405fe5c182ab585102a1912`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:09:20 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7bf435709d1c27794da4aa58bbf1c4a90e82ff2338f06023036bd847c51bc`  
		Last Modified: Mon, 21 Apr 2025 22:36:52 GMT  
		Size: 122.2 MB (122241957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f92641ca33d600d20c6c4ddefa7ed5fd77ebf74e63eab906d908ebbdf3aadb`  
		Last Modified: Mon, 21 Apr 2025 22:36:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:559fd9fe1db3adfefa9176dd8e534567a0dcd570ce116690ee117a87a06c8e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1578aee7d442256c1f939576436657b19e7466985f6a27b1ffc09fdadbdb717e`

```dockerfile
```

-	Layers:
	-	`sha256:8ae1583b635707cce56ef259c6804a48d60263ba271952b9f1f75038cf5f0d7c`  
		Last Modified: Mon, 21 Apr 2025 22:36:49 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:79d7b9df7d2897b1a1971225d07b9397ce16c1c022b5e84c684a59e566002f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125293326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547d66631de2684cb65dc1ab1d79016bddb4cd30610cbb52d493765c659b8b24`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 21:47:46 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5cc54485761ae69a05b08a84359a87e39a46bace5d6d721b8ddc84655c07c3`  
		Last Modified: Mon, 21 Apr 2025 23:32:56 GMT  
		Size: 121.9 MB (121899846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8d7e7521df94daabe7501a4699d1e759aeced889be19afd68c5fc119af5336`  
		Last Modified: Mon, 21 Apr 2025 23:39:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c17b305ad9ba093381584c38e3e857205b23a830b2080bd98c0fb759f0eef8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 KB (237060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647c2fbe98e0a5833c24177eef76e947f85ba8db1e34619fa43913a3d8ed8163`

```dockerfile
```

-	Layers:
	-	`sha256:2a8717b2cff4d3b690d6af03335b1b7692ea03d9350a4219a7ca2850781f0854`  
		Last Modified: Mon, 21 Apr 2025 23:39:14 GMT  
		Size: 211.8 KB (211795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80d4553d9c2c4c130ecdd7bca934274fa2509cd123241b1c855558f1c38148ef`  
		Last Modified: Mon, 21 Apr 2025 23:39:14 GMT  
		Size: 25.3 KB (25265 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:0fa2a871a421b78a79bc6c8518fb98e33b213c9f27f3105f846559e1ad7ac105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123840396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a9989fa517f2fa126701f4485c087b261ff3bf27422dc2b34b80d03471dd22`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b785d572112487c9c64a58663acce46f9fb0896716bd7f1542c938cc5d7af07`  
		Last Modified: Mon, 14 Apr 2025 21:54:40 GMT  
		Size: 297.9 KB (297860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49c3c4d9fc32722fbee95cae35a84bb5c2c18fa016fa934c1de17d28a4bfa33`  
		Last Modified: Mon, 21 Apr 2025 23:29:01 GMT  
		Size: 119.5 MB (119549349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abec6860d06d448af01636870dc630a04d594155fdf78807a5bb8d51510c6b2`  
		Last Modified: Mon, 21 Apr 2025 23:33:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f5b7acef1065efc6fbe1506b6f4239fd6f2fd6979d7e3c99f31433aea4fef35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 KB (237157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8c055bcade8e70fb86c9610133104bf07310afa7c7d5f66cd76853ead26ab1`

```dockerfile
```

-	Layers:
	-	`sha256:5d260dbb3b9389d4a3553fc9d34a15b305e2dc69007a59596894dd6995b0d49d`  
		Last Modified: Mon, 21 Apr 2025 23:33:16 GMT  
		Size: 211.9 KB (211855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f85a6815dfe1979b681a32c9d240b952b4bb5db47f9b9dcbde14c7449b022a56`  
		Last Modified: Mon, 21 Apr 2025 23:33:16 GMT  
		Size: 25.3 KB (25302 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:db68ba764484040d1e901bc350d207f755a0279a8fb420840de85082ce6af3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128802872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c7ce95adf8fd56cc20dde74a4499fca0615390f3da0531b45428343b7b898e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689995964c02ae5829f0ebbc101aa49deaad9cc40bcfc7378d2d077f9e20f4d1`  
		Last Modified: Mon, 21 Apr 2025 22:37:41 GMT  
		Size: 295.6 KB (295614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22385500e9d61ec2b239f5d3bd81241409c720a3ebb2a4cf2d458346f64bcc50`  
		Last Modified: Mon, 21 Apr 2025 22:37:44 GMT  
		Size: 125.0 MB (125043477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c3deee176fdd208576023f85d8f57fa91553c0c4cc82e38dfdd1bc2d6b855`  
		Last Modified: Mon, 21 Apr 2025 22:37:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:93dd14298bbcdead0bddd049a4ff24f13a4e39dc948298fa162075be8f5c7da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 KB (236833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf42c8b05ca43e26b4bf6db300d56cf95860174d1a66adec83f31c672cfcb5b5`

```dockerfile
```

-	Layers:
	-	`sha256:cf95ba9138bf195b27c79f1416529201b52055187adc7099954daffa7e3b4c68`  
		Last Modified: Mon, 21 Apr 2025 22:37:41 GMT  
		Size: 211.7 KB (211734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6432774282d7c6795b2dd37112074ff2a80615cb8bbf066d66fe3029707b0f02`  
		Last Modified: Mon, 21 Apr 2025 22:37:41 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:fb48862c27f3e7bea59f9d934b2eee908f46290420b34a018a80588b0361d00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125557276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab2a5d78d974af83af32030ec76874bdb5826999a0f3c4ccadff2952aaf1f4f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c634d4cf55ec6e141d2ba75283fb1b12400db05f7be71416f24292b8f98daec`  
		Last Modified: Mon, 14 Apr 2025 21:55:29 GMT  
		Size: 298.3 KB (298278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffb73d167b954c764acdc0a85e569cafdf41ff90d8b4ea6c273076608592e7a`  
		Last Modified: Mon, 21 Apr 2025 23:41:09 GMT  
		Size: 121.7 MB (121684495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1518c20fedd79c094e8878853c20d6e8eaf4feb4868654fe966f5c098dadc2d`  
		Last Modified: Mon, 21 Apr 2025 23:44:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:3914f6ea465c102e52c1734c96d41502e35fb2f19987000c4ba8bfb2d07ca782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 KB (235122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b67fd4f59bfae6d3cd749f6f548b8eb12b45f9a031dcabfb48ad471be539b4`

```dockerfile
```

-	Layers:
	-	`sha256:f552f17fc17199a3b6a7352a94bc86c8332016c03ddf024efbeeebaf2503745b`  
		Last Modified: Mon, 21 Apr 2025 23:44:44 GMT  
		Size: 209.9 KB (209922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93f6ee6f56d1a68d7054096ba808c0e2fc89b10367df34cfdbc776380f12969f`  
		Last Modified: Mon, 21 Apr 2025 23:44:43 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:7639995b02eb54e3ac0595460d293a6f5f9dfc4f8d2fa016912aa4659f56ca15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125685489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b01fc166ef5cc5ffd7024dd7c14e0061cc8890b38dae0df70651ba91207c65`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 05:52:00 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb12bf697d577c42f53f652ba0fb4c4093c94ce6986095953e539f07ea9b28f`  
		Last Modified: Tue, 22 Apr 2025 00:14:55 GMT  
		Size: 122.0 MB (122038546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f502594edad3bc3b730630fea1e813153b0baf2fe1d4a78546af1fb4b05ff9`  
		Last Modified: Tue, 22 Apr 2025 00:14:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:0277d52d46e97705b490c4d3e34bdec18fed9f9f907eae6de7b4fbf01f04a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 KB (235118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869be5d8666a0813cb735a4135f047ed7d6d3047c177e719be020c0a580738ee`

```dockerfile
```

-	Layers:
	-	`sha256:b3d8658abf18c628794a1aaa59de3265a2b4a49c08476ae87a8aa308ba30869d`  
		Last Modified: Tue, 22 Apr 2025 00:14:38 GMT  
		Size: 209.9 KB (209918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b9c045045620224ff693adccc5c7f7159f989f6f04c59e098d628a96617d0f5`  
		Last Modified: Tue, 22 Apr 2025 00:14:38 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:75d3795d5fd7bd8e40d75dc355ecf1e333ba2c59f86b4aef60a1c11cc06900ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127885690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737d14eb3f97b48cae7c9096a79d0d6ff6a00e73a5f6a1a52f027059869d48ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eef4e818bae24bd18b41ddb9fab07f5996a42edf17784ae06c4953fb5f8fd4a`  
		Last Modified: Mon, 14 Apr 2025 21:55:41 GMT  
		Size: 296.2 KB (296189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221a3257b37adc23c0f99fc0f36d93743cedb18eca41076488eabc753a5b4701`  
		Last Modified: Mon, 21 Apr 2025 23:08:47 GMT  
		Size: 124.1 MB (124121776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45140448ec35edb302070dd4d3345c3a7426f0480cd8167c4c4c8d05dd035b2`  
		Last Modified: Mon, 21 Apr 2025 23:11:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:2900bb9d3ac78dcf1146dc12af1e3a64f9e009e7f30a7d447da8cdc9b72c2784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (234990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbe5a4c085f8b3ebb1baa76769f52f48800c2358c09ece40318fa81bfb21f0f`

```dockerfile
```

-	Layers:
	-	`sha256:ab081a2f90ea53e3964dc2b06b782b440602fd03e317cdf20c1dbb3a5e0657a9`  
		Last Modified: Mon, 21 Apr 2025 23:11:42 GMT  
		Size: 209.8 KB (209848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7053d44d8cf7fdaa1bd9501ad745b19d1f1d32eb1edc70c36f6c4ab0517de0bb`  
		Last Modified: Mon, 21 Apr 2025 23:11:42 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json
