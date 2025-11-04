## `buildpack-deps:forky-curl`

```console
$ docker pull buildpack-deps@sha256:10a482d1e1b8878bfd1540b55fd9b0d741037576ed9c8173bbfd5c03b13c0a51
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

### `buildpack-deps:forky-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4ef474eafb2281e7c83f676d6b734724f4bc691c2f79d911b0ea445a3e873322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75783029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229c1be27d798078cfcf51b7909db501316141c138239099fdacb66f979b52cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1760918400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7671d30ee0069a32147537eef1beaae52a71b59148743b8ebecaf97652901808`  
		Last Modified: Tue, 21 Oct 2025 00:19:29 GMT  
		Size: 49.8 MB (49759136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c2fd0983e5dd95ff783e7a6b758ba8883a82b7e9c343a901149c14d81c6f95`  
		Last Modified: Tue, 21 Oct 2025 01:42:22 GMT  
		Size: 26.0 MB (26023893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6869769d09bdb5432426b63105f9c7a569bb27788caf3d5567b9c67700a9b9f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c548319d1f3d54f175d9393ea3e1f60bcd639f75716801ef4104d8fe7d0b8ec`

```dockerfile
```

-	Layers:
	-	`sha256:25d9d4a05fdc2dc5ee7707ffbae783f3e11e57ba03fe1e7ae47fb9050ead7690`  
		Last Modified: Tue, 21 Oct 2025 10:21:01 GMT  
		Size: 4.1 MB (4124722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8c217e4ac4382d568a2e08e108f59e3c0cf5162c94349350813dae8e5ff3ea`  
		Last Modified: Tue, 21 Oct 2025 10:21:02 GMT  
		Size: 6.8 KB (6816 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7735958689d459517df689bed4f112d9b1202558b5a30ff2763cb81a4ae54bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70030145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f6237b11640e8a0b46b2babc6bdd40140b815b6a0668b84ce698d5130e2e57`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1760918400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8d985114d6343216c46b3706ffd32abaa547ef65adf34aac773cf8677bc44aa8`  
		Last Modified: Tue, 21 Oct 2025 00:20:38 GMT  
		Size: 46.0 MB (46030435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8010abf91353efb25458a75f4596b03a8d71a09a8edd6953ba9ad16d1415cc1`  
		Last Modified: Tue, 21 Oct 2025 02:44:42 GMT  
		Size: 24.0 MB (23999710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:744beb666e761fb73ad8e19accb3af897029c19ece62d76c712f862594ecd5d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4133101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddbb382a8ca787da3372eea82f97ecce5ddc68ce5536170f00d20b03164e0b8`

```dockerfile
```

-	Layers:
	-	`sha256:f5916c2fe13ab45ffb198a5d89c58b8a7f43d5c83f289d673356441b1ff29eee`  
		Last Modified: Tue, 21 Oct 2025 07:20:27 GMT  
		Size: 4.1 MB (4126221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8dfe2a75d72e68a802c26580e36c5b29119019b78336a475b57396637ed6ca9`  
		Last Modified: Tue, 21 Oct 2025 07:20:28 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:121b88b81cea96d9bead08d4c76402d36e20f30871a34e363e6d6bec4490f9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75255554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67520f1a64af46ef9d49e69da672acb280ed54a5966fcb90c43795777dca82f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1760918400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f6aed6c6f2efe803974216c59eb03806f2c41bc69dd9196f4b2f7cddd7e58f63`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 49.9 MB (49888482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11839fb5d6866dca3bea3efa274945a8c3723bf835fb6ad17497421280974470`  
		Last Modified: Tue, 21 Oct 2025 01:46:43 GMT  
		Size: 25.4 MB (25367072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:50c09f9a7ae5b429ab7c5992b1dd8e26cc7653e4dba1b575bc813337e5e809cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314614959743474273a0919fa24071fd7a3f2e4bef50946ef5d023e30c03eb20`

```dockerfile
```

-	Layers:
	-	`sha256:1afb300a16495c9e355235267a58289a9940c5050876c4e683af5a1b7a38ed3f`  
		Last Modified: Tue, 21 Oct 2025 10:21:09 GMT  
		Size: 4.1 MB (4125616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1702b30db4d796a05d599ac47623ad595d82f9ff1d4d71330e67aaccbce363b`  
		Last Modified: Tue, 21 Oct 2025 10:21:09 GMT  
		Size: 6.9 KB (6896 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a81d3cda208924b3b528a8fdfff1585a618544dd5c9628f8a458a2696b76bf2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78384214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6828e37315c8efd34d12dd6f9a93a80404c69b02cf46fb502d4cf0a5a3910072`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1760918400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bef87153a80d12c20903cc117b0638354009942edbd8ed3d2109a962622491ad`  
		Last Modified: Tue, 21 Oct 2025 00:21:54 GMT  
		Size: 51.1 MB (51134403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f73306b9394ed7f30a96e0fbcfc141cdabfb83109d8e85bdac496e2c9cdcf3`  
		Last Modified: Tue, 21 Oct 2025 01:53:28 GMT  
		Size: 27.2 MB (27249811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:95bfc39cbc7e4dcfe789fccf0747a9b4c4e619905e6588696c7e345896258d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd6dd2b3a52fc7e5d492abaab4aa75a90177da2c78adc6c751c0a4e53d60d53`

```dockerfile
```

-	Layers:
	-	`sha256:d3661313fca710cbc34d5115d742d918402bb9bbae247f72568e228e02bc42ed`  
		Last Modified: Tue, 21 Oct 2025 10:21:14 GMT  
		Size: 4.1 MB (4121839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38fc12bcfbfed0c77d82dcdf44b49518f238647a35344dda61bf375ab42681b3`  
		Last Modified: Tue, 21 Oct 2025 10:21:14 GMT  
		Size: 6.8 KB (6794 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cbf949821e731c813f8bc8ae85811fe99f1bc7f6d7a0e1063797d9f3dedbf97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82113616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807bf6ab5043807f97ccbe53cf2fe2650736ea154e97bd353858dd0bc99bb506`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 06:26:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9422d47ff8508a211c5181db20a5b72bab47758f9bcd0687b05752ead1b35a5a`  
		Last Modified: Tue, 04 Nov 2025 00:14:32 GMT  
		Size: 53.3 MB (53315240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11aed674c331384a39236b4b411559b275037202a43d78e434b1d5c25b1e6d72`  
		Last Modified: Tue, 04 Nov 2025 06:26:53 GMT  
		Size: 28.8 MB (28798376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ad08b61ff416410a9fb4cd5e96b8381245cf53969171833704caf14736975d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bea5b276cac62e39382bdc193166cc22f2ece72df87509bb722c9763e45ee72`

```dockerfile
```

-	Layers:
	-	`sha256:e930d45be413860229058e733278d8cdc2af65b2b8cd2effab256f4f4d369567`  
		Last Modified: Tue, 04 Nov 2025 08:21:23 GMT  
		Size: 4.1 MB (4102144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbcbe52b3945b27eaacae78ee63ab431b37f5001439075376f95312dfcf3f958`  
		Last Modified: Tue, 04 Nov 2025 08:21:25 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6162289bfb96a5e8e0dfcb129a1ee28b99bd9d0498db57a4e8d5bf997a7062bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73362044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2ca0f11232b8a16e35fd239e47938d07475257e2e08c1d6bff85a0f7c142eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1760918400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:900b76287341e8d31ab6f7e93e1704f0b3f8f921cc26e9b52c61d9ca744682fb`  
		Last Modified: Tue, 21 Oct 2025 00:21:40 GMT  
		Size: 48.0 MB (48011809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b707e625b2b66ed8212d08094e38d3d8ad6190ee6fb155233b24c4272dcc4f`  
		Last Modified: Wed, 22 Oct 2025 18:02:35 GMT  
		Size: 25.4 MB (25350235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e064de98ab5205eea084a77aea355bf5393c379ae69e0deba504d66ecf151afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c4b260a7d7853f3481f1d7de3e279bc802721833e99034c73ceeb79a278c79`

```dockerfile
```

-	Layers:
	-	`sha256:7607a60ce410c061a126d46a716c9d23775645de77b0ab65e749148825371d19`  
		Last Modified: Wed, 22 Oct 2025 19:20:03 GMT  
		Size: 4.1 MB (4117210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dfe15745566eb72d8a0f5d250d10f3777b904d5b2f1872585e5f3abca0a1d3d`  
		Last Modified: Wed, 22 Oct 2025 19:20:05 GMT  
		Size: 6.8 KB (6848 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:415abc22de7288e36b221084e2638acc086ea41ba193f475977e313c8ca92fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76837617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd64699c661d6861f552de4d9dc54e3ef54fe8cf0df136d24c2160310dedb74`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1760918400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4c17c2477a00887cc596493d4aa463fcafb677435d66760d41166feb0acd2773`  
		Last Modified: Tue, 21 Oct 2025 00:22:26 GMT  
		Size: 49.6 MB (49620788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fe8a7e87d33de6f27420b538e4d4def300139279c514e15386689dae092d6`  
		Last Modified: Tue, 21 Oct 2025 12:37:54 GMT  
		Size: 27.2 MB (27216829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:93e7f59e63eb31e72b605af8f8375768fb1500b52793ae5841a5904d97c2c8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a89cd9e360f6bcbe1c9cde2496d465b45558c9369dc31063b8ad1237d6825f3`

```dockerfile
```

-	Layers:
	-	`sha256:606986c441f4f041355faf7956b16ac22c143af68d23cbd9757d9e4af9da6985`  
		Last Modified: Tue, 21 Oct 2025 13:20:02 GMT  
		Size: 4.1 MB (4126130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0abc78adb48bb1c45162cb1bd1ddefd1cb28aa8bbc7f051cb5f05f0b2e4b488e`  
		Last Modified: Tue, 21 Oct 2025 13:20:03 GMT  
		Size: 6.8 KB (6815 bytes)  
		MIME: application/vnd.in-toto+json
