## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:bb8c8cf2071038149d9964394194d8d1d2c12581f66e79592b2be7150c3786bb
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e0ca53f8ac7950a2da3046d291d2ceb499e9c24cc65a2a90685d9a1e4c3c2452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75595633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116397d9f51a7a971c19ea0219e55dc13fc5f9de2d9146c09b681254f6a000dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:40:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:099d3355eff9ccff1f5ee3b288e1ead2e7035e89d68d0fc80f60a9bd7a9815e3`  
		Last Modified: Fri, 08 May 2026 18:23:36 GMT  
		Size: 48.7 MB (48702238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fa57e83b29efeaf3d37af3434d6c21acf443c2346367f49caf4c6efea18b60`  
		Last Modified: Fri, 08 May 2026 19:40:55 GMT  
		Size: 26.9 MB (26893395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:59bac7d844808db728797fd42abd51bf46626c900821da533f596daba30f234a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4074720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605b2facb4d2c603dac15811a049648e3d21e9b2c801068ab51bb1e07ae746d4`

```dockerfile
```

-	Layers:
	-	`sha256:43768bb7b107f6e5689720488dfc695d9964becf44dd7c148066e5d4c61a08e3`  
		Last Modified: Fri, 08 May 2026 19:40:54 GMT  
		Size: 4.1 MB (4067959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d59724792f9c8de97a32be2abc9bc945af9108eae81af48465e5013f9b3fe64`  
		Last Modified: Fri, 08 May 2026 19:40:54 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d926c02fec9b208e3b2f95501de1f9b92eebd5a318dfc00f71eda35057175c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70215223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab45a2e3f95c5d1a3d1cc90f13dea5b09e1a15618598930aa3758ac9d64714e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:44:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:79db944cb324910e68326e7a22d4bc47bd01eb269d35b1d153975be52958d92f`  
		Last Modified: Fri, 08 May 2026 18:37:35 GMT  
		Size: 45.6 MB (45609975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ca5da1f5f4fb120cd7b2b40034ee2f9bf3ebf8737773b984403a970bf3e2fd`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 24.6 MB (24605248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4e6b023584652bb7d2d77e5ad4c757a738d65a6a4cfd7e1369450056ae9ade03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4076271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4006636d2a1906810dd86e93d4ce884c7a6e94a6d37dff30ab7686b0872c0dfd`

```dockerfile
```

-	Layers:
	-	`sha256:d461c6361ff964a33a8b4b4655b4b485535a0ed3ab414340520743ef1d7c04e1`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 4.1 MB (4069446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04c6e96bb702751bea2d891b71df4a5f71d551cc56d30eea6265e3aee4d428a`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 6.8 KB (6825 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7009993ef47ec2d8339aa964d540a2d9cba3ff8b5bd8762dec13cb4275f65cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74905477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24505763049b7e05e191f9336a929271c61a78a7912c09c2d1eebb7139b34667`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:42:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:99699fbc842c790e8471e4039d9c409499f27c659ef9c4d3336a0743660ec819`  
		Last Modified: Fri, 08 May 2026 18:26:06 GMT  
		Size: 48.7 MB (48734151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a8fe1ac3f05529fe3bd8a59a20b641133e27374191e01da78aeed091f2bc7b`  
		Last Modified: Fri, 08 May 2026 19:42:43 GMT  
		Size: 26.2 MB (26171326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7fbb5cf828880934b6e06ec3420087aa013d782fbc80d3f612bd489d1e8b81e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488cd8ab064c5a47de905c3081a3e9a1d56518b63885d7fd37cbdc357a8c12c1`

```dockerfile
```

-	Layers:
	-	`sha256:fe0aadc911749f75ebca3976d826753eb9e5e224bd40c30f59c401383644bf17`  
		Last Modified: Fri, 08 May 2026 19:42:42 GMT  
		Size: 4.1 MB (4073318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec8b40c89a2ece08f7decf4ecc0d0d36855f0356dc41f41b5bf23f9143238ec1`  
		Last Modified: Fri, 08 May 2026 19:42:41 GMT  
		Size: 6.8 KB (6841 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:737ae0f7cc4d7cd73f5fa85f443266e2585961bf1cc38b771a334981efe92d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78216277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8e86c5486cea9dc75613259b442618a113aa15f6258a0ec9e9567a026c110f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:44:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:673cf326009083501c3fabdd17567c937b894deb57d94461178ef18820adb917`  
		Last Modified: Fri, 08 May 2026 18:32:00 GMT  
		Size: 50.0 MB (50006715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e321fedc955b961c2c658a44d5ca3cbf39d67286d1387087c4563c14de6beaf2`  
		Last Modified: Fri, 08 May 2026 19:44:11 GMT  
		Size: 28.2 MB (28209562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0fadf9a19dbef48c9fef15c860f4aeabf316e2e14fcff00bbd9fbf2a020051ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4071801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa0fa1b5352b762844d63347591375038b576343aa2151f609bc1b0fea48a34`

```dockerfile
```

-	Layers:
	-	`sha256:d91b8ee3f27825016e498ec85bb9797527d62f1127dc7b0e7f68fe7035e2034b`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 4.1 MB (4065062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2509f9891fc4dceb2c88fff83dfad790637af9ffd5669415f19a740d7a0e1fbd`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 6.7 KB (6739 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:160aa9cf692e522e9ae0589f5c44af8152479a9e9ef105e4fedb864cdef3e47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83314825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe7c93d89e6542fa81d493336b0afa72d894c854e5ac15ddfea3293a8131ea0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 22:31:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9f402971e72fa142c9d15dd5eaca638787cb5c2e5a412bb3f2a7c4f896ed18ae`  
		Last Modified: Fri, 08 May 2026 19:45:34 GMT  
		Size: 54.0 MB (54028078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14bf1fa31e28d06ce5dc3e4b127ed62c78c28290930f8041edab4719b7e2e73`  
		Last Modified: Fri, 08 May 2026 22:31:40 GMT  
		Size: 29.3 MB (29286747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:955600b26b12dcd06dff05cdbc4f20996def3b57c2861310473e500256cea7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4078610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49027fb10f9e8b4fce700431b4b01046dbb52e09ea739ff4259af058924473a`

```dockerfile
```

-	Layers:
	-	`sha256:fb4e78f905f682b850e23d193e756e6b2ea412f731d640d93cc92bfb7c77c340`  
		Last Modified: Fri, 08 May 2026 22:31:40 GMT  
		Size: 4.1 MB (4071817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43ee172202585c9151859e3eb4f2acf8e73d204b6317534660a07d1ae31ba57`  
		Last Modified: Fri, 08 May 2026 22:31:39 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0c00682c6ff2598f9f32b8f879ca65894d2c43492b2bde6eedc90b7859d4fe60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73292007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500a21f01fd577386280d234e1ab10db0b0f5be95935ec05624201d0f7d69779`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1777939200'
# Mon, 11 May 2026 00:52:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:291921d355da34dfbce324263312328392c6a6c78ee971f9b4d7d37f1527cd2e`  
		Last Modified: Fri, 08 May 2026 20:26:01 GMT  
		Size: 46.8 MB (46838649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340855859b1344ded89a6e027caa6be811a60e26a4f08013b27235c463879b0e`  
		Last Modified: Mon, 11 May 2026 00:53:36 GMT  
		Size: 26.5 MB (26453358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3a416daaacc1722697125455fdb52c0c4be2fc7203b61ab6fa520bab5a09dfff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4066457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c12a27be6bb0922620a9513ea0cbf5d5584969f53252b2b8c203f82e83bc067`

```dockerfile
```

-	Layers:
	-	`sha256:8bf8e8999479568e023e249a98ff58774e7faad36b273162f2cbdb341cbe0d35`  
		Last Modified: Mon, 11 May 2026 00:53:33 GMT  
		Size: 4.1 MB (4059664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:089157629e8a35d8b0e8d79870e867a180d5be43fb8ca0842d8b4e58ea078127`  
		Last Modified: Mon, 11 May 2026 00:53:32 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:699d74153d3fc03a7c8c6f3dc236386f3189c7b2ca0a1f9b3d14809f9f10efcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75135034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3efe2be412163a1afbd1502d0fa247fc9f2ace1ef909d4dbd43ea09a5e3369b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 20:53:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:107669ad500d1f91592ad03e52cc25095058c6b4b2e83b9adad6737bfa81cd40`  
		Last Modified: Fri, 08 May 2026 18:28:19 GMT  
		Size: 48.4 MB (48444076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc97077ab9739db4cafdc266dad352532794bc43462c59a59b2c72e9905c9a6b`  
		Last Modified: Fri, 08 May 2026 20:53:40 GMT  
		Size: 26.7 MB (26690958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8b2f1d2d3ab46a0b8c0b268c3b1976ec2ebbcf220ed674ebe2be2c67bee33ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4076132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07576b521049ff8a104d387f59d0af8eb0974940b7195cf2308665569a1d714`

```dockerfile
```

-	Layers:
	-	`sha256:8b5b80ac85c360205a1cf3b8285c34584415c7f9945135d121977653d5d1c3d0`  
		Last Modified: Fri, 08 May 2026 20:53:39 GMT  
		Size: 4.1 MB (4069371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b1c1916932050ae3bfdf06375eb7ecba6089eb2409898ca60673b8e09e7c10`  
		Last Modified: Fri, 08 May 2026 20:53:39 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json
