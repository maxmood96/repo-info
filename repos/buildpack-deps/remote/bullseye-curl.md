## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:2567bf03e9dc0e2634c95e4bbdff4bb1fd4504c957b64466b08d1db39508d356
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

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0389b6043df8a79629b67340730c17dc0e5624a1b032d698be02ff9f8193ef52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69562593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7bcd43ffb9e3b64784ba4f9b383cca4444a34edb288dfd1a4a6e3a6a1ce457e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:42:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f53a3a71a19cca6d8312e9c60a5428b23742024a0057b1f0e46517df6ae4a9`  
		Last Modified: Thu, 11 Jun 2026 00:42:31 GMT  
		Size: 15.8 MB (15790824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cb163b1d4f2ec53e2cccc63b31981950b54ea2d844c26d4b89d73e795b13a9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4644287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7545b04b5b2d04a2e6611acae861cfead4fbaa37f1dfcd859fdc8343c7e51672`

```dockerfile
```

-	Layers:
	-	`sha256:9f11887b2a4e8b7801a10715068f9b2614065e1d39da987653e9a44232836b8f`  
		Last Modified: Thu, 11 Jun 2026 00:42:31 GMT  
		Size: 4.6 MB (4637523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724a3b0a1f91fcddcf8df7d26ff604b136192facf6ad8321cec8d5e2a9ce0aca`  
		Last Modified: Thu, 11 Jun 2026 00:42:31 GMT  
		Size: 6.8 KB (6764 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2e24d6727e858665f46a19a526780ba2ad3c9eee562cfc1d4df13c91ce99c1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63969400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597c4642435a19756c95b11f7cfe24fcb55cce3f87bda60ceb90b5f80f408265`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:24:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:057662c04791d47966179d44811cec5af4565f7f7a6a4690c7d8e834d0ba3bd2`  
		Last Modified: Wed, 10 Jun 2026 23:40:48 GMT  
		Size: 49.1 MB (49064004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa240a68c3059c2e50ee1949050052855111d59f6865103a70421028ec0d924`  
		Last Modified: Thu, 11 Jun 2026 01:24:38 GMT  
		Size: 14.9 MB (14905396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa9d713b77fcbc8addce53d998acfa0036b9baf8646a04f1224fe8a233c8ab60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4645987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641e6a2aa286d59f3970fd02dfb7f54002e03a076052e0855aaff3e00eed3be6`

```dockerfile
```

-	Layers:
	-	`sha256:9a2ed76fa5d2c9c2085b53a8fe2a714adae6edbc1b4e38a563bcf25e7f14aab0`  
		Last Modified: Thu, 11 Jun 2026 01:24:38 GMT  
		Size: 4.6 MB (4639159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c796a4ece53a1fbb8135db709417f2e281ec32aedb67f268617ac76028ad1e3`  
		Last Modified: Thu, 11 Jun 2026 01:24:38 GMT  
		Size: 6.8 KB (6828 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fb5a29660efcef32c61dc4ffe24388b10c91611a3e693d1ccb4292680bb048d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68038947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68ee2c74ce1be7ef53c06523d1c007dce7d520dac93513b4946661e6bd742da`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:43:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8698eac281c2783fff44c0d5a2c381eeb273791e12f4dc8b407db26260bc3b85`  
		Last Modified: Thu, 11 Jun 2026 00:43:55 GMT  
		Size: 15.8 MB (15774833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:248092afc5c7d03d50a422024beaece9d19d6b3a8fc19e082eeae6e04633ed81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4643981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274f6ec1e6da73828fa4c7fac67e5c1d09232519a495af6dc74d6c6724567455`

```dockerfile
```

-	Layers:
	-	`sha256:e8bdbbad71d50e0fadcf92425287fd3ddda38b4e7ccb54d99b7ef6bc9973f35c`  
		Last Modified: Thu, 11 Jun 2026 00:43:55 GMT  
		Size: 4.6 MB (4637137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aecda9263a2e90b7d19b775c75014785f5001d3597169b5b6d6691f421c37e73`  
		Last Modified: Thu, 11 Jun 2026 00:43:55 GMT  
		Size: 6.8 KB (6844 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ffd57a15e0b7e002eca4cb0fb67727ef4d030529ada727530e7a2b04a4c277e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71008514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1455279c7009ae3d52bfaef9a2847bf80c0d454720d70374c9aa0ddf6ba4266`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:44:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fa94b3659141003eaf4c6c1ec8d2e2140d97afd4e23da5fb64936eff3ddbe795`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 54.7 MB (54712857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7baf1917f31dc6264a068963cb19f53c4fc1fb3df24b85fb7b1a7235134b9d`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 16.3 MB (16295657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3af6ae1fe815ad424076136abd3cf70610d1900b3c197fe42d142f5c4124020d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4640768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a177f50596260205efd6e145ad433dfd61c28704e35c8ee2b225218c7d90f841`

```dockerfile
```

-	Layers:
	-	`sha256:ea664203a0e162f1a3d38034e4966f2a04414064c5b66f68a3e120a53572241b`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 4.6 MB (4634026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24bb2641e66e2158a1fdfb0f8704edb90f4b22ae89763a02abc7d429f4088343`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 6.7 KB (6742 bytes)  
		MIME: application/vnd.in-toto+json
