## `golang:1-bullseye`

```console
$ docker pull golang@sha256:ca1badcc20ee594a684d3617dac7f6ac15722ea5cdeb359189a675848c99a585
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
$ docker pull golang@sha256:37cfa6749a73a61d2c4083405035470491e0c0aca247c588b018b9d397b20b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 MB (253307792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5940357a447aef454e4cacb12cdd53a3c55389100386662ccbb8b26b269780f0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jun 2024 19:06:26 GMT
ADD file:2fd9c13efc7b13ca68928f53acc0c79d5841bd49e5aea46b2e1906120bba2a4f in / 
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
	-	`sha256:6c9f7b7d6baf92c8cec25b325ea14db33b8c298218a5bcd368bb24184c5645b6`  
		Last Modified: Thu, 13 Jun 2024 01:22:39 GMT  
		Size: 53.3 MB (53322503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f62fa3097190d71f8c07279b0414992956a17136d2040113e1f4910937c092`  
		Last Modified: Thu, 13 Jun 2024 02:39:25 GMT  
		Size: 15.5 MB (15530528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd553a7e4abf06bba101ca3a36c88140dd098954e94bafce76ee81b84c8c57ea`  
		Last Modified: Thu, 13 Jun 2024 02:40:14 GMT  
		Size: 53.3 MB (53313183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193e3f725d9c29c6f0c5604f85b1f2998ccc4bff75b657a3bc04578e7ca3a3c5`  
		Last Modified: Thu, 13 Jun 2024 23:13:12 GMT  
		Size: 67.0 MB (67026319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4e333f75cdf8d0faccff8152d9880003b584f6ce457e88161caf95ef6ba28e`  
		Last Modified: Thu, 13 Jun 2024 23:10:02 GMT  
		Size: 64.1 MB (64115100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822a8054e22ba2741330ac812fc2c802a747d1fae59fafe60a085bc88220b472`  
		Last Modified: Thu, 13 Jun 2024 23:13:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:9f25307b51e11ec5a5859f352583a8d16169322ac95fe0526793162199e3bed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 KB (24303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018ac5a1e87b6c64036d839e76fa299d3821d193e0f00248d61a1692cc00ffcd`

```dockerfile
```

-	Layers:
	-	`sha256:a8277bb78b3b7e61e7ec500b661f62de6a70b5b5b2c1eb5eacba217ec3951777`  
		Last Modified: Thu, 13 Jun 2024 23:13:05 GMT  
		Size: 24.3 KB (24303 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; ppc64le

```console
$ docker pull golang@sha256:e0d8345f730b11dfb7cdc358accaaad304a37d5d79af3cac6bb08e3c4418f7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281429963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0519bd2965aa1b9d848c7bff01ac15f0d213ff52d1c0b7065f247ebd2a484fd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jun 2024 19:06:26 GMT
ADD file:32733696002797fb377d3d8094c21c0f41f25da6f371eb4a8ecb6fa5c3ef1048 in / 
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
	-	`sha256:7afd12f588c414c122b8d3022d60effda2738a394347f5b3cbdebfe1420a8bf8`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 59.0 MB (58968957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918a353cdc3445173a18fe2f058dd7abb46fe3acfde05a65233cd1b979bd3d09`  
		Last Modified: Thu, 13 Jun 2024 02:01:07 GMT  
		Size: 16.8 MB (16766853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44a70314a2227a3d4a36c3baefe93d6e718bb4dd984f85adc8cb091a68f88b3`  
		Last Modified: Thu, 13 Jun 2024 02:01:25 GMT  
		Size: 58.9 MB (58874053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a19c01b7e1a02f4f1ed0311925772037de2bd368cdacbc8b87db481554f997e`  
		Last Modified: Fri, 14 Jun 2024 00:20:10 GMT  
		Size: 80.4 MB (80379103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236cbdc316b6a948ffe0177ed252011a6646360d0cbcf8cbfc819b8774160a29`  
		Last Modified: Tue, 04 Jun 2024 20:19:26 GMT  
		Size: 66.4 MB (66440839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0286200bb2227b16f8696e74fff047eec9f1495f6afdcb936f890e0e4cf8bbd`  
		Last Modified: Fri, 14 Jun 2024 00:20:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:ab8f3f6fc307fb2fa788b25a7af133ee1d35c38e15fa838a53767577e5a46abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 KB (24284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc699240eae55918b2bae0387ed4695dcd352fcfc2bb3502c7f97af48e9453b`

```dockerfile
```

-	Layers:
	-	`sha256:0d6727d1ae24b41c97e488b020bec53c20cc0012476ccacec338f67b5ac62354`  
		Last Modified: Fri, 14 Jun 2024 00:20:06 GMT  
		Size: 24.3 KB (24284 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; s390x

```console
$ docker pull golang@sha256:6aaa0cc3f457b268acc0f83038c1e4bd6c1fb8e50b2064e965bfa4b97f1d9baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257089302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef49239581a09ce46b6f33d434268bf7d0e2c1b0ff56fc74f60e6fb0222d05ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jun 2024 19:06:26 GMT
ADD file:1f0333c084fe60bf682ad64dd7db93b2ca069c7e1d09bf26e7e65dedbd65b0f3 in / 
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
	-	`sha256:db300ed0c60856815a390ef84dc7c5441283ec11483c9da25ac0daf34bac6e83`  
		Last Modified: Thu, 13 Jun 2024 00:47:59 GMT  
		Size: 53.3 MB (53337540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b507bf58c92373ad020c252404bcc63be7764e5ba99e1b46dbe95f2fb0d32531`  
		Last Modified: Thu, 13 Jun 2024 05:31:46 GMT  
		Size: 15.6 MB (15642492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3e3e4d728c88a0a3906e1d03b1ffe00d8ceb7ae7abbf81186d2f281bcbf540`  
		Last Modified: Thu, 13 Jun 2024 05:32:00 GMT  
		Size: 54.1 MB (54076476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d20e02a88b6a307c10bbe5bf5ffc34edb1c3f16a52899ee619525d63575f6e`  
		Last Modified: Fri, 14 Jun 2024 04:41:43 GMT  
		Size: 65.6 MB (65627387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fb824bc24fdc7f4fb089d47d141644e86949635714a893519e6ce56fa54e32`  
		Last Modified: Tue, 04 Jun 2024 20:22:15 GMT  
		Size: 68.4 MB (68405249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e64959716d56a588bf72a4ee8c2b01bacaed3653d6da2a2a8619b70d23333f0`  
		Last Modified: Fri, 14 Jun 2024 04:41:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:73a510e94ab6b5db1d06833f5aee73c89e0bc9279f80ca95ea5b48e6b5588ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 KB (24242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7c4d22aabd353bb6ba9bbacc37b543252d11576ca56b1f2e7077734c1fb6a6`

```dockerfile
```

-	Layers:
	-	`sha256:b6a0cab9094fbace378bbf1b9be5f0783495e56f1f0179d2ad0b88ed26678851`  
		Last Modified: Fri, 14 Jun 2024 04:41:42 GMT  
		Size: 24.2 KB (24242 bytes)  
		MIME: application/vnd.in-toto+json
