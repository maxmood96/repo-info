## `buildpack-deps:plucky-curl`

```console
$ docker pull buildpack-deps@sha256:6cc7c25edb8d120f09266b3131318bf06694bd1742d54a612a40e16b5283b066
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

### `buildpack-deps:plucky-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d13f56973c1249a335c57009ae6c8e1ac77d730e51baadc1f0de89af2f3fa355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52959175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1749a335a437cec5a55613de1d87c943499cb41aaad3f07620c8273d2b8ede8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:4e91a036bb7fd027d02229e0891c09685c9a8e10b2e913caca8513e5a856c07c in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:54cf94bf6a9e27dfc420b4583d0f5e04f7b0d32156b29a9de5758fdbe214f0bf`  
		Last Modified: Wed, 02 Apr 2025 05:19:59 GMT  
		Size: 29.7 MB (29710540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb773b17182ef566fe250d1ef4a9725e0a89f5c05ca0d8fe047fe2a03beb20c`  
		Last Modified: Wed, 09 Apr 2025 01:11:49 GMT  
		Size: 23.2 MB (23248635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aa5261f5d855543487a24060a59e3b490b657e60cb54c1ccc0b2465feace1f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1d7f51fdf93481ff98767b636742bd4625ad9f1d7da2e93e2416cf2de95f35`

```dockerfile
```

-	Layers:
	-	`sha256:8db9d8058b397f6edfed58810c7c717925b59ce18fdb4782879b3b883a666554`  
		Last Modified: Wed, 09 Apr 2025 01:11:48 GMT  
		Size: 2.5 MB (2462087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11dad06b499f37e7485b82b8f0143ad0ee13e25c38c39b58ab5854c966689ad`  
		Last Modified: Wed, 09 Apr 2025 01:11:48 GMT  
		Size: 7.0 KB (6968 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:295e4b44f93becc9b552b526c6d1f8da812f8e5f7baaf9f0ade5fe12fe0a9396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45170665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a8ddd2f5b51b07ac2285b60c84a4422fb24cc4b68137dcd33d55d29512098a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 03:57:17 GMT
ARG RELEASE
# Fri, 13 Dec 2024 03:57:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Dec 2024 03:57:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Dec 2024 03:57:17 GMT
LABEL org.opencontainers.image.version=25.04
# Fri, 13 Dec 2024 03:57:19 GMT
ADD file:6f9e46de69cd0f87c8e7f99c02f9c86d7255b291b3d64c9acf6d3664842a11b3 in / 
# Fri, 13 Dec 2024 03:57:20 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:30edb5d57d6dcf9a2d6c372642827a2271cc4b4b697e28bf865c61a4cbde43dc`  
		Last Modified: Fri, 13 Dec 2024 04:29:57 GMT  
		Size: 27.7 MB (27738902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f812cad0ddfcb6da97c6cca7682590669793920cf55e9ec9857cda771d0d13`  
		Last Modified: Wed, 12 Feb 2025 18:36:50 GMT  
		Size: 17.4 MB (17431763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7a44d53012db2f8c3e9fdf6375e8de44f6c5e6ff111518aa877a0f2979ba53bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805d41b2f343359cbbfba3807e36484da3bcc4e2e9bb9e9e475cc4a2a81b5732`

```dockerfile
```

-	Layers:
	-	`sha256:91ac471b1fe798d1e2472b5a5f9ef769352d8027245b2b894e6be07389a6a82f`  
		Last Modified: Wed, 12 Feb 2025 18:36:50 GMT  
		Size: 2.5 MB (2457123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e9e031ac7b16289f360380d42efb25248ccf0fbb11d58eeeb07103dc9340ec5`  
		Last Modified: Wed, 12 Feb 2025 18:36:50 GMT  
		Size: 7.0 KB (7028 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4541c1d6d913847d911eaa7f5cfbec70b6b5dad2e8d893e3e68c39063c87205e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50724719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54273dae0416f8511a5bc0343d981b9b8e4e337003d1dc0e0eb1b9e785d278e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:d0766346daaa36639d276d990d55abccbdf93fd9980f0d012754faed6cc4715b in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:83550439f8b8ffc46f3be5ee055a935afe082f64085b9655d484efceeaba62b2`  
		Last Modified: Wed, 02 Apr 2025 05:20:06 GMT  
		Size: 28.3 MB (28259438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c6bd250a3bc0a3b59bfdbb171a708f8995f0a9d2e88b4b2b1d4f6a3fd0e786`  
		Last Modified: Wed, 09 Apr 2025 06:12:26 GMT  
		Size: 22.5 MB (22465281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f2fa9623b25eb29c680752563da6cef22f708d491fd207095ffd4845d7b107b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cac9e7a0cacb221a9ffbf8b13574aaa0b3063fe9a877ec1e1a57127a95e3a1c`

```dockerfile
```

-	Layers:
	-	`sha256:df575839ab7ffe2855b17cdff273d214c99120472ed0799521322ce8284219df`  
		Last Modified: Wed, 09 Apr 2025 06:12:25 GMT  
		Size: 2.5 MB (2462344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:900093d19b8ad26102b66772d0a93a8a82d90df8062dc14e84af4df777e02272`  
		Last Modified: Wed, 09 Apr 2025 06:12:25 GMT  
		Size: 7.0 KB (7048 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4746cec19d292656a71bbc3becf80f8a54b04f35f65cfb5d1849067f527e0d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57837112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a23d57957c01674d49695002692878e050000b7653a0b4516d258bcc49ea752`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:41c2fca5f24b15b1251f0b546f71308553df3bc7d31d166d24b77ec92e53c124 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5dbbb3ddafe1fab87a2b1a49d634441bb6180275ece999d452a8dec8150303fe`  
		Last Modified: Wed, 02 Apr 2025 05:20:20 GMT  
		Size: 32.9 MB (32917064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf6a4eb24ef45e6182e7579d5054b4183a66a460076a476ff25e624c4681d06`  
		Last Modified: Wed, 09 Apr 2025 04:32:28 GMT  
		Size: 24.9 MB (24920048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c14734e74520039bcdb0efdba65c1a206ccdbc82af0c75fd97ba168e98f1d4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3151f6f9dc40de7ae017a5e284e005e9e34299724a4aff625d2346404303b06`

```dockerfile
```

-	Layers:
	-	`sha256:5b1b6de3cbaebbbbb3693425f100cd2a0d8613a6d9cb154d476477f3f20dc20c`  
		Last Modified: Wed, 09 Apr 2025 04:32:27 GMT  
		Size: 2.5 MB (2465769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec0c4c9a38cd760343623f5bb875b2eb77b71450831805a947838d2adbcf507f`  
		Last Modified: Wed, 09 Apr 2025 04:32:26 GMT  
		Size: 7.0 KB (7000 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5c737bba0c81ecb7e4507f55350e8df1abf4fdf07af92d41d8920e3d46e5140f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52392722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f624b0ea804e7e5888ce651f4e43c00e5755a6961833215a08454a9bcf96de2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:e1ade0e6cf3587e52fd2e150b2140bd7286f1ee2e92d7688f7a8e9295f045099 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e94e661d55750b27c664c062defe70e7670822fb9e808139123296023b7710c3`  
		Last Modified: Wed, 02 Apr 2025 05:20:27 GMT  
		Size: 29.7 MB (29709622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b558e2c1a19e40220bf31e3d0070d8d63c7e158ae6110e51725275b330f1f1`  
		Last Modified: Wed, 09 Apr 2025 05:25:36 GMT  
		Size: 22.7 MB (22683100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3b13f68d905665ec6c6bb9c569814658ce469a93874cbca2bff84628d4fda0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a579ce9726701ecf554408ab53794bd03c8985778e10176e2858c4fb72f08dc9`

```dockerfile
```

-	Layers:
	-	`sha256:59c2431006feaca87b798e6b458811cad582ade0c265e2dc6c47509ea861e0eb`  
		Last Modified: Wed, 09 Apr 2025 05:25:33 GMT  
		Size: 2.5 MB (2455355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b033f197ec18c8759b1bdf12e693ad9b6fb7b36d3b370d796437f5bf9ce6a7`  
		Last Modified: Wed, 09 Apr 2025 05:25:32 GMT  
		Size: 7.0 KB (7000 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b17c76ca3741ce5dba173d1dbcbb290c97b0a3f9000009a5506b363e004d6ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52675976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d485385696aeec743fe7de95bd4fea2801c1229e27a0de8ef090e3b24f0bbdfe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:3187e5e8dafde316503f01473967b5018998dede98c27020e30f819899f6f60d in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0da16fa1ee9f8c39405683939ed3b583090ca47b5e4b8aad0a1993291bc12217`  
		Last Modified: Wed, 02 Apr 2025 05:20:34 GMT  
		Size: 28.5 MB (28538092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48d924dd8dd7d642c1ddf208f8b6cd8d159007414bde5bf9a8ba8d05ba940bd`  
		Last Modified: Wed, 09 Apr 2025 04:14:20 GMT  
		Size: 24.1 MB (24137884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07339490fc2cf0670a32f52169eabef300e90a889dcf977768a750f25965af89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fc9accee70a3a2b282a2804ef96c611117c410a34ad29300f9c8f13bd91075`

```dockerfile
```

-	Layers:
	-	`sha256:7860f1cbec376546f6aed881231861a3b4108de23da90cbc4ad779f3102709ff`  
		Last Modified: Wed, 09 Apr 2025 04:14:20 GMT  
		Size: 2.5 MB (2464115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3763605144ce4ccec5b64cdd00dfa17ec86c2ac91d0b73d4c9e2457e5f0bceb3`  
		Last Modified: Wed, 09 Apr 2025 04:14:20 GMT  
		Size: 7.0 KB (6968 bytes)  
		MIME: application/vnd.in-toto+json
