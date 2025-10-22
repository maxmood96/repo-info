## `buildpack-deps:questing-curl`

```console
$ docker pull buildpack-deps@sha256:ef060bef4dd7d5b23137aa1cc1aa1cba08cb5957217714b8594ef45406e7fd44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:questing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a040345d0c22ae53e68d13cfc69a5cc1805d0ad90f07c67ba1d19f64e90293f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53389259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d9e13b3256266e369650d4280af98914ec503cd3202b627a826d0a84d77bbf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:7992b30df2d5e1a9868a357037fee7a935fb600c535045c3dae00a6d2da0ffea in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9b965cd3592863b7a60b38bfeed24007834fdaf4994cb2c642c14d872f7ba0d9`  
		Last Modified: Thu, 09 Oct 2025 21:06:04 GMT  
		Size: 34.5 MB (34453346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7576d1bb6bbc5cda3456d256501881b6fe33fdd86baf9d81e296b44b4629ac72`  
		Last Modified: Thu, 09 Oct 2025 21:09:12 GMT  
		Size: 18.9 MB (18935913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ed92322437cd5152108cbdb792b7664bdca066478801e37f31c5e74cf3f16647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a028aff9137e36a2be677bf7c49d448790150e3ee7bb1370ba82ea8cd57ca63b`

```dockerfile
```

-	Layers:
	-	`sha256:a5668a421b53e1cf3fa0f16b87144eedfd14ea3d6389d4dc9f5fab80dfec2b02`  
		Last Modified: Wed, 22 Oct 2025 05:33:28 GMT  
		Size: 3.0 MB (2963926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a5137a58a093b07fe464f477dd626ba834c73bf2dacc686930d069917dedec`  
		Last Modified: Thu, 09 Oct 2025 22:21:19 GMT  
		Size: 7.0 KB (6977 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:24284529237f0b87a79c60fafa8dcfa75693fdea642b6745129728b7d04d2155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49151082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e618484212f6fc9ce86646c1a286dfb35ba1fa3410488a816617883841f23189`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:8bbeb482f2b247bef1627efb419885c5e995c29ac97454dfbe51dfc4ecf549d2 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d9a0dc3298847c4f5e3ffc1427dcb99ebe4c8fbb1c040628256b603b41f715b`  
		Last Modified: Thu, 09 Oct 2025 21:05:13 GMT  
		Size: 31.8 MB (31837227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5789843bac3bfe60c050b74177d6bdef81818507b015abb59a7fdba7199764e2`  
		Last Modified: Thu, 09 Oct 2025 21:08:26 GMT  
		Size: 17.3 MB (17313855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:28d7a8432c30be69f2daf774f2ce50705ab97a0df72c46405506e8201083c4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2972472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913f356905e35843fc70da00490e846ec83a76817f5870eb80bdcbd0751da995`

```dockerfile
```

-	Layers:
	-	`sha256:a104db8d85652fd0893c20a7781a55ce81d60907bba7f3db828878cf01ac96c1`  
		Last Modified: Wed, 22 Oct 2025 05:33:24 GMT  
		Size: 3.0 MB (2965431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55a93f2110aa4e61b602f831e6438c3651561af08ef55504a201d67752ca62be`  
		Last Modified: Thu, 09 Oct 2025 22:22:39 GMT  
		Size: 7.0 KB (7041 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:682064ceceb79a1c97e25fd617cb3c479eb73f8014569b03b1e82aa9530e2ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52565501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2068e8b6c14900fd580e7668b008d677b190af1eb91b66aefe5fc7bfa9d7ca9f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:8ccca3821827ab9c5998bd942e103c70878335f75be5b71b28f3fbe104f6c658 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4d90657552ac1b6284508877841188af829f382e60eeb51a71e7aa12b4a521b8`  
		Last Modified: Thu, 09 Oct 2025 21:05:33 GMT  
		Size: 34.1 MB (34071074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae8e65d481c24454a1936d3603010aecc1bac389df893175bccd3d0809a7506`  
		Last Modified: Thu, 09 Oct 2025 21:09:35 GMT  
		Size: 18.5 MB (18494427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a220cec1950bec0f27451bc692d3987c633c3d234aac40649249371a9622983f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2971243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb8483b9fba9877f683f84c4ff51c5f37676fd31f3c7952335ffe294484cb4c`

```dockerfile
```

-	Layers:
	-	`sha256:8637f3b85d88c8070a6f880ea194cefcfc574976815044b50f8b14c5526e2fa7`  
		Last Modified: Thu, 09 Oct 2025 22:22:45 GMT  
		Size: 3.0 MB (2964185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a30f6b2c97be8d23c5214570b33e5c94bd084b13069468689ce0fb06ff85ae48`  
		Last Modified: Thu, 09 Oct 2025 22:22:47 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bad5153ce0963b666ef1ec8a2380d10016a204d07f0bdec053090355e69400c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60533253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0093398592e022755b2af5752ad4fc5e808a390df86ce65abfb5fe972c1553ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:dd403b9e32771d28688bbfb2437ede4cacfd229282ce79665f1d1990c3d4a564 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e02566c32e850e556611ce9d93fecac8301b5b6b4936adeb96fa33621c166384`  
		Last Modified: Thu, 09 Oct 2025 21:07:23 GMT  
		Size: 39.6 MB (39595315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea1422c4072975afe2319ab216c1ad9e050b6a8b262c31c31b2150e681cb0c6`  
		Last Modified: Fri, 10 Oct 2025 03:13:46 GMT  
		Size: 20.9 MB (20937938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aec45fedc4da0faa1bc52c037b68c4788c844004b008657d694dd1666f078a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0f799856d6f1ec0c92d41217605cbc618646a01f2a977e05d09de088450c78`

```dockerfile
```

-	Layers:
	-	`sha256:1d0fda2779aaeb8a9bc24a23ffe9adbe9200335ccacec6fd3cd055e25ac645bc`  
		Last Modified: Fri, 10 Oct 2025 04:20:03 GMT  
		Size: 3.0 MB (2967754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2627e6117e45b21409dd6e200454b55cef86d4e804941ce7b033ec90d663c2dc`  
		Last Modified: Fri, 10 Oct 2025 04:20:04 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c1ea0ba663284611b69054ab216d5a98bc33b11ce137f75cc0ffdc5133f6ef50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55047354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de85bf635e11e5b79fd0b9747a0c8a81f9c0d8e5edab1de87f6c5d5dcd4f1b83`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:d010b851ba09c7b22e7c06ab89aea9736e9ba461b1db1e6347edd26e85142fd1 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3dc034e8b1803c3caeaa0e732c54a197159456b92e58767392c621a4d6017f47`  
		Last Modified: Thu, 09 Oct 2025 21:06:29 GMT  
		Size: 34.1 MB (34093464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a511c49d832edb64e439df348a903968f91f662cdbd34c3e67e37dfa8463ce02`  
		Last Modified: Thu, 09 Oct 2025 22:23:09 GMT  
		Size: 21.0 MB (20953890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0cea8900a3595d03169153ae33ab0647df5babe5477db749cc76371754055878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2972934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614ef72f874c51d7e5903b308b70a92c6b778ef3bad85dd55c533045d948e156`

```dockerfile
```

-	Layers:
	-	`sha256:c0112e80a9f1fde6d7f70aa84e1fc6bad10a4702e2bb0a18c0b585e4de11e76c`  
		Last Modified: Fri, 10 Oct 2025 01:20:07 GMT  
		Size: 3.0 MB (2965956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbcce127355631755fb2fa9a704285b372693afa22d27d18247368ba9b1faaed`  
		Last Modified: Fri, 10 Oct 2025 01:20:08 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json
