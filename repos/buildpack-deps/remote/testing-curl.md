## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:20f395b618b8bc9c65a57c137c54e5783503c715d8500457e4e4651705950b75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8e382221cc815f9979d2c8a3838b02df32f99c3cfcd733fc5dbbb12ce821e31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76664746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae25f94bd6438654ece599bd74b7d4b6cea728b87f4443892d2af9bbad30ce2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:41:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:447e2db1403dde86cfbb4e736a0555036d98321ddc327da9305db2a007cde1f2`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 48.8 MB (48757790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fbe9d185e99fa84c122139e8f5eb118264f12c2739d72b125a4024012aa961`  
		Last Modified: Wed, 24 Jun 2026 01:41:37 GMT  
		Size: 27.9 MB (27906956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d7ef80804213c8d9635e410a22bdf82978e6f252485616d7825b44dd2a793fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ae9ace5073fe0ef9d64dffbdd6c47030e7837fefff904526c118ee3ed8eb30`

```dockerfile
```

-	Layers:
	-	`sha256:7c6dbe5dcedf4983e677cf4cf8dc8225fe104bfdecc0e8d633cc86fd60b60c1b`  
		Last Modified: Wed, 24 Jun 2026 01:41:36 GMT  
		Size: 4.0 MB (4044900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31c117241515701528611b3cfe5af3914e6be29b6583695e01b6941ec8b67844`  
		Last Modified: Wed, 24 Jun 2026 01:41:36 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:74ce74d09c3a82f153f033343f93f3e99080aac08bc0744399c033db2a7fbdb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70956117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8eaf031a742e34d14d8cbb5e6e3ac4bc1787c630f20283b5da2c2f1fc6a690`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 02:24:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:36ada862ffe71636cce33b70f21dd2f7cfc66ebaeabbfa49191690cfe0284fba`  
		Last Modified: Wed, 24 Jun 2026 00:27:47 GMT  
		Size: 45.7 MB (45653092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf71912b2942b0ebe3b4c7af5551cd81a88d82445a23cdcd992766cd0205984`  
		Last Modified: Wed, 24 Jun 2026 02:24:21 GMT  
		Size: 25.3 MB (25303025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ca34d744c483c7145d39b221006a445cfdda9c12d246c297640259bd2cb764a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4053224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8e490bfb303ccfa934c256b4ecc83ef1a3935a2dbdf4f28f9bb21c8c51036d`

```dockerfile
```

-	Layers:
	-	`sha256:f2c12c11c5316a9a633e04ef765f3baea97dd43a4172ccdcabfc2547ae5ae5fb`  
		Last Modified: Wed, 24 Jun 2026 02:24:21 GMT  
		Size: 4.0 MB (4046387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f209b294281cdcda63b07da558a1648800ab05a9313b490799c085b837a923c9`  
		Last Modified: Wed, 24 Jun 2026 02:24:21 GMT  
		Size: 6.8 KB (6837 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:40ddfd7920e9330367e594dda7461fc28a27f6f8619947c02ee453bfe374482c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75880135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2186c50b5a5e4a70031a7967ed134c9389d40eb78370c0103737317c2066211c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:45:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f5991d5bb2fa21186c9152bf0a9fa1c9c73892f68235c440c9967628fa5ecac9`  
		Last Modified: Wed, 24 Jun 2026 00:27:35 GMT  
		Size: 48.8 MB (48768712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6ca5e706504383a18ce6cb67cbeb352fc200523287b4db4c777b56d674314f`  
		Last Modified: Wed, 24 Jun 2026 01:45:13 GMT  
		Size: 27.1 MB (27111423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:809512de9e7adf0111ee4b1562446f184646209f953171145bab1ab7561d3e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceae88ec13481985f682a17dd99c6bc187a82e376c2c1732aa5d60be5d04c457`

```dockerfile
```

-	Layers:
	-	`sha256:cec7957209cef1ede91208460380119181b921aa85714503bae7169d856fa2b0`  
		Last Modified: Wed, 24 Jun 2026 01:45:12 GMT  
		Size: 4.1 MB (4050259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebd7583cb6bebdec3d4a2937976d1d3cc404d8e778b69a1f0810f8b08d8dfd41`  
		Last Modified: Wed, 24 Jun 2026 01:45:12 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f39107c58ddbc954226963550c901e73aa1d7914f05f58eea63f844d5ab6bf88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79082165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3464716767029115a615886685ef5d0cabfd5b3003d0923d4f85b0f861605e65`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:44:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9b65e2e922e5570b1d72c057efc4f398b0b14051ad2a0b581d6669e50195e288`  
		Last Modified: Wed, 24 Jun 2026 00:28:28 GMT  
		Size: 50.1 MB (50051032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfcdfe53f6d94291d31eb390003496590b495637ff3e5a6cf06797e1f95ca6`  
		Last Modified: Wed, 24 Jun 2026 01:44:13 GMT  
		Size: 29.0 MB (29031133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:47d6a3031d9efa2e7f8bc9f86a67b1f72ecb35af03869b4d9557a20d2bf79a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4048766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d8d7f50cd8cec6fd6399315849c480972867da01cd2e835a8457f026deb7d5`

```dockerfile
```

-	Layers:
	-	`sha256:f14306b40f2a4d90cc210b62fd7fbe5132d584ee27dbe39e253190537ef835f3`  
		Last Modified: Wed, 24 Jun 2026 01:44:13 GMT  
		Size: 4.0 MB (4042015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b943ae6e43386f67c32bec5d68c8ef0de4b16c240ee14aafc7396b47a817c5dc`  
		Last Modified: Wed, 24 Jun 2026 01:44:12 GMT  
		Size: 6.8 KB (6751 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e59d4a1cc7bf2d9cccb2cb8b74000e9aad4b5738a77b83db3a92d85c40da06c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83389746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23c234428286e8dc259b2a67d0392189cf93ddfee226f25a0ba1e70cd78defc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 04:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a6e9fc5fff5ecef539442636839ebbab04ed9b3cd7caa39a93b1023297047494`  
		Last Modified: Thu, 11 Jun 2026 00:22:03 GMT  
		Size: 54.1 MB (54103105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ae67043641e8afbaed6931d7c5b7fbf2860dd1ffd02c08f3ccdcf4f71c0dc8`  
		Last Modified: Thu, 11 Jun 2026 04:44:57 GMT  
		Size: 29.3 MB (29286641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6a768843970cc5a5c1ec40372a84caa397db30720c9da9936ff2604496398380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4059606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43003b6ba0a062ba2a740500e50bfcb4ce18d4079842bd4ca16b9a1e7bab0457`

```dockerfile
```

-	Layers:
	-	`sha256:d4a631d8671cc5c5eb944f74b1e55b6d19fbab3c432346aa817c6430f002e75d`  
		Last Modified: Thu, 11 Jun 2026 04:44:57 GMT  
		Size: 4.1 MB (4052801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:657505c9093e3fc1b5b4ced68a1537c7c953f4bcc136771c43c130d7c16f7d72`  
		Last Modified: Thu, 11 Jun 2026 04:44:57 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:fae1724b3684936ba0ce968cbd78fe646590dbacea098e7f500e303899a407c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73339756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352dc96fc9928c2c1fbf7249068f53fd88ab0562736a4c05227f172f400cd510`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1781049600'
# Sat, 13 Jun 2026 04:38:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ed3cb07ce8ad88fd9ce6ed049f21f5d3412d5a91293105a260fd0d8e0631f44`  
		Last Modified: Thu, 11 Jun 2026 02:45:18 GMT  
		Size: 46.9 MB (46868403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb714707e363663ab0edd89dc96807f795de4da64598f885f54d7c7c44ada6`  
		Last Modified: Sat, 13 Jun 2026 04:39:40 GMT  
		Size: 26.5 MB (26471353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:61a58d1f1b42b2636ae62cd00348c677201e3d9d2188508015f8522816fbd120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4047453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ff97dba573db87577a3d12f9e012e04281a5526a4b4814001eb788792d58d2`

```dockerfile
```

-	Layers:
	-	`sha256:5d06fe1f49a2b7eff8ce155f7c8b25c938d8e8b80af7181b572a66f487594d3c`  
		Last Modified: Sat, 13 Jun 2026 04:39:37 GMT  
		Size: 4.0 MB (4040648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ceed0e155877499fa0c62198bbc0a50efcb5fbe21983b0abd8458746f306b37`  
		Last Modified: Sat, 13 Jun 2026 04:39:36 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fd50bbd6aec15035cb2188f37b21e9daa24e5ec5c3b392e664d04f0d719237ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75994522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7273eac213a88d1d6e0c6995fda172e6f175067d4d6b57b2789638dcbd7b6b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a0b2fd23e0800fbbfc85ca591b838ee879d8a24facc5eea58fda6e804f1b9315`  
		Last Modified: Wed, 24 Jun 2026 00:27:12 GMT  
		Size: 48.5 MB (48491838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43575a3ea94da16bd123e8c57b5643233473a759e5bc49fa7c335021337677df`  
		Last Modified: Wed, 24 Jun 2026 02:46:16 GMT  
		Size: 27.5 MB (27502684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:530f1a2a4e9dc08170af730a85d9c232b528969e36a457063c5bfeabeb8a49e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4053085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3273028a4560c0a4fe6fc6d5eb2422cba0bdc743dd4ba41fcb467384085f40`

```dockerfile
```

-	Layers:
	-	`sha256:9cf672f5a97162cee4bf6ef58e3e0af87f884ea3d65363c662acc5395008f664`  
		Last Modified: Wed, 24 Jun 2026 02:46:15 GMT  
		Size: 4.0 MB (4046312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41d75d298016e169167bed2e8d8a0df033c9cfd67a288cbc40cf0c5197d4c667`  
		Last Modified: Wed, 24 Jun 2026 02:46:15 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json
