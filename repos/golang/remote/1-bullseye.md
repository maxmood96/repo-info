## `golang:1-bullseye`

```console
$ docker pull golang@sha256:48ac5022f9740543cac0eba41a4e37b721073a0103349e416678e0142a53b49a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:1-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:350907316d2e2d0df6be33e65859e41d18123bafc832b279abf45e553b9b5f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285547082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4c8b5c4ad308991be5980398bafe6801e7b64c9fe7f54b688a192baa4f72a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Oct 2024 17:43:12 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Tue, 01 Oct 2024 17:43:12 GMT
CMD ["bash"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06817e07ed0f03c17ad0a7aa8ef22b2a6fcf2b939d6212ab0861571ef18a45b`  
		Last Modified: Thu, 17 Oct 2024 01:10:51 GMT  
		Size: 15.8 MB (15764889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2173ffc78585eeabe33105e00a7be99b0cad17d5e6edebf7f760d7824fa76969`  
		Last Modified: Thu, 17 Oct 2024 01:11:06 GMT  
		Size: 54.7 MB (54723650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4403a37342b449bf426c7f4be7ee1d4985afe0f247434f3c6f7a3a8b035c61`  
		Last Modified: Thu, 17 Oct 2024 02:54:38 GMT  
		Size: 86.0 MB (85971392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac1f1163629431c9f488c4d6ff6afb5c73021839723b50bafe245663ad3d9df`  
		Last Modified: Tue, 01 Oct 2024 22:18:51 GMT  
		Size: 74.0 MB (74006382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ef78c048549e8324e79737fec6e5a323293ea25c59b9926e6a25c916c39e31`  
		Last Modified: Thu, 17 Oct 2024 02:54:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:b711b352ac0652dee56b04687621293497542bfe165795a28dadf1240b22de1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061205b2dca3b99dac530586864f2a2e42d752771aee6807bf049bf860e27c9e`

```dockerfile
```

-	Layers:
	-	`sha256:12f402d09e8701cf20318b71609d269bda57051bc6371777104004928b9c44ae`  
		Last Modified: Thu, 17 Oct 2024 02:54:37 GMT  
		Size: 10.3 MB (10256502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a4aa3c4e60aefaba6e5b0d1d452d5218f6c8df6c0768037382687fe4c699c6f`  
		Last Modified: Thu, 17 Oct 2024 02:54:37 GMT  
		Size: 26.4 KB (26387 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:ae524f92dd59c4f10146fbdf2031aac55c913c086ce47f31fcc69697f3783614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252794656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b4d5917c729584e4872fb3a81abd0fd56b8bd1e7e74734ebab9dbe810853a5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Oct 2024 17:43:12 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Tue, 01 Oct 2024 17:43:12 GMT
CMD ["bash"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59299672bdf285da5ac04bba51bc8d7065d56d84dc91659b563a337a1ef7326`  
		Last Modified: Thu, 17 Oct 2024 03:38:03 GMT  
		Size: 14.9 MB (14880063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39efe447d42646f3185dd530992915f4ee5284d42835f09c0a8c04ba06ba134`  
		Last Modified: Thu, 17 Oct 2024 03:38:18 GMT  
		Size: 50.6 MB (50618781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801a5c06e432e106bb520490b3d4c98dbb729cea570c6495f5f07fe3b0d08be4`  
		Last Modified: Thu, 17 Oct 2024 13:16:43 GMT  
		Size: 64.9 MB (64892674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda832285c268d03f9079f25d645da4f232d333a236aca4f5406f4294d01f183`  
		Last Modified: Tue, 01 Oct 2024 22:22:37 GMT  
		Size: 72.2 MB (72161385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d57ec9543fcd77bb29bf2857b0b52daa69307f3a48bc17669f4b96ed6ec093`  
		Last Modified: Thu, 17 Oct 2024 13:16:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:7ce22e575c799a7cca2f47735b93da0cdf2a91bc38984793d8981c536a78ba71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10089535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5273c549894f8fb394c0c76175e716621e4645d091b29d67601bf6a67468ebb5`

```dockerfile
```

-	Layers:
	-	`sha256:57abc6b5bc6b0172fe329b3a6566a373fb83334625100512668188ccf288fe7c`  
		Last Modified: Thu, 17 Oct 2024 13:16:41 GMT  
		Size: 10.1 MB (10063052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f914d29b6bdf693697cbac1c7e5c92cb524ce2771da28fb472538e6ef1a39d41`  
		Last Modified: Thu, 17 Oct 2024 13:16:41 GMT  
		Size: 26.5 KB (26483 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:4c48b45eb935b2460736058b2c8a2b55d4c4f749e0741adc0861706e9bbd3b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276346371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b57c9c3b9580e0da229b5c5906974de0c26be5b38dcfb20a90315f785c23e8c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Oct 2024 17:43:12 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Tue, 01 Oct 2024 17:43:12 GMT
CMD ["bash"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181aac8447b7f0be083cdefe7039dafbc9a5e8c0a2c94de7b46d053e538a50d8`  
		Last Modified: Thu, 17 Oct 2024 04:37:01 GMT  
		Size: 15.8 MB (15750225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0134077e35514883cdc89f46185c7eae106a74a0895bfbc1494fdde44310f977`  
		Last Modified: Thu, 17 Oct 2024 04:37:14 GMT  
		Size: 54.8 MB (54834752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7d91c2012f9b7969c22d2713c9dfe2c38481b03f3ecdb922b2d945a63c70c7`  
		Last Modified: Thu, 17 Oct 2024 12:31:01 GMT  
		Size: 81.4 MB (81382208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37a00ec5f007d0ae73647c82b7d81d98a44fb7d073d06e633d656bca79db62a`  
		Last Modified: Tue, 01 Oct 2024 22:22:17 GMT  
		Size: 70.6 MB (70644133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2fb88848010f2cfffdb1323dd24c5b70d1eef2e8a13fa38817c83c50e25d0f`  
		Last Modified: Thu, 17 Oct 2024 12:30:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:a0cb596cff9b70f6846cc416115bdf5ca44db81e6b6c9ba14dce275db7f7bc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10284720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df418857d3e5d1ac7059c0e23a708511cafca50188bcd93adec745cbc81cf4a`

```dockerfile
```

-	Layers:
	-	`sha256:8f80aadd65e96c29d32706928eb69702999d96549e57975ab175662b2847f6a2`  
		Last Modified: Thu, 17 Oct 2024 12:30:59 GMT  
		Size: 10.3 MB (10258206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ee22ac20892fa16d30a969fd766881389fde7ced1c177a66fb0e2b60b4c9f9`  
		Last Modified: Thu, 17 Oct 2024 12:30:58 GMT  
		Size: 26.5 KB (26514 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; 386

```console
$ docker pull golang@sha256:d6a6e419e95f8718b5cc347114c060ab98c0a3f208854fdab145c4b845058069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 MB (287656495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ac8f83b1a2f119d041d80877160093c6aba471cdbb23910fef2a588d1c2650`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Oct 2024 17:43:12 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Tue, 01 Oct 2024 17:43:12 GMT
CMD ["bash"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000ce4e381f50a8f76ae5a1d4bcd9702f5146bac4fb30afc4e12c284ee68ca9`  
		Last Modified: Thu, 17 Oct 2024 01:10:55 GMT  
		Size: 16.3 MB (16268542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d0b1f51e6e34773cde9f3b41201942ff88384d907912b25ff3349f296f69b8`  
		Last Modified: Thu, 17 Oct 2024 01:11:14 GMT  
		Size: 56.0 MB (56032019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad1d4368ca12d220e98ddbf34cc81c7497427a4c6172515b17c27c50b254c9e`  
		Last Modified: Thu, 17 Oct 2024 02:54:46 GMT  
		Size: 87.4 MB (87397740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d4de23fe72666a7f8131049dc36e9aa2ba3bb48644c246b44b0b9d60e95bfa`  
		Last Modified: Tue, 01 Oct 2024 22:19:00 GMT  
		Size: 71.9 MB (71880213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54977882034de142d84c1586911f44f4e74be9ba9456809d721060a8161540f`  
		Last Modified: Thu, 17 Oct 2024 02:54:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:738e0e696b3c8cb06182a49c077b05a03fcdb24aa0438c182b4d054cdb2d9d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10272854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ab49b4d4a069c1f95bfe09797901b0e4b931242b1160f12f819aac0ceaba45`

```dockerfile
```

-	Layers:
	-	`sha256:122e4cfe53acb97ae103edde5402ec69cc53647dc9b48e7a9efc3a41ea1fd52d`  
		Last Modified: Thu, 17 Oct 2024 02:54:44 GMT  
		Size: 10.2 MB (10246500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f8ab2c5d580151e2fe8eb2849179d121bc80d877409eac43e4542137dda7f04`  
		Last Modified: Thu, 17 Oct 2024 02:54:44 GMT  
		Size: 26.4 KB (26354 bytes)  
		MIME: application/vnd.in-toto+json
