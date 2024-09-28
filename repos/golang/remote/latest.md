## `golang:latest`

```console
$ docker pull golang@sha256:4f063a24d429510e512cc730c3330292ff49f3ade3ae79bda8f84a24fa25ecb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:31817d38d90894d73ce3fe3b7f01c5f213ac7e9681bf462d4ad65afa8e902c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304264834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8027d6b1a7f0702ed8a4174fd022be03f87e35c7a7fa00afb2bf4178b22080d4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Thu, 05 Sep 2024 16:50:05 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb015951d08f558e9805d427f6d30728b0cd94d5c9b9538cd4f7df57598664a`  
		Last Modified: Fri, 27 Sep 2024 06:06:31 GMT  
		Size: 92.3 MB (92260969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bff916ab0c126c9d943f0c481a905f402e00f206a89248f257ef90beaabbd8`  
		Last Modified: Thu, 05 Sep 2024 22:02:55 GMT  
		Size: 74.0 MB (74003284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d3574b34bd65a6cf89a80e5bd939574c7a9bd3efbaa4881292aaca16d3d0dc`  
		Last Modified: Fri, 27 Sep 2024 06:06:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:da57e9ee9aab3b78019d71896de2fdec69314e53b2328b6d4ddfdd4081cb2133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731837ea26eb6fc21983853bb4f53f9f312ce836e3d30cad24889a4d0cfc6106`

```dockerfile
```

-	Layers:
	-	`sha256:1966a16968678bbc63d1967f7c884bb69c10b7e561306ebf12ec444930d675aa`  
		Last Modified: Fri, 27 Sep 2024 06:06:29 GMT  
		Size: 10.3 MB (10266097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df5c888f3383fd386e834b650be1fb42628c580f3e2af3d1052cc8632654c0f3`  
		Last Modified: Fri, 27 Sep 2024 06:06:29 GMT  
		Size: 27.5 KB (27527 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:dbd86c2b98a95b8af47295b1c30bdd9836e1f8686e81a36bdd76d2fce985142d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (265004997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ca200a33dd2416191dc9079027128a3597d421ff29b3c3dae2f95c1b371316`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Thu, 05 Sep 2024 16:50:05 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d8069439bcb2f814251e906dcc07c3e02aa2c77623cc5603448c7e08e710ab`  
		Last Modified: Fri, 27 Sep 2024 07:38:54 GMT  
		Size: 59.6 MB (59639666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81438da5a2fa9a50ef48bcca0b787690bc1d2357f9bcfdf28c23fcdea5f8703a`  
		Last Modified: Fri, 27 Sep 2024 23:09:05 GMT  
		Size: 66.1 MB (66118259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfeb4cb216a5c9d7c74247031f4f727e785d2b0477ebee2ffd136b94b292ead`  
		Last Modified: Fri, 06 Sep 2024 05:24:37 GMT  
		Size: 72.1 MB (72141455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f292cf4185199c49cac0c85b7c7edc97553dd765d16a75c1f2d738f66e0d3ca1`  
		Last Modified: Fri, 27 Sep 2024 23:09:03 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:5d6d8a884b469297067936ee61c251910e238808d46304b039adc009e9960815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10102487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcacc30df67de0a66824bd75074da0655ac88ce77b653efb15c145df6ce1ff81`

```dockerfile
```

-	Layers:
	-	`sha256:ea2707f09381d9a2daa5513c8334040f922d508b5b81ef1ba3aafe53169d42bd`  
		Last Modified: Fri, 27 Sep 2024 23:09:04 GMT  
		Size: 10.1 MB (10074832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21bf1ee1d49e567335a1491d3b5375b76273d2307e033d7b8d792a716d24821b`  
		Last Modified: Fri, 27 Sep 2024 23:09:03 GMT  
		Size: 27.7 KB (27655 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:78df5ce03dec2202c06b2a63c3d4a93fd91fe53cfc7cbe62839ca1a349b51882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294447334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723e5b94e776fd1a0d4e9bb860400f02acbe62cdac487f114f5bd6303d76fbd9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Thu, 05 Sep 2024 16:50:05 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600c2555aee6a6bed84df8b8e456b2d705602757d42f5009a41b03abceff02f8`  
		Last Modified: Fri, 27 Sep 2024 14:29:36 GMT  
		Size: 86.3 MB (86293923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a355a3cac949bed5cda9c62103ceb0f004727cedcd2a17d7c9836aea1a452fda`  
		Last Modified: Thu, 05 Sep 2024 22:09:14 GMT  
		Size: 70.6 MB (70624628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6564e0d9b89ebe3e93013c7d7fbf4d560c5831ed61448167899654bf22c6dc59`  
		Last Modified: Fri, 27 Sep 2024 14:29:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:9b20aa388b99a9fc219eb3ca3e863b69db8bec0f147ee0592da3dae0bb013bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca7b6ff212dea346ea98a810a7d1e0cbf621b8018769ffcb23c8b8de283c747`

```dockerfile
```

-	Layers:
	-	`sha256:0e7bb2297d7aee04e322a83b360bbfa4892aca656c3f9a68cb10257f43f7b2a2`  
		Last Modified: Fri, 27 Sep 2024 14:29:34 GMT  
		Size: 10.3 MB (10294023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b09852188990c879d68804e6960eacfad83d1437c9a4dd5ab4d455d5cc64044`  
		Last Modified: Fri, 27 Sep 2024 14:29:33 GMT  
		Size: 27.9 KB (27891 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:c6bd30114843d5010f329d7bcc1fd1f110cb65b1ff57bdb82b4a7462aed8ce12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303197241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc387907cb81a8b5fcd1b33eb5f7e037b6bc7b8245c027c00f3fa3480b6e8cc5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Thu, 05 Sep 2024 16:50:05 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173ceeebced8e0220c3a89ff17a261e20756481c2ad65c5a4388bd4cfc63c575`  
		Last Modified: Fri, 27 Sep 2024 08:07:07 GMT  
		Size: 66.2 MB (66210942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6875fe8be31fdc328a532e234ad19719c3e43a6c3653e470dee26dbe9134e952`  
		Last Modified: Fri, 27 Sep 2024 08:59:01 GMT  
		Size: 89.7 MB (89657896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead5944571d35e19fa81ca655e6b7753cdb3e37418aa683e0c2a9c169e5d7256`  
		Last Modified: Thu, 05 Sep 2024 22:02:55 GMT  
		Size: 71.9 MB (71856183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ded643c60e89e16044604241821e6b053052f5e3b6c01d0f80209369cebc5ad`  
		Last Modified: Fri, 27 Sep 2024 08:58:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:c7cd068dcbc6e1c55c61d2772af8264a899bff5569b0b6e59b46fd622c5c2357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10273827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6145cf8d2a3e072460b744c7baf7629be212ac89e0807f51d90bc698a076661a`

```dockerfile
```

-	Layers:
	-	`sha256:4e8e56774dbe8ac2c885e8d920992dbc3d5fa03a003c7346fb2d0ce84b07c2d8`  
		Last Modified: Fri, 27 Sep 2024 08:58:58 GMT  
		Size: 10.2 MB (10246353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c212a06b6f955f9afc512bb6e83147af9afa7f755baea7287430f0797ead74a`  
		Last Modified: Fri, 27 Sep 2024 08:58:58 GMT  
		Size: 27.5 KB (27474 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; mips64le

```console
$ docker pull golang@sha256:fe4d24f57fd4a8eddd25bfaa7bd1489f5238f84ed6fd04445673930406b21527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274615915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e53b3e2ef8dc6b2db67221820bc8625543779234e3bd898ddea24656d4686c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:6f3430cc82064e0f2b15b01e40de05ae0823abf169e966aa55cc0c0ca4257c22 in / 
# Thu, 05 Sep 2024 16:50:05 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8e971619a39dae5a1330b75e3fc755af3e819283336ace59f4eb8cd8574c0ed6`  
		Last Modified: Fri, 27 Sep 2024 09:10:53 GMT  
		Size: 49.6 MB (49561615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44bb6c0f1b34dcdcd0b16bcd5637d2885844abedb2e641e353a1e5e633d9d40`  
		Last Modified: Fri, 27 Sep 2024 11:01:24 GMT  
		Size: 23.6 MB (23647347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e054123b78b936d75ee48cb51d153c75001aa8c7fee6cbc330793865d0faac`  
		Last Modified: Fri, 27 Sep 2024 11:02:17 GMT  
		Size: 63.3 MB (63297296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09472b71b92f7b91583d21acb979121251561ee59ae641004efb6f98dec68b2`  
		Last Modified: Sat, 28 Sep 2024 14:34:48 GMT  
		Size: 69.8 MB (69831737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f92ff5c1684aca058ae9537bdbaf5bafd344391c0d79677375775ca94fc2195`  
		Last Modified: Fri, 06 Sep 2024 01:28:00 GMT  
		Size: 68.3 MB (68277762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209e0115ce84c00be91e6d1a5e9c46ee77dd2c8e22496c9874f3a8b67d81fa51`  
		Last Modified: Sat, 28 Sep 2024 14:34:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:67d3c3f2b39a850068080f3a920d21faa55733e853655b0a0016651858ca4ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef81c6fbdb13dd3df0444556ccdda78b02120db06f38d151fcea96a2947cb9ec`

```dockerfile
```

-	Layers:
	-	`sha256:d0f0a31d80bdceaa255acbe999437c686943e34c2d709161e454021d38d88115`  
		Last Modified: Sat, 28 Sep 2024 14:34:41 GMT  
		Size: 27.4 KB (27406 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:168d146651f71728023d2a68c50915ccd1b55671a20abcac4402c15ff2d35e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310133776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620d77a86810823e232f427154daeb7d3ab754c1850689e2919f8dd9099ec231`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Thu, 05 Sep 2024 16:50:05 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97eb7cde179faa3a93bcdf596b7c5c5f95041da9780e3617267f455de14b8578`  
		Last Modified: Fri, 27 Sep 2024 19:42:17 GMT  
		Size: 90.2 MB (90239780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e5b8a4bec9158fc0bc52aa7bb2055ac421fd36de9ea98898a7188751ff7da1`  
		Last Modified: Thu, 05 Sep 2024 23:28:18 GMT  
		Size: 70.8 MB (70798979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327a53ea6b0494b9c12d73228cf534fa6d73a57a6b1d2b28586545735555dd00`  
		Last Modified: Fri, 27 Sep 2024 19:42:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:ce6c3640594b1345eaee01a7d2ab98f242544bdc472e668251c87432bb92287a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10266545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc11174e39f0bf63a710a310f541d53cce1db8d2e3bcc77dc229e98ba812881`

```dockerfile
```

-	Layers:
	-	`sha256:685b6898e17c4494edfb474f2e6bc563e6c0b5338ba37c5b5e6e1ae743e481eb`  
		Last Modified: Fri, 27 Sep 2024 19:42:15 GMT  
		Size: 10.2 MB (10238952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04fc8950506dbc1988d23bec69ef3d5bc7d9cf23067d1284475bdedb7c1d442f`  
		Last Modified: Fri, 27 Sep 2024 19:42:14 GMT  
		Size: 27.6 KB (27593 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:884a93ea840528ca231dfd5b43e8fd86a0394b9cdad8a486fc75e612936946d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277234263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3917ecd6b2876281000800bacbc31528312c7e33a1be2946aba9845711a88c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Thu, 05 Sep 2024 16:50:05 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c2ab927f160ed7c9e45e2262d1e5004e91be0fea253f83137dd350eacb8400`  
		Last Modified: Fri, 27 Sep 2024 12:56:06 GMT  
		Size: 68.8 MB (68828179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492964f2ae9970b6023102de0a48c54b43149da01ab6bb1b356e5cf44a9f6145`  
		Last Modified: Fri, 06 Sep 2024 03:36:46 GMT  
		Size: 72.9 MB (72920040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bcf50f186bd4791032a9b66a2d3d924a7458eb540dc761402dc91fca805588`  
		Last Modified: Fri, 27 Sep 2024 12:56:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:631cb639617bb55b6c54b72927c7c5b705f66d5c8c7823788a84b94e914e224f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10130023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c2683882bff4e24e6cbc05d3f67afed31be551b838df5777dfd904beea00f4`

```dockerfile
```

-	Layers:
	-	`sha256:2a43f72f0caae5903581fd472382ac484aa14ce46ea2a1c2b219b9ce4ebd3ada`  
		Last Modified: Fri, 27 Sep 2024 12:56:05 GMT  
		Size: 10.1 MB (10102496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d8627fc283e7831ecbf4b80ff10452c73e7f73f745d13f473f086fc250ef070`  
		Last Modified: Fri, 27 Sep 2024 12:56:05 GMT  
		Size: 27.5 KB (27527 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - windows version 10.0.20348.2700; amd64

```console
$ docker pull golang@sha256:5d5a07a31ab9dfd63886e061d350bdf794c3431137efe077fbd060d3abc5ca18
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1565299402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300435b66223816997abcfdb6f31d49e3830dacc240d7ae2415371a4a132f2b4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:01:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:01:13 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Sep 2024 00:01:14 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Sep 2024 00:01:14 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Sep 2024 00:01:15 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Sep 2024 00:01:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:01:31 GMT
ENV GOPATH=C:\go
# Wed, 11 Sep 2024 00:01:37 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 00:01:38 GMT
ENV GOLANG_VERSION=1.23.1
# Wed, 11 Sep 2024 00:03:40 GMT
RUN $url = 'https://dl.google.com/go/go1.23.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '32dedf277c86610e380e1765593edb66876f00223df71690bd6be68ee17675c0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:03:41 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e70f49c20671d030640819fe99e5b846a1ee5d8fb54950cedc8bffd9c6e29a`  
		Last Modified: Wed, 11 Sep 2024 00:03:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7599a220d99a5983979a2065f169fff89d4ac209d3ad341f6e11abeece8339d6`  
		Last Modified: Wed, 11 Sep 2024 00:03:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f726ad3a1e48a9ea73e77512f6f3aaf77051e52138fef0fabe83d10356188556`  
		Last Modified: Wed, 11 Sep 2024 00:03:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbeedd49da6baf674ed68e04cfa55364041bfd3b70d60c5f46f3b5c673b0508b`  
		Last Modified: Wed, 11 Sep 2024 00:03:47 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a120805c5139fe19432413b01774c55fe1593495966fedfb484316001dd50a`  
		Last Modified: Wed, 11 Sep 2024 00:03:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5010db3b75e0a589feff552b65d39808ef3ac6e6ae01cd982d64ffdf4c9dfe`  
		Last Modified: Wed, 11 Sep 2024 00:03:49 GMT  
		Size: 25.4 MB (25430526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bf413e96f658b2a166655b10f293f82c04512e88f3c05145dcedba34f8f0ce`  
		Last Modified: Wed, 11 Sep 2024 00:03:45 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7beb51ae082094234d5bb9a42204cb0805c7d4c3a4d5f1b30f08f6dfc3dd67`  
		Last Modified: Wed, 11 Sep 2024 00:03:45 GMT  
		Size: 336.3 KB (336263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ede37f38dfa3cd5022991843081e14382488928f40fca1ecc38efc74bfaa8c3`  
		Last Modified: Wed, 11 Sep 2024 00:03:45 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bdfe800dc36d8ceb8f648238c2c0e6f0d72274752fe15497e99f69712c7cad`  
		Last Modified: Wed, 11 Sep 2024 00:03:57 GMT  
		Size: 77.3 MB (77329741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bfc9fd2237a63248c24f2d2b4341b9597abe5da57d5f8a3c18bf279b7ce63e`  
		Last Modified: Wed, 11 Sep 2024 00:03:45 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.17763.6293; amd64

```console
$ docker pull golang@sha256:cb911449313ff7c9144bce748286eff1d33c663a8bbec96003b79a21587d9746
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1823383576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c1196954dc0424a87a4d7a90da28d019ac34911e106189b1923ee367e0bd10`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:01:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:01:44 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Sep 2024 00:01:45 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Sep 2024 00:01:45 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Sep 2024 00:01:46 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Sep 2024 00:02:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:02:04 GMT
ENV GOPATH=C:\go
# Wed, 11 Sep 2024 00:02:13 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 00:02:14 GMT
ENV GOLANG_VERSION=1.23.1
# Wed, 11 Sep 2024 00:04:48 GMT
RUN $url = 'https://dl.google.com/go/go1.23.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '32dedf277c86610e380e1765593edb66876f00223df71690bd6be68ee17675c0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:04:50 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c04bedb30d57245be0be7ce7146db3e3c564b56c572b18242a5decb16ff9dd2`  
		Last Modified: Wed, 11 Sep 2024 00:04:57 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b352097a953ef27941a57f1c9da3e9200cdeaedc1eee69eaaacb5db453aeb6e`  
		Last Modified: Wed, 11 Sep 2024 00:04:58 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b50cd90e9fa3a4f5bf519d3c39db19d418a8a6746fe474459447df2622af6ff`  
		Last Modified: Wed, 11 Sep 2024 00:04:56 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe427b2f4f242db027284ec365333af7afba7d4f159272889ac2f7ce62dca80`  
		Last Modified: Wed, 11 Sep 2024 00:04:56 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffab171d9f058752f3a36355d4530a0447c6252214d0b9739b4b69a2440d6ae7`  
		Last Modified: Wed, 11 Sep 2024 00:04:56 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d1f00b154aea8b49eb5cb510f8636232e04b67c95e08531bd451d88b1fe823`  
		Last Modified: Wed, 11 Sep 2024 00:04:58 GMT  
		Size: 25.4 MB (25437046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8024e23c792c0c1c5d31eeb589d814a03c4d630bf3d1fa26a0457d4851dac8c9`  
		Last Modified: Wed, 11 Sep 2024 00:04:54 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3ff680dde76271079ef10a54fc504f77d4c5df0ebdb5a3b94ef1527cd28d82`  
		Last Modified: Wed, 11 Sep 2024 00:04:54 GMT  
		Size: 335.8 KB (335801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5a849a0da86b63c35678b21b42b3435f645e7a59989161eee7dd5f2243a565`  
		Last Modified: Wed, 11 Sep 2024 00:04:54 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868b84a71ae6e7ebbe505ee90b01fbf644b553fb6cbbad9c16faff97f655ba5f`  
		Last Modified: Wed, 11 Sep 2024 00:05:06 GMT  
		Size: 77.3 MB (77331795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b616a32799159cf09285bd4cb65b9264e90a12c193305e8610e9d1ff67273276`  
		Last Modified: Wed, 11 Sep 2024 00:04:54 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
