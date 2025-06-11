## `debian:testing-backports`

```console
$ docker pull debian@sha256:5c7e4d47818ae51065460d69cf2058ff3c75271d1f882712299dd5ffd7a4fbe2
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
$ docker pull debian@sha256:313e031290f22b066095510db02ba45eaebaf81ba5383173674b2cf14d83f672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49254079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5198d7bf6b17f0b18e178f5a2050e0c7d775baa2fedaa861bf980e5c9d9ae7a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4ff4bffc3f08cd1d95feabad784f3c375e82ea1205f7a5a16592da1233a7f424`  
		Last Modified: Tue, 10 Jun 2025 22:47:35 GMT  
		Size: 49.3 MB (49253857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b646fdd45bb0ae1a0641ad73bcea4ab02436f9369ca6f5c75e12de3310502ed`  
		Last Modified: Tue, 10 Jun 2025 23:31:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8130bfdc02b4a8248b536556e27327bd147fd3e2733719d60fddb60894e2d677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3ab6a8dd13c28b22b4e7374ca39befa3c2698cf4762f7f66c10c998c623255`

```dockerfile
```

-	Layers:
	-	`sha256:1b4329b25cf4a2112cb9f1dfaf0f0e73b714bd9b0ccc0ec7b273e03d58a98498`  
		Last Modified: Wed, 11 Jun 2025 00:29:05 GMT  
		Size: 3.2 MB (3167838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65440defd89b3883bacda7cee1475f4ddaabc0b92331af8419d905916951301b`  
		Last Modified: Wed, 11 Jun 2025 00:29:06 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:fe30036759e5519f0f6197e4f97ffb8f7aaaa6f050627d16a42fdae4aa04432d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47445632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3571a941d1a23de659f21e4cf7f9f5a4f47b7d75479d8a76cdfe880d71decb5d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'testing' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8973cdba35bda42e9660b2a491bf855c44e4522c2b3f210e4dfe25c5a9f83eaa`  
		Last Modified: Tue, 10 Jun 2025 22:49:25 GMT  
		Size: 47.4 MB (47445409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5663e0d7b9e6c3953626a69503adeef989cf9aec7da9385548cc09a973cde2c`  
		Last Modified: Tue, 10 Jun 2025 23:24:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:dbd17303d21bc9f7642260ee187d826ac225ba2b06a631f5360494bc05a83a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3185917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc6e8ff5fb54fdee568ad548bf24484c888889c250de4af8ae03deddb073988`

```dockerfile
```

-	Layers:
	-	`sha256:99122eaace6c8087196d49c413ffa34efe22df3acf3ab3f0b071fd69f4dbd390`  
		Last Modified: Wed, 11 Jun 2025 00:29:11 GMT  
		Size: 3.2 MB (3180028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4bbaa4bc048defafe68821906fda89250835aba5ce9b6b1432e1dfd8985b24a`  
		Last Modified: Wed, 11 Jun 2025 00:29:11 GMT  
		Size: 5.9 KB (5889 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4bfd962e1d890c9117c523f208b340f975c7a6d05b93e499df6239ecb4247895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45702266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f621607f0083fedc5806c63aea59606d4857f054d682ee6e2b563bd8e32737df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d4fd96ab718ea83d8a16feaeee1ddb3d6a21e9db8faa26eea7dbded40d84704f`  
		Last Modified: Wed, 11 Jun 2025 02:05:42 GMT  
		Size: 45.7 MB (45702043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17f0d19916a0484ef30fc8826475982cf8ae35e7390e71786de709ce96aa8f6`  
		Last Modified: Tue, 10 Jun 2025 23:26:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:045b29c6601b8aed87bd5d785f155f65c77a8284537cdcdc9877ffa0e55f5a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1618e20b4091d619bb1eab632cc2e57e3c45fc9bfb01caca13f87626e266fb99`

```dockerfile
```

-	Layers:
	-	`sha256:519acbcb766902265ec94e551d0f90b560f1e24672e8b7e187edc9738b99a697`  
		Last Modified: Wed, 11 Jun 2025 00:29:16 GMT  
		Size: 3.2 MB (3169212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:963e2cd374a35362a42e99db127739f86f923d61b33b969e85a38c7802bfd3c8`  
		Last Modified: Wed, 11 Jun 2025 00:29:17 GMT  
		Size: 5.9 KB (5889 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1335526ed4d9e385cb4d55b837e9005879d10020cfc316df30459677a6a2a26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49621750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63034c98dda74ea5d4c7bbc65e4491a59032b7b614cbd3d7d25d3ab94ed835d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2584ee33622825de68aac8f6321753e02da0f3221630beb0c925bab76ac076f1`  
		Last Modified: Tue, 10 Jun 2025 22:52:06 GMT  
		Size: 49.6 MB (49621526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0822ca51558e8749214494edc5e1cc2dfb72a8f5957cdfada8b85f6870da6e7`  
		Last Modified: Tue, 10 Jun 2025 23:31:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c403cdc6cb0c85974b4088a0a164f8e2b2bef89e30ff3e6af170a777e764595e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff96b354e7f098a672222423cc8c85b853faef7af199cb7bac8f7143d51abfe0`

```dockerfile
```

-	Layers:
	-	`sha256:f238225fc0b26d81745460475085569afe4ca0c2c4b087f03aeb730d53c614b2`  
		Last Modified: Wed, 11 Jun 2025 00:29:21 GMT  
		Size: 3.2 MB (3169319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf3b00b47b82f8a786f80b9a4940a3946b1693c88c882b19d9d3269fba7d4460`  
		Last Modified: Wed, 11 Jun 2025 00:29:22 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:46d2def09ecbfd15122bf11af66fc8802fcbc1b9d560818a2be749a76937121e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50765835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ea357c642931bd81142de4e125e983c1f249e73ebb44be8eb389cb55aa473f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:20edef130795139e4061e6054325e5c84743bae712f0f35af4d731a501c8cd31`  
		Last Modified: Tue, 10 Jun 2025 22:47:33 GMT  
		Size: 50.8 MB (50765612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145d2dc02dc6c69d8edd07e2b17098ec983f863075b8d8541f71748017443d30`  
		Last Modified: Tue, 10 Jun 2025 23:25:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f0f88502ede6135db17a38654ed360d88aa2cc27da8b35e396a9528b29daefb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4c05180cd08248894754b6e94e017ea972a53a0a2f95bd5fddd9f1fb2ee432`

```dockerfile
```

-	Layers:
	-	`sha256:8a555bc43a250daa2ac7cd5c9ff6fd970573087e78f54e57b333e9082fe5bc29`  
		Last Modified: Wed, 11 Jun 2025 00:29:26 GMT  
		Size: 3.2 MB (3165042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d821a768e040583dfc3f5a34b8402c99a770ebfec25fa517916dde49dbd9295c`  
		Last Modified: Wed, 11 Jun 2025 00:29:27 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:725e438be6fa3fb01820c6414a1e389d735f69dd9d9fc6d17ad1f16f7ec24534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53091154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c574b385e6c3caa9a9f0a850f279d8aaae656c826bce357ff0db425e8d816d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0c6457f694fbdaf02bab289aa278962ffe34817c6b1567f0311b7021b6a6ef4c`  
		Last Modified: Tue, 10 Jun 2025 22:51:18 GMT  
		Size: 53.1 MB (53090931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5351c4ba024434246f3a28225101ea497d0aa81882e06e830784312b2bd6c119`  
		Last Modified: Tue, 10 Jun 2025 23:32:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:dd35bfc7acc84014fe9be0677600a4b274fefce0f28746dbc9324b3617f10e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3186463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb93608860607dba469538cc0cf991bc293db8336a23cf0f20c34cbd5b3d5ef`

```dockerfile
```

-	Layers:
	-	`sha256:8e4d1505af4b1a69fb7ff4b6651597f60ccf0acac62248784dd8631e56a49476`  
		Last Modified: Wed, 11 Jun 2025 00:29:32 GMT  
		Size: 3.2 MB (3180600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:305f34e276820ed0a28a24bcb1d0328ea0c515c0fedf840c5d6f0ea3bcce7b2b`  
		Last Modified: Wed, 11 Jun 2025 00:29:33 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:eba058f835b20558caedfca73094ce2a1e6133dbfd891091fd2fb3f7fc146d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47743564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8c356dc3b0d45184c8b175d99819da596c793cbbaa4e657e1a4f1983a52446`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c34f754d6e3c3ef9b6c04dae2b40106b1e62576b355acd817f055ce6df0a03c5`  
		Last Modified: Wed, 11 Jun 2025 02:05:42 GMT  
		Size: 47.7 MB (47743343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a850db49fd534b39b5f394e496cb8628099810b2ef5618398e82227acf28260e`  
		Last Modified: Tue, 10 Jun 2025 23:26:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:05b87d46f3d82da765d25926ca17e3d50aacc59dae3d4d6e028ff749b180c530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3166022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbbb3f07cf140f6061fce80459b01aad36e1a23312ec44553bd477452088509`

```dockerfile
```

-	Layers:
	-	`sha256:4489fead6061391c16165e029463d1e26254c3cd3d9cdbac20b1445d490aabf7`  
		Last Modified: Wed, 11 Jun 2025 00:29:37 GMT  
		Size: 3.2 MB (3160159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:451ca081e4d65de20763572eacaef8fb0be6419703ac39378d9a1589e7c06209`  
		Last Modified: Wed, 11 Jun 2025 00:29:38 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:3123e0213f77f24df5b7c172994b10ed6b82e857a72a488bc0b33f96bac9dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49329989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5bc6c443d3c2bfed31afff1f95e4e517908e419b143661892dc2e7acdc2c04`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d36874750d91bcfb68b6278bc4ac7b65b49eaa71d557564fe1954853bbbd7588`  
		Last Modified: Wed, 11 Jun 2025 02:05:42 GMT  
		Size: 49.3 MB (49329766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16433fc1bba003f3ec2c5417774d146b0aaec698bb0663773435b67c96079ef6`  
		Last Modified: Tue, 10 Jun 2025 23:31:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7ba930dfc48255a4a83e9489ac197da9b3f24f1884f8a51d3367137fa7860c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3184375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcbd958feeb36487b3d35480a8697d74076d3f99b206fbd295ac145ba70f213`

```dockerfile
```

-	Layers:
	-	`sha256:7754cb2aa9f8f01341f743962ecb6677b6e3c27136693ba2aae9bc574ddbc2ef`  
		Last Modified: Wed, 11 Jun 2025 00:29:42 GMT  
		Size: 3.2 MB (3178538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39bb0c83d78eabb771de98978fb32d39e1d6d2f5709bbc20df91a334ff6d7ab`  
		Last Modified: Wed, 11 Jun 2025 00:29:43 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json
