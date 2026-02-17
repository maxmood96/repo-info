## `buildpack-deps:resolute-curl`

```console
$ docker pull buildpack-deps@sha256:05b0d33003467ba6ef507853fafb9c6f3f9913ad04c81dbe43ae3122b54db0db
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

### `buildpack-deps:resolute-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e3ed9d8b3c5c4f37c6f3beb8d120766c60545237ba15dfd34c264fff12701962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59216486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44298f81cac571d61b2420635f1961b2c4fad1b9bd5950cc0b01433f5294537f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 21 Jan 2026 02:04:52 GMT
ARG RELEASE
# Wed, 21 Jan 2026 02:04:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 Jan 2026 02:04:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 Jan 2026 02:04:52 GMT
LABEL org.opencontainers.image.version=26.04
# Wed, 21 Jan 2026 02:04:55 GMT
ADD file:5a3b3d88836037412b2e65304a34ae9b8902e2e18f2142a9d7bd31359c280c79 in / 
# Wed, 21 Jan 2026 02:04:55 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3c261c4d22b0eb03c17e9c8acc3b714b4abd96cd3b2435def412cb5367ae9e85`  
		Last Modified: Wed, 21 Jan 2026 02:53:34 GMT  
		Size: 33.7 MB (33675624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55883c6a0c594fbcd6607363867fa967d79095f04962e66e55fc017c45bdf9ec`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 25.5 MB (25540862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:adf31ef0ffb78cc6cc95c93084d89e57e8157c35cb62dd57150dbbf008314c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4193035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1630245a69b9b9fe17374412bc489e225c4e01a136f2eb1f4a439c2fce1554f`

```dockerfile
```

-	Layers:
	-	`sha256:67b0eaee03ddcddf74c4245a9a14f57656278cad5b4e30a8c06aab15520f3709`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 4.2 MB (4186100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a01f8336676d33204509d35e9c58ff354f0d897a5586968e31c07b8b46ff38e`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 6.9 KB (6935 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:531ac6c6610092c3febb6405f9e151105bad381be22c305b45814b6c6b8b5319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54443977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5803bc2f71b87be38c1d0347b3190c9214a29b66d39c277be098acee96172a21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 21 Jan 2026 02:05:08 GMT
ARG RELEASE
# Wed, 21 Jan 2026 02:05:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 Jan 2026 02:05:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 Jan 2026 02:05:09 GMT
LABEL org.opencontainers.image.version=26.04
# Wed, 21 Jan 2026 02:05:14 GMT
ADD file:64f8302e71f30ce19eeb546a74e2f2ee518a1401afcf8395ae4cf115f7f4007f in / 
# Wed, 21 Jan 2026 02:05:14 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:340f1c91e91d4fc6dea29a48d805d764635f314ec829f043b408b97d421fefcf`  
		Last Modified: Wed, 21 Jan 2026 02:53:47 GMT  
		Size: 31.2 MB (31166507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd26212152f3531f73c0efa5d9e16bb1fa6f236b022d20f6d2a2aa31de3742`  
		Last Modified: Tue, 17 Feb 2026 20:11:45 GMT  
		Size: 23.3 MB (23277470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de6f9402b8f512aa8d748f6bbf81088ea58ebfa78de1538ecc63c6d8c6986e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4194601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94941b32d45fdab134bc0598eef251aef867df70f0d4fe83cde66d567a9d41f1`

```dockerfile
```

-	Layers:
	-	`sha256:0bf6fcbea92bbe50ba854ebdabe152ba1849541519e895327b0d139c67bb79b5`  
		Last Modified: Tue, 17 Feb 2026 20:11:44 GMT  
		Size: 4.2 MB (4187602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51af4bb406b771eaccfee9655d06aebd64ee47a70afc22e22f1aa405625cee59`  
		Last Modified: Tue, 17 Feb 2026 20:11:44 GMT  
		Size: 7.0 KB (6999 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e5da9d1d19f745820bdf0130fd17790e98a04e6ac02150b495e87807576823db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58344157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6787c8699a7103ec56bbe9b5985a399c4914650e4bb040242ee61764838dc557`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 21 Jan 2026 02:06:33 GMT
ARG RELEASE
# Wed, 21 Jan 2026 02:06:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 Jan 2026 02:06:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 Jan 2026 02:06:33 GMT
LABEL org.opencontainers.image.version=26.04
# Wed, 21 Jan 2026 02:06:35 GMT
ADD file:a11224ce0bf3c5f80538743d4c0625b9323c82858600072ca8c1663ae7960103 in / 
# Wed, 21 Jan 2026 02:06:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53aec10ada41ffe8ba1d5de5418a311240cc814b8b270a9f91d069cac334f70e`  
		Last Modified: Wed, 21 Jan 2026 02:53:41 GMT  
		Size: 33.2 MB (33228686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900559816bd40c452d3861268a03da469284a99c9639d5aaa515e1c92b085722`  
		Last Modified: Tue, 17 Feb 2026 20:12:12 GMT  
		Size: 25.1 MB (25115471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:74f51effe4b634940bf822776da45661929d8745380ebc3e9ae1fee44603b6cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4193373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b54df42a82060f5adcebf02b0b5c092319b6aa087f205d29095b89ebe36bcc2`

```dockerfile
```

-	Layers:
	-	`sha256:1a1c12734e7f9febc57f1d46945958bdb830bf9a3bedaf7fa54972e473f17205`  
		Last Modified: Tue, 17 Feb 2026 20:12:12 GMT  
		Size: 4.2 MB (4186358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bae78e4c9d6c0af4d6c57dc4813ca6b8ab35b1a8e90a65023e2e5871448cbb6`  
		Last Modified: Tue, 17 Feb 2026 20:12:12 GMT  
		Size: 7.0 KB (7015 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9faaf8db70b50cabd8c2784e866f6d72f456a01dc61acde0319aaca67ecab010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67129777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1222c365691c8c86dab08fd44e082387cf26ce724528c4a07600f70b9f87d39`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 21 Jan 2026 02:05:01 GMT
ARG RELEASE
# Wed, 21 Jan 2026 02:05:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 Jan 2026 02:05:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 Jan 2026 02:05:02 GMT
LABEL org.opencontainers.image.version=26.04
# Wed, 21 Jan 2026 02:05:05 GMT
ADD file:965035165b5a9607aa8c5bb045af27bc17ad5f8ba33ecbe10426988d7c087ecc in / 
# Wed, 21 Jan 2026 02:05:05 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:13:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b5ed12c0213034851f152051b56017b1e654738743050659fce37a1a1aabcb6e`  
		Last Modified: Wed, 21 Jan 2026 02:53:54 GMT  
		Size: 38.8 MB (38812135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218b035f88d928ca302b9ff3aa9991b0d88cdc1af3c26cf3a2e90174b06d0494`  
		Last Modified: Tue, 17 Feb 2026 20:13:43 GMT  
		Size: 28.3 MB (28317642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d164e471ca336239a8e5e03f40a0a427b2038b2fdd657c8fdc4f15d662ac8bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4196890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef491fd90ec92609fc35afb3f06395e86f8ef86ec5c6996a6110f7a95f7b69f`

```dockerfile
```

-	Layers:
	-	`sha256:4fdce5b4ce184287d4bd6dc900084df511290e39d1a35cc7da5befaaa0a7c76d`  
		Last Modified: Tue, 17 Feb 2026 20:13:42 GMT  
		Size: 4.2 MB (4189923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af1876ba8d325717746c8e693aaa94fc414b1dd401f8236df1abe2812664402`  
		Last Modified: Tue, 17 Feb 2026 20:13:42 GMT  
		Size: 7.0 KB (6967 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bc9d0b87a56b9dd6899c13feb4a9463232e2cd3a9a1e9a1dd28b0aaa5bb95df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59484964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f014ad2944f9ff96580cc70e51941b7d1a560e79fed467209a3093b1debb9418`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 21 Jan 2026 02:05:26 GMT
ARG RELEASE
# Wed, 21 Jan 2026 02:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 Jan 2026 02:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 Jan 2026 02:05:26 GMT
LABEL org.opencontainers.image.version=26.04
# Wed, 21 Jan 2026 02:05:28 GMT
ADD file:a31148f1b2b73c9ddb2dbcb9c6eaf377794bd2a5545e9afc25bfda0d0fc4e29c in / 
# Wed, 21 Jan 2026 02:05:28 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:10:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:880c3ab78503e9d5bd5e9fa7f060185c8b708bbe723e3ff052d6be540d75a79b`  
		Last Modified: Wed, 21 Jan 2026 02:54:08 GMT  
		Size: 33.4 MB (33399085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f623ab4e89aede42d0ac17c3ab466b025e769853ef72fb583d67b2bf772fa96`  
		Last Modified: Tue, 17 Feb 2026 20:11:14 GMT  
		Size: 26.1 MB (26085879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b60c8479d2fa413ac236c3646eda630a6efae8a7f8aa134b182d82668acc9270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4195066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce308e3f02f8a08f17e6dc17c02bfad293525460faa392a0506bf899238b6687`

```dockerfile
```

-	Layers:
	-	`sha256:2de53a3fb4b5672b9ef6230bb6f242224255bb13a4820febfc9b82f68dad75e2`  
		Last Modified: Tue, 17 Feb 2026 20:11:13 GMT  
		Size: 4.2 MB (4188131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8815df94abf69c08cbba2425d70cd1d48cc3272425d388ed56d1fea1b2a0776`  
		Last Modified: Tue, 17 Feb 2026 20:11:13 GMT  
		Size: 6.9 KB (6935 bytes)  
		MIME: application/vnd.in-toto+json
