## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:f945dcfdb1e77d015c0b397a2e20db2d948a998de5a8478533121d2f44bee88c
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
$ docker pull buildpack-deps@sha256:139f681a4cb4df9d568c1cb692c1c3446f4fc10a11552435971c190bc43d7b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88789143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62db256a1e05e3dcf5787f4d84241c230aa2b2ca3c4cc90795a57528c265103`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 09:12:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450086accc6bf61159108eda83fd8a98ffb3d28b7b751cdd690a270df67a3fd1`  
		Last Modified: Tue, 02 Jun 2026 08:11:15 GMT  
		Size: 13.6 MB (13631676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a4502a619876b8a7826e9c38e999c517f266ca04e89c208a5583056e6bfaf1`  
		Last Modified: Tue, 02 Jun 2026 09:13:09 GMT  
		Size: 45.4 MB (45424662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5186cd63e7d185ca27f626db42fc84a7238f5c8328cc91aa0619ac20b27ea6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fa435e1a1c1e368f320c0ac3fc2b2974380a641aa4b229b5e2e295071685e3`

```dockerfile
```

-	Layers:
	-	`sha256:3489d8852c39ac7d35e19a9630e3a94a389fc89da3a934e9ec4fbff79310994d`  
		Last Modified: Tue, 02 Jun 2026 09:13:07 GMT  
		Size: 5.3 MB (5276076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b919d31bbfe8ccb6a84c4410f8075d647b88d72a8ace85099b4fcd620331a79`  
		Last Modified: Tue, 02 Jun 2026 09:13:06 GMT  
		Size: 7.3 KB (7261 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:486cff0759d0351c732415d44664788bd5adf1649a9f4966069287949788ebbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88586881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5876b4900a67f9be3708c266a3e5b196bfaad1ecaa19b1b011726f23899488d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:36:59 GMT
ARG RELEASE
# Wed, 20 May 2026 01:36:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:36:59 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:02 GMT
ADD file:6d117ff682b1d31146902ad551197b012e75561d62d92d029219fcbf5c493c35 in / 
# Wed, 20 May 2026 01:37:02 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:09:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 09:13:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a2dede8d0e9ca179460cb274dab10c5c4b741cf1544b130df872809a4467e3e4`  
		Last Modified: Wed, 20 May 2026 02:15:37 GMT  
		Size: 26.9 MB (26859709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b118b4a0c6ca2ad4f0b7d3f4e7f824e209e719825c9725ce8c175f943f51da2e`  
		Last Modified: Tue, 02 Jun 2026 08:09:35 GMT  
		Size: 12.8 MB (12788925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86f8d7e733608db1d7c68cf03f7e3309fd2fff04c29d71ea92c207bcfff41dc`  
		Last Modified: Tue, 02 Jun 2026 09:13:37 GMT  
		Size: 48.9 MB (48938247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:89ec3711da91babefdebd05ebb401a4c3ac43dbf34545963ff4585c1ccd4ff95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5284699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fad5591b2dadee860cba07f8009e4d38e470330bb4dc71d5993b22560774fbd`

```dockerfile
```

-	Layers:
	-	`sha256:94497618fcee51520758f45b8c9eb716251f1065f44d589f65f2da2e2cb588aa`  
		Last Modified: Tue, 02 Jun 2026 09:13:36 GMT  
		Size: 5.3 MB (5277374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32668f6622a97cc54ff7614d43fa1698e8b31f0ae516c5080920b2cc058e8f4a`  
		Last Modified: Tue, 02 Jun 2026 09:13:35 GMT  
		Size: 7.3 KB (7325 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:25f311dbe384f354c13fcd75644c66ff1165493b5dda619d964288e9fc194bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87649864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcfda4f26f90ae7c4c8184669a819759008050a3aca602da9bc3877c71f3936b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:11:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 09:12:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b224b62323017769a142e9665ce9c8ea5728f289ccf479c861e9809bad5d8376`  
		Last Modified: Tue, 02 Jun 2026 08:11:26 GMT  
		Size: 13.5 MB (13466558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e08eafc6c229e820cd66a3b4e4d2fa50aa50bb9bc990e4456e2368cb77f6a7`  
		Last Modified: Tue, 02 Jun 2026 09:12:43 GMT  
		Size: 45.3 MB (45306900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c84f66480143466f0269f5bd96bc8d3d1f474226550c1e410cb33115f4bd532e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bff688b2d3f5bb0ef431f58d8d272f785d74837dc7139896f4af3002a42bfcb`

```dockerfile
```

-	Layers:
	-	`sha256:3a882bd634b292d5b159e919d7732f0aa0b9149cdb40610536524da866789819`  
		Last Modified: Tue, 02 Jun 2026 09:12:42 GMT  
		Size: 5.3 MB (5283268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b2236eb4bb12242c089b428c79beeb9f1215ee0492c07bb379ea402b671caa7`  
		Last Modified: Tue, 02 Jun 2026 09:12:42 GMT  
		Size: 7.3 KB (7342 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:687e60404dc460b93c42deada27dedb83844462dc25a74ba5380a24fcde01d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100664910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda542d4c13b4e6e3b6cb2da72ab7c4baafda874da47f431a469c756bcedf175`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 09:12:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187aeb2a9889fd701a0c7ee32834f3636fe8324b6c4bdb83baad19d7d389c281`  
		Last Modified: Tue, 02 Jun 2026 08:10:22 GMT  
		Size: 16.0 MB (15961906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4062997331ce0a95193beeeeffabe9870d8b52791710c25c92449b6c22aad75b`  
		Last Modified: Tue, 02 Jun 2026 09:13:08 GMT  
		Size: 50.4 MB (50388905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:797cd03f886991bc5912187b7bdbd97e96c85b166b15df40b96dd22f48e1a63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5291224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4c5e9246fd5585c47c22645ddcd69192c021390d34a727b4aa8f6feef19933`

```dockerfile
```

-	Layers:
	-	`sha256:d9c297bd57a9ca19371d90701bce85df3a05c3b0d2eb606768ed3d19d8e5422c`  
		Last Modified: Tue, 02 Jun 2026 09:13:07 GMT  
		Size: 5.3 MB (5283930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c33f8333d862eccb2687d3aad99a235a584e61f585fd2e004f69fb5e8e4d673`  
		Last Modified: Tue, 02 Jun 2026 09:13:06 GMT  
		Size: 7.3 KB (7294 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:22dc7c465b9df98b04a71823e1876c07d93473d840937b82ac9cdfbfaa9bf346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99153063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a5df21453150bec2d8280e2c08ad144a8e48656c6674c7d5a13727df9493c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 02:06:08 GMT
ARG RELEASE
# Wed, 20 May 2026 02:06:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 02:06:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 02:06:59 GMT
ADD file:f1fd7ee282731834f2f36b17e9b538e569ade4ce8b89924b635551ff3a45c706 in / 
# Wed, 20 May 2026 02:07:03 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 18:04:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 23:08:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:924f9a731915e06f77b3487378ddf9426f8422fa1d96461bef1d0e0a35c36743`  
		Last Modified: Wed, 20 May 2026 02:15:52 GMT  
		Size: 31.0 MB (30965919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6165c45f7d3fe380ace51e4cc852195290eee963df6a38f7a335b47ef781490`  
		Last Modified: Tue, 02 Jun 2026 18:05:26 GMT  
		Size: 14.3 MB (14337475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d29f8b733601a7bdffb1d722ee43961e11975ae214b5596abc73a36270c020`  
		Last Modified: Tue, 02 Jun 2026 23:10:46 GMT  
		Size: 53.8 MB (53849669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cf23f683d57e8d911967fb149480823e2cb2cf9c07cd954b9fe91918310a42c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2de033fafa1c835eed28860d7973124e351d634de8b370eb3d57daf1c8dde75`

```dockerfile
```

-	Layers:
	-	`sha256:f5068f6fef7c7744f127cb1bfd74885ec1aed052df500c6b863cc8d7e0ba8730`  
		Last Modified: Tue, 02 Jun 2026 23:10:39 GMT  
		Size: 5.3 MB (5266472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec6e4bc13fbd0bbde127c568f777669b240688681d783acab7d492ff6d52da2`  
		Last Modified: Tue, 02 Jun 2026 23:10:37 GMT  
		Size: 7.3 KB (7293 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:37350fe0a842c0ecb09124a7bf8e34398ea3ac3a7348082986120ed490514ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91666708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de9bce5994b22bbf1911b6e29dfc52e91720e87668a28ee2843caf7ba7a62c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:09 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:11 GMT
ADD file:b574b1e436c2db4e4d66f69c75e47a9aebf0da1ad375147eb2c0b7ff76c6ab7e in / 
# Wed, 20 May 2026 01:37:11 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 09:12:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591d53e14180df305f0fe02c9303d41b73a2de4393458677c78c708d80d4d6eb`  
		Last Modified: Tue, 02 Jun 2026 08:10:13 GMT  
		Size: 14.9 MB (14944603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cb41df27dfa7f083e1e5f3ac67744db7ef082b8f8a3dc3c7dff9d63fe0281a`  
		Last Modified: Tue, 02 Jun 2026 09:12:26 GMT  
		Size: 46.8 MB (46809270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a20b54c2b0909c140dbaa6697098bce3593b76055be6df697fe576963872dfcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5285670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4ed8abe0d80ae25aa49424606b11489992e8f56bff3fa775088fe1adc80117`

```dockerfile
```

-	Layers:
	-	`sha256:d81a8af874450ba4404777d34d81e6963a52b739ad02b33401730660def43a30`  
		Last Modified: Tue, 02 Jun 2026 09:12:25 GMT  
		Size: 5.3 MB (5278408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0111197e86be04ed8ba944cd05b235c2da81c8243338c24540492a65aad9c9f0`  
		Last Modified: Tue, 02 Jun 2026 09:12:25 GMT  
		Size: 7.3 KB (7262 bytes)  
		MIME: application/vnd.in-toto+json
