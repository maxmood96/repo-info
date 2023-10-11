## `buildpack-deps:buster-scm`

```console
$ docker pull buildpack-deps@sha256:8ac49cbf136e81a2a51dc27feaae9563820b78fc33412ca5c891982e769696db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ade82879ae8d9e78c762d573b1af9f00ee480f8567e7fb20e46881afe8b9d782
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119966533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ba0f4ae24f85f392a56498e222fc3f5a37a5d5ccbb17634da639dc7e013a3e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:13 GMT
ADD file:5a868c8105f7b621ffe46e19453d846faef824601a70979f6ef2bb46076151b5 in / 
# Wed, 20 Sep 2023 04:56:13 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:23:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:24:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0dfc3f78750b97e03b66f316b37e155e3de173a8ac79942f0511888531fbe5ac`  
		Last Modified: Wed, 20 Sep 2023 05:01:23 GMT  
		Size: 50.5 MB (50498165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830b67cf52132f96464e9186a134b45378cef272f020722032b8d0ccff73e2ca`  
		Last Modified: Wed, 20 Sep 2023 09:32:05 GMT  
		Size: 17.6 MB (17580790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dedca5333820ad46911bb546a9751d6641b13d86f87175818a188b41e0b7fa`  
		Last Modified: Wed, 20 Sep 2023 09:32:20 GMT  
		Size: 51.9 MB (51887578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:59e3ce119afa9de6ff0d4b6e281d14470622ffa12c9fbb953916d25a2cb2fc2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109589972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da97f38b19c65c86296697603f880556bec23ede61a2a9edb02537e34b3a9c3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:57:44 GMT
ADD file:61a164f3dead6329acddcce40680f06b7b0f27e5620a1afd975e186153e42077 in / 
# Wed, 20 Sep 2023 04:57:44 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 15:28:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:28:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6e2ab1511f035b8d0208496939ad6f66778c120d1c102125b629bdb138ce4a14`  
		Last Modified: Wed, 20 Sep 2023 05:02:14 GMT  
		Size: 46.0 MB (45966225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b42b2c67c3bd9bb3552fc4424f51e962669da3a9daf4294ea3a82867faa9ead`  
		Last Modified: Wed, 20 Sep 2023 15:37:25 GMT  
		Size: 16.2 MB (16213379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77af292e4101bab353aa314a3d1abfee18e65d9da12d6550c323dfc8367ebe01`  
		Last Modified: Wed, 20 Sep 2023 15:37:41 GMT  
		Size: 47.4 MB (47410368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1413a4e9eb3fefe019551feac441c7d8762a6b47ce848ee0963e3948794dd457
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118969283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5309fdc8abff9c9bd288a5d9862dae03ed5949c549b9b753f7bd506700c0b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:34 GMT
ADD file:3ec160f0e210563bfac108f23e5034dda5bc7b513b824ee276e4fc6daf80c89e in / 
# Wed, 20 Sep 2023 02:44:35 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:26:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:acd8b5ac4bd39653c2ebe6bd243f4ad2ee504ec9f8feeda9ef727446baf30721`  
		Last Modified: Wed, 20 Sep 2023 02:48:30 GMT  
		Size: 49.3 MB (49290887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f93259912ce217fd32c44f7d2af6614e607291b48753b975c9833a3f154800`  
		Last Modified: Wed, 20 Sep 2023 09:34:01 GMT  
		Size: 17.5 MB (17452055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c73f033657a4472c3fc5bd132b5f8afd8892dba766e81ded996a4cd0898b9b`  
		Last Modified: Wed, 20 Sep 2023 09:34:15 GMT  
		Size: 52.2 MB (52226341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b9714a557ba551d0e25530e69b9c38752fec848204c2e0791697c79dacbd1d67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122841335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce745aed3b333b25b3e5c0db30d1014e3561c2f1044192ec0991f69bb7cecf8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:41:14 GMT
ADD file:47cece2eff96bf7383dd2a9c5632f0ad7bb31b3a459677530f77a78e22658e98 in / 
# Wed, 11 Oct 2023 17:41:14 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:14:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:14:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:62bc68699d611f4c048328a0468ebc10de528260c7823c8938796da30db31a17`  
		Last Modified: Wed, 11 Oct 2023 17:46:45 GMT  
		Size: 51.3 MB (51256071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a664405fd519ae385ebac7659c355b2c380dd5c84037f38e6d3673b2bd9795c5`  
		Last Modified: Wed, 11 Oct 2023 18:25:03 GMT  
		Size: 18.1 MB (18097310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c138636d1c51e715c73bdb28e49fb18fc2d82cca0a21d5641a911f48cd3ff695`  
		Last Modified: Wed, 11 Oct 2023 18:25:25 GMT  
		Size: 53.5 MB (53487954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
