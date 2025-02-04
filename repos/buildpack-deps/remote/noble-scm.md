## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:f959f0254d86cc97e2059af1122ad1f165cfa093674942e174afe65157ff9d88
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
$ docker pull buildpack-deps@sha256:b79f7b47aed24f23f5486c1047e9a8c86c3941402091c178acc9f1ef1aaf6e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91072684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bca72d95b85c99311d1c63dd2fd9ac0b4bee3b2ed93eb890c666eb04e8da7e`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bca5f89848ce8fced9fabc99051bd86546e9b21ec911faa12d1b57517b419d`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 13.6 MB (13612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c239591c8fa2f14b9d884080d6e6888af267d5581800cd9aca9df2581c579ded`  
		Last Modified: Tue, 04 Feb 2025 05:20:45 GMT  
		Size: 47.7 MB (47706161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db5fdb66e6c16e33934375372f2765e3ae9ba4dd6bdabb2c088d421f30df9443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5227624d892aa0359b9c2a9210f2fe3f732bdf2819487b88202a10c76f5877f7`

```dockerfile
```

-	Layers:
	-	`sha256:9a022b0c23577f479164b46a47db9343c2b2b7c92c88c45d94c1b7a74ea7f1ea`  
		Last Modified: Tue, 04 Feb 2025 05:20:44 GMT  
		Size: 5.1 MB (5073857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751a37c758d13b6de22a81dd98828f7660e054da7277039fc7fd8fed7a65aa67`  
		Last Modified: Tue, 04 Feb 2025 05:20:44 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0b56579480d6397bd5904d59064ec81635b77d166f46104541e603def87e8dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90729381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dceb0746fb00b326873deb1d09413664f9eab1363a66ac1be5a8592b02d734b`
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
ADD file:22301ffa2fa465db7a0f07e0c3ddc488f07cc6a745c39e6f450fdbe37da97418 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Mon, 27 Jan 2025 05:10:02 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d26a8223ab81b7619d0fa204eaa4a52bd9e82a52dc44e8e3fd181d828b57c69`  
		Last Modified: Tue, 04 Feb 2025 10:45:28 GMT  
		Size: 12.8 MB (12770649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dcbc6f6efd6544a8f23370c197b454bcf746c394d4ef4477af75913c1ea6ca`  
		Last Modified: Tue, 04 Feb 2025 16:25:45 GMT  
		Size: 51.1 MB (51083749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:12e6e05eb77a2df0ff2692a72d1b55fbf62bc28433b50eb32bd0f1eeffaeb667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7859dabba24d21ee40c29f20195b2f9602c8ba3cb81666e71d071a3f02cd1a`

```dockerfile
```

-	Layers:
	-	`sha256:43452194efc019e23d864284d2b4e0ac99986ae801336f60c9be12c716c4fc3e`  
		Last Modified: Tue, 04 Feb 2025 16:25:44 GMT  
		Size: 5.1 MB (5075155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:186f392c923d1f4f3fc877b5ff95c05a0234e01b3ed48db5a2d2a45e2a05df79`  
		Last Modified: Tue, 04 Feb 2025 16:25:43 GMT  
		Size: 7.4 KB (7364 bytes)  
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
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
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
$ docker pull buildpack-deps@sha256:ebb0c15867c113ac70cf2e3fb3b8edcfe47418958312d031c552e9d276900c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103327115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830a0edd5fa8e5a71bd82022de78784ee5cdd0b58de4123e6da3ee12e955c6d5`
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
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb3acc4132c7aebe44f31c42e40cc094c5403d3a66fea37f2373bf78812b25b`  
		Last Modified: Tue, 04 Feb 2025 07:28:52 GMT  
		Size: 16.0 MB (15958943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e5d3f04eecd25f382d7c6ac4ac3b8ddc8aa83c84e0baeb7ee7fd926a1b15c3`  
		Last Modified: Tue, 04 Feb 2025 15:53:17 GMT  
		Size: 53.0 MB (52978348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9e6dc36ad3409a4d9763210ac8ef014c45522317bf23fb0884e4fd47e0ed2a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5088884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5b4ee7117375a6e21812ee23e0ae909606ea66ab90de39232f880a62132e3d`

```dockerfile
```

-	Layers:
	-	`sha256:5efa67d3a9927cc99fd246457e268d1b5345b41c211f71d3c441eb39f3615caa`  
		Last Modified: Tue, 04 Feb 2025 15:53:15 GMT  
		Size: 5.1 MB (5081547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70a4c7f1b7c40f1f45de9263596e160ae3ad546b0f7e97e2ac8fbd8648198a5`  
		Last Modified: Tue, 04 Feb 2025 15:53:15 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ac57716a31f673328d41905ee068cbf3d1e07eb18922ce4bc381166457a0bcb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101521077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9355b669720be435491e9014a723aa6ca9b19f0e95d1305384a0097607d3c47`
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
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Mon, 27 Jan 2025 05:10:15 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1ff2b444c4e8d1278840900c3e27c00e5987f3c54a529299dbf9a2ed443657`  
		Last Modified: Tue, 04 Feb 2025 04:47:44 GMT  
		Size: 14.3 MB (14317230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec5a422d511e6bec6d017fced317ebf97a5f77ec1f6eff36a777fc69635d1c3`  
		Last Modified: Tue, 04 Feb 2025 08:19:44 GMT  
		Size: 56.2 MB (56219937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:13ed8342d52d164a346aa9b5cb66623fe05636c2934ea795ba1b9e598f5399cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89c54bf63e8b39c08bc48b092a6c6475acb1a690c25fa70405580bc272a43a9`

```dockerfile
```

-	Layers:
	-	`sha256:e76485709ee792b4459b34b590a90e627928fa8bd423b6e42b45b5f7ba2a63de`  
		Last Modified: Tue, 04 Feb 2025 08:19:36 GMT  
		Size: 5.1 MB (5064381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b25f7384c82f182e09fec7b22eaceec3f8a595bcd3522a657ed9ee9e8c29af4`  
		Last Modified: Tue, 04 Feb 2025 08:19:35 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:14f5b18a8d3325c0aceabebe8cd762bf3a65f728d72f7b061c7e9df305b9a0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94420581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7cb2db7e6b493a23389546282950b17a58fe374836a93a6806036f3dae3468`
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
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Mon, 27 Jan 2025 05:10:30 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cacc91036ba2e7e50d76ff2b2593ea149a0df971bb8069b913263b87ff517ac5`  
		Last Modified: Tue, 04 Feb 2025 07:34:27 GMT  
		Size: 14.9 MB (14937386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ae03e34cf459247f3c12fdf3d38cb8c622dd2d321ebd9a1ced772465e12c97`  
		Last Modified: Tue, 04 Feb 2025 11:43:56 GMT  
		Size: 49.5 MB (49455632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1525fcbfa02c33484bb09e040a04e9b78c06c3672bf65abf24411ee3e09a500c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5270daea82df40b76ac970b7fa7c5f3be156d08cf87ed6a6907edbe2a94055b`

```dockerfile
```

-	Layers:
	-	`sha256:c35fa74f8bb61c22c923b1e0ae52e265c1c6f23b8b4bd3db45b9054419060965`  
		Last Modified: Tue, 04 Feb 2025 11:43:55 GMT  
		Size: 5.1 MB (5076189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb7c13a886117d13a191bcc5c275e7edeffb54e8f7d21e7471bee9c043578fb`  
		Last Modified: Tue, 04 Feb 2025 11:43:55 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json
