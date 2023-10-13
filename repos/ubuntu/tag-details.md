<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:23.04`](#ubuntu2304)
-	[`ubuntu:23.10`](#ubuntu2310)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20231003`](#ubuntufocal-20231003)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20231004`](#ubuntujammy-20231004)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:lunar`](#ubuntulunar)
-	[`ubuntu:lunar-20231004`](#ubuntulunar-20231004)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20231011`](#ubuntumantic-20231011)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:aa7ee6b60c8e983b14149a97c4aae054bf2f6a4524f7be2f082871e7110b7c1a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:20.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:3246518d9735254519e1b2ff35f95686e4a5011c90c85344c1f38df7bae9dd37
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27506442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df89402372646d400cf092016c28066391a26f5d46c00b1153e75003465484d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:edaedc954fb53f42a7754a6e2d1b57f091bc9b11063bc445c2e325ea448f8f68`  
		Last Modified: Tue, 01 Aug 2023 06:54:06 GMT  
		Size: 27.5 MB (27506442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:06e174da2c1a4cd683a888d933a235407a02f2d98fedb49c34601b293fc5e36e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23612914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eba8b8e77a0ca1c3d8315507ef4e67d817fb199a4cdbc603a0e06fb1b9f78ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a50255c0017d09ab86514148fe36d006a4ad9a46633b82efd4b0233a9c9082e8`  
		Last Modified: Tue, 03 Oct 2023 11:16:56 GMT  
		Size: 23.6 MB (23612914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:af43d52ea8f98c8ab92858a37b87be1805ce16f5300cb38b9958e63ac6b25902
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c9d636caddd81490d58a714937f112702f9239c98950221e9fd0dd9735df9d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:82d728d38b98752cba7d2d7af8ee1cfe67ccdc5915814420650e78def5d1cebc`  
		Last Modified: Tue, 01 Aug 2023 06:54:12 GMT  
		Size: 26.0 MB (25974619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a305c3951a3741555d5019870f4827c4becdcc95df539ce7ed364ab5ab2db342
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32070704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92643ae09f6e607311cb05e4f0f7679c0873b7e4c235e1b57f5e409cfc47c50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:36 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:20:40 GMT
ADD file:822df76493d1d533c1a283ab7bb20ce81309f57279422a0eebb2ffb9fab55963 in / 
# Tue, 01 Aug 2023 06:20:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fa78ce4014add322eddde3378405efe21c85e886c0195e18533d5991d5477833`  
		Last Modified: Tue, 01 Aug 2023 06:54:25 GMT  
		Size: 32.1 MB (32070704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:5ad386cefcdbd1248f73a3bbcfbf529f39864dddcf9497d9a705540afd23e6e9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26351280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5079141aa115a82eb5f952b45f4cf336075d4dc4bc3ea2cfdab4351497d2fc9e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:17:39 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:17:41 GMT
ADD file:36efc3ec29bb54e0987fe91be1aa7cc849909b3cd2534af3de2d3d07a03804cf in / 
# Tue, 01 Aug 2023 06:17:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:773e1d05400f41114172ea2dbaa16f037c5812b7d1092cbf0df5d19e69586402`  
		Last Modified: Tue, 01 Aug 2023 06:54:31 GMT  
		Size: 26.4 MB (26351280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:990350fbc1af973523f0aaa5ec8ad96ab1ad6193a657557628e6aa35eaa2ca2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:22.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:b4b521bfcec90b11d2869e00fe1f2380c21cbfcd799ee35df8bd7ac09e6f63ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29538209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3565a89d9e81a4cb4cb2b0d947c7c11227a3f358dc216d19fc54bfd77cd5b542`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:37aaf24cf781dcc5b9a4f8aa5a99a40b60ae45d64dcb4f6d5a4b9e5ab7ab0894`  
		Last Modified: Mon, 25 Sep 2023 10:30:37 GMT  
		Size: 29.5 MB (29538209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:212b9f426e7be12bf9a80b65e1a14fc39e319cff3a7857772b21c02f1eaff610
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26629612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3f9d425ffe4e459ab4cfc7b6f32c504d3f86b0fcb2a1b58d7646ab045ca4c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:56 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:35:01 GMT
ADD file:4b9d52f97ed5796b14772a84c1e7213402430d32312d15ae04a2dcc9fc485a52 in / 
# Thu, 05 Oct 2023 07:35:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4091a3a7d6aa711dc0e0bbacfd3546df44ca257c300de1ad00fbdc95e218f7bd`  
		Last Modified: Thu, 05 Oct 2023 07:43:39 GMT  
		Size: 26.6 MB (26629612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:f58b48967ecc767fc238144ffdb7eb668cefcc8438de8f8a59c4cefbbf29b323
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27351199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9e5b7213b4e0d99cddc039011cc60bfd76ed5ef63bbd837ab0b8416c305c39`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c391327a0f1df5790bcb00ac010a1a3924c9e4387ce36b290bc16fd9f4cc5740`  
		Last Modified: Mon, 25 Sep 2023 10:30:43 GMT  
		Size: 27.4 MB (27351199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b4b8cd982d392ba99d1a5d81fc9fccd2fe9f86b7ba43ad5ae52178410b03661d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34564928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38923d6791a09ab860360e561db13df5ce51bab6f32bd4d42bcd1b54cde82907`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:20:46 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:20:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:20:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:20:46 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:20:49 GMT
ADD file:4e52928c778d7e98d90ccfcaacd039ae1fdde494dfa310adbe229d7051c30918 in / 
# Mon, 25 Sep 2023 10:20:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:53cc531c2e6e7ce32a82e9a21f71c9b4d11b0ccd1ef71c8c9e1493d2ec8969ad`  
		Last Modified: Mon, 25 Sep 2023 10:30:56 GMT  
		Size: 34.6 MB (34564928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:7c789f181465e5474aa9093b939a9992e2e67637c827a1b81e7890c3f04f6bf6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28024260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04042eae942dd0a766b4d45f17617014c8c3e464113d08a245ee7b43ddfb1f6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:26 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:26 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:28 GMT
ADD file:78683f2464233172a7cd0d6adc4c7d9fb3ef05fa67ca22e6fbaca0325496a536 in / 
# Mon, 25 Sep 2023 10:17:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:594ea103c983265390944410c6ac8624359909261a656484e971d00ca0ff8b20`  
		Last Modified: Mon, 25 Sep 2023 10:31:02 GMT  
		Size: 28.0 MB (28024260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.04`

```console
$ docker pull ubuntu@sha256:ebeab264a6aa31d73b4571f5ef7534b2180cc2a5011422c09ca45934e63f101d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:23.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:24898c8e1ac370d2d309d6d9df56af52bebdad86925c623b5e87e12404453518
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26873617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21098a29e034a8f6f1952d1d8a49b5732b70e532c31f0e88e1ff499c6540c57c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:28:31 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:28:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:28:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:28:31 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:28:32 GMT
ADD file:7392bed4dbab9fb7c9ad5bde6f3bfcde3bcbf1885c336af9c231af6defaa31e1 in / 
# Wed, 16 Aug 2023 04:28:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:10fb01f4f619bc954ba611cebca23f2b96d255c7ead4040b449f063e530df1a4`  
		Last Modified: Wed, 16 Aug 2023 04:34:32 GMT  
		Size: 26.9 MB (26873617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4dc1dd258d16171c6cd696ed5420402319d7cabe638b176b471495e94373f2a9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24629439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83502f31cce9655561356390e34e8d506e888f6ce4743a8400bfa765f6eedb8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Oct 2023 12:25:21 GMT
ARG RELEASE
# Wed, 04 Oct 2023 12:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 12:25:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 12:25:22 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 04 Oct 2023 12:25:24 GMT
ADD file:b92305119eab5dd3dfb00f4d83cd84e00c8ae57143739329da5a19aeda55be4e in / 
# Wed, 04 Oct 2023 12:25:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:725335f54d3eb8903e713867d9f04db29fbc8835da3539fd3898faa22eaf016e`  
		Last Modified: Wed, 04 Oct 2023 12:33:24 GMT  
		Size: 24.6 MB (24629439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d68d8bcae123a839bc72b91fa9df55956be3fcb2dbfc247acb7f65908eaa6c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26064545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c8e9335de75964dd320b20b4290408432be2962faf7ad36d3a47d48f3131cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:15:57 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:15:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:15:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:15:57 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:01 GMT
ADD file:adea2962926b29b76eb8da76ae9e830c5ad7050ae9b19f5427191b338c8a2c56 in / 
# Wed, 16 Aug 2023 04:16:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2b2d15932a31f0857b9499cc218b8777708cb1d73ae6ef680f624ca7d4342763`  
		Last Modified: Wed, 16 Aug 2023 04:34:39 GMT  
		Size: 26.1 MB (26064545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1306e75f505a2305f2c46f51f33be8b8599923bd5a652c3b5dc37333db4f44ab
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30905042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91733a8763fe80d6e620ec400c2721ee45c0f80398506088d1278d6531299a90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:16:31 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:16:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:16:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:16:31 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:34 GMT
ADD file:a9d35b320d969ee1ae8a7bc83aba49da30d93724befb5948c680066ad4f1acdf in / 
# Wed, 16 Aug 2023 04:16:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f51cbff870f31d4c4397c2f21529046998f8d6e7748fd6f059b325a0759c7dd4`  
		Last Modified: Wed, 16 Aug 2023 04:34:51 GMT  
		Size: 30.9 MB (30905042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:ec9620bbf89d1a3b1171f961340a890166607be3423d96e740f6d56f36ccb125
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25691524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1289eb3132a14bc161676d7f928d557bf63eb8561718e9d5247e16e88ebee8ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:29:27 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:29:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:29:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:29:28 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:29:29 GMT
ADD file:14fcf0756fb29b609af54412c31e2ff9acbf4634984ce95bf204c67668706cb5 in / 
# Wed, 16 Aug 2023 04:29:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b1e434384d3d3b546e155df0cf143c8c0a92bf766c6808bf2e3e1d2f22010839`  
		Last Modified: Wed, 16 Aug 2023 04:34:57 GMT  
		Size: 25.7 MB (25691524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.10`

```console
$ docker pull ubuntu@sha256:527def7ad4b6f32f5188f36daf7f29bcc307542fd1a79c2326d3ed3ddd8b3351
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:23.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:7e44d7ed904145328785378ddac5de49ac931d3b28b72f6c9f5fb350f9b4a849
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27277147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8801a7ecb54952ea17852be887c1d858fd7bd78dcee093afc11fee7ed53f7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 Sep 2023 05:03:43 GMT
ARG RELEASE
# Tue, 26 Sep 2023 05:03:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Sep 2023 05:03:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Sep 2023 05:03:43 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 26 Sep 2023 05:03:45 GMT
ADD file:5fb49f260a0c3bf404c0fe31d8f0f812e9c143bd48223c4f15a85168758eb880 in / 
# Tue, 26 Sep 2023 05:03:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:97e98d3adb77a3f73850e0a81cdde417afce9cd9dce78c444f99b9258caee9fa`  
		Last Modified: Tue, 26 Sep 2023 05:33:55 GMT  
		Size: 27.3 MB (27277147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2a465a4c4831c57977b6646e481f504061294f1bf1ae1b99fb5d93c67b8a471a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25201383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc753c284b47a7a5ff3ec2e926551ba95dc6c9072415649cb13a9cdff503dc04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:02:33 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:02:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:02:39 GMT
ADD file:1be1311acbd557f7769fb5c1913ef56305431e7547f96c20ac36284fdd926223 in / 
# Wed, 11 Oct 2023 18:02:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8761b0d436cd2e1ff47496b7cc353cf0b49347ffc92b070c31a5cf5431041614`  
		Last Modified: Wed, 11 Oct 2023 18:18:00 GMT  
		Size: 25.2 MB (25201383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:bb9a61edbd6cd4f0b8458daa9a78bc09ff7ffe638e7da0a85dc28a5b6c26adb2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26356283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461b48f7d9e026c91692982d4ad80e66be3245f28c14eebf5e1c2fd88c95bbe9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 Sep 2023 05:06:27 GMT
ARG RELEASE
# Tue, 26 Sep 2023 05:06:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Sep 2023 05:06:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Sep 2023 05:06:27 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 26 Sep 2023 05:06:30 GMT
ADD file:0dbbd4de9483bc32897d525742b94aa13ebd3a6aac7f1844d94d7f4536b2bfb8 in / 
# Tue, 26 Sep 2023 05:06:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:afcf80ae17bcd3e5b46853b0fd5d9358fc62ae2b878d7ccb081bd357330cd0aa`  
		Last Modified: Tue, 26 Sep 2023 05:34:02 GMT  
		Size: 26.4 MB (26356283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:7b532d2ce398e717ab17c9280bfac4f8cc34e8104313149c6891f9f1ed3648c1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31341680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9cdbbf45d488137b78c5d4e544935a5a2dd90921911c5c2ebc35b3453cf223`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 Sep 2023 04:52:53 GMT
ARG RELEASE
# Tue, 26 Sep 2023 04:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Sep 2023 04:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Sep 2023 04:52:54 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 26 Sep 2023 04:52:56 GMT
ADD file:cbeb7f814c9eebdbdc6b8e10fb87ba8334b3f6203ceb166c48f6d7492ab07c4e in / 
# Tue, 26 Sep 2023 04:52:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3261179759b520c84edfab6a5842534e3552b99a5f71b1e44ccbd6017eab30b5`  
		Last Modified: Tue, 26 Sep 2023 05:34:15 GMT  
		Size: 31.3 MB (31341680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:a353c527eb5233fdfc2ad112c7897cce7da6ac28b24d3aaa8f441f27ddf613c9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27072390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12eca28f81d0bd51084742dc133e32c215a83739fc5603306f1ad774311dc6ba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 Sep 2023 04:58:19 GMT
ARG RELEASE
# Tue, 26 Sep 2023 04:58:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Sep 2023 04:58:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Sep 2023 04:58:19 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 26 Sep 2023 04:58:21 GMT
ADD file:e86e9b7546a97fa45e9c726cc317a624a7f94b0bd6dd413d89946ff778b18c77 in / 
# Tue, 26 Sep 2023 04:58:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:56312385d597227d0c1232049609586ed3412b04e6ec96c5f6626f5f50f438fe`  
		Last Modified: Tue, 26 Sep 2023 05:34:22 GMT  
		Size: 27.1 MB (27072390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:aa7ee6b60c8e983b14149a97c4aae054bf2f6a4524f7be2f082871e7110b7c1a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal` - linux; amd64

```console
$ docker pull ubuntu@sha256:3246518d9735254519e1b2ff35f95686e4a5011c90c85344c1f38df7bae9dd37
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27506442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df89402372646d400cf092016c28066391a26f5d46c00b1153e75003465484d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:edaedc954fb53f42a7754a6e2d1b57f091bc9b11063bc445c2e325ea448f8f68`  
		Last Modified: Tue, 01 Aug 2023 06:54:06 GMT  
		Size: 27.5 MB (27506442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:06e174da2c1a4cd683a888d933a235407a02f2d98fedb49c34601b293fc5e36e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23612914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eba8b8e77a0ca1c3d8315507ef4e67d817fb199a4cdbc603a0e06fb1b9f78ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a50255c0017d09ab86514148fe36d006a4ad9a46633b82efd4b0233a9c9082e8`  
		Last Modified: Tue, 03 Oct 2023 11:16:56 GMT  
		Size: 23.6 MB (23612914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:af43d52ea8f98c8ab92858a37b87be1805ce16f5300cb38b9958e63ac6b25902
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c9d636caddd81490d58a714937f112702f9239c98950221e9fd0dd9735df9d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:82d728d38b98752cba7d2d7af8ee1cfe67ccdc5915814420650e78def5d1cebc`  
		Last Modified: Tue, 01 Aug 2023 06:54:12 GMT  
		Size: 26.0 MB (25974619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a305c3951a3741555d5019870f4827c4becdcc95df539ce7ed364ab5ab2db342
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32070704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92643ae09f6e607311cb05e4f0f7679c0873b7e4c235e1b57f5e409cfc47c50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:36 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:20:40 GMT
ADD file:822df76493d1d533c1a283ab7bb20ce81309f57279422a0eebb2ffb9fab55963 in / 
# Tue, 01 Aug 2023 06:20:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fa78ce4014add322eddde3378405efe21c85e886c0195e18533d5991d5477833`  
		Last Modified: Tue, 01 Aug 2023 06:54:25 GMT  
		Size: 32.1 MB (32070704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:5ad386cefcdbd1248f73a3bbcfbf529f39864dddcf9497d9a705540afd23e6e9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26351280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5079141aa115a82eb5f952b45f4cf336075d4dc4bc3ea2cfdab4351497d2fc9e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:17:39 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:17:41 GMT
ADD file:36efc3ec29bb54e0987fe91be1aa7cc849909b3cd2534af3de2d3d07a03804cf in / 
# Tue, 01 Aug 2023 06:17:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:773e1d05400f41114172ea2dbaa16f037c5812b7d1092cbf0df5d19e69586402`  
		Last Modified: Tue, 01 Aug 2023 06:54:31 GMT  
		Size: 26.4 MB (26351280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20231003`

```console
$ docker pull ubuntu@sha256:7d5a84286eb1bfca4c48faf202b892e799db2a6e0d28ef12a4933484bf6bde47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 1
	-	linux; arm variant v7

### `ubuntu:focal-20231003` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:06e174da2c1a4cd683a888d933a235407a02f2d98fedb49c34601b293fc5e36e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23612914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eba8b8e77a0ca1c3d8315507ef4e67d817fb199a4cdbc603a0e06fb1b9f78ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a50255c0017d09ab86514148fe36d006a4ad9a46633b82efd4b0233a9c9082e8`  
		Last Modified: Tue, 03 Oct 2023 11:16:56 GMT  
		Size: 23.6 MB (23612914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:990350fbc1af973523f0aaa5ec8ad96ab1ad6193a657557628e6aa35eaa2ca2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy` - linux; amd64

```console
$ docker pull ubuntu@sha256:b4b521bfcec90b11d2869e00fe1f2380c21cbfcd799ee35df8bd7ac09e6f63ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29538209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3565a89d9e81a4cb4cb2b0d947c7c11227a3f358dc216d19fc54bfd77cd5b542`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:37aaf24cf781dcc5b9a4f8aa5a99a40b60ae45d64dcb4f6d5a4b9e5ab7ab0894`  
		Last Modified: Mon, 25 Sep 2023 10:30:37 GMT  
		Size: 29.5 MB (29538209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:212b9f426e7be12bf9a80b65e1a14fc39e319cff3a7857772b21c02f1eaff610
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26629612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3f9d425ffe4e459ab4cfc7b6f32c504d3f86b0fcb2a1b58d7646ab045ca4c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:56 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:35:01 GMT
ADD file:4b9d52f97ed5796b14772a84c1e7213402430d32312d15ae04a2dcc9fc485a52 in / 
# Thu, 05 Oct 2023 07:35:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4091a3a7d6aa711dc0e0bbacfd3546df44ca257c300de1ad00fbdc95e218f7bd`  
		Last Modified: Thu, 05 Oct 2023 07:43:39 GMT  
		Size: 26.6 MB (26629612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:f58b48967ecc767fc238144ffdb7eb668cefcc8438de8f8a59c4cefbbf29b323
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27351199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9e5b7213b4e0d99cddc039011cc60bfd76ed5ef63bbd837ab0b8416c305c39`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c391327a0f1df5790bcb00ac010a1a3924c9e4387ce36b290bc16fd9f4cc5740`  
		Last Modified: Mon, 25 Sep 2023 10:30:43 GMT  
		Size: 27.4 MB (27351199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b4b8cd982d392ba99d1a5d81fc9fccd2fe9f86b7ba43ad5ae52178410b03661d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34564928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38923d6791a09ab860360e561db13df5ce51bab6f32bd4d42bcd1b54cde82907`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:20:46 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:20:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:20:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:20:46 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:20:49 GMT
ADD file:4e52928c778d7e98d90ccfcaacd039ae1fdde494dfa310adbe229d7051c30918 in / 
# Mon, 25 Sep 2023 10:20:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:53cc531c2e6e7ce32a82e9a21f71c9b4d11b0ccd1ef71c8c9e1493d2ec8969ad`  
		Last Modified: Mon, 25 Sep 2023 10:30:56 GMT  
		Size: 34.6 MB (34564928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:7c789f181465e5474aa9093b939a9992e2e67637c827a1b81e7890c3f04f6bf6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28024260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04042eae942dd0a766b4d45f17617014c8c3e464113d08a245ee7b43ddfb1f6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:26 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:26 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:28 GMT
ADD file:78683f2464233172a7cd0d6adc4c7d9fb3ef05fa67ca22e6fbaca0325496a536 in / 
# Mon, 25 Sep 2023 10:17:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:594ea103c983265390944410c6ac8624359909261a656484e971d00ca0ff8b20`  
		Last Modified: Mon, 25 Sep 2023 10:31:02 GMT  
		Size: 28.0 MB (28024260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20231004`

```console
$ docker pull ubuntu@sha256:b1830156ff6bfa71ac8f7c343482b9c0d3216632a9e90b7e5d450befb251c9b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 1
	-	linux; arm variant v7

### `ubuntu:jammy-20231004` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:212b9f426e7be12bf9a80b65e1a14fc39e319cff3a7857772b21c02f1eaff610
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26629612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3f9d425ffe4e459ab4cfc7b6f32c504d3f86b0fcb2a1b58d7646ab045ca4c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:56 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:35:01 GMT
ADD file:4b9d52f97ed5796b14772a84c1e7213402430d32312d15ae04a2dcc9fc485a52 in / 
# Thu, 05 Oct 2023 07:35:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4091a3a7d6aa711dc0e0bbacfd3546df44ca257c300de1ad00fbdc95e218f7bd`  
		Last Modified: Thu, 05 Oct 2023 07:43:39 GMT  
		Size: 26.6 MB (26629612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:990350fbc1af973523f0aaa5ec8ad96ab1ad6193a657557628e6aa35eaa2ca2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:latest` - linux; amd64

```console
$ docker pull ubuntu@sha256:b4b521bfcec90b11d2869e00fe1f2380c21cbfcd799ee35df8bd7ac09e6f63ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29538209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3565a89d9e81a4cb4cb2b0d947c7c11227a3f358dc216d19fc54bfd77cd5b542`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:37aaf24cf781dcc5b9a4f8aa5a99a40b60ae45d64dcb4f6d5a4b9e5ab7ab0894`  
		Last Modified: Mon, 25 Sep 2023 10:30:37 GMT  
		Size: 29.5 MB (29538209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:212b9f426e7be12bf9a80b65e1a14fc39e319cff3a7857772b21c02f1eaff610
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26629612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3f9d425ffe4e459ab4cfc7b6f32c504d3f86b0fcb2a1b58d7646ab045ca4c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:56 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:35:01 GMT
ADD file:4b9d52f97ed5796b14772a84c1e7213402430d32312d15ae04a2dcc9fc485a52 in / 
# Thu, 05 Oct 2023 07:35:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4091a3a7d6aa711dc0e0bbacfd3546df44ca257c300de1ad00fbdc95e218f7bd`  
		Last Modified: Thu, 05 Oct 2023 07:43:39 GMT  
		Size: 26.6 MB (26629612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:f58b48967ecc767fc238144ffdb7eb668cefcc8438de8f8a59c4cefbbf29b323
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27351199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9e5b7213b4e0d99cddc039011cc60bfd76ed5ef63bbd837ab0b8416c305c39`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c391327a0f1df5790bcb00ac010a1a3924c9e4387ce36b290bc16fd9f4cc5740`  
		Last Modified: Mon, 25 Sep 2023 10:30:43 GMT  
		Size: 27.4 MB (27351199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b4b8cd982d392ba99d1a5d81fc9fccd2fe9f86b7ba43ad5ae52178410b03661d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34564928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38923d6791a09ab860360e561db13df5ce51bab6f32bd4d42bcd1b54cde82907`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:20:46 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:20:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:20:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:20:46 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:20:49 GMT
ADD file:4e52928c778d7e98d90ccfcaacd039ae1fdde494dfa310adbe229d7051c30918 in / 
# Mon, 25 Sep 2023 10:20:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:53cc531c2e6e7ce32a82e9a21f71c9b4d11b0ccd1ef71c8c9e1493d2ec8969ad`  
		Last Modified: Mon, 25 Sep 2023 10:30:56 GMT  
		Size: 34.6 MB (34564928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:7c789f181465e5474aa9093b939a9992e2e67637c827a1b81e7890c3f04f6bf6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28024260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04042eae942dd0a766b4d45f17617014c8c3e464113d08a245ee7b43ddfb1f6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:26 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:26 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:28 GMT
ADD file:78683f2464233172a7cd0d6adc4c7d9fb3ef05fa67ca22e6fbaca0325496a536 in / 
# Mon, 25 Sep 2023 10:17:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:594ea103c983265390944410c6ac8624359909261a656484e971d00ca0ff8b20`  
		Last Modified: Mon, 25 Sep 2023 10:31:02 GMT  
		Size: 28.0 MB (28024260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar`

```console
$ docker pull ubuntu@sha256:ebeab264a6aa31d73b4571f5ef7534b2180cc2a5011422c09ca45934e63f101d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:lunar` - linux; amd64

```console
$ docker pull ubuntu@sha256:24898c8e1ac370d2d309d6d9df56af52bebdad86925c623b5e87e12404453518
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26873617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21098a29e034a8f6f1952d1d8a49b5732b70e532c31f0e88e1ff499c6540c57c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:28:31 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:28:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:28:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:28:31 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:28:32 GMT
ADD file:7392bed4dbab9fb7c9ad5bde6f3bfcde3bcbf1885c336af9c231af6defaa31e1 in / 
# Wed, 16 Aug 2023 04:28:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:10fb01f4f619bc954ba611cebca23f2b96d255c7ead4040b449f063e530df1a4`  
		Last Modified: Wed, 16 Aug 2023 04:34:32 GMT  
		Size: 26.9 MB (26873617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4dc1dd258d16171c6cd696ed5420402319d7cabe638b176b471495e94373f2a9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24629439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83502f31cce9655561356390e34e8d506e888f6ce4743a8400bfa765f6eedb8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Oct 2023 12:25:21 GMT
ARG RELEASE
# Wed, 04 Oct 2023 12:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 12:25:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 12:25:22 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 04 Oct 2023 12:25:24 GMT
ADD file:b92305119eab5dd3dfb00f4d83cd84e00c8ae57143739329da5a19aeda55be4e in / 
# Wed, 04 Oct 2023 12:25:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:725335f54d3eb8903e713867d9f04db29fbc8835da3539fd3898faa22eaf016e`  
		Last Modified: Wed, 04 Oct 2023 12:33:24 GMT  
		Size: 24.6 MB (24629439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d68d8bcae123a839bc72b91fa9df55956be3fcb2dbfc247acb7f65908eaa6c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26064545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c8e9335de75964dd320b20b4290408432be2962faf7ad36d3a47d48f3131cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:15:57 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:15:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:15:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:15:57 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:01 GMT
ADD file:adea2962926b29b76eb8da76ae9e830c5ad7050ae9b19f5427191b338c8a2c56 in / 
# Wed, 16 Aug 2023 04:16:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2b2d15932a31f0857b9499cc218b8777708cb1d73ae6ef680f624ca7d4342763`  
		Last Modified: Wed, 16 Aug 2023 04:34:39 GMT  
		Size: 26.1 MB (26064545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1306e75f505a2305f2c46f51f33be8b8599923bd5a652c3b5dc37333db4f44ab
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30905042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91733a8763fe80d6e620ec400c2721ee45c0f80398506088d1278d6531299a90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:16:31 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:16:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:16:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:16:31 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:34 GMT
ADD file:a9d35b320d969ee1ae8a7bc83aba49da30d93724befb5948c680066ad4f1acdf in / 
# Wed, 16 Aug 2023 04:16:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f51cbff870f31d4c4397c2f21529046998f8d6e7748fd6f059b325a0759c7dd4`  
		Last Modified: Wed, 16 Aug 2023 04:34:51 GMT  
		Size: 30.9 MB (30905042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; s390x

```console
$ docker pull ubuntu@sha256:ec9620bbf89d1a3b1171f961340a890166607be3423d96e740f6d56f36ccb125
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25691524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1289eb3132a14bc161676d7f928d557bf63eb8561718e9d5247e16e88ebee8ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:29:27 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:29:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:29:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:29:28 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:29:29 GMT
ADD file:14fcf0756fb29b609af54412c31e2ff9acbf4634984ce95bf204c67668706cb5 in / 
# Wed, 16 Aug 2023 04:29:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b1e434384d3d3b546e155df0cf143c8c0a92bf766c6808bf2e3e1d2f22010839`  
		Last Modified: Wed, 16 Aug 2023 04:34:57 GMT  
		Size: 25.7 MB (25691524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar-20231004`

```console
$ docker pull ubuntu@sha256:1fb2e8014872b7372d830254271344ceba8f921ac1d56da586050e663ec9d1a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 1
	-	linux; arm variant v7

### `ubuntu:lunar-20231004` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4dc1dd258d16171c6cd696ed5420402319d7cabe638b176b471495e94373f2a9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24629439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83502f31cce9655561356390e34e8d506e888f6ce4743a8400bfa765f6eedb8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Oct 2023 12:25:21 GMT
ARG RELEASE
# Wed, 04 Oct 2023 12:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 12:25:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 12:25:22 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 04 Oct 2023 12:25:24 GMT
ADD file:b92305119eab5dd3dfb00f4d83cd84e00c8ae57143739329da5a19aeda55be4e in / 
# Wed, 04 Oct 2023 12:25:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:725335f54d3eb8903e713867d9f04db29fbc8835da3539fd3898faa22eaf016e`  
		Last Modified: Wed, 04 Oct 2023 12:33:24 GMT  
		Size: 24.6 MB (24629439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

```console
$ docker pull ubuntu@sha256:527def7ad4b6f32f5188f36daf7f29bcc307542fd1a79c2326d3ed3ddd8b3351
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:mantic` - linux; amd64

```console
$ docker pull ubuntu@sha256:7e44d7ed904145328785378ddac5de49ac931d3b28b72f6c9f5fb350f9b4a849
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27277147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8801a7ecb54952ea17852be887c1d858fd7bd78dcee093afc11fee7ed53f7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 Sep 2023 05:03:43 GMT
ARG RELEASE
# Tue, 26 Sep 2023 05:03:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Sep 2023 05:03:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Sep 2023 05:03:43 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 26 Sep 2023 05:03:45 GMT
ADD file:5fb49f260a0c3bf404c0fe31d8f0f812e9c143bd48223c4f15a85168758eb880 in / 
# Tue, 26 Sep 2023 05:03:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:97e98d3adb77a3f73850e0a81cdde417afce9cd9dce78c444f99b9258caee9fa`  
		Last Modified: Tue, 26 Sep 2023 05:33:55 GMT  
		Size: 27.3 MB (27277147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2a465a4c4831c57977b6646e481f504061294f1bf1ae1b99fb5d93c67b8a471a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25201383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc753c284b47a7a5ff3ec2e926551ba95dc6c9072415649cb13a9cdff503dc04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:02:33 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:02:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:02:39 GMT
ADD file:1be1311acbd557f7769fb5c1913ef56305431e7547f96c20ac36284fdd926223 in / 
# Wed, 11 Oct 2023 18:02:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8761b0d436cd2e1ff47496b7cc353cf0b49347ffc92b070c31a5cf5431041614`  
		Last Modified: Wed, 11 Oct 2023 18:18:00 GMT  
		Size: 25.2 MB (25201383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:bb9a61edbd6cd4f0b8458daa9a78bc09ff7ffe638e7da0a85dc28a5b6c26adb2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26356283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461b48f7d9e026c91692982d4ad80e66be3245f28c14eebf5e1c2fd88c95bbe9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 Sep 2023 05:06:27 GMT
ARG RELEASE
# Tue, 26 Sep 2023 05:06:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Sep 2023 05:06:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Sep 2023 05:06:27 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 26 Sep 2023 05:06:30 GMT
ADD file:0dbbd4de9483bc32897d525742b94aa13ebd3a6aac7f1844d94d7f4536b2bfb8 in / 
# Tue, 26 Sep 2023 05:06:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:afcf80ae17bcd3e5b46853b0fd5d9358fc62ae2b878d7ccb081bd357330cd0aa`  
		Last Modified: Tue, 26 Sep 2023 05:34:02 GMT  
		Size: 26.4 MB (26356283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:7b532d2ce398e717ab17c9280bfac4f8cc34e8104313149c6891f9f1ed3648c1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31341680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9cdbbf45d488137b78c5d4e544935a5a2dd90921911c5c2ebc35b3453cf223`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 Sep 2023 04:52:53 GMT
ARG RELEASE
# Tue, 26 Sep 2023 04:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Sep 2023 04:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Sep 2023 04:52:54 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 26 Sep 2023 04:52:56 GMT
ADD file:cbeb7f814c9eebdbdc6b8e10fb87ba8334b3f6203ceb166c48f6d7492ab07c4e in / 
# Tue, 26 Sep 2023 04:52:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3261179759b520c84edfab6a5842534e3552b99a5f71b1e44ccbd6017eab30b5`  
		Last Modified: Tue, 26 Sep 2023 05:34:15 GMT  
		Size: 31.3 MB (31341680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; s390x

```console
$ docker pull ubuntu@sha256:a353c527eb5233fdfc2ad112c7897cce7da6ac28b24d3aaa8f441f27ddf613c9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27072390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12eca28f81d0bd51084742dc133e32c215a83739fc5603306f1ad774311dc6ba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 Sep 2023 04:58:19 GMT
ARG RELEASE
# Tue, 26 Sep 2023 04:58:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Sep 2023 04:58:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Sep 2023 04:58:19 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 26 Sep 2023 04:58:21 GMT
ADD file:e86e9b7546a97fa45e9c726cc317a624a7f94b0bd6dd413d89946ff778b18c77 in / 
# Tue, 26 Sep 2023 04:58:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:56312385d597227d0c1232049609586ed3412b04e6ec96c5f6626f5f50f438fe`  
		Last Modified: Tue, 26 Sep 2023 05:34:22 GMT  
		Size: 27.1 MB (27072390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic-20231011`

```console
$ docker pull ubuntu@sha256:5c629220043676156e797624fc7ae355e758a6dea351ee4cb3c2855923ba66aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 1
	-	linux; arm variant v7

### `ubuntu:mantic-20231011` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2a465a4c4831c57977b6646e481f504061294f1bf1ae1b99fb5d93c67b8a471a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25201383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc753c284b47a7a5ff3ec2e926551ba95dc6c9072415649cb13a9cdff503dc04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:02:33 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:02:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:02:39 GMT
ADD file:1be1311acbd557f7769fb5c1913ef56305431e7547f96c20ac36284fdd926223 in / 
# Wed, 11 Oct 2023 18:02:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8761b0d436cd2e1ff47496b7cc353cf0b49347ffc92b070c31a5cf5431041614`  
		Last Modified: Wed, 11 Oct 2023 18:18:00 GMT  
		Size: 25.2 MB (25201383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:0fb34c7833dd5068f98180c802000187ca9a0c5fa8960b6c50d4965c34bb1e43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:rolling` - linux; amd64

```console
$ docker pull ubuntu@sha256:24898c8e1ac370d2d309d6d9df56af52bebdad86925c623b5e87e12404453518
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26873617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21098a29e034a8f6f1952d1d8a49b5732b70e532c31f0e88e1ff499c6540c57c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:28:31 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:28:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:28:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:28:31 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:28:32 GMT
ADD file:7392bed4dbab9fb7c9ad5bde6f3bfcde3bcbf1885c336af9c231af6defaa31e1 in / 
# Wed, 16 Aug 2023 04:28:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:10fb01f4f619bc954ba611cebca23f2b96d255c7ead4040b449f063e530df1a4`  
		Last Modified: Wed, 16 Aug 2023 04:34:32 GMT  
		Size: 26.9 MB (26873617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2a465a4c4831c57977b6646e481f504061294f1bf1ae1b99fb5d93c67b8a471a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25201383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc753c284b47a7a5ff3ec2e926551ba95dc6c9072415649cb13a9cdff503dc04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:02:33 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:02:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:02:39 GMT
ADD file:1be1311acbd557f7769fb5c1913ef56305431e7547f96c20ac36284fdd926223 in / 
# Wed, 11 Oct 2023 18:02:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8761b0d436cd2e1ff47496b7cc353cf0b49347ffc92b070c31a5cf5431041614`  
		Last Modified: Wed, 11 Oct 2023 18:18:00 GMT  
		Size: 25.2 MB (25201383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d68d8bcae123a839bc72b91fa9df55956be3fcb2dbfc247acb7f65908eaa6c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26064545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c8e9335de75964dd320b20b4290408432be2962faf7ad36d3a47d48f3131cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:15:57 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:15:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:15:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:15:57 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:01 GMT
ADD file:adea2962926b29b76eb8da76ae9e830c5ad7050ae9b19f5427191b338c8a2c56 in / 
# Wed, 16 Aug 2023 04:16:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2b2d15932a31f0857b9499cc218b8777708cb1d73ae6ef680f624ca7d4342763`  
		Last Modified: Wed, 16 Aug 2023 04:34:39 GMT  
		Size: 26.1 MB (26064545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1306e75f505a2305f2c46f51f33be8b8599923bd5a652c3b5dc37333db4f44ab
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30905042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91733a8763fe80d6e620ec400c2721ee45c0f80398506088d1278d6531299a90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:16:31 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:16:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:16:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:16:31 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:34 GMT
ADD file:a9d35b320d969ee1ae8a7bc83aba49da30d93724befb5948c680066ad4f1acdf in / 
# Wed, 16 Aug 2023 04:16:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f51cbff870f31d4c4397c2f21529046998f8d6e7748fd6f059b325a0759c7dd4`  
		Last Modified: Wed, 16 Aug 2023 04:34:51 GMT  
		Size: 30.9 MB (30905042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:ec9620bbf89d1a3b1171f961340a890166607be3423d96e740f6d56f36ccb125
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25691524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1289eb3132a14bc161676d7f928d557bf63eb8561718e9d5247e16e88ebee8ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:29:27 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:29:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:29:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:29:28 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:29:29 GMT
ADD file:14fcf0756fb29b609af54412c31e2ff9acbf4634984ce95bf204c67668706cb5 in / 
# Wed, 16 Aug 2023 04:29:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b1e434384d3d3b546e155df0cf143c8c0a92bf766c6808bf2e3e1d2f22010839`  
		Last Modified: Wed, 16 Aug 2023 04:34:57 GMT  
		Size: 25.7 MB (25691524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
