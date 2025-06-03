## `buildpack-deps:questing-scm`

```console
$ docker pull buildpack-deps@sha256:3c9ceb1b29a3160c2d8a8a8471dff397f58dbba94455655975636ce8fbb488d4
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

### `buildpack-deps:questing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4efc49b1dd7571377d7e86ff93cbbf4b7ff4acd93579f3f15d687a88b5b30f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98200934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f22bbd54ba81e7559df43016989392b1e6638694902af1667da7efde0b645e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:05cc544084bb3fa6b9d35c9616e72a64a3e4639021957070a288f64f014f1b24 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:15d8b49a304e2f84c28f203b3109aac57a5f04130d8a13ab89db6528a8bc2e3d`  
		Last Modified: Sun, 01 Jun 2025 05:26:34 GMT  
		Size: 29.1 MB (29106436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524a2d370386a0cd39d38026a460d26ce31a6221b6ab8aaa1f19d25d8002674a`  
		Last Modified: Tue, 03 Jun 2025 04:15:37 GMT  
		Size: 19.8 MB (19839541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65512b0923851ed2aa5a6489177af45593736a397a79a9354c144106ef1c87b9`  
		Last Modified: Tue, 03 Jun 2025 05:12:01 GMT  
		Size: 49.3 MB (49254957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2f247e88d62731458de06a97e9ec298a21dc939d6eb406b4a0501ddfbc442324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb44294638f5ce29f53d0d835e44ffee3a7e36cd9b49f8476817ba63b59f14e`

```dockerfile
```

-	Layers:
	-	`sha256:5360b4dedd8aa0a496ddcf18ff7b085a4813ff998e1633c7a456e598f8f34071`  
		Last Modified: Tue, 03 Jun 2025 05:11:59 GMT  
		Size: 5.3 MB (5259935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:711f94840f486c01dd896203508ac10e1a6892061f031699f29351f62c53815e`  
		Last Modified: Tue, 03 Jun 2025 05:11:59 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2f9e34d9891e7dd6fabf500a3ada42865d8a572a5b3211ac04968df3527a60c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95218360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc909d6abf6c51a4a347cce45b62c38e334e6be441fe1a14e0bb91674097b381`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:64488fb6b3ce2ee2840e65c2ff29f801f160033b9aa156736e9515d881ca5bd4 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0ae13f6240d71b4e49221ea0402dea6bd07e09d94c8c5c453ccf627c165d648e`  
		Last Modified: Sun, 01 Jun 2025 05:26:47 GMT  
		Size: 26.9 MB (26913307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53874f6a00ca89fc01eaa92fabcc2ef180611cda1ffaa63785cc0f2f13acd225`  
		Last Modified: Tue, 03 Jun 2025 04:19:48 GMT  
		Size: 17.9 MB (17859666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b98d9371863e08ef17358bdbe165e029982ab1846faf3e5d299c8111ded84a`  
		Last Modified: Tue, 03 Jun 2025 05:15:31 GMT  
		Size: 50.4 MB (50445387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:878736a63ea9887e5de2f0e9eab0bb70401506ed80e2f5d45de84848d4bf503c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1c90813f2c6a859c72676f2f15a24b0d317ef628d0258c5978ca99a1b2bf71`

```dockerfile
```

-	Layers:
	-	`sha256:2cd1a90222ad06fa00f7abb8ab9ff1db8b8b5b49e3b8e8caff0a3c10d8407fe7`  
		Last Modified: Tue, 03 Jun 2025 05:15:30 GMT  
		Size: 5.3 MB (5260425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66bbce0b415c5bd57342cd9c8549c88b1ef396d4bbe20a50cb604c7a3efd4483`  
		Last Modified: Tue, 03 Jun 2025 05:15:29 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:12ce9766a896ab8fdf0ceeae9e6a07006c788d0064d7197525d10b6a29f134d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94663262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c78cc8fbbaba3c49e66d2a512a2cd96da3a117d843eed504ea977415af865b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:e7d95872fd9b2265d0ef9932a3a613bcac89a6887fad274039f57708e8466742 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f553ab7f5e64c9213adb141dbb943fcf439b06bda49c21d9637656e0e1033744`  
		Last Modified: Sun, 01 Jun 2025 05:26:41 GMT  
		Size: 28.3 MB (28284813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb9e72daec54872584552e76e8bb0b85cb4e28ed8bcaeb98ea9fe184f899e81`  
		Last Modified: Tue, 03 Jun 2025 04:20:52 GMT  
		Size: 19.1 MB (19146322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0758ecb86e4624ed6dc39005328cde6fad108972adac3ce2501336c4b8f2b1b7`  
		Last Modified: Tue, 03 Jun 2025 06:50:10 GMT  
		Size: 47.2 MB (47232127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f4aae248a43b7ee3b910be52f9fecf2ce35a905c98046f178c646fa03403bcaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e4112827f16c02f07376aba4e216ef95d9ca23192fa9afa8a01ce116394653`

```dockerfile
```

-	Layers:
	-	`sha256:cccf51f974ad3142ff0313613ee79a76532d0b6780a98cc137d613c360d80b24`  
		Last Modified: Tue, 03 Jun 2025 06:50:09 GMT  
		Size: 5.3 MB (5266320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddc16b90a9c89f42dfe20e11be24116a9e36ab94f8bd5ff05bc36bcfcb7edbb9`  
		Last Modified: Tue, 03 Jun 2025 06:50:08 GMT  
		Size: 7.4 KB (7403 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3077360e231ba3ae5fed94c5acf6e30674fad7d15bdd851e2ca7bba5d83505d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107359880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140a5485ca21e0865415b0f15ece74fe6b0aa8dff12f8dfa6226a1db4e330890`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:13d7a96466458c3909b82b8ab831f9a568057a566ffa930b3df35fc558dd9a4b in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4a6626be4dde51767d2f322fcce23eea122e82b08f99962b3dc7ac890938cdd0`  
		Last Modified: Sun, 01 Jun 2025 05:26:53 GMT  
		Size: 32.9 MB (32921224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a6a2b121e6a335d78f4905325ed4812e495517ab4b9b91b7eba68099bfbc10`  
		Last Modified: Tue, 03 Jun 2025 04:20:35 GMT  
		Size: 21.6 MB (21613543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68617ded14083d61c71972a6be342cb6d6131d50e46aac3ccf0aeb996dc205e`  
		Last Modified: Tue, 03 Jun 2025 06:36:16 GMT  
		Size: 52.8 MB (52825113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e29d2eed90b2a81f1a9609546df16736110c6cf58bbf82ca6f82040d7b80367b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a6ca4b65260e62f36968e832103892c6439e9c6409926643e08cd31c2a43b2`

```dockerfile
```

-	Layers:
	-	`sha256:4b0672616c3c0ffba3aae0e8ffbbe6c796416ee73dd08f05700d104393c6edac`  
		Last Modified: Tue, 03 Jun 2025 06:36:15 GMT  
		Size: 5.3 MB (5266983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1134c1a0091c5c4101f562c234d8bad5fd2fa369588af60e07d6f0f1d0dc5c2`  
		Last Modified: Tue, 03 Jun 2025 06:36:14 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:92d99562cec64d25131437cd30d385e5199c274f647246695dc6791b3bee938c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104905411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc9b35b3863b3f694ec2893608fcb558a144540dbdd19cf716c301c4400ca5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 04:51:05 GMT
ARG RELEASE
# Wed, 14 May 2025 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 04:51:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 04:51:06 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 14 May 2025 04:51:36 GMT
ADD file:0cd658103d02bf6846dbd2f13752c91538b4521bf27ad3ef8f782d20b0f83446 in / 
# Wed, 14 May 2025 04:51:39 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6b6ac20521bb58fca960ddf3a7c726f8140f436dafe253d6ed5b0749b388fa99`  
		Last Modified: Wed, 14 May 2025 05:18:07 GMT  
		Size: 29.8 MB (29759113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca9b80989299965c9f6755f5840f8c611f6382b2f6f805aec3b88374f28e6de`  
		Last Modified: Tue, 20 May 2025 00:47:39 GMT  
		Size: 19.8 MB (19790435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672a8136e711ca2b79356e618f52f148f3de569595ab11ee67aa99bbcc3b56a7`  
		Last Modified: Tue, 20 May 2025 01:13:09 GMT  
		Size: 55.4 MB (55355863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:77cdd14da73b4eeefe47859e4d6be2bff4b305d90d9618834d96c1469bb99d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e3ea992113a77ee2690e066d08f559f6dc61c96c685276f41f6092bc51f35c`

```dockerfile
```

-	Layers:
	-	`sha256:2b6b4f7024e962d5f84eb24d7afa0a11c3fef7d86b067d3ad08b73220046977d`  
		Last Modified: Tue, 20 May 2025 01:13:02 GMT  
		Size: 5.2 MB (5233570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12399b2aec57cb4e44e7a7938381927aa01f450223097c87782ed74f734e0118`  
		Last Modified: Tue, 20 May 2025 01:13:01 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c39f28f1be489530325c8bf6e8f5e3175b29c5cabc08dd82f21d9f250babeb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99093692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7de01ed73775a21d99c1846bda47a9f7382fc413fa265c2a57f594ed51fc9b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:8419b0c54ced109f1a86ac0df8febd2313936943cc6f5e51f8cc6789fed40a0c in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f83117ffdbeb353c4d64f37cd0b900511b0f13104632ef537330017b9342f673`  
		Last Modified: Sun, 01 Jun 2025 05:27:06 GMT  
		Size: 28.5 MB (28523638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb9c85ce7fb406691ad8c01800f1b0cbedcb1b2a1f99617eed4b5888d15dda3`  
		Last Modified: Tue, 03 Jun 2025 04:18:52 GMT  
		Size: 21.8 MB (21756689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd56e409834b5f6151e5d905d4c560b677cb9078c1db432899e4888c9c1b37ab`  
		Last Modified: Tue, 03 Jun 2025 05:19:34 GMT  
		Size: 48.8 MB (48813365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4c157e35d8edd9c580609433eeec2f9c30caccc2dc2e55a0b99e563cc7be1582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7c4190493a7d41d5e3603c4f63555c50de9c1e04b031c62e36d00390409eb4`

```dockerfile
```

-	Layers:
	-	`sha256:b541ee9bbb34ffd1e01ac10eb73cff0d3ed242d4af726491e5f85a6c44fd3444`  
		Last Modified: Tue, 03 Jun 2025 05:19:33 GMT  
		Size: 5.3 MB (5261471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:092ab0add8163552230096a8725f08eebee332d44bd76fb92f63223b5aeab44f`  
		Last Modified: Tue, 03 Jun 2025 05:19:32 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json
