## `debian:trixie-backports`

```console
$ docker pull debian@sha256:a7c794d72353a24a94fb79c1f0e2341b34b6bbf6e8fd06e48e5519cbca60b104
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:af948f117671acb4132d88f1f88141f20f43e2868b6c3227c900cf99c5f62f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49285852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830c665f45107ff84a0a111e17e2299004385073284db3f144c61683eb6f0536`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:02:45 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4544a72d6b0e19b9a259f245ed6827995316da0a09d42394e27603b8381ec18b`  
		Last Modified: Tue, 04 Nov 2025 04:02:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c24eea164e2bd07ab25ab2fb9ee4e9b27e51afa82f8166aae5a937b71a49000a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b68601e5e0a52c7d6f168732dd191891b29e70a21dbf8d40d7ef3e9aa32942`

```dockerfile
```

-	Layers:
	-	`sha256:b53064faf931c2b616d30714d0a52df1cf4aa0e9bcf2c20e878a196a4cdcb7c3`  
		Last Modified: Tue, 04 Nov 2025 10:29:59 GMT  
		Size: 3.2 MB (3170024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec24d366ac54037009bd7ef7d2f54785dac5816ad47da68efa614857056385a`  
		Last Modified: Tue, 04 Nov 2025 10:30:00 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:60d55888d8e12b04ddf4572daeda16b90183c2c7b50f21d22461be2c5a9c4f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47449649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16aa47ff32e218cdfe9530ef2bc6e373c1c34ba34b14c0b0d9878da7a9d70c7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:20:30 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ece3d43cc91380b968e97ebcb749d1c0cc4d780ea6ab83e3cb6fd3762b28d8b8`  
		Last Modified: Tue, 04 Nov 2025 00:13:14 GMT  
		Size: 47.4 MB (47449426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60968a27b1b9f44b1d699bad6f44ffb91627fdbfbc1929a5b4026723606508c`  
		Last Modified: Tue, 04 Nov 2025 00:20:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bf6f7426b4935102c0333046db77a1178d57aa1d4c0b2196b4a6f06f8f03e0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63063bb5a16e1c4465559c569cdd7d9376a0dbb5de78c77a093efcb04b4f3d36`

```dockerfile
```

-	Layers:
	-	`sha256:e976efd6c04020ef3127d38f85ac55dad20ebe2fe36473b0302ffaa4f311e4bb`  
		Last Modified: Tue, 04 Nov 2025 07:30:03 GMT  
		Size: 3.2 MB (3172961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb7c1b5afa67defd5fa1bf96698b4d4f745d4fbed2b338fd71feef1a163c3e35`  
		Last Modified: Tue, 04 Nov 2025 07:30:04 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e24d2edbeca46d796d03818d6c4300a93dd20c0a1f5b36f064b58999443a6c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45717358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac89c73a8860af57a0bf91c8eb2feb4a55e4ff3265930d32e2b496fdda407078`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:16:21 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:caaccdf8fb49cd124dc4c23baaca3be5aad18c1263c8afe3356d15af000e612d`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 45.7 MB (45717135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57cd9cb7022554709bd9106627bb3bad7944219c25ba675029de578c848f682`  
		Last Modified: Tue, 04 Nov 2025 00:16:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5e4bfe4de311960334377aada36fb288d8fab2ba019ac0f93707a1b761193ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb755614e2dc3424057d22f2c7dba28d776ab09295e20578d50030ed3246d5d2`

```dockerfile
```

-	Layers:
	-	`sha256:7862102508a951f32fcd853e8f3f9bcd2d8cf219b50ed44794474b8fe2184755`  
		Last Modified: Tue, 04 Nov 2025 09:49:37 GMT  
		Size: 3.2 MB (3171398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad26da0f3b95308587f1ab9067df5b6c7683ffe58ab9f799d5e6979833c2f0c2`  
		Last Modified: Tue, 04 Nov 2025 09:49:36 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:90dd8b0ad14e8ebe97d77761077b4bebf6dc4046d85267d79de3fd9d00e355b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49650653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719a5a8424f1f765d7b56cf8350a2cd1a20846f8433b58d7aeb8eecf76cd8dda`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:18:02 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76f06485d7004df1b5af81f205c6b8fe3a12079bb577f168cb84ddc1af48995`  
		Last Modified: Tue, 04 Nov 2025 01:18:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c342b99816f32555f22599533cf0ba445f808b7c8830e3a42fce7acad2c83d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ba10fb032b95665f7e0df7e617182bea82b6d37b1a2f2d05c7598b2eeda52e`

```dockerfile
```

-	Layers:
	-	`sha256:f548ddf40d003042a96ddd8cb4899e7d7cb5bffc624cea16518f431553412b8e`  
		Last Modified: Tue, 04 Nov 2025 09:47:18 GMT  
		Size: 3.2 MB (3171505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fba36e320388d19100778f9199c6bdbd52a56f8f09fa81dff20184264fe68aa`  
		Last Modified: Tue, 04 Nov 2025 09:47:18 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:8af1451caaed6a1202bae30a4b7fc9c520bb97039ee121cacdc17490d5c6db50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50801461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8459e505e9b1eded4e6eeccd7cccf3244cef646a9155fd6b12c1714e3e9cbed3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:17:49 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:933c2eb03a495d1bdbab772ff092366c6df6bb75cafd8749623e94908401abca`  
		Last Modified: Tue, 04 Nov 2025 00:13:58 GMT  
		Size: 50.8 MB (50801238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4f709549ab080b421519efc02af16d11ea0d93c02b1bc019ea4b53520a1d1a`  
		Last Modified: Tue, 04 Nov 2025 01:18:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b5e254d46c71060cd44da709cac822efe5807bf9b3298cdc486c7af633e8a461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be92588409498b04f4ec3fab4b15464ba0017f1653a333a18736f17e2070df96`

```dockerfile
```

-	Layers:
	-	`sha256:78ce78c0667a5955ada04149594debbbfaaa91e819aa6d1f24054c6114dca1c4`  
		Last Modified: Tue, 04 Nov 2025 10:30:15 GMT  
		Size: 3.2 MB (3167227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43d070d761076624fe32ce6411cf050f5348bfcd6c7c2df46cd9910aca5d5912`  
		Last Modified: Tue, 04 Nov 2025 10:30:16 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:022c929877b5192f0286fabdf3a4d87d9d09946b694f302a3b146e6f15dfbf36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53110350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:309becf4b6e3c5311280f48b879291f99c369529ce9480e3e4fe9acb136332a3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:49 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f97b74f644ed65527d413340c5828e3be3f9c4ab84d90cd2c41fc5afd5ba20`  
		Last Modified: Tue, 04 Nov 2025 01:20:09 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:27f2b6b5dd894c4510c9ff3e1b4e90cc761bc792e110202dfc93e736557d52f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8c09616b0c3fd704e1555957402a0017bf7640c6fa51d5ba5b9be66c7a9086`

```dockerfile
```

-	Layers:
	-	`sha256:ec10dbf91169fc78b903c47dac140c79d38484356d1b2bc89e911152b2553549`  
		Last Modified: Tue, 04 Nov 2025 10:30:20 GMT  
		Size: 3.2 MB (3173535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a62c5702d5533e88f92145319de37281d2dbb384f50b5c55704a6df79ef4095d`  
		Last Modified: Tue, 04 Nov 2025 10:30:21 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:8840665111a068825beff33e2b3ac106b128afb57db43739e4486897aeee8c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515b77f759a38cd4a7b813413da363f6a1aec5c55771fc811de601815e76dea1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:23:27 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4e1c32ed7d0367c2a3b90b2f374f3f260880d0511aac6a128e163c0850b8bd`  
		Last Modified: Tue, 04 Nov 2025 01:24:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0504c1bcd73f65a037eeea3c611e9b7ce08d061d1584f8328151d7ac54db9d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06087deb4d5c98ec7d4c0463f0cad8aa15ea96e9490fddee320f48470aefd484`

```dockerfile
```

-	Layers:
	-	`sha256:bf622b29889812c52dc7e79b4ddf3214b15148c87bb525874123599c39cb579e`  
		Last Modified: Tue, 04 Nov 2025 07:30:21 GMT  
		Size: 3.2 MB (3162347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1994dc0ac4bb6fded33e3679a6f07dcd674e7933aa02322baacad497959b6b39`  
		Last Modified: Tue, 04 Nov 2025 07:30:22 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:a9e61cf0d0168db7bbd4e6dd9adc055318f23e9d185e766f31123b5d29a148c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49352522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5161b27b27403f6dfb26117298ac382e24998ecf0e30200eca4e725cf3114c22`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:43:09 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5dec0b9f1299b580c5b19a8cbf0173d732d9b3b6f7a5137df42612867b0c116`  
		Last Modified: Tue, 04 Nov 2025 06:43:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2f8a1cd6fbc67cee0e73e9ccc540c9e5ec7fb5e345ed371ad21de89ab155cf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2442755b43b3c38d9f37c936f2d06ee4628c644f30cb23deda08a9d43f8e1e`

```dockerfile
```

-	Layers:
	-	`sha256:1d7cd8976ceedb30edaf15d33d3fc51e53e34eeef4b4777a6e4a965ab8562618`  
		Last Modified: Tue, 04 Nov 2025 10:30:27 GMT  
		Size: 3.2 MB (3171471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56961a093a3d229dafb15820a670f488b4e9612d286618e7e09564122765bfd7`  
		Last Modified: Tue, 04 Nov 2025 10:30:28 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
