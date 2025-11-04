## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:2ed0ecd20e1fefa99e9a23bb47157b976ec5f05d004676028ebc5a3cf1d29302
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:64cde4d223430d90e1b924ac6cb66b98c47f09a255910179bb7000a6a0ab6dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74901021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5807f958d324cd263ac4a32c3752e147c61a2cfb47b555fdf2f436469197b7c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3143549f2b8b3ad8d79efdc47824641c6771796b3770f3c637a38aabd2b3462`  
		Last Modified: Tue, 04 Nov 2025 04:14:53 GMT  
		Size: 25.6 MB (25615393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d30a8a8816862666fde38fd7c3f2d3e489cf88c176384d955143be9f8253c11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d11bce21094cbaaaa27e98e1c096c81286a62555ba1eae9d8a77d0fe003a5f`

```dockerfile
```

-	Layers:
	-	`sha256:0d5d1420820d82dbc3f94fbe89e127847e25c373389aab690c08b5496dc6d30f`  
		Last Modified: Tue, 04 Nov 2025 11:20:58 GMT  
		Size: 4.1 MB (4118844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ce3228e94a6e1d3f1446b50fab411c80bb5632329449de3b34b5ab62707293f`  
		Last Modified: Tue, 04 Nov 2025 11:20:59 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:299ad5b1767c7a2a9504527892e634bd1a1c386212d1a55a7385b49777982ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71792555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1870bfd20bb4afcc8c3dc5b86291c7055ea4341fb37adc6c6cdbdd45db88ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:28:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ece3d43cc91380b968e97ebcb749d1c0cc4d780ea6ab83e3cb6fd3762b28d8b8`  
		Last Modified: Tue, 04 Nov 2025 00:13:14 GMT  
		Size: 47.4 MB (47449426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e91b819b99c2c8690acb5b01465ae84356bc40a50656db0ab817eb28337198`  
		Last Modified: Tue, 04 Nov 2025 02:51:11 GMT  
		Size: 24.3 MB (24343129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0fbdb6f08160dc6e1220268c86e89d27e8de7c748b6c32a6c6385821c94064ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bc2212b3db85fe4280adedbbc8a9c852c464851d5d7ced47b80d5d24ab3b41`

```dockerfile
```

-	Layers:
	-	`sha256:5427e2415e325957e12f249c2bc5ab6e6cedc15d338337fbb460e593a57dc5e2`  
		Last Modified: Tue, 04 Nov 2025 08:20:59 GMT  
		Size: 4.1 MB (4121834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2811a87cb0162a12f9c56cce6b48bfad5bd21c08a55b06facffa4245e10b561`  
		Last Modified: Tue, 04 Nov 2025 08:21:00 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c7919bb027a384f24eaa6ced89957359c317c3edffd9fdeed99611aa2bc75147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69334250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffd08cb7878ce5b9f79b36db88ab755f52c5b68c6691c41872b57af59569b30`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:40:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:caaccdf8fb49cd124dc4c23baaca3be5aad18c1263c8afe3356d15af000e612d`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 45.7 MB (45717135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1368971cf52e52bedcc9c34f098c9d72d70d67b7064ef11faefe431b570e27f9`  
		Last Modified: Tue, 04 Nov 2025 00:40:16 GMT  
		Size: 23.6 MB (23617115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cf33a8e3a9e4e865554e9597f152c4b820dd7add2a20bb893a03f244c6725e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab921f242f2f5d99552c0f477d7b803e0adb1001b2d6b7b411b38bf82f796e0c`

```dockerfile
```

-	Layers:
	-	`sha256:8b2bdba2cbbbfc1d69b545a1d3e98355cf8e2ccc00b323a792ffb39eeca0d1f7`  
		Last Modified: Tue, 04 Nov 2025 11:09:08 GMT  
		Size: 4.1 MB (4120345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bba7779f199f959aa675d2c340a447f18d0c6ee48a6ac3ca3fe9484bec03c67`  
		Last Modified: Tue, 04 Nov 2025 11:09:08 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2c1e9b9b17f2cea6cfde08d86e05f8e7829cc42c19d77504a7b78963ad6862b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74668007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092b4f9f5da1be03bf942b6edfad25747079c631395f813d86c9914cdd2e602c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f766ef2ec48737a0f300405019c312acd667d14467b50c402750d1454e3591`  
		Last Modified: Tue, 04 Nov 2025 01:30:11 GMT  
		Size: 25.0 MB (25017577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ddf10ad8195661578e8c610fb4187e7c27a381608e8589a6cf2a1eb65aa9562b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a43766596dfdeba128d0a5b0e3a5a452ac0695522c57b2cd507a20f138bab41`

```dockerfile
```

-	Layers:
	-	`sha256:257ab5c5c515fd401452f054c6ac41f34f11dade023de841f7ef0cffacd96c8d`  
		Last Modified: Tue, 04 Nov 2025 10:26:22 GMT  
		Size: 4.1 MB (4120386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724454c56649279089a4c41ea6c829e096176472da03afae69773153faee7d38`  
		Last Modified: Tue, 04 Nov 2025 10:26:22 GMT  
		Size: 7.2 KB (7178 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5bbbafa54c503abb3e0c5a8808c582b4069adf3131dec85d6e50ceb8c1a03f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77577205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18185b8d8c966f82b4782a0514d39c78a83a7343e76bc5af5d24d9b7e674ad99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:933c2eb03a495d1bdbab772ff092366c6df6bb75cafd8749623e94908401abca`  
		Last Modified: Tue, 04 Nov 2025 00:13:58 GMT  
		Size: 50.8 MB (50801238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac49d94324079b69237b0b1612a8d78112618ce6800066877fb7d7a38ff9e74`  
		Last Modified: Tue, 04 Nov 2025 01:32:28 GMT  
		Size: 26.8 MB (26775967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:000c6eb195d5cc8a635fe62d581a49a561069602792657bb2eb850fc3bbc570b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d80885d1e646d3f2ba0318ecc12445fe987c9310f6162e215760f215da69acc`

```dockerfile
```

-	Layers:
	-	`sha256:2c0116a5a90d750c920ebb3fa236856622ae171ddd0b939ea58c69dc5d23b951`  
		Last Modified: Tue, 04 Nov 2025 09:26:56 GMT  
		Size: 4.1 MB (4115952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b939618dd562296ea2cb441580db302c0009036edc130489434b6c1bbba6f3`  
		Last Modified: Tue, 04 Nov 2025 09:26:57 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c3c3f9c4ca2ce647ec7c24fb12622f40fe344f6c8307f4b6d1393fe3005163bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80106760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a46336f05cf00988685a920ba0522c279a066418c07e407dd83cc74542fb25`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c598502b2d4d7d278f56bfb7b6960ccd64d116b7bc7b02516bad5cdad4a631`  
		Last Modified: Tue, 04 Nov 2025 06:28:57 GMT  
		Size: 27.0 MB (26996633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6025e079c1ace6f4c9be10250b09658183690acb8fd42dce86a6d32307cada2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144c77b9fd928d449799f081f638ce2f8c4a7f54905605b5640a831184dddccb`

```dockerfile
```

-	Layers:
	-	`sha256:73ee5246fdfef4f103b47654f8b0b9557062a77abbd0d4e881b6da02452e4d2a`  
		Last Modified: Tue, 04 Nov 2025 08:21:13 GMT  
		Size: 4.1 MB (4122690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a679869adcb6c152468a9993a99990fea1166cf3961ace4e52c6f8aec1577957`  
		Last Modified: Tue, 04 Nov 2025 08:21:14 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4548580a24f3c30de91f1db6e1b941200fe1746b4cff1a95134e51567ac67bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72724180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d7098f368f0b845afa6586462918a1989742829483eb5ca57ea005e525b534`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c640441904d97046ee4a137483e3b6745e0a18782c3b688fede8e9ddf18261f`  
		Last Modified: Wed, 22 Oct 2025 18:09:29 GMT  
		Size: 25.0 MB (24953874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:089e2bd695fb7bdd244b441f94e4724e409493eb148173595429d045c9eb0a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4118521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d866d005aa053255bc5f40ca2dc51429ea233d443c6c7ee5d033b211e538517`

```dockerfile
```

-	Layers:
	-	`sha256:18dca1e03417b8df4c711b7709eeb0acbd77a3b6f766ab1d4ff5cae4b7e4ebf5`  
		Last Modified: Wed, 22 Oct 2025 19:19:57 GMT  
		Size: 4.1 MB (4111354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cfcdb9894264a2abf895c1e78fb5ea2f5115f5c46d1051437dc7d43661ef61e`  
		Last Modified: Wed, 22 Oct 2025 19:19:58 GMT  
		Size: 7.2 KB (7167 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a2b87cfffddb1aa2f1aed8453ed1a73f1196fcf3a4e56b880ed30a282410a746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76135917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4882539d34b91f3dee2f7bc62a35c6b0ac1082200b6a3353197cc3d0c3ce0db`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 10:03:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205358f383faecf1c434c76ac887bd7a626ec58dd373ab479cce2de6c6d63849`  
		Last Modified: Tue, 04 Nov 2025 10:04:16 GMT  
		Size: 26.8 MB (26783618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:32803cfbc206641575bd5b0600401916dbd70fe61e714e616dee18778ff51ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bbf463f3f89f0c0a3bc9ad88947ef9c8a51c803e90a18895d3d577741033f1a`

```dockerfile
```

-	Layers:
	-	`sha256:fc5bea27a62f1202c6f85273000d8681f3b7ec6f8b810e076bdd93f78ed52860`  
		Last Modified: Tue, 04 Nov 2025 11:21:20 GMT  
		Size: 4.1 MB (4120254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59aa19ac9230176c6ce8fca4eed75a6784abf9d7e2a4b018bdd3f27576d99114`  
		Last Modified: Tue, 04 Nov 2025 11:21:21 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json
