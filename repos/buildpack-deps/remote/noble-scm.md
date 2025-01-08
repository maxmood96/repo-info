## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:722970809edab74b0a85408f69d6ae9af04fbc3ad50f8ee4596345f89baa01a7
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

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6d50b3e92542a04322fbc2914286d49e5915ddaffcf191c07e06661fad7f646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88764230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131aa2852b90e0ada1162bf44687db88ffbac12639b7a8d6f057c2bfa7a0354e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5235aa939f41c34b69f4fe37736745fde8e1a4676950add7459e7b957c4cfd55`  
		Last Modified: Tue, 03 Dec 2024 02:28:51 GMT  
		Size: 13.6 MB (13617608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cf16388a9a3471d6a91777a42a673b8db99767b831de048212ce4136744cd4`  
		Last Modified: Wed, 08 Jan 2025 07:28:31 GMT  
		Size: 45.4 MB (45394654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3f04deeea996b84aa1dd1dfee85837b0a2f1bfe56fd34469d8686c2b2df4193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8858ee1939cf86150c60e81cac0c8fb87a608744c7ec96f3a8af6fa531324a19`

```dockerfile
```

-	Layers:
	-	`sha256:addc9e17fc74d7040b9ab7245bbaadcde580f924bbad026c4091e477cab1bf6e`  
		Last Modified: Tue, 03 Dec 2024 03:17:02 GMT  
		Size: 5.1 MB (5076115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd67f97ec250bb62ffa5140cbe45a6491aab2a87e36613851e4c406872536f6`  
		Last Modified: Tue, 03 Dec 2024 03:17:02 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c2fe6de00fc138830d287fb0dc0f6b911dca32d344e4701eed3aa2b0c86a015f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88588787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bcc54a6f059b5e96eb76abd6d7c54f157230e6b9450227a6df12a929e8bbf5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f072a621863f98c6e93487af2148d3199cc2cf579bfe20feab8e50641003f0`  
		Last Modified: Tue, 03 Dec 2024 07:39:05 GMT  
		Size: 12.8 MB (12774963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335cf1f7da64ab01e02577f00ca7c83d14ba94593eeb2b94921fa0dd578a4e4c`  
		Last Modified: Tue, 03 Dec 2024 17:19:41 GMT  
		Size: 48.9 MB (48944185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:36916e586b63927eb00c8e6fc63fbdc374caea9a8df5db0df3a2bab37d3fec16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365716965de5497a66aa242643334c3251b18756a3f44fc87b04e53b504d7903`

```dockerfile
```

-	Layers:
	-	`sha256:dc29ff92dbf3d2987aeef7bb9b8c549b1acc9af15014d4fe428d6a049cd9aa52`  
		Last Modified: Tue, 03 Dec 2024 17:19:39 GMT  
		Size: 5.1 MB (5077409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45fd512c1fead54e3108bb7fe7ec75f4060f3a0fd9edbf39d3c7428b311bd686`  
		Last Modified: Tue, 03 Dec 2024 17:19:39 GMT  
		Size: 7.4 KB (7365 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:69e40459579cbc0b138d9a20aaf0d3486dc42eb8b3a836e30cf427ab277de42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87703768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c718600a8934d0b44f5569edde9431dc42eb30d26710bcc02a6d96f08bac5ffe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Wed, 08 Jan 2025 06:48:47 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331da7d4a8631a606292d353129b9398a4db3f2798d686a807920d0a81e2c741`  
		Last Modified: Tue, 03 Dec 2024 05:40:42 GMT  
		Size: 13.5 MB (13452932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04d25eb37c1d037171f5c201d5753407b0902b0f09c9b548efca5b1d914b62`  
		Last Modified: Tue, 03 Dec 2024 11:53:13 GMT  
		Size: 45.4 MB (45358165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eb791a3b3cca1c3b2935910956af05c9087a209ff88a70ac70ef9205d8c79156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5090699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef7269cc872128c8e5932c12378ebd1a268b567dc24551c926c91fa85e57050`

```dockerfile
```

-	Layers:
	-	`sha256:1ada12157811656b092a572f885b9ac7f9ea75283b5e90e82f9b3c671db09087`  
		Last Modified: Tue, 03 Dec 2024 11:53:11 GMT  
		Size: 5.1 MB (5083314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31276f86b42d0658076bc44da5d06e42007914f26474b55afed3926035e7dad`  
		Last Modified: Tue, 03 Dec 2024 11:53:11 GMT  
		Size: 7.4 KB (7385 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:384d387998aa64a6f5d109bff122bdea8b9ab1963ae663995810afaf4a7d2428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100926550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6946101467ca3a91ca35f8d779b675ebf382a27e84ec752d94adbf307d0d7407`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb006e560e9a807b6372fb925c588d9d83a6052a65248653a1f5708527a24d4`  
		Last Modified: Tue, 03 Dec 2024 04:39:54 GMT  
		Size: 16.0 MB (15980138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9deff409e8ce76af2a5a7095a7e708fdcadb9e212359c8655149b857100b432d`  
		Size: 50.6 MB (50557592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c0e1990e1e896cfb17ed7ecabf67bc00438fc31b10d3dfff8831d270ae4fc861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5091142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa976460f062d23b11e4b7e0374784807e804a1c84c7238400828ea4535f2be5`

```dockerfile
```

-	Layers:
	-	`sha256:98cb5d30b844718d1d8bbdaf254185490e39d7b24a525348d26bbaa41ef83c76`  
		Last Modified: Tue, 03 Dec 2024 09:46:21 GMT  
		Size: 5.1 MB (5083805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f843b90490e92473c16e8e26ee5619d996af35343267bf4b7e5e268185f27b`  
		Last Modified: Tue, 03 Dec 2024 09:46:20 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:bfb5191debc6043e213d5fba8deaf56abc330de1eae2e2d4fa1eb38d09f1863a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99158620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1c3db312baebc205d4ae5320db8ea455b1d2c806396175a7f8f3d5d53560d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:23c2e341d6cf3572f2762ef1304c406cf6d4f5ee8ee8719ef289a3b75a8323aa in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0dcc8c973ba119a0fb5275114fd0456179bba1132bdc69f2afa4e1c4a235c540`  
		Last Modified: Tue, 19 Nov 2024 17:38:52 GMT  
		Size: 31.0 MB (30980838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bf3edf440eb67602bc2c6173f31d3292b752b03bbf690c473a5038b858343`  
		Last Modified: Tue, 03 Dec 2024 06:44:43 GMT  
		Size: 14.3 MB (14321082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505f2c8e1079fb73360d2ba6b4c3130e06fd9586abaa35474f69fd6f08ac0c3`  
		Last Modified: Tue, 03 Dec 2024 09:51:22 GMT  
		Size: 53.9 MB (53856700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2ad46ad8d7e5e2137bad7101c0d437b7fee331f0b8d0e6350b5887027183d1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5073996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d3bd34af4146e39294b5bbb3fa5cef688457671071e5506732c9f6c13431c6`

```dockerfile
```

-	Layers:
	-	`sha256:0a4cc0ae30668e7591cd209c89d192583fba68aabb43372e03f01edab1d00e88`  
		Last Modified: Tue, 03 Dec 2024 09:51:14 GMT  
		Size: 5.1 MB (5066659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b02388bcac06974d94d50c9bf05df475bfa01487bba4a6f5101eb76f87477102`  
		Last Modified: Tue, 03 Dec 2024 09:51:13 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f6aa36b071cd1ed3f37f0b7bcc5a2325c8ea64c33d9746502b6992862e3e3cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91894284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5d4c058ad27c00d235e7baf11e7972e559d439a340e03f8b86d1a4b2fd0639`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35190d0c1306f85de6133cb1ceca330cd03ee2f6baead3be847b0c8e4273f57`  
		Size: 15.0 MB (14960770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05107eaec609414c9540f16903f6f4fed09e9055d47bca5a3188db8c2f781888`  
		Last Modified: Tue, 03 Dec 2024 07:57:25 GMT  
		Size: 46.9 MB (46912688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6ed16ad608670de1d059165b62dc4296f911a80f55ef213cb9ac578a594dcd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3f3c4fa5ca2bd0225ba612c07217a53faef57db897899cceeaafa4923145fb`

```dockerfile
```

-	Layers:
	-	`sha256:afe48d2c0a0654f448b9f66dbab36a88607d875e7c911c05e8c35914c9cffc68`  
		Last Modified: Tue, 03 Dec 2024 07:57:25 GMT  
		Size: 5.1 MB (5078452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95f4e0a101ac487e58274d0e6e005419118d9466a66d95d30a72475ea5022f9a`  
		Last Modified: Tue, 03 Dec 2024 07:57:24 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json
