## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:41bfec9f80f4fb5b214da80c857e404d9c2b7b8430981b6c9d642ac345067fea
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:d6d0958d1356d5302577fd55adf612e44942fa2c36594f8c2d2a30e9f7bf4b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53755047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cff25852153d9b041efbb05dcf45b9fa2380267609f6fc43dd1d778ac93a3c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de03f72044f48acb9229642df2d73a80eeb717ee8466b10bb0221d42db407d0`  
		Last Modified: Tue, 01 Jul 2025 02:12:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:949fa84a2ee29808c94a211de3574288dc68417f0cebcba505b653994501c2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4030148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbac22fbbe4e94b6270e07e2a4d0d57c828bb585b06842d46c9aa24ca8627a64`

```dockerfile
```

-	Layers:
	-	`sha256:df77974e03d4f404d5ce52b8fe0e9803656cc28e1fc903f58c0b80b012abb921`  
		Last Modified: Tue, 01 Jul 2025 06:23:47 GMT  
		Size: 4.0 MB (4024301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2603b18ae26285bf5ba1f7389ecfff13054c82393eee9730e6949426941b523f`  
		Last Modified: Tue, 01 Jul 2025 06:23:48 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:f44fe1cb81fe77e1c3a9b420e3e3606afa76bb8e6451eaeb13b2bae4f3e57282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49044184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f64d7179ecbb38655bb4782fb49cd3e9d76c363dddbd6af65cbb7f0954d9fdb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:efcf40eae0046ccd92d3b47ff685e1e9cf7a34d0a92f6de893078f115e01f20f`  
		Last Modified: Tue, 01 Jul 2025 01:15:14 GMT  
		Size: 49.0 MB (49043960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4c530dfe3c35890c2d16d3a1a22455e03c47be1b00fb701632f8885439d0c1`  
		Last Modified: Tue, 01 Jul 2025 02:12:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6e6a4ae4a4bd5c80b7967d7c7fb3c8352f40605a74542d4be36c23b87223aab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd10165940f5a8aae02efe7098cf357fde2ff9bc9122bf1065ce7c82a362113d`

```dockerfile
```

-	Layers:
	-	`sha256:a778796094a93f7534313f0b2071a5a92731d59b2134530360d00766b8d392b0`  
		Last Modified: Tue, 01 Jul 2025 03:24:55 GMT  
		Size: 4.0 MB (4025863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a84db63f8f4a36f5f29197bbd15488f50fb01d7de1f863a720bb18968145b6c`  
		Last Modified: Tue, 01 Jul 2025 03:24:56 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1168b6b669e9cc6afbf352519ee04a4233f0c39e17e5bbcb7a434f9c207793de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52252480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581835b95178eeec00a3123246b6870153553fae5c52abc44b5f80ba73d8f3ee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60048776700cb99ca6cda3cda3ef3818ac460e2ceda318768e72e2b01602c543`  
		Last Modified: Tue, 01 Jul 2025 02:12:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a7fd40656efe41b910397c66972974afe95bafbbe036ec828cd4438f48385c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4029796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2b63df745a44211670c646928fbb3f44af1a3840673d306370d3fedca193ef`

```dockerfile
```

-	Layers:
	-	`sha256:07800634365333d86df3f578f31ae63646e336970069d7982e4c5c9e074f8f46`  
		Last Modified: Tue, 01 Jul 2025 03:25:01 GMT  
		Size: 4.0 MB (4023881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b559d2a951d29f1d3fc317d3e489036de89d88595ef46b07a1565b9e854231`  
		Last Modified: Tue, 01 Jul 2025 03:25:02 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:1644d4d534cc17c6c3c612f95e83a8208a6183cffdd687a860bcc4bda753a717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54690159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dac017bd4e928a074617338f3ddaa9cfe47087a500a05638c250ccd09376ea4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a7b96ab801267098c868bb59ed64caa660a335a05cb99c84935ad31a2aea45`  
		Last Modified: Tue, 01 Jul 2025 02:12:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:aa13f6ee95b7fd2ce6f2dd68f2fb715f474d6642688f268b293f75b2877f5d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6875e2cd0aec7038544440e09e06452bd08c1e700613f0874e2a2508cfb26a`

```dockerfile
```

-	Layers:
	-	`sha256:06c52c8917ad0f1f2a4219e71076c3b7e93bec17e241702e3a12e17808ce7d3e`  
		Last Modified: Tue, 01 Jul 2025 06:24:00 GMT  
		Size: 4.0 MB (4020855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf58cb8a30afb8fae670d6fab76f88e893e9d5c6288beec9aa8c12eda9fbffd`  
		Last Modified: Tue, 01 Jul 2025 06:24:00 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json
