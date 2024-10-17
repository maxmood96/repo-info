## `debian:trixie-backports`

```console
$ docker pull debian@sha256:22fd500f08b73fd2ecdd76b431cefc7020d2ad49b8e6cd4143866ecef4a835ca
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
$ docker pull debian@sha256:1267923c619ee5def03216507595480faca1092ebc1611d9bb477a78555d04af
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53238963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655790310709c57765b72828f221283f692291a09fc4c7fca3cf5478d79ffa45`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:22:22 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Thu, 17 Oct 2024 00:22:23 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:22:28 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e155fbbd3ef115cdc11a5fb249b55d7b70acc80f857011b5898b4624377121`  
		Last Modified: Thu, 17 Oct 2024 00:26:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:308845b62b86b5de23df1d2538783d211ffcdfd4a92a9c74dbffdf6d566f793f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50146321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8b3092e25aac878b9bd42a956fc653967bb2a3a5cddb4d8dc79aadd6f9387a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:55:50 GMT
ADD file:010709d78fdc05933a72549f7cb322633ad7dbe3d97bfcbda0aa10337118fb24 in / 
# Thu, 17 Oct 2024 00:55:51 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:55:56 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f9250cc0718983393b852e9ddb20839b610fbab7fa648abee09b726c74343ff5`  
		Last Modified: Thu, 17 Oct 2024 00:59:25 GMT  
		Size: 50.1 MB (50146097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80b98595d538eb16731477aabc364e7e2be206758e55234545bf718aefed64a`  
		Last Modified: Thu, 17 Oct 2024 00:59:34 GMT  
		Size: 224.0 B  
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
$ docker pull debian@sha256:b1fe3d4f699162db4464e9b66ec419ae36c48c2432457538bbc7a734e1abf741
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54077679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf2fc722e05e19c01e62861a880deaf956b9f7dace8315415660a2f7c6a9629`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:40:55 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Thu, 17 Oct 2024 00:40:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:40:59 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a59559521df839e245332d5a16e23ba795763959727cef4438da2596126781`  
		Last Modified: Thu, 17 Oct 2024 00:46:01 GMT  
		Size: 221.0 B  
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
$ docker pull debian@sha256:d9f5c8b326e774f2058b6c45dbb46c8056078f9beca35bab6f4984fe1cba2bdb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51493024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513743bf8a8cb49ba143d74d76845f3631c231bc1ad4908634823d0394027e52`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 12:27:18 GMT
ADD file:da1da406a30d8c871e2184104ce67d821e790fe334361223691352f3f2de2066 in / 
# Fri, 27 Sep 2024 12:27:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 12:27:32 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0a4dce9b327b8993d0aa8d580f47160e8320c3015f48472eedbf0d06fbb649df`  
		Last Modified: Fri, 27 Sep 2024 12:33:20 GMT  
		Size: 51.5 MB (51492798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852249dac58832478044fccbb116f71432524b611f5009e918d6a491759eff74`  
		Last Modified: Fri, 27 Sep 2024 12:33:30 GMT  
		Size: 226.0 B  
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
