## `golang:1-bookworm`

```console
$ docker pull golang@sha256:eae3cdfa040d0786510a5959d36a836978724d03b34a166ba2e0e198baac9196
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

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:bfab16ae1c7f13e06060055b73a71773199c65060f9417fcd0e55197d07fc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296537594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3da86bc11c2f877b403005f74ddf88fd340df8491518699a2dace70729f8365`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:25:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:25:49 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:25:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:25:49 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:25:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:25:49 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:25:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:25:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbceb003542957cee7df7b79249eaf0a71d21c5203d086969b565fb6dec85d86`  
		Last Modified: Tue, 03 Feb 2026 03:28:33 GMT  
		Size: 64.4 MB (64395971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d008c3f38986d44f1b6d856813cdbc2a9a52ef5dc087e4267a64043877fe184`  
		Last Modified: Tue, 10 Feb 2026 21:26:19 GMT  
		Size: 92.4 MB (92444866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ede2856567d2593950de6f98f5d2763ae304caeb0ff577a1318c065a8fd650c`  
		Last Modified: Tue, 10 Feb 2026 21:25:34 GMT  
		Size: 67.2 MB (67176670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6118fecef0033245b81c35f0d4b7665697c66691d88f774978bf9f5cce7b267`  
		Last Modified: Tue, 10 Feb 2026 21:26:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:dedf2b8ebe657365bc916c345b331beb316f0f2d65677e92ad677dff4d323ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c10954255c1cd68e6a19112a6e88e5268c79c4ec0866374238591ecefb434de`

```dockerfile
```

-	Layers:
	-	`sha256:b2178ff5edfddf34fde75e9f01cc7863f16e5c1f30563bfd5dd0af4d596f35cd`  
		Last Modified: Tue, 10 Feb 2026 21:26:17 GMT  
		Size: 10.5 MB (10497855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7942eda3d5e84ea439cf9da24d7ca857fae1dd63b43251d4ed14f69d44096772`  
		Last Modified: Tue, 10 Feb 2026 21:26:16 GMT  
		Size: 27.8 KB (27797 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:d58c42ce1f9a045e073b19fd2eb8c44971d483dec2f7389c9c3fedc63846c9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257836048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946c207947c60b2cc2a16e1b3774e268d84cd0e95ad9c535bf570ea95eeb0aa4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:25:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:25:35 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:25:35 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:25:35 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:25:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:25:35 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:25:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:25:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:424cab4c9a6a41cd57ee6de8e95726c4d76fe3e913bd9c7731865fd244771971`  
		Last Modified: Tue, 03 Feb 2026 01:13:26 GMT  
		Size: 44.2 MB (44198733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fc27aeb6b79b5764735a819c5fdf5feb13c904bdffa0dee2b4c1c5f3935e7`  
		Last Modified: Tue, 03 Feb 2026 03:30:05 GMT  
		Size: 21.9 MB (21942045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb0551578bad740c3a20b6a29166ce3ad8980e037c23d30c90a060f62da5338`  
		Last Modified: Tue, 03 Feb 2026 05:00:10 GMT  
		Size: 59.7 MB (59651962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910470118e15f580470a69a6149eeed150be5a52c68590aaff4220375ff0900f`  
		Last Modified: Tue, 10 Feb 2026 21:26:02 GMT  
		Size: 66.3 MB (66310266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb468d6c3aa96f0258422956f98c08c3bc799ec9552ffdc9be6851ba4d40573`  
		Last Modified: Tue, 10 Feb 2026 21:25:20 GMT  
		Size: 65.7 MB (65732884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ade8b376e8f620bfbb0d9dc772f4d2144a480cca584feb3af97f8d454e9f11`  
		Last Modified: Tue, 10 Feb 2026 21:25:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:857995b6932cc519c8928ff589d3b0976e4584d91f10251ec683ee5451a90ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de3e86f0e634a2497b714c5d3e20aba4b82a88a5c16bf150845bcd63792dcdb`

```dockerfile
```

-	Layers:
	-	`sha256:1bf3be948ff3879b5b18ef0f938f3db6d5ce27f1f7b501b5775b7cea0e844ef7`  
		Last Modified: Tue, 10 Feb 2026 21:26:01 GMT  
		Size: 10.3 MB (10304567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3db5cd640c073fd7047c2a33a1f115cc7e189be5c4926f8a30b825ac148ba38b`  
		Last Modified: Tue, 10 Feb 2026 21:26:00 GMT  
		Size: 27.9 KB (27903 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:ed34fe6f4f402071cbbaf5e0d5a4915cf4fa432a57c71936fec61fc8096201b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287059988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f444cf0b430c75ee7a5ac148abfc7733acdfad1f428a30f884d6833c2aeacd2f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:25:52 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:25:52 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:25:52 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:25:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:25:52 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:25:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:25:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e9aa4982c2a67e202ea283fc3760e94d8d8b16966c616e01ad0238abbaac82`  
		Last Modified: Tue, 03 Feb 2026 03:46:50 GMT  
		Size: 64.5 MB (64479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871532a807f5701ea9feda3ee0ce6d140f3380326492f719109a64d2c44af707`  
		Last Modified: Tue, 10 Feb 2026 21:26:20 GMT  
		Size: 86.5 MB (86525342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5a418ef96019867316412a90ec8973c4ade493b1d6671994ae31514a8ef6cd`  
		Last Modified: Tue, 10 Feb 2026 21:25:38 GMT  
		Size: 64.1 MB (64084003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548871bae46ecdf2baaa934bfe70de6c281116530b489502aaa0dbfdb73888cd`  
		Last Modified: Tue, 10 Feb 2026 21:26:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:07d06d699d0a7e3ff6c6f23dd74eb843af9643db5866dfe31f9129ca200a486b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:622f0868a7d917a6c556dee2391779f05adbb5875184fb06f28488af0f2d1830`

```dockerfile
```

-	Layers:
	-	`sha256:0d2b8a2008073e083e31fc4520e96fd132ef43db916583f1ab773fb256a5c27f`  
		Last Modified: Tue, 10 Feb 2026 21:26:19 GMT  
		Size: 10.5 MB (10525703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:786c776a1c7fa1ec780ce9b37605907afc6ecf089323977efc123f154cb3ad61`  
		Last Modified: Tue, 10 Feb 2026 21:26:18 GMT  
		Size: 27.9 KB (27930 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:b16d308e4537f383c0e1168f4b269ba65867285f5b7c2c272c401f49bcda71af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (295968539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129bed9e8a0865d3842bc962d892978e76019470ba43d2fbd1eec25b1afc749a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:25:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:25:51 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:25:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:25:51 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:25:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:25:51 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:25:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:25:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a7f977a794a5fd56ece19f51541cec3b8ba447f10234ab001213bf850f92f64d`  
		Last Modified: Tue, 03 Feb 2026 01:13:34 GMT  
		Size: 49.5 MB (49468454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50ea552b26a58c13b4166d933269500891fb4897db09bc72d932372276b158f`  
		Last Modified: Tue, 03 Feb 2026 02:49:31 GMT  
		Size: 24.9 MB (24872100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc15e0cd687cd62190081200fbe30ab5102ae840cc68b0386259c387aef2b9a`  
		Last Modified: Tue, 03 Feb 2026 03:25:00 GMT  
		Size: 66.2 MB (66234564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306bdfb5e331a6759fee4616d69875696044145678886ffb56d2487e049921f5`  
		Last Modified: Tue, 10 Feb 2026 21:26:19 GMT  
		Size: 89.9 MB (89871525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbfad3c600a3a9c8302db25d37648349b37e769601e5490f9bfb9f615fe5677`  
		Last Modified: Tue, 10 Feb 2026 21:25:34 GMT  
		Size: 65.5 MB (65521738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548871bae46ecdf2baaa934bfe70de6c281116530b489502aaa0dbfdb73888cd`  
		Last Modified: Tue, 10 Feb 2026 21:26:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:bd73490909929d5166f05f5488869bfa7ac9aefee41f689805066006ec85581a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10505184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393119ec6f50b0f5b686f1507a51cd9acd195cbc23a4725ca3e6b69a12a615f4`

```dockerfile
```

-	Layers:
	-	`sha256:8bac1bd5c655a63c88f6d7cd9cf4338a661cc7cdc2ea90b3894a529c8a0c8017`  
		Last Modified: Tue, 10 Feb 2026 21:26:17 GMT  
		Size: 10.5 MB (10477425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e438d592c822ab2dc5df52d1cc7aa1055780d74000ad86e3382cb5dac86368b`  
		Last Modified: Tue, 10 Feb 2026 21:26:17 GMT  
		Size: 27.8 KB (27759 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:9f780f355c0f1275157775294b076a0a2eb2b3c4b133d6e0c9b5c6d3c55ecb26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268490029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aeb0f571db5abc98843f1b3861d825d26ecb660de8701e7be90248259f60301`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 16:06:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 21:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 22:18:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:24:37 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:37 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:37 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:24:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:24:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:001d31ce76be3df3174382025b0b9e2985ddc96d785143497e14a46cdcdcf951`  
		Last Modified: Tue, 03 Feb 2026 01:12:32 GMT  
		Size: 48.8 MB (48763257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e910e12f1ba466db5d640f799037fd1161885165d6ef1a46de53b55b08cfb02`  
		Last Modified: Tue, 03 Feb 2026 16:07:24 GMT  
		Size: 23.6 MB (23615398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e0ad746711a3754afd4dc1df1be9308a858da3b48f46cc1d318cd1dbf2cb47`  
		Last Modified: Tue, 03 Feb 2026 21:29:58 GMT  
		Size: 63.3 MB (63310108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2164c80380b0dcd60ea92fbd5645d9478bdfb6a0b5dfaabf0daa2a974ecfb949`  
		Last Modified: Tue, 03 Feb 2026 22:20:18 GMT  
		Size: 70.0 MB (70021714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f4b21db9e8b72856ef3b37b567c6f4eaf21673d1c15aba8838a49684db0da7`  
		Last Modified: Tue, 10 Feb 2026 21:26:36 GMT  
		Size: 62.8 MB (62779393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0cde1fd5f96d21451bb13d246f09ba2b435654879b64124320a2d051f8d71f`  
		Last Modified: Tue, 10 Feb 2026 21:26:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4678b14828832504edb4dcdf80e0728c8b038142e948a661c1a4e6471e63774c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8291d2de63586ec24ca972167a828f5a57f1e56ad63a426a6b4b1e8da018a8e7`

```dockerfile
```

-	Layers:
	-	`sha256:da10963ec69a683b6fbc78778ed2f6b08a26764a00aeff9675b3418307f11e56`  
		Last Modified: Tue, 10 Feb 2026 21:26:30 GMT  
		Size: 27.7 KB (27654 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:2b4dbbf7c3325978febbd744c9ba87cf7017324eda00d95fd69e651e3a4a6b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (303026835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d1664f34140edd1ee34a957791d20e11881034ad1bdc215b0e08285f65a7135`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:22:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 10:35:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:26:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:27 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:24:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:24:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1311f6670d65067c1adb8d518ab8836a9d3d42058afdd776824845f91935c9`  
		Last Modified: Tue, 03 Feb 2026 05:22:25 GMT  
		Size: 25.7 MB (25671343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3c21a9818f8ca2f73ccd29b595b5a2bc7818b3057c3895ec555bee901eb365`  
		Last Modified: Tue, 03 Feb 2026 10:36:21 GMT  
		Size: 69.8 MB (69846016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bf9d9076f39b8e2c0aced7f1f28dac543d58a8aafe215df11bf80a17810efe`  
		Last Modified: Mon, 09 Feb 2026 20:28:08 GMT  
		Size: 90.5 MB (90451427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb65e50af4c9d9d06b20c69b0731fa5479387927e011d4a6cf02c0de9c35733`  
		Last Modified: Tue, 10 Feb 2026 21:25:51 GMT  
		Size: 64.7 MB (64730602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ec2ea4c7ecfac088e7f60c9c0bcfa17286ead05e35ca5655100798438ff4c3`  
		Last Modified: Tue, 10 Feb 2026 21:25:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:82f71dd779baa8bc5592c000a9a2bae8390a91abd50bf03d7a300de0573a6ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10498197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3dc1defc67533cfd1ca4aa6b3d09188d450b7410301cc98f4ee92a74575a560`

```dockerfile
```

-	Layers:
	-	`sha256:45ff9a4a318884c262c1f60c3d5f49ae12088b5a22db30f09fdae75d14f8e3df`  
		Last Modified: Tue, 10 Feb 2026 21:25:49 GMT  
		Size: 10.5 MB (10470352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f371f03932934f74a7a02426da0acfab58a7b7747095f12f5d535c86d26dc1`  
		Last Modified: Tue, 10 Feb 2026 21:25:49 GMT  
		Size: 27.8 KB (27845 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:d9b87cb7603d984097e53395486ed380e1afb821314327025590c87abaedf92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.1 MB (270121374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e738fcb7ff6450a02e59480b4c1271fbc1ff2bc857b46e1d08c9f4312812dcc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:28:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:00:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:24:12 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:12 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:12 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:24:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:24:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3072e3eb8c224dc593a4e18a3785b06d51467102b1cd9dd426d3d31d0e6831b8`  
		Last Modified: Tue, 03 Feb 2026 03:44:33 GMT  
		Size: 24.0 MB (24033633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61724404ca7e7ee67a943113b2e679af71546a07f66af094570e811bbc9fa743`  
		Last Modified: Tue, 03 Feb 2026 05:29:11 GMT  
		Size: 63.5 MB (63501320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be60f9687e53e1d931599c2c97d67403bb6a6a87fba5a8672d8f14c72b51e5e`  
		Last Modified: Mon, 09 Feb 2026 20:00:52 GMT  
		Size: 69.0 MB (69045163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0267cccbf93e93da2ed1297ad6771262243fba5de764f475d84248f8d84f3c28`  
		Last Modified: Tue, 10 Feb 2026 21:24:50 GMT  
		Size: 66.4 MB (66402757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fd64ef6e056560c7e86ccd7e2ab07ab01bf15e5bd3af2790908475a5799625`  
		Last Modified: Tue, 10 Feb 2026 21:24:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f7f87fdd64f648cd0f07a84dc94efbb8352131131432a585d442f07c6fbaf1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b94e49dba678c30391860e1ff438e1c002333e2076ab0fee204ff8cd8ae929`

```dockerfile
```

-	Layers:
	-	`sha256:d048057d6bb59579dcff0facbe5ad253673531379b9c8552473c4ebc8418ed49`  
		Last Modified: Tue, 10 Feb 2026 21:24:54 GMT  
		Size: 10.3 MB (10329613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:614e128480d136d8dcf7c7ece3cee62d477b87e83fe6450677714edb08ce4e2c`  
		Last Modified: Tue, 10 Feb 2026 21:24:53 GMT  
		Size: 27.8 KB (27796 bytes)  
		MIME: application/vnd.in-toto+json
