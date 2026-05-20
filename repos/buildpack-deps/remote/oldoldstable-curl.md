## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:814107a337a1ad00b1527b64335ed06c5851f6cf4a82653453f5850aab83c77c
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

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a3c87ab79551a22cd08fee98ad38ae7193a0a50086c2d0af7cbd0e88f639eab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69559710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31253fd5b2a8d7db323cf17fbc54b5cab8120231ae5bc0a58adc4794cc7d3fcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:23:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a725631376ff1c8c144d62e01c2dd134ff006899cd43c1aff2afbb3141faf91b`  
		Last Modified: Tue, 19 May 2026 23:23:13 GMT  
		Size: 15.8 MB (15790858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:50da054d6ba7445fd6fcd8ae243d235fe6cb6024550e9c4d1f91220a13f54a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4644283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c971c0119e3d6b7231798ae2ece48a1470530a54413195f181efaf4430035f`

```dockerfile
```

-	Layers:
	-	`sha256:ea7eada9390a066e04faf441f55a70d0bccbf86255c5711db46e10b7a22ba284`  
		Last Modified: Tue, 19 May 2026 23:23:12 GMT  
		Size: 4.6 MB (4637519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e00ad808fbf2aee801f7da761c4f4c720760c2974c6ffbfaf57c6030e94e736`  
		Last Modified: Tue, 19 May 2026 23:23:12 GMT  
		Size: 6.8 KB (6764 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3cbaea61f13ef1c978dc5e3523d25873e1b70958393fa1b9591d948b3a83ce15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63960176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44228415dd1e883f837e10a0e76114394ba2283d29cdd3f79fc02907cb415aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4cb33fa51e00f2c5cad3e12a59f701c1cb73526295425e2f64b4cb13b9375c4f`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 49.1 MB (49055106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba52e9af1266c17416a17c315f698fb07fc71701dcf95b70a57e9d0f65c70ea`  
		Last Modified: Fri, 08 May 2026 19:44:47 GMT  
		Size: 14.9 MB (14905070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1eae36042625ff7470cd9e195c87427e56ee16b4ef9a5fb97e7333756786de1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4645982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae19f06cc82c5ad35ea6d86dd66ab7d31ca97bbb7cfe7d9eea0982e2d1b01624`

```dockerfile
```

-	Layers:
	-	`sha256:c53e9065a4dc2b158fa14997169fcfeed70cb588008119f30f38167eea833b11`  
		Last Modified: Fri, 08 May 2026 19:44:47 GMT  
		Size: 4.6 MB (4639155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:974b0c4f067ef868f0b565704e87b95cd4ffce50c9acecf84db4dd16eb870ad7`  
		Last Modified: Fri, 08 May 2026 19:44:46 GMT  
		Size: 6.8 KB (6827 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0c971bac7fd8a7587109ab63c71cfba6a6475f2b840195d1225c343ea22f19d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68031458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec2b50fa2d11a1ff94fe9d42f2a14e491933f78aeb8e7555de7174e4ccba4dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b862d1986560a28dd19f86c2aee630b1502d7f508a9266ed7d99d6f03a48419`  
		Last Modified: Tue, 19 May 2026 23:26:59 GMT  
		Size: 15.8 MB (15774880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fe542c8b0c001d542ada6a081a83e5820105b7c8ea10ef55e92157fc2dc7c6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4643977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e28fa271124d8cd1994251690605cebe04e90c73d0c16d0733914910785760`

```dockerfile
```

-	Layers:
	-	`sha256:0c924a06fb8335973785caef2c6b74ed9c79823ef62286355304bd080a4b7b76`  
		Last Modified: Tue, 19 May 2026 23:26:59 GMT  
		Size: 4.6 MB (4637133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:438b58de38112f3926c6477f0849a6030af8fba2a8ed585f05412eb409ae9bb2`  
		Last Modified: Tue, 19 May 2026 23:26:58 GMT  
		Size: 6.8 KB (6844 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:576c0b696b6422ffc11fff24f4af087e116740b350383e480c7cc438b023dee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71000940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87c331c023550bd1a52496922164899f7a84050d7247e5776970d5a52232a42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:43:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:caf67df8e858ea1242ba8175484d5f733d658c733fcfe8f173a3140308e3ffa5`  
		Last Modified: Fri, 08 May 2026 18:30:59 GMT  
		Size: 54.7 MB (54705343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bebb3bb20b05d30c1a5354688795bd554c50c12bfa7e9190aa4a54c7dce2a8`  
		Last Modified: Fri, 08 May 2026 19:43:41 GMT  
		Size: 16.3 MB (16295597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:60e8fd768f37bc2081ae6b32085725bdcdeb38a7aa6415b7c6382365281e898e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4640764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73ad575011483f91e980534a8ba54d6fc25f99b1dcda4118914a29711823c66`

```dockerfile
```

-	Layers:
	-	`sha256:312a964991b4d2502d1ffd4c7bbec549ad2d85a27889bf444178c7ec98c60104`  
		Last Modified: Fri, 08 May 2026 19:43:41 GMT  
		Size: 4.6 MB (4634022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e9a9f56fbe225cf4c2622aa62a5ee43d7aa8b8d0ad2b63adb789eda52669a05`  
		Last Modified: Fri, 08 May 2026 19:43:40 GMT  
		Size: 6.7 KB (6742 bytes)  
		MIME: application/vnd.in-toto+json
