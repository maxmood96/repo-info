## `debian:trixie-backports`

```console
$ docker pull debian@sha256:faa263739d0dcb08e8b525b4384408cd1781b7bba0796868f18c247a1e879f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:e39e73e4d61bad6bea2fb84f457313cb6324d14a47b24f78d2a4cf78180a7192
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53178259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d9cbe39511dfee8ffc66b620f000d64158b714756589eba79eba5b752ceaff`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:31:34 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
# Fri, 27 Sep 2024 04:31:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:31:38 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45911c485bc573b6a5d7f0ce13e0bc1ee1e1987e7248badf6837b31c1d0d5092`  
		Last Modified: Fri, 27 Sep 2024 04:36:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:94b321c59ef4fc929040b7f7228faa7feb99a497f46646c430eac9f333f489b5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50140897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3d3fe226b46020e3e55c37098d58be10bd54810a6b39bff337d16803213759`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:20:21 GMT
ADD file:3b9d682e7d68f9176882ad1aa7f4dcae0a81c3f93bb197b8d0a3982c411d2ae0 in / 
# Fri, 27 Sep 2024 03:20:22 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:20:25 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:655ea019a1ac93e4a06df6c69d688fcb77e3e8581a9c73eaec0ab2559d7233f0`  
		Last Modified: Fri, 27 Sep 2024 03:23:36 GMT  
		Size: 50.1 MB (50140675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686af32c84a13466526924a1bbc0ea1e170dffe13ec76d8b3b809e54e4a13e73`  
		Last Modified: Fri, 27 Sep 2024 03:23:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:52242ade5dde26246741cca016d3172fd22754436fa5c975c90a668fcd2f0e15
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47634176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f8ba1d6131b761bd3c2ae9d09f9af7a6fff1eda11f47bac56a4e73e1387103`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:15:43 GMT
ADD file:13242b1f67d07c997aa23e4b688f29c3a6c6dd2678f15f8738e88d4e66cd5ad8 in / 
# Fri, 27 Sep 2024 05:15:45 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:15:48 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2e00dc0285e0f577d99c5fb34081dcf709cc26a9e85129b9e7bf7486f41e9f93`  
		Last Modified: Fri, 27 Sep 2024 05:20:03 GMT  
		Size: 47.6 MB (47633953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe49c26d40cad0fb4ef055b6155b16999828177a2519fbaa37c1bc40596dc23`  
		Last Modified: Fri, 27 Sep 2024 05:20:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:0bb40f361959f0bd1ad9329942c330c48515441e4c665758fca25b2e038d9282
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53616824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d09aeaac92ddacd3a06ba9782731c24139b02a33e941aec8977aac895836b9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:36 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 27 Sep 2024 04:39:37 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:39:40 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211876fa43c14a344732571bec70bc57f5e13c6ac6d883dc301b9370ba6a8f7e`  
		Last Modified: Fri, 27 Sep 2024 04:43:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:77b1a04072b18267f674850aca95335e25b352be233831708aecee7e08393398
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54060185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd05152c7780ff1cf5bfafaffdac35f97565e00cba8331d45a496338d0286c6b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:25:06 GMT
ADD file:ed6c137f2444326ea2aab7c98ae002052b2a872d9931a0de81cfd9212f14f4fc in / 
# Fri, 27 Sep 2024 07:25:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:25:10 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a2ccf63332f54ffbc2e94366ea06b762b69ecfb3e405c902e5a835b8aa2dce0a`  
		Last Modified: Fri, 27 Sep 2024 07:30:29 GMT  
		Size: 54.1 MB (54059963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0409d00f6165955cdf5440058343f98058c38a2b496bb5863002dfb6ec373b6`  
		Last Modified: Fri, 27 Sep 2024 07:30:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:51e92f476c65933f8b5cc3fa07a8fb3bc865a78d103fa2d234f969e539bb5bc0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52096617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943522ae4f007195f784ba08a40dec7bf3fb37568fb9e7bef0b585c137b46899`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:07:36 GMT
ADD file:36ad397edf2d75e04dad5f0c65abe533f9f2e989bf5ea18e70a4df00cc6e490b in / 
# Fri, 27 Sep 2024 09:07:41 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 09:07:53 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b62fd707f1ed2218f3c1012d35ec60cef1c2b262cc2ca3f48b17a6725ccdf4b3`  
		Last Modified: Fri, 27 Sep 2024 09:15:53 GMT  
		Size: 52.1 MB (52096393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1359abcd6692c11f56f77150ce2c435b046101991f395eabb8dfd586d6a8fe`  
		Last Modified: Fri, 27 Sep 2024 09:16:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:0011ea1ea3cd0a53c3c2726ead1b1b7494a4b7053b2bbe7de97251d126839a59
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57100582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8e0ada2b4fd8ad21330f37c04e2bb0157c311cdda957bfbe507e24de3a0fb3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:34:36 GMT
ADD file:330305dfad891b7801b7bc1444b22086f483c0101ecad9aa8a8e0d005896f0fd in / 
# Fri, 27 Sep 2024 05:34:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:34:42 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1c9d9c0ae5911d02f7f099685f31c9a3bdecfb20000d904113c26e622dbe3be3`  
		Last Modified: Fri, 27 Sep 2024 05:38:22 GMT  
		Size: 57.1 MB (57100357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69d4479b0b85256ce17229674314b626c8c19570a36d504e63cd61f13a98a90`  
		Last Modified: Fri, 27 Sep 2024 05:38:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:96aad8116036d4d010e4f2bc278ad248e89c7656c58e10752ed50c12bd55ea8b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51475751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42d8ce856fd234709ff99aaa64a19e9aae2f6e872f552ddc579f496fd9237e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:28:03 GMT
ADD file:3536049154c2250abe969642d7b35b085e3d25447b8953cc1e072b690a306aa1 in / 
# Wed, 04 Sep 2024 22:28:05 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:28:17 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:38a3e7af214e5e0705f0ceebc8bef13cf31414ef0eb3f3ad8a05574549c77869`  
		Last Modified: Wed, 04 Sep 2024 22:33:47 GMT  
		Size: 51.5 MB (51475526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe853d9c0fbb58c46d314446eeb6458612c8bdf15d74756dcf70dfbbc608cd3`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:a32895ed5e20fcee4559da7a1ac2518809785c186f087f4adae78b8cc69bab83
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52771257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18602316883d3c666b5b45a45a6bbafb1735beb3b0f474d4c5d00fdf02dfdc13`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:45:24 GMT
ADD file:62bc4f2057452df8dde276d456f3954e7e27a723040dd9314069695b18b4c75a in / 
# Fri, 27 Sep 2024 02:45:26 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 02:45:34 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5d4e554dd357d755b1103e6fac1ca2fe641d4ec4ce0581cc222f4bffe8b54c0c`  
		Last Modified: Fri, 27 Sep 2024 02:48:50 GMT  
		Size: 52.8 MB (52771035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f1072b535cafb335f746b5e43c1d1c9289b43ddaf30e4f36d52dfb56b09885`  
		Last Modified: Fri, 27 Sep 2024 02:48:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
