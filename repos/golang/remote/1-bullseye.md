## `golang:1-bullseye`

```console
$ docker pull golang@sha256:ad2f3e545901a9a0ca269088752f49c5b4974c89229fa951286a1fa8c5b2773b
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

### `golang:1-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:88841011b5b74c87aac78910b7f30124d3092efc3e31785def9f675fe25d7f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280726751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572b0a8902d89501026407519329673ca6ee998aa425129ad0b6a5a724b5e938`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jun 2024 19:06:26 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Tue, 04 Jun 2024 19:06:26 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065842589d7a62a96a08c1acc0bf9e7c0b5442f2770276be18328b755d1ffb99`  
		Last Modified: Thu, 13 Jun 2024 03:50:44 GMT  
		Size: 54.6 MB (54589356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f839669823b6f523bc6a2caa358e532a143a913fdb09f19348fd0abe79581a4`  
		Last Modified: Thu, 13 Jun 2024 18:15:06 GMT  
		Size: 85.9 MB (85927651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07eb097ec984f8c4edf1d2aecdf743590a7507dece360821699c4093f95aa79`  
		Last Modified: Thu, 13 Jun 2024 18:15:07 GMT  
		Size: 69.3 MB (69345561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a50161aa8005342d2196a84327cb9226497a6c090bfa81c8b95ce420a02230`  
		Last Modified: Thu, 13 Jun 2024 18:15:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:9b90537702b15b533fd072bff3128dd71db72296b7e128d827e379137b6d84ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 KB (24242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e566f5c75d211c43d7cfadc116a7f78577a8d665161c8b827d9368a461f3e7`

```dockerfile
```

-	Layers:
	-	`sha256:79f6df63d37d3e33e39fbcc1f994175757cdc81dc5e58eccd13b82ccc25f44cd`  
		Last Modified: Thu, 13 Jun 2024 18:15:05 GMT  
		Size: 24.2 KB (24242 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:33c56240c03857e657acfeb038daef65a6f89b3482dc70afebcaab866b5e9f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248055531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a344e837022d2e3de28e24f0eb3318464fed07d6e2102d5420bcf3e7d589461`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jun 2024 19:06:26 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
# Tue, 04 Jun 2024 19:06:26 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d823c90ec6db52ee3c5a3a116b21e47442be8c0e35cc53f6f7f4db398ba08fe`  
		Last Modified: Thu, 13 Jun 2024 01:34:16 GMT  
		Size: 14.9 MB (14880170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738fc6141957592e4d069a8fcb0615b3f6dd757c25ee58dd7023fb923a7a4ecc`  
		Last Modified: Thu, 13 Jun 2024 01:34:36 GMT  
		Size: 50.4 MB (50359459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9fd76866e79e0f83b42bb402be90dc5536247b1e0a57784080d7554e5e6019`  
		Last Modified: Thu, 13 Jun 2024 19:29:54 GMT  
		Size: 64.8 MB (64845923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f2d60982f3278ca26e0dd4a91fb30e80076051e36da023e58e47681cc2934e`  
		Last Modified: Tue, 04 Jun 2024 20:20:28 GMT  
		Size: 67.7 MB (67713391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3568392511b452f58ff4f46c71c9613f26c400d5a27097509e8f4ede8a255df`  
		Last Modified: Thu, 13 Jun 2024 19:29:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:467f0ce4d94255426da4faf59407ef4772494a3f4dc8d641c0367ad845e8f0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 KB (24338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43980bad919ccf11e2e1e284fadd90b60ce35c4a26e5bebc173701b4df4f78c7`

```dockerfile
```

-	Layers:
	-	`sha256:ec286a2c05a5d701a73ba1ee8b56b08a80976b9b22126af3807b70c8fe54c4aa`  
		Last Modified: Thu, 13 Jun 2024 19:29:51 GMT  
		Size: 24.3 KB (24338 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7cd2e4831229f4a833edf8592009382ba900c5686af049c3345be254747ea0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271793329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8cf9f58fcbfb8d7d0059359c53727400a31b96daccf9f265f2ee0be75e51ab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jun 2024 19:06:26 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Tue, 04 Jun 2024 19:06:26 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b5bb8f5d471015f3add7e778bc507fc4a6f1fce8561c2b0a336734a55a365`  
		Last Modified: Thu, 13 Jun 2024 01:31:15 GMT  
		Size: 15.8 MB (15750467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a7ca076c1ea04622ddf9f43ff2f138f6c50a40118747a45d2618cc64591d6b`  
		Last Modified: Thu, 13 Jun 2024 01:31:29 GMT  
		Size: 54.7 MB (54696375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448ed5a541ae38a34945925dddc0a33d5ba9f4a79c92e4e1804f739bdcf91e0e`  
		Last Modified: Thu, 13 Jun 2024 18:03:41 GMT  
		Size: 81.3 MB (81336338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c0d35bf3e901b1024e7abc65a8b1332e085c592b5bdd1d9422364771935e1e`  
		Last Modified: Tue, 04 Jun 2024 20:19:51 GMT  
		Size: 66.3 MB (66270410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cff45d7c2938a8bba4026408b5f756945830f912916508e390a95576980b086`  
		Last Modified: Thu, 13 Jun 2024 18:03:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:8be3229727e27b4072284b2de3d1327b6df4c1ce2db1d7f9d0615194b92e3839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 KB (24558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c419a53f75edd9b1b37f5705dadb2b12be9d08665b3fb9379d711b6246c186`

```dockerfile
```

-	Layers:
	-	`sha256:2735c2887afc18f2134ee4e00cd6c5a44e3a396b9a22768848ae65ec1661e6ad`  
		Last Modified: Thu, 13 Jun 2024 18:03:39 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; 386

```console
$ docker pull golang@sha256:2936a1d7662a96bf22dce41676c1bb2ac4d685557d15d3e91fd0ff4647498924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282970688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3941eb00dcdb8388648832da880d0b9c11e16880af6ad5c3272eb5b4974b01d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jun 2024 19:06:26 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Tue, 04 Jun 2024 19:06:26 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b98f88bb530423206e6a932f7a0f7e81cc72458b59be08bcec8aa0490df79e`  
		Last Modified: Thu, 13 Jun 2024 01:20:13 GMT  
		Size: 16.3 MB (16268880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4e6f3cca702057a7a6cdbd9b2d2f758e1d85524fdc9fc26824db70376bce11`  
		Last Modified: Thu, 13 Jun 2024 01:20:33 GMT  
		Size: 55.9 MB (55929392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32958c43fe0a0b20598e8ccfea43b859711a8781a969bd1e10202049f85a863`  
		Last Modified: Thu, 13 Jun 2024 01:59:20 GMT  
		Size: 87.4 MB (87351163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5884200f4042317ed37552318ef139be72505fade51964066b89ef55c8a84f2`  
		Last Modified: Thu, 13 Jun 2024 01:59:20 GMT  
		Size: 67.3 MB (67344557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00db2bce83bdd91e87dab649f94e7dcb1d548ffa3f0bd598237111a45afb3a0`  
		Last Modified: Thu, 13 Jun 2024 01:59:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:2b63634d78e4673edd613ee7632ccb537c32287fe1e14ea3a8147a871ea5e5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 KB (24209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e171aaa4ff30f7ac15287185d9b9f2bf6de13216d6b7f4ce46a185a4088dbb`

```dockerfile
```

-	Layers:
	-	`sha256:a330e10d988ba66ecdf5dfbcd2f5a8f367a06a44f275d5a186515fa45f67a7d3`  
		Last Modified: Thu, 13 Jun 2024 01:59:18 GMT  
		Size: 24.2 KB (24209 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; mips64le

```console
$ docker pull golang@sha256:8d0d475ef2cfc3e643a638765431f7a38177f56c4247ec9f5b36c512d92fe458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 MB (253306818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ab1de744afe67c562d562f5639429ecb8a98aaa014b7b2effe5c3141665fb9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:11:41 GMT
ADD file:21c5796082f318cf57901c774792fb836e16ed2e984bfd93de345b83005884b5 in / 
# Tue, 14 May 2024 01:11:48 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:08:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:10:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fc8239cb1934c4e9e9368d2009f62f73698f5ad0167ec8a7f5128c5b24848b49`  
		Last Modified: Tue, 14 May 2024 01:23:03 GMT  
		Size: 53.3 MB (53322052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae485d7e63e18bea6220a5c2d4a706379e1cf701af08f3d2bc40119bd3dd7ae5`  
		Last Modified: Tue, 14 May 2024 11:40:25 GMT  
		Size: 15.5 MB (15530346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b7741bff2a58b71ac6371e1fbf6f9dcb366c82fb6243829c330c2a13b5037`  
		Last Modified: Tue, 14 May 2024 11:41:09 GMT  
		Size: 53.3 MB (53312597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2e80da688fec7e0edcd71c8c6b09d3f6725926d2793b140f04730c604a146c`  
		Last Modified: Tue, 04 Jun 2024 20:26:13 GMT  
		Size: 67.0 MB (67026546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151c71941cdaac9c029c10e5d752fec37cd8e6bc5fe2e3c8b92f03773b8bdfa1`  
		Last Modified: Tue, 04 Jun 2024 20:22:40 GMT  
		Size: 64.1 MB (64115119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a37f5812be036782d0e27a92acb11cc8d9bb02f3afa56a3b787b7af089ff1b`  
		Last Modified: Tue, 04 Jun 2024 20:26:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:653cd75dc05faef894411e03c759bc4bc6cdeab8229396925196e2b6ef4864d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 KB (24256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3924d08499fab65bbe1d07b288059a61c4386611bdacb241d73c501934d4508`

```dockerfile
```

-	Layers:
	-	`sha256:e6a706f5ba9fb26cc8e223c306033eb21036672c9a9b6fd74b1a9f508b6ce4cf`  
		Last Modified: Tue, 04 Jun 2024 20:26:06 GMT  
		Size: 24.3 KB (24256 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; ppc64le

```console
$ docker pull golang@sha256:623bb25ace2b71c9e7b9fad3bea315a6f245b2f1d7d08e206fa29d826e57440b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281430189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbab2de9b31b777c6a172cbfbf9c80d62a7b8afceb9092a8f573a5a3769876a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:20:13 GMT
ADD file:4b54ed39e81b5ea585c47d145304cf7a54b08e7b1ac284a533f59d1a4768da9b in / 
# Tue, 14 May 2024 01:20:15 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:58:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d13e42d2790e01b63e6e5f051b276a525e360366071e8144b80a7a814c950f7a`  
		Last Modified: Tue, 14 May 2024 01:24:27 GMT  
		Size: 59.0 MB (58969434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fe3151b57b060a2fe0ca52c8936b461c9e0545bc85c0c2eb5f57ea98c7a94a`  
		Last Modified: Tue, 14 May 2024 07:11:41 GMT  
		Size: 16.8 MB (16766925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435512f1cbc8e07bb0a635d32fa068bcf448922bef667d36de93d14ae1a1efaf`  
		Last Modified: Tue, 14 May 2024 07:12:00 GMT  
		Size: 58.9 MB (58873785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d9ce51ce89f01c2199211ec8cabb9e159ed1bcb3302d50bb57b7741f942aad`  
		Last Modified: Tue, 04 Jun 2024 20:21:43 GMT  
		Size: 80.4 MB (80379049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236cbdc316b6a948ffe0177ed252011a6646360d0cbcf8cbfc819b8774160a29`  
		Last Modified: Tue, 04 Jun 2024 20:19:26 GMT  
		Size: 66.4 MB (66440839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec89a7ea705862508c083dc8706bb2ce5a3269fea1744c6b60b8c9dfaadabc4`  
		Last Modified: Tue, 04 Jun 2024 20:21:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:7e04122d15988533fc293b603052203acfa72e8ef2dd19dc96aa426b621a648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 KB (24235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a34b8f08202758c30fbe866f34fc3c38cdf65d9d34b979d71ad21e84549c5c`

```dockerfile
```

-	Layers:
	-	`sha256:0a868e2abb78e54760f647598d0183fafc3e4831d82352a18130e0f1980b8868`  
		Last Modified: Tue, 04 Jun 2024 20:21:41 GMT  
		Size: 24.2 KB (24235 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; s390x

```console
$ docker pull golang@sha256:97bbe44b30ce3fd42745f85aa17aa07e4a91733b16c2471435f0118b7f949667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257089685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602f877b2cd791d208bc2bec130f4cf582d2f5ea4c9c0f9b94a59426b443eaa3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:51 GMT
ADD file:a0baaba4b04b93c49efe9fdafcb2308d4f775370b8e2a926df265487484d9788 in / 
# Tue, 14 May 2024 00:42:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:43f368780ca3724d6cdfa64641264541097ebb1b158cd3e0439fbf1846f179e9`  
		Last Modified: Tue, 14 May 2024 00:47:50 GMT  
		Size: 53.3 MB (53337573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a81dfed6865ecaa40f3f43b4bd4c389449dd3e0fcdc04d95ffd4c8e09fa9cd`  
		Last Modified: Tue, 14 May 2024 01:30:16 GMT  
		Size: 15.6 MB (15642393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0bebc382626195b064b7bc5d045ae9224b0d8f3c00157347449a593b555471`  
		Last Modified: Tue, 14 May 2024 01:30:30 GMT  
		Size: 54.1 MB (54076843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a8499340a59a282f621b25fa7e6398d67bdbd606dfc84958167dfd818817ee`  
		Last Modified: Tue, 04 Jun 2024 20:24:15 GMT  
		Size: 65.6 MB (65627469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fb824bc24fdc7f4fb089d47d141644e86949635714a893519e6ce56fa54e32`  
		Last Modified: Tue, 04 Jun 2024 20:22:15 GMT  
		Size: 68.4 MB (68405249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754c81849f5b133832c34187e8c4fe62177ff6a724a82e221040e62bcf2a3404`  
		Last Modified: Tue, 04 Jun 2024 20:24:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:2c0795f75867376295d3c49bf97bf728638eb2b3829cfb691ac3d6c1a9a14581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 KB (24193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5a5ee843677fc30bee3d890338236c469b6e36990aee67c33a592d43a94cda`

```dockerfile
```

-	Layers:
	-	`sha256:fe4459177157fa982379c5bcb0c537b3cf2b133554bca5c90463854c2b76f958`  
		Last Modified: Tue, 04 Jun 2024 20:24:13 GMT  
		Size: 24.2 KB (24193 bytes)  
		MIME: application/vnd.in-toto+json
