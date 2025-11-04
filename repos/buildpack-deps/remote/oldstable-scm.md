## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:91712f381ac69b69d8fc8a3e6d1a9ab7c268deca9d6eb2ad1984337b22a1e43d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2637ed71dcd6755ffe7ac1be1b620e2fa193b1aa1fbd54875f568c4b5bcfcdd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136905866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a5d3d43f39c710ab4b4b606adcdf7b81747189055b82e8366956dc8b5e4d6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279d33abc52c7384e0cbbb666ea22064ea29b50a968ec29ae3ad817f62e16e7`  
		Last Modified: Tue, 21 Oct 2025 04:46:37 GMT  
		Size: 24.0 MB (24028898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa5a418829f3daa90a80438cd84706b5f7fa0c795eb7936874864ef1ab7b0c`  
		Last Modified: Tue, 21 Oct 2025 04:47:27 GMT  
		Size: 64.4 MB (64396405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4f69db58912873eda77bac8742773c520a14e1092e0c5bd29ed6a5fa308af94b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7972758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8797a31a3c92723e3959c326d06cbd90a34ddb1149e8a114c9e68ab27c30f74a`

```dockerfile
```

-	Layers:
	-	`sha256:dca1d79748e1aeab19fb5a97c8145735b260bc2ad8561190f68ca18bb0746d56`  
		Last Modified: Tue, 21 Oct 2025 10:19:58 GMT  
		Size: 8.0 MB (7965405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e0ae39cd5dc4118e8d6807fa23e94730b58537bb7d5aa236e7a7df595b1998c`  
		Last Modified: Tue, 21 Oct 2025 10:19:59 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:eab2b623b872b86624ba16bf9a23dc36681f22e12120ab4b5e2d783c76de9818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130732405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed54528c455c6ffd810b5d3e74515e89d269e5f3742cb08b9a8a4b2a9db5cae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:27:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:51:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d0780482d9b97d506bfd55bf3b805f2de1b9731c75e1b5800b5d53bb5388e1d8`  
		Last Modified: Tue, 04 Nov 2025 00:12:37 GMT  
		Size: 46.0 MB (46016089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68533da42b7795728d851e519aa05d6a90a43ea0bd8e6cf63e7cd6acc86ac61f`  
		Last Modified: Tue, 04 Nov 2025 01:28:06 GMT  
		Size: 22.7 MB (22705759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15672bb6096ab5577e4b18af07dd846508a657cffbc1c2eab8f3e8e8739f219`  
		Last Modified: Tue, 04 Nov 2025 02:51:46 GMT  
		Size: 62.0 MB (62010557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:63b3529519b815b17eea4ecf13544768df96dd655b5c5f0753d48abb2eb892fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ca03885728360708d24b2ef6700303549108d2945d84116cb86dec4e968a3c`

```dockerfile
```

-	Layers:
	-	`sha256:ccee096f27287eb6996f90e10591a4145368564f3ebccb992afb198c4ea46032`  
		Last Modified: Tue, 04 Nov 2025 07:05:20 GMT  
		Size: 8.0 MB (7967263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e293fbcff8e1aea71b7afbac1bd282433e7c474b4cb2ae620196b7a367909d0`  
		Last Modified: Tue, 04 Nov 2025 07:05:21 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1b3a7dfe3c6e23613fbe3fee73c1279bf76c75d6f1cc2b909338c27e7bdfba21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125783103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45320865fa4712522c4ea920ae1316759924ec89257f1aed70222d8320e7a56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5dbe800c0d6104b6df988b153994b0d1b5c022197b54cf928820e3c23d00c7eb`  
		Last Modified: Tue, 21 Oct 2025 01:16:21 GMT  
		Size: 44.2 MB (44195910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178651637d26f6ae6fc6c2a3297b37f8bbef12e80d822930b05b14f51a262382`  
		Last Modified: Tue, 21 Oct 2025 02:43:48 GMT  
		Size: 21.9 MB (21934505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14411cad8875b2a42f951ec95179ed8a844d1522990ec8b96f1c4d269ce3c71f`  
		Last Modified: Tue, 21 Oct 2025 04:11:04 GMT  
		Size: 59.7 MB (59652688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9405bdf46bc6bda470b492da226630a43ce8752433a20727f1881246cf3d2a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eacba2b1c1023434e56a369339e4a372c8a2679cf75e03ecafbd9c7a6fafbf3`

```dockerfile
```

-	Layers:
	-	`sha256:77b31dfad0f3b4fc3f32a34faa650596d8e153306d2401d5ac873eaa58dd7125`  
		Last Modified: Tue, 21 Oct 2025 07:19:58 GMT  
		Size: 8.0 MB (7966682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96355444d7fc92e6c3fd8eea075d22aba287b8e2b990ff5e3554059cc634d29f`  
		Last Modified: Tue, 21 Oct 2025 07:19:59 GMT  
		Size: 7.4 KB (7417 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d693689cc6091a0be22663dd8acd3f4e24cc1f985abb06cdc342459e4385c603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136327918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ab2ac400d0926e0b58496030aa6e1b60884dc35a1304ec47d0b9c82acaaf5d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7397bc0ae282f3ecd02217ad720d86eab3a3d325f0bfed57fc864c2281a58`  
		Last Modified: Tue, 21 Oct 2025 01:46:17 GMT  
		Size: 23.6 MB (23597991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd15270faa4e93fc4bcc62caecce8d2f5dfc1443d3c99572dfb689973b24c0a4`  
		Last Modified: Tue, 21 Oct 2025 02:35:23 GMT  
		Size: 64.4 MB (64370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:30a4fc97b2aa0b74fffa2ee264bf9869f52494d96944969bbbf2c8c33e0ea634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7979231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2cf887aa41f259c3cf523e87f54b655bd63c54f45a395aa0e5f2a37628180c`

```dockerfile
```

-	Layers:
	-	`sha256:78fe2c5c16f12a8434fd914d312770e7eb540e35c164ba64c22d864c2a3c29c2`  
		Last Modified: Tue, 21 Oct 2025 10:04:26 GMT  
		Size: 8.0 MB (7971798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6cb37422828b3c1740c917e72e0ede0518d6c30f61fdd653cf8c88b85ded5ea`  
		Last Modified: Tue, 21 Oct 2025 10:04:27 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:48445d63e09de4fb4d7d5221b5b237afd93d85ddb858040d8d06f456266026b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140562830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932a578bed415deea6676e579dd00eb0d662e5b5a31ef9bc2f07fc2b10f9c6a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3426ba65368da59a25d050cab9d7713d7873264014ab6dfaa6b0c33f0632cb80`  
		Last Modified: Tue, 21 Oct 2025 00:20:21 GMT  
		Size: 49.5 MB (49466720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f14d3e3fda83046fcd165bb976221020273830b54d963f634e53e7796b47053`  
		Last Modified: Tue, 21 Oct 2025 01:52:59 GMT  
		Size: 24.9 MB (24864208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39058bc352da86cee9643b9b447133a3295983ec455cdba2fac6cbbed8726db6`  
		Last Modified: Tue, 21 Oct 2025 02:35:47 GMT  
		Size: 66.2 MB (66231902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fb8ccbabbc68683fd4aecf6de516378b2a1962c3397361ea18b6768a44b455a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7968894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa974f85bd41d40c91873b052ff3b00e8658a9d368fbad4639919db143dc014`

```dockerfile
```

-	Layers:
	-	`sha256:93f7ba452ca7dd431ef30b2aaa9012ba78f2b2e1699ab3505cadb5eece7ae1db`  
		Last Modified: Tue, 21 Oct 2025 10:04:33 GMT  
		Size: 8.0 MB (7961564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4133a9819b4bb9f315e3a8814721f8103b6b0238a9034798f572bc89c469d086`  
		Last Modified: Tue, 21 Oct 2025 10:04:34 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:086cd1779eeb997cbde1dfbc1af1ffdb21a49b0c42aa8bfd5f202419320c54fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135683961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4870f1811ad7825f7436aa1c996010a24f4cd34cd2242cd08b6aac69fc9c915`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4ff7a7a0be4afa0c088333063434d872e5a67b49bc2165e0d5f1c8b45e31c387`  
		Last Modified: Tue, 21 Oct 2025 00:19:28 GMT  
		Size: 48.8 MB (48760743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ada83e05f36ace3b39ede326eee5e8c640f47f0d217601cc47ce49334a0f7e2`  
		Last Modified: Tue, 21 Oct 2025 17:26:33 GMT  
		Size: 23.6 MB (23613801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20eca72dd31bb50cadfd79b7ad12f89f5688c744f6a098004e516ee38f52407c`  
		Last Modified: Tue, 21 Oct 2025 23:43:20 GMT  
		Size: 63.3 MB (63309417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2d31031eb9cfe7db4b8f9b6f3e1b405b0c60c8883bb8c8e5b986961451caaddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4b488346370f601e4ada90d3cc2a91d53bbabf8155aee620cf76e35d3c29bf`

```dockerfile
```

-	Layers:
	-	`sha256:9efe47e506eaf9790350e68beb1acc4c5e8daa353387484a2fcae49e821f71cf`  
		Last Modified: Wed, 22 Oct 2025 01:20:07 GMT  
		Size: 7.2 KB (7186 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a4b6d6c3346e6a48c7fa3e56a4b4babcaf261319f65f43c44c150ac848dd61aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147844967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff81997b1f577a5dfa4255f3c2613e17d2ab37b640d4d5f35186cd8fd1772028`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:24:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:24:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a69074b98f99ca928580ca93ef45b80d247ceb89abd2c09f9515ba7ef4ea70`  
		Last Modified: Tue, 04 Nov 2025 00:24:46 GMT  
		Size: 25.7 MB (25672054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f89c76b3026966e039b432e1b66b1655c47c97f236438dc626e5acdead5cd`  
		Last Modified: Tue, 04 Nov 2025 06:25:48 GMT  
		Size: 69.8 MB (69845633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a43eba88c9e50e532ed63c507949b6848497894eaa40397031e0e7887291c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db042ff6105b75f8b5b83b5cbc0b45c890dad28aa9df15a33a2a6e77809723dc`

```dockerfile
```

-	Layers:
	-	`sha256:ab598439e18c1ff8c4dff0304429f20326de2e1aa224cf45e1f1c3e865912793`  
		Last Modified: Tue, 04 Nov 2025 08:20:18 GMT  
		Size: 8.0 MB (7973276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54c12927b3639be1f0e144b9a3fff303bbbce3b25313580d380f721abffa8e23`  
		Last Modified: Tue, 04 Nov 2025 08:20:19 GMT  
		Size: 7.3 KB (7342 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3c80ff02de7bd44636ab549bf537c4c4067b18f39d7e75cbae02837e96c17d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134666235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9714e6a4068cddd05bcf0f02653c4a6d3905273d9699d4f18092695fb09cc2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:769a86a44e9ad2fad1b0132047fcc9c080f859777f09d3856b818bc85f1c5895`  
		Last Modified: Tue, 21 Oct 2025 01:19:50 GMT  
		Size: 47.1 MB (47137521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca271e8b0e27269a77c65ea555986eaaadf5db02b1ac24f66f8ce2e45a475b`  
		Last Modified: Tue, 21 Oct 2025 22:50:23 GMT  
		Size: 24.0 MB (24027291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944e6bdda425b877e973cde5b6c8eeabf7eed45bfaba0fd705b4f180a07f001f`  
		Last Modified: Wed, 22 Oct 2025 06:00:23 GMT  
		Size: 63.5 MB (63501423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6fa386d2925bc30b42efb5dd6daea14bd1f51837cc64262f3788805fc94c0af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dee257afef5cd63d49a5b31cb02f27ff654f5b1bba7cb55045f5c1f657e9a27`

```dockerfile
```

-	Layers:
	-	`sha256:a35e3ac1b21f5f2a70fa2340245d284a8192eaf13acc8b4487c8bcbc40157c0d`  
		Last Modified: Wed, 22 Oct 2025 07:22:20 GMT  
		Size: 8.0 MB (7961718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89f304af6998124e058ac37873dabdc97cb57bb49d0b8987d39ae897fef16585`  
		Last Modified: Wed, 22 Oct 2025 07:22:21 GMT  
		Size: 7.4 KB (7351 bytes)  
		MIME: application/vnd.in-toto+json
