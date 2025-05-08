## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:1a78f7d023653898b592416c05ba80ebc427000ee63ca77c8809c6e78be79613
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:focal-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2ecd5cec4c7a628e6661f781e743b0514fdbb101f95ebefe044f81ea8a180ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38660725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0be8081e327c452fe1325fb16cd594fc199d5f2ba7ae7e4a2c176794d737a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7577a2ab12ee9be5df3b0c322f8c7e4cb7d72c7826b239c5a9581720d332213b`  
		Last Modified: Thu, 08 May 2025 17:06:51 GMT  
		Size: 11.2 MB (11150331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a031e87e52845470de0d85073c559da717685438f432fac55b32f00865831a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3058924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466e5455aef4055c097738a9c21784078d747d98b56f11f94d3a1469097f0caa`

```dockerfile
```

-	Layers:
	-	`sha256:9fe89f6aa63c3f3457abfc6672b43fb72a84922fc5bce119e952ae632e8c39ec`  
		Last Modified: Wed, 09 Apr 2025 01:45:55 GMT  
		Size: 3.1 MB (3051999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf59eabe19b9801d31f65f605c389acbb469ced483fe713d87d269b3f2d7e00`  
		Last Modified: Wed, 09 Apr 2025 01:45:55 GMT  
		Size: 6.9 KB (6925 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:147e0956376da13e02c1d4a7bf6f8f2d4f3bfa40915d6a7f4d06994322e34227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33245002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a42900e9fb786c5eb091f0feb6d5284aa621a01ad777d5b21fee19b5051ca1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da7e36a763f959e9959a67d83a9318d563b85525cd5898dd19774da499cb0a5`  
		Last Modified: Wed, 09 Apr 2025 11:32:37 GMT  
		Size: 9.6 MB (9620939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:71b3d0c5927be732464b4f4b295c1cd353e33b30c0988d0bd6bee18ce7bdf1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3061240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582b6e3582d8855be355a638251063aa052a79e36a29a835421908a50a5e2894`

```dockerfile
```

-	Layers:
	-	`sha256:da760ce81f2df7e009294fbc5d0d8f6394e6ef39efed54d9e44b2d7f86028187`  
		Last Modified: Wed, 09 Apr 2025 11:32:37 GMT  
		Size: 3.1 MB (3054256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbe40dde02a7c69d4eada2a5628597b0e3a65593ca3ec79947bd8f515c6801b`  
		Last Modified: Wed, 09 Apr 2025 11:32:37 GMT  
		Size: 7.0 KB (6984 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:96008de169a0ad430cba4b9c2c3495c12d987f85cd7fed8ae381e30a219e5326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36968618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b555efbbb70ff8fd0e142256f910efe2f14c5aa88ecbaaad5829cc58e4ebddc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03900f2fdf5974424bfd298551b0e62da0045dd4710d9615492752026efcb4f5`  
		Last Modified: Thu, 08 May 2025 17:36:33 GMT  
		Size: 11.0 MB (10990957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8e765e9582698eddbbe18f9ead2cc38a02adb67760e359567c02c061d3653314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3059251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ef2da8d469f7dd1c5896a033af04271fb12ad049cfc48ee6d47b7ae135dd99`

```dockerfile
```

-	Layers:
	-	`sha256:7f503f0d6270eac1c7211f40d1adb5b76f07b0bccf0e1ef5f97640ad285d4d35`  
		Last Modified: Wed, 09 Apr 2025 06:08:33 GMT  
		Size: 3.1 MB (3052246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f974eec672c8acae09b12f7fa89090e71eed89ac8f535c556d71b9389fefe62`  
		Last Modified: Wed, 09 Apr 2025 06:08:32 GMT  
		Size: 7.0 KB (7005 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2040bd2bb4474aad738ab0735dffaf1267e367d6595aa7caea280415e083d7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45040037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ff646ac4d707fa9a587ef118da8b571fec0696a5f2fc5609260671cbc711ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbe8b02ff52733b6c9023254a29940996cd72195264668a2791dcfbd8d98610`  
		Last Modified: Wed, 09 Apr 2025 04:26:54 GMT  
		Size: 13.0 MB (12963091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1ef81cb813b8d262dac48febe9dfb168ea3f4c2c70aa621b4bd2fb92744e31f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3063392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb6138d595c56a0bc1b7f81adc699ef38b89ad249216718eb1e1a6060a847d8`

```dockerfile
```

-	Layers:
	-	`sha256:b2c7c08e6a97d539f69929ef8f14a7911dac24156060003fc41947d105eaf4a1`  
		Last Modified: Wed, 09 Apr 2025 04:26:54 GMT  
		Size: 3.1 MB (3056435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d0f1db07496460dc2346befeaada3c0c079509d9ed8bdfed73b96cd1650af9f`  
		Last Modified: Wed, 09 Apr 2025 04:26:53 GMT  
		Size: 7.0 KB (6957 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0c8712ac0bb26713e1e9ffd9b086a40e8b7e1cebc9f2bfaf4c26ef648796540b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33111460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137a66cba2c93a33bc7eb02f9a796cac344a035081e1b3e130fc4cc13fe74913`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:40f16f8820db6e5c845f62edc4f313f39cc0c4b33b63dfc2181b08f422b6f190 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1b71767744c54ea4c5171dede3cd089fefd23a403f2d9d5b60b7805c8104f77e`  
		Last Modified: Tue, 08 Apr 2025 11:48:50 GMT  
		Size: 23.5 MB (23473487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8c71bcc2b7ff6cc6b41d2703cceda9d805c102b3c6ef2da7396fed3127ae5b`  
		Last Modified: Wed, 09 Apr 2025 05:12:31 GMT  
		Size: 9.6 MB (9637973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f20b6f66dd90c27df6edd9ec2757b74bcd8e4b8788c8b9f64b6b869742c13c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92877895fb82df82c428d6584576986b511e7563fdd0e8ac84db6a094f559dea`

```dockerfile
```

-	Layers:
	-	`sha256:2daf7676893c9d4bc8d82585825041255f793a71b73bb9d8df1843259f4090eb`  
		Last Modified: Wed, 09 Apr 2025 05:12:30 GMT  
		Size: 3.0 MB (3046025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0149a8d0a163fa86a12ba5ab6550bff1bdd3b1b9e24969a0ffb4d5d8c83ffac3`  
		Last Modified: Wed, 09 Apr 2025 05:12:29 GMT  
		Size: 7.0 KB (6956 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9f1dc50549dafa583c57a87efc81e7c373409ba369b992b35bdabfa23875e3ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37070439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b780a50c3ffbef94fe864bc7148c8a5a5468fac1eeae87d48eb2edf2bd578816`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:82f0132f510f24adc12d74491187647b94a14baa7a57fd22a67a5c3767541496 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b35596e17e863edd4c594d026a60e36f73cc6a076370f55a24732114fd25ff68`  
		Last Modified: Tue, 08 Apr 2025 11:48:56 GMT  
		Size: 26.4 MB (26368190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4495dc22cf93325906d3dc47401597dbe3f0e5d18ba19d26285034bdf0c41a02`  
		Last Modified: Wed, 09 Apr 2025 04:10:51 GMT  
		Size: 10.7 MB (10702249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d03319034605653b0dd5610df1cc5a67721d2372401fd97bf6b897faca66ae4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3060342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711a9052a68c322044280e86498d11cd0f8f922a34b824e7353af3b279737838`

```dockerfile
```

-	Layers:
	-	`sha256:34f234384713bdc896b9d0234d32a9ec9b88dcb0a44d8c704d48d432dc8fcdd9`  
		Last Modified: Wed, 09 Apr 2025 04:10:51 GMT  
		Size: 3.1 MB (3053417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb69569834ce7266fca5329668d01c06cee5647020d58c7e360e1e5b194986c`  
		Last Modified: Wed, 09 Apr 2025 04:10:51 GMT  
		Size: 6.9 KB (6925 bytes)  
		MIME: application/vnd.in-toto+json
