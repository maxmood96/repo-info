## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:0ee37727793ffc315f2a22a704767f9ccee5711aebb573d04c4500b82b352c0f
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

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b3965b386cbda02f0b375e37e2a3cadda2d59865dd4de02e8025671cb2cb815b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76130414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ccba197902a5acdd764e8c87d76e22f33c3e214508339bf0b8a8ba3684edd3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6828c7dda7e5e4b9c82ddb483379bdc791aa9b7cecdce2c883c603e7806ea9a`  
		Last Modified: Mon, 01 Sep 2025 23:07:56 GMT  
		Size: 7.1 MB (7106278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3856fb40e8823986f0d2b16e4bb928a603347223ee232458482a4a5a7b70b7`  
		Last Modified: Tue, 02 Sep 2025 00:12:14 GMT  
		Size: 39.5 MB (39487201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b198a17f0568b7e3bc5c04488cbfe35139de3befaac1a8508837ffd57eeea5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549f45c2f7c4418688c8f668b736e712247cf3648bff90eb94559ac4e8cf9fe5`

```dockerfile
```

-	Layers:
	-	`sha256:0b6b164c4cd7b05b52190a315968a6006e0b967d46907835af5a67112b439727`  
		Last Modified: Tue, 02 Sep 2025 04:19:43 GMT  
		Size: 5.8 MB (5812698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80912376a1c4a1bd214d2b3dd79e73f2f68afb244f66923cd71fe06b79212b07`  
		Last Modified: Tue, 02 Sep 2025 04:19:44 GMT  
		Size: 7.3 KB (7323 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3f1cc6e581c34cc874cab705a373cd13e6cf6406764523f77c4a4ad76311dc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75904916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e0b2c94a1c5f5a4311ec74dfcebd1d65dc1040acb3595ad71059948dfffc58`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:7939f961de8cf091ed251aa1d8e432c16ec7506130ed39a1db4028efdad8fbfe in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:33392950d914bf1e16e980fc0bbcec6367a2d2b8ecbd726dc5fc65b4c96ce79f`  
		Last Modified: Wed, 01 Oct 2025 18:17:15 GMT  
		Size: 26.6 MB (26643435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9171b5af741a0ace05e08730bfd3e3d15b256638bd578879f8bec957a53865fb`  
		Last Modified: Thu, 02 Oct 2025 01:11:04 GMT  
		Size: 7.0 MB (7009648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ad66e157af2e652af3caa8bd7ad08a7179d484f1b6882961c023ec58b25c05`  
		Last Modified: Thu, 02 Oct 2025 02:15:10 GMT  
		Size: 42.3 MB (42251833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6a5cdba9c7597b9f9cea28730d6394ee323006493ef2894b0a2ecb8f9077e45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5821365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29af769892639733d21b40cbbb16e854bb4f1a78df8923b82363c2c535958589`

```dockerfile
```

-	Layers:
	-	`sha256:e09a84db7a849819f8af8d8e64874a910bfedfa28a7fe17a74dd90153a00fbc2`  
		Last Modified: Thu, 02 Oct 2025 04:19:49 GMT  
		Size: 5.8 MB (5813978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a45bbf037fc4872259915c020062e207f686ba29fd12170f7ea2f73cdead484`  
		Last Modified: Thu, 02 Oct 2025 04:19:50 GMT  
		Size: 7.4 KB (7387 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:84a1620a334fbb2de619997422e99abb4d31dc64f5e8b158273302569d07af78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73817717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6768513c81e369faaa9094cf09f73943a1fc4094cbdfc3ec67150585f3772e34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544fbec883712e8b92ee5a8fb96accd816f1bd25c1cb91370bc6a156f3923503`  
		Last Modified: Thu, 02 Oct 2025 01:11:19 GMT  
		Size: 7.1 MB (7052114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0761247749305bde9fb9bf7bfca381206a20dfde11549ca1ba13996d4f60209`  
		Last Modified: Thu, 02 Oct 2025 02:14:20 GMT  
		Size: 39.4 MB (39382496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:872f592fcfd1152989bc6383983e002b209c27475b538dab78f32beb0453e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5826496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7c853dcd17fa77ddd05ff5103ebcb93c085881728877b4de2af64dc532a252`

```dockerfile
```

-	Layers:
	-	`sha256:6b387d85e53d0c3ca58de3db9fe8d8886af71127054edd83c3355a9d6b0d8ca2`  
		Last Modified: Thu, 02 Oct 2025 04:19:55 GMT  
		Size: 5.8 MB (5819092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860fcaa6f50eb6de4bb4e8a44243f7bb5dbcb96514aca7fc2d19c9fcba20b5e2`  
		Last Modified: Thu, 02 Oct 2025 04:19:56 GMT  
		Size: 7.4 KB (7404 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f7aee72c4eb16396af56097003fdded10cd399a713340c862158031d8376529a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86388321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5ab7fbe4a05f7430c1c1bee3571c7ba65efeb96d606f49c246a948e822dbf7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3f77bc9e4ab6e5fb5af578f087cd1cd7d1b42df4ce3edcb7205e77fa641e55`  
		Last Modified: Tue, 02 Sep 2025 00:12:15 GMT  
		Size: 8.2 MB (8184933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06d2fcee6246a83413eafcec3d64fbc5be759a0ab354df9c761fc5007cd6746`  
		Last Modified: Tue, 02 Sep 2025 05:24:06 GMT  
		Size: 43.8 MB (43760164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c557e4c516cd035070f634249571f7de23b5d71cd921d082337255fc341d5708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bda4174e70a34b84ec6730eb648439b415d71519fbd00baf6259440fbb73e7`

```dockerfile
```

-	Layers:
	-	`sha256:65f5a2ed2cead9f696a06e19ab5b6a70641bcabb6784c0e32c96d2bf36cee8fb`  
		Last Modified: Tue, 02 Sep 2025 07:19:36 GMT  
		Size: 5.8 MB (5820542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8983fbfdb20106c5b678fbcf2392ba47c51f4e310c227909963185fa08022212`  
		Last Modified: Tue, 02 Sep 2025 07:19:37 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3d135ccb3c6c545e7e72fe371bb9eeeef730fdfe419f3e034ab5038d6b77a00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76467012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debfad22e69534d7b0d2beb1dd5bc731487353379a97f218eb246bfc1ed22f88`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:c50534025103b387d6edca09570ec78d030f9514a469228d4d2c12ddbc059678 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d152ae8117dc009abe5def1b70dd1fee217a52c100ea2406284b82890b29223e`  
		Last Modified: Wed, 03 Sep 2025 03:52:06 GMT  
		Size: 27.0 MB (27042655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2827b5fd296164594bbbb195caef81b70a3799001441c64ed9d1c44305d6ade1`  
		Last Modified: Wed, 03 Sep 2025 16:00:58 GMT  
		Size: 7.1 MB (7118262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d419b3a38152e2f0763a6d96e4ff0628be5a7d8f45e983beaa5a6c0de269436`  
		Last Modified: Fri, 05 Sep 2025 14:52:58 GMT  
		Size: 42.3 MB (42306095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4744aabdc1e5fdec85d239396cd5de1b0983d2b81920f7448dd7f4887d412863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df848d755aab47630db4c0f31861ad4ed7e8bca27178d3cf56639c4ce37f4d8`

```dockerfile
```

-	Layers:
	-	`sha256:7507524d2390556a63e7f162d738dfb1d846feaee21810dcdab30c9b5ba4688b`  
		Last Modified: Fri, 05 Sep 2025 16:19:39 GMT  
		Size: 5.8 MB (5803084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d48e383861d16cc90e7043a7cdd1e477ec3d005296374ed74b7afaff303e4a8c`  
		Last Modified: Fri, 05 Sep 2025 16:19:40 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cb1dd6c16e527015d3eada940a47ef3b912f0afa71e9e788859d810daa3ed12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74441299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0218f861b0f0a4ebf561fab8b72bf29434d8b70dcd79b05d573614916cf5cf45`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c17dd0c731fba631ccfc3aeb70e205e57d15badc6b26edc465d60bb61dd3c1e`  
		Last Modified: Thu, 02 Oct 2025 01:11:00 GMT  
		Size: 7.0 MB (7018299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7a6b2fe5670a7425cebb606528db0b3bc0b822a68bc9de4e677f95e0e8f766`  
		Last Modified: Thu, 02 Oct 2025 02:39:57 GMT  
		Size: 39.4 MB (39419587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7ceceadf25f3c01eabc20d628d0022353453e1f83a38083d5020eece77c81e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005660f332aa0ef882856316ae2d9ade4212b9a9861b469d49cc7155c76649fc`

```dockerfile
```

-	Layers:
	-	`sha256:c23a36a111813823d7296dc875fd20a422b9a750f82516e64d39b5f556617df4`  
		Last Modified: Thu, 02 Oct 2025 04:20:11 GMT  
		Size: 5.8 MB (5813617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0d3cb54c89cd7a4c2fe215cc9d4d84e299629fc7706f54616edd3f27165fbe4`  
		Last Modified: Thu, 02 Oct 2025 04:20:12 GMT  
		Size: 7.3 KB (7323 bytes)  
		MIME: application/vnd.in-toto+json
