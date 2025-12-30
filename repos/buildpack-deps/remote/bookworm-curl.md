## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:a8535ee86f19c9c1ce5bcf976676c0c113aa4e34ff8c78b3c546aaccdf588ed1
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:36ddd30ca6102231dd7128c1434a620ed04bb3f5182fbce81a5cfe571e9c1567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72510140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b524cbf5f2d273289292c58134776afc4cb3ea57e0bf8a3644d973235dd5fb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c22046a8f391b7e83976a1628aa39bc21434b76d2bcdb6ba2c79301dc152fb77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab98a1c6349af1d7446009980f76eaf6215f726cafb94381c2571c3936d812f5`

```dockerfile
```

-	Layers:
	-	`sha256:788ecdc644599f062de50c4181b079c13b980a96b64d76bd5f108cf3736d829b`  
		Last Modified: Tue, 30 Dec 2025 02:20:38 GMT  
		Size: 4.5 MB (4513691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccaf57eeba17e0bbfe6443e35d276751109513a2461128f01360fcbf03217efd`  
		Last Modified: Tue, 30 Dec 2025 02:20:39 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1ba76fb208a9547139c4c1a5fa3eef77cace1d38916cf4455cf5719a904edb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68721707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8160b8f9b88669d5f947582b6983030291b082fd0d0fa7c027d84fb2787f96`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:28:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:382890ab3968ba1cefa561463cb731ea178ca7d67e9b6d5bb6fac532b4127c25`  
		Last Modified: Mon, 29 Dec 2025 22:25:07 GMT  
		Size: 46.0 MB (46015872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f922b13fca1ac9a337d28b41c5bbfa20f6d0bc0a979682648a1f6f51b92fc0fc`  
		Last Modified: Tue, 30 Dec 2025 00:29:08 GMT  
		Size: 22.7 MB (22705835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cfee7c5066a906164d5733521efd0511044f1bea24390d0f1fbcaa307a5f5e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee254fd9a259d5c5e62aaf8892081386e5e654baa83ec2f023eccb84421f230`

```dockerfile
```

-	Layers:
	-	`sha256:04bf3d266468dc900bf545e645acff26768b194d43258fd6ccca13177454aa81`  
		Last Modified: Tue, 30 Dec 2025 02:20:43 GMT  
		Size: 4.5 MB (4517507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2afddaae3d384e231c8819542347ac4345e2b65496ba4acec1992df774d7d2a8`  
		Last Modified: Tue, 30 Dec 2025 02:20:44 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2e0aa1f7b33792ae7daa8d950d41ca24a390c671f09f366be2c1a60897387948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66130892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e947ea59f8938ec0eee7d1c192dec80867d953c958e0ccb478c8aaf2e9dd8cc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb8db5ae0eab82c780cd4fa20967bd3633799cf8ed89cd7858d72dcce53203`  
		Last Modified: Tue, 30 Dec 2025 00:33:50 GMT  
		Size: 21.9 MB (21934762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:931d913d80e5e325d5e09ed327ecef87248d9e22e225b112fe6120517c39b1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee696b032d0470ca1a8d485c1757d043369e6250b4f91c96b023c66f0d6bf5a`

```dockerfile
```

-	Layers:
	-	`sha256:a75b18bca72f0a2166bce693815a104a69d234dbeb7ce9d286e6225b36f5cfe7`  
		Last Modified: Tue, 30 Dec 2025 04:06:17 GMT  
		Size: 4.5 MB (4515980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c46cf0d5536a41df5fd63014cdbf83177e94b19ca48011b776bb7515a6eac8`  
		Last Modified: Tue, 30 Dec 2025 04:06:15 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cb44ddc9759de01da5d7d36c7256b201fadb1c239d25e145c8f5bf52cf5f25c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71957527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1225ad1e904ea2ba8d2891f58e39bd5b9eef6b5197804661389867b1677f74`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a00d1b6faee5f1373704bfff005845c65c750913979f50ac398bcf42fb2a7edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b1a58c3c24146cd61131fd95e90e3603621b6443003f48ac9cf960f7b22a1d`

```dockerfile
```

-	Layers:
	-	`sha256:a523e2d2c2577d8f8524116b3fb644a2a54c673c92be56d61d8a35295c144147`  
		Last Modified: Tue, 30 Dec 2025 02:20:52 GMT  
		Size: 4.5 MB (4513952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:752b064d41e283e958825e9e0571cc74912aa666304670a2674c114a95448387`  
		Last Modified: Tue, 30 Dec 2025 02:20:53 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:bb003fcd4bb60ac7dbdab25cdbae8570304388199e180e7dbbccdc775c8e99a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74331345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e50bad35853e1f2398f6fd8fe303c09428bff29405c6de422e7bd4040ec5659`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d27cc9ffb7903d292157edf3b1fb57175a2a59b66ae4855d328a6a97d9b4a6e9`  
		Last Modified: Mon, 29 Dec 2025 22:24:49 GMT  
		Size: 49.5 MB (49466879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63bb42155eb2fe3cb6496304c20382db95885b672da0e34a3fffa188861a6ec`  
		Last Modified: Mon, 29 Dec 2025 23:47:31 GMT  
		Size: 24.9 MB (24864466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fe1be8d6e39eacbe76ef7516cf8c853203ce718c4941db0af51f9f619fc5ddb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199e3e205fe6bdca1fe563610d9833e31a0f3b85ac2d42a77e922620bdd0e7a3`

```dockerfile
```

-	Layers:
	-	`sha256:e6f96d72805444fd682a58354a44552443eed3bf9037b7255ae52786cac8a4d3`  
		Last Modified: Tue, 30 Dec 2025 05:20:12 GMT  
		Size: 4.5 MB (4510811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2d175ec8725011a71598d24d24f19621f05c7742fd3d8b448c9193c943cda61`  
		Last Modified: Tue, 30 Dec 2025 05:20:13 GMT  
		Size: 6.8 KB (6795 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:95207c8cadeeb5610c46ddd3d5d44071bf8f33980b5628fbfdaa5352387a1645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72374737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa5ddd42d58e7bf7a7825f2a59bd588a7143015c89c796947b41f5cd20fbd3c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 11:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6a43d59f754c088126249c7de1413be451574eda24274414bef9aea85a3ac886`  
		Last Modified: Mon, 29 Dec 2025 22:38:14 GMT  
		Size: 48.8 MB (48760925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec26c7ec0c76b4716fe076707c8489ced71c06858c4f9f03f18c306cb4344cd`  
		Last Modified: Tue, 30 Dec 2025 11:50:06 GMT  
		Size: 23.6 MB (23613812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7f073a79da8093e86f3f618ef27c73af9a5baac45ff19d971cea6961d2661b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16181d99b8f0c6fa978c1f693a502f349125c122c066fb2d1d5a7fbbf03aefe0`

```dockerfile
```

-	Layers:
	-	`sha256:4a81918a2c90a7eabbde5e6197a4fbf405d555e5efe2e5fff35cc7dd2476b901`  
		Last Modified: Tue, 30 Dec 2025 14:19:54 GMT  
		Size: 6.6 KB (6649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fe581d6ee8cff3559b9cbbe598339ebb601d77981d35471db97a0e77b40c8663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77999163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25289d2b21f541ad45f9d127a49417668b7bc84f9f56137fec36374baa8ccff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:30:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7517c515ac5fd6799cec288b72512b8ea3fc54d2d37de5af54d06ba0ea2f21bf`  
		Last Modified: Tue, 30 Dec 2025 01:31:20 GMT  
		Size: 25.7 MB (25672165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c177b58333b126f7b3b31cdb7ab74443d387dcdac2651bb4d40016d9c2a9a1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92b89adc6a43c87fe1e9c375efcb21c0a9f980d924eb65140dba1e922356575`

```dockerfile
```

-	Layers:
	-	`sha256:918bca50a3d5e5dde7baa16275b806a4f9fa1e0b35cd42897e53cd76e5874ff0`  
		Last Modified: Tue, 30 Dec 2025 02:21:04 GMT  
		Size: 4.5 MB (4518315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d21bf280d8bf90630fbee57ccc77b9ff26635e584da149e65925cae03125c8`  
		Last Modified: Tue, 30 Dec 2025 02:21:05 GMT  
		Size: 6.8 KB (6849 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:880ed03afbd065ac36712ff14e2b45f80b8d0e62217a35eb07bedac3288856f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71164851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822d5297028bbde8c7cd5f133e3d4db480df6bd31fb042ccbdca9c383002abdd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ce8a6983b315f7ccc96b582192afffde7bfdc0a45f357f2cd098b4f88aab2be4`  
		Last Modified: Mon, 29 Dec 2025 22:25:37 GMT  
		Size: 47.1 MB (47137727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acc4c1479120c6249296b3550670caa7738ba389b23a7ca3973f7732c12c0ab`  
		Last Modified: Tue, 30 Dec 2025 00:42:34 GMT  
		Size: 24.0 MB (24027124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:724ac91bc698d5cef262986fab23612a34d6daf5a87bbe1d473e17a20e5dc3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84add104ec6c67486c3441a9b5d0086579b7cd3b4c506a480d17b224b1854480`

```dockerfile
```

-	Layers:
	-	`sha256:effc0f0b8be8e518a6e4ca057e204826dae510f09e317355600fe638049f4c91`  
		Last Modified: Tue, 30 Dec 2025 02:21:09 GMT  
		Size: 4.5 MB (4510495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:891fbba3b8e42e9a069840e6aa2d8d5c1bb61d64f604240afad6720a420a5d83`  
		Last Modified: Tue, 30 Dec 2025 02:21:10 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json
