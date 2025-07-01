## `debian:testing-backports`

```console
$ docker pull debian@sha256:f9a865a60bffbfcc5ef80cbf2be85ab4d7a58ace445ea6f8ddb9049ea4c1be07
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:6c0c5947dcd89c3e58cd8de906722e1b9dda23a8aca8119243886773a4e9c605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49264095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f25ecefdd906beb2e9c77958e8e2cf3e58fe49d6c26fdbdaab6bd2fb8854119`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8428338b5b0c78b619fd003ce0b25251e613f875f63f2cc98f8197270957b1ae`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 49.3 MB (49263873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666e6540d40a655b5b5c3b0732bdcdf3e77ccce75325c6cad3e11382261ca3c`  
		Last Modified: Tue, 01 Jul 2025 02:12:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0518e83fb5f3ccb7911a34b08b52063000087ded30b451081a6deff213b95f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5962dc12202bf2ded151571bf2656af65ab555782777fb864ab0ac65d6a023`

```dockerfile
```

-	Layers:
	-	`sha256:9f33d16d71f357e14414445e758b8074f6cee514499cb0a0f526348d0b1208c6`  
		Last Modified: Tue, 01 Jul 2025 06:24:45 GMT  
		Size: 3.2 MB (3167842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f1f0f1cd517495af8a8b17cdb4f0978156079eea9fcf244322f951b2be6de7c`  
		Last Modified: Tue, 01 Jul 2025 06:24:45 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:be52e41bf15a1032ef4267f7330be660e967e7cb19ad54ab2502912565725590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47435720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23378938e89f539be13fe7d5c3d979cf7da4ce087f0e15b196115e705da4fe4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'testing' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3f77b16adbe2d2d4eadf5cd0285af46fbcea527fa537f9bf8c691e03594c4509`  
		Last Modified: Tue, 01 Jul 2025 01:16:27 GMT  
		Size: 47.4 MB (47435498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c88702221fabdaee036265c1a86b70c4e0d521d40c0317e9b81dabcc6e8aa4`  
		Last Modified: Tue, 01 Jul 2025 02:12:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9d4924a1f30666cbd68b81130cc1485512632e618faa28ccb92778ad98d2b599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3185920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26e9249573d6ef56586ba475aa638c413db45b73008fa441e6bad7672db24f5`

```dockerfile
```

-	Layers:
	-	`sha256:4652c4c1947f593b7287920d3fcdd572685e12b126f18ae782e6d06f20990a01`  
		Last Modified: Tue, 01 Jul 2025 03:28:52 GMT  
		Size: 3.2 MB (3180032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2458f2e78926686ca9d88f887befee30ae117c3945c11cb7c49371f5901b8fa5`  
		Last Modified: Tue, 01 Jul 2025 03:28:53 GMT  
		Size: 5.9 KB (5888 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6c3c0ab26bd43ed623cf44b3c3a27e052fac5f53ca860635aac6abe753df2904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45708299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84f4b4088ec97e2085beb137ec6b20f2daaa0584506336c464d0e4fb7245ed5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f20646c4a2b733cd102fba447ae91517a497a95d6f1d8645a9dc108ed363e4b5`  
		Last Modified: Tue, 01 Jul 2025 01:17:59 GMT  
		Size: 45.7 MB (45708078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abae46ad21532af9b835dbb5c602c7f1998b87fbcb92ce9e3286250e14cbc92d`  
		Last Modified: Tue, 01 Jul 2025 02:13:58 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fc744b6388d4594fcc8d28491121d56a24b0abb0ee16f07d1c36dcbb95211a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b624fb7c0330537751346d888632b0807aa44cc9c9990ff99fa0a9576b259305`

```dockerfile
```

-	Layers:
	-	`sha256:d2b25883e6e437a5c9a4ec984fab0909fcd4c99e9b5c96644e716b880216973e`  
		Last Modified: Tue, 01 Jul 2025 03:28:57 GMT  
		Size: 3.2 MB (3169216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e00af756f2f9c047c726fdd0188f90659178151d6a36b5b662edf7f460c8016f`  
		Last Modified: Tue, 01 Jul 2025 03:28:57 GMT  
		Size: 5.9 KB (5889 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:980d75062355adad7ce7b66334e53384dc47dc4b8f55402435fc85de323213d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49630374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec733833251919ae83538bac6212b14a6aa981534fb2be58424498714c9491b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:01b2e9155b8de3974ab3f0e86d953fe45550043dcfc59bbefeff90be80100bbf`  
		Last Modified: Tue, 01 Jul 2025 01:17:33 GMT  
		Size: 49.6 MB (49630151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e677919706ec96ab3463189714b13c84d57901c709e750af03c0ab3d781ad85`  
		Last Modified: Tue, 01 Jul 2025 02:13:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:78d64108d6723f57270f32270968484b330ad6c9cec479b083f0b9a1fbcf8778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea109c4910934d317db9a86b85e5893350d350129c3d8b0c2f9e3d567b0623ce`

```dockerfile
```

-	Layers:
	-	`sha256:b2b8082742ab3cdfef77a9252b4546ca5ea2ea7ea9ddf65bb07a88c1e62345f2`  
		Last Modified: Tue, 01 Jul 2025 03:29:01 GMT  
		Size: 3.2 MB (3169323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea71f19921c1c2aadb9e9faa975f678ae10091a57c03760351cdbba518a7a3b2`  
		Last Modified: Tue, 01 Jul 2025 03:29:02 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:44de1df451824b659ab8105b600336c3b9de8ef26b9aeb887a86118e557185b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50786976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70434db6df186ef0cde5a8bcf66742eb75a079e98250d14bb7508aefd71664d1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e5d44060ca935b22b7533a0d87a3e28a3cab4a6f8808b854b08efeffdfe8e460`  
		Last Modified: Tue, 01 Jul 2025 01:14:59 GMT  
		Size: 50.8 MB (50786755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1d5755c37a3482be2b18a0df289867c7ab36a7cd52316ee61321b986d4e3c1`  
		Last Modified: Tue, 01 Jul 2025 02:12:07 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b8bf7ab9c3bec78b0d96b1bbdb82bccea6923b77b49c202d78097ddf36ebefcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefe53040937eb5e37f04eeeb655126391d42525c02e44cc2e8db89f457b9729`

```dockerfile
```

-	Layers:
	-	`sha256:dce2bd0fcc66b05839cd7eee32e62d902b904eac83904de8fa0ef879b0ca13e3`  
		Last Modified: Tue, 01 Jul 2025 03:29:06 GMT  
		Size: 3.2 MB (3165046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4f1d8b33be7ad63e9e4f4be042c5aa7a0a996920ed8aa2c6c36cab4bc554a2a`  
		Last Modified: Tue, 01 Jul 2025 03:29:06 GMT  
		Size: 5.8 KB (5819 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:230c805e5b02934ef450810f499eeb7517867292a4451b8bbd1e292997dbdf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53097456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057897804bb2a62c19ea2b7bf2ffca771eae28a275289db57f6eef4c578f83c9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1b728f09c0d4a884c7e578388880f5403741a8474ca8476b12d102d5483ef593`  
		Last Modified: Tue, 01 Jul 2025 01:18:12 GMT  
		Size: 53.1 MB (53097233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9333dbf3430ec8f19dd40418fc0776bd80054d2b7591f2389bc7a43418d6a3ad`  
		Last Modified: Tue, 01 Jul 2025 02:13:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fb46aa1a62cfb970ea8bce8ef4632e6c908fa1323c13efb0b0e1d6d5657acfe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3186467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b278a7431eb7b741b39feb2ab45337b464b17947c1a5133896b2d45f69069923`

```dockerfile
```

-	Layers:
	-	`sha256:efccc51c6fa60d74d08131c07856ebedd8ff1ea06c05e85480f2354c2fe35a63`  
		Last Modified: Tue, 01 Jul 2025 03:29:10 GMT  
		Size: 3.2 MB (3180604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0646b55f5307615d2778c5424a8f31f9bc3a6f516726fe024efdf4c1a810f891`  
		Last Modified: Tue, 01 Jul 2025 03:29:11 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:d7b35d7f11d04ee970d5d092772b3aebdef6408e8a948b1bb4f437ff0ac8cf16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47750375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af443618778b29bb124b5b53c8e47bb7c84986a1f10848ecc43b428bb97604a2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cad096fe59c84bb10fa3b327f5392eb4f35089b477bcc986db58dad1cda53332`  
		Last Modified: Tue, 01 Jul 2025 01:20:02 GMT  
		Size: 47.8 MB (47750152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9333dbf3430ec8f19dd40418fc0776bd80054d2b7591f2389bc7a43418d6a3ad`  
		Last Modified: Tue, 01 Jul 2025 02:13:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c0e33892e8c2acc4669b9968fb788c018c13d3f90785d8797ac033cd7cfeb338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3166024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bede50734be571ca8530afbbd33a219c680427b02fc40e01540678e868ed00f4`

```dockerfile
```

-	Layers:
	-	`sha256:0ee1fdb6ccfc66e01c2ff6ff4197d95eb6996bb263b96efffe2a6a3bfa6f7379`  
		Last Modified: Tue, 01 Jul 2025 03:29:14 GMT  
		Size: 3.2 MB (3160163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:236ef392ff140201228ddc2b52b36d05233f208ffcac970d59bf55e37ecd5833`  
		Last Modified: Tue, 01 Jul 2025 03:29:15 GMT  
		Size: 5.9 KB (5861 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:344e8aea5b81313fa8eb90f97dfbaba5c777063eb75fb865e72f5d9a7efbbedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49343881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e273fb0536c12b2e5744dbf6c604677da0b4606e5252e8e68ae4b857b375f1a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fe21c97c0cb8e48407e6d6b9e8a182aca6131bfbfd02bc56f0254723e44651ce`  
		Last Modified: Tue, 01 Jul 2025 01:18:03 GMT  
		Size: 49.3 MB (49343659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625f09167aef6e12548b321ca85ca02c382f359ed96a32d24e7387dd7566d634`  
		Last Modified: Tue, 01 Jul 2025 02:13:26 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1df6364bfe84c51fdd73cf1d51f63500558d7a42e1db9c1a390ed89ca32101f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3184379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08703b6d725dc8bb33f476d5c8a44f49aa65a15cd6bec2f91299fc3897ea049d`

```dockerfile
```

-	Layers:
	-	`sha256:b8ee6a3a265b33e7ecd7781866dfe0a6cf055f54bca650f963da23239351a3d1`  
		Last Modified: Tue, 01 Jul 2025 03:29:19 GMT  
		Size: 3.2 MB (3178542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05b82d12b2f64e8b6f8c2d0530f5152dc9a7ebe6792584d59b679cd552c1954f`  
		Last Modified: Tue, 01 Jul 2025 03:29:20 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json
