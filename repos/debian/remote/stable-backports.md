## `debian:stable-backports`

```console
$ docker pull debian@sha256:db18f999a7e8cdc7b8d5b389bae2b54e69ac6192e4afbad333b92117f9d235a7
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:3bdebd897ede16290f42e9a86fa12c78a2ed3270fcbbba6afc6a8e5ad9c2da49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49285847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0eda4d7335a35843565d328251a8168f3ab55ebc7fc23c22dfb8201161864f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1762202650'
# Tue, 04 Nov 2025 04:02:28 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:84372eb38d4833df3b31f4418f269262680a4bf8409cb9f8591a50381d617473`  
		Last Modified: Tue, 04 Nov 2025 00:14:02 GMT  
		Size: 49.3 MB (49285627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8266910b8b9cd2261c201067b4894b94533684163cbf974f99e94f71fa9634d1`  
		Last Modified: Tue, 04 Nov 2025 04:02:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5f47f2944dd378ae04dc27bb260ecbade5929b499cc72a8f7b1be863fa4df3d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf24bb8ab7d80018ac8b41cf73aa31ef29cdde1296b90f18a0df2f62aa14cc7`

```dockerfile
```

-	Layers:
	-	`sha256:4055614e587abc32f1a699284678b7d281fee198ee2cc6e530f2df2919cb2bbb`  
		Last Modified: Tue, 04 Nov 2025 10:28:37 GMT  
		Size: 3.2 MB (3170024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29c3fef1475df74d67ba9f94455e5cdae8e3e982292002b1442ebeb34ccc53c8`  
		Last Modified: Tue, 04 Nov 2025 10:28:37 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:dd8345396cb2d6ce3f7ce7bde65b221eb5eb9c1f2b6122041de818d0cc919db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47449646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574810a1b7f717cd010efc184a819d8a78d8b98451175302ed110fc9dd3203d0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1762202650'
# Tue, 04 Nov 2025 00:20:18 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:13e2b347cffdfa905cf7541d0015dc671cf86dbf35766385bc92b9d27b7cc42d`  
		Last Modified: Tue, 04 Nov 2025 00:13:01 GMT  
		Size: 47.4 MB (47449426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a914c765a7fa2bf97503d5a6262cc0b4972847689d00398a0df446308ac394`  
		Last Modified: Tue, 04 Nov 2025 00:20:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:63bc22f2cb5a0cfb2ca587b586345612d2ec1c633ecf31087e75c0a2f29ab319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13f590bd05596c8d8f684810eaf13e2c7d8b18d5db68397e4aa750294a1412b`

```dockerfile
```

-	Layers:
	-	`sha256:ad8966ff3f37f5218c6ce1a9aa16357ade145ab94fcab47a98497daeeda52ad9`  
		Last Modified: Tue, 04 Nov 2025 07:29:22 GMT  
		Size: 3.2 MB (3172961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:135bfe798fe0a04bb8e8478736844dc4e873eac8c612dfc5482f0c7dc49be7e2`  
		Last Modified: Tue, 04 Nov 2025 07:29:23 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e847b0a4a1654986a5ebdbf5f2e15fedf706423f2a586227a497f63d2655d239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45717355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38786e965baecc2538807f83240e2efc7453dfbd062830ce01df3720e07aeea`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1762202650'
# Tue, 04 Nov 2025 02:04:40 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8548a26c531eed7b805bb7ae11cd32dd49190b229695fb8c55c5b02079736fb5`  
		Last Modified: Tue, 04 Nov 2025 00:13:47 GMT  
		Size: 45.7 MB (45717133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee67a352ca8ac2c6a99fd3cb288e957ad15cdfc6303ad7d69c3d424d086a909f`  
		Last Modified: Tue, 04 Nov 2025 02:04:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5c1eb343b030cf3c0e1e9c066b344cf3b6bff58f77be66fed8922a513dabffa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9c7cb4fd1d8b49f7b7516636e13158159bbf7d2ef3cc8e6589e8d775dc63d6`

```dockerfile
```

-	Layers:
	-	`sha256:a50974c951bcf2d25412d502ce0dd81d78e9496dd3f2cec70e688aca66c1a26a`  
		Last Modified: Tue, 04 Nov 2025 09:49:57 GMT  
		Size: 3.2 MB (3171398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83ff59f7efd506061fda0b38d96bc4fc29fe6d847734dc3c43db06720de420cc`  
		Last Modified: Tue, 04 Nov 2025 09:49:56 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4beb1f5593dfafb5f79b667ea876979b4346778e13e8616ae2cf1360a1acbf49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49650652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a300f329e9ba4ce76f0f00446a6bfc1011672b68f944c65143a7fedf516ca7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1762202650'
# Tue, 04 Nov 2025 01:18:12 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2ffc998a473ede0dfe27f997f21f569a692b69104446c1304067ae7728452d14`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f9ee2c1333f816d381bffdfd93d0d284b85740173ccf703f55c92ce7272a43`  
		Last Modified: Tue, 04 Nov 2025 01:18:26 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7f1d830a09fed971bf2ea916e6c1f7fde36e960a245ebdbdf552603a9e1b601a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79500e8b43023232b1bbc33b2fa78a31f21bbaa366b89bfac947010e2999f077`

```dockerfile
```

-	Layers:
	-	`sha256:bbaabb6b158d53f594a5e04a72335756af386374fc75ccfc5b675f65b0668dcf`  
		Last Modified: Tue, 04 Nov 2025 09:47:42 GMT  
		Size: 3.2 MB (3171505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58c2e526ff294b35dd17644a696bcde4540184cb133d26faa9aff9d2c8d6c6a6`  
		Last Modified: Tue, 04 Nov 2025 09:47:44 GMT  
		Size: 5.9 KB (5851 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:8afea27e60d52cc356fbfbacc0a886c49d354e0d7d002ee1a5d0c2ed1ae57ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50801463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e503b8b864ccff4cd110ad24d2990a96f4695699d95d564b765ea93c18799b96`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1762202650'
# Tue, 04 Nov 2025 01:18:23 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8dc3c18198ce8ecaa38307189c4eafd9fc2946e130972bef16fe3094eac2f823`  
		Last Modified: Tue, 04 Nov 2025 00:13:52 GMT  
		Size: 50.8 MB (50801238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c877099afc3c71f82dff8e5def1a9160b56be5023784600171ba80539a51eb`  
		Last Modified: Tue, 04 Nov 2025 01:18:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9c3ced67d430bc7f33d1d25a56f30471771effdb0d3ee0a7d24cc592f14c7d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafa42d3381b4c5c3fc3560feee6801bb91ce9d87c6a7311e9dfd971f6f73e99`

```dockerfile
```

-	Layers:
	-	`sha256:82ce9346a95d6665c96d44e166b4155f19148f6e5cc27dc9f668cf21408e84cd`  
		Last Modified: Tue, 04 Nov 2025 10:28:50 GMT  
		Size: 3.2 MB (3167227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeba6a720bbb9c272deeef0afb0057579de0f497fb7a1cd1bff5eb14fa49d97e`  
		Last Modified: Tue, 04 Nov 2025 10:28:51 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:4aaf3b5e0845a01af9534fc4482c121f870f81359fe251dbce06bc4b099ecf9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53110347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd01573bee2047f0459cc9ffe2c152d6f775d19300221328c3e8ad0832cfee7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1762202650'
# Tue, 04 Nov 2025 01:18:34 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:46b431f623a507173c940c0c884455f9fd317cd31beba14dc949da60b58bdc2d`  
		Last Modified: Tue, 04 Nov 2025 00:18:03 GMT  
		Size: 53.1 MB (53110126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53986dc7f55cd04fe212bbde3538eae98b5818d4ea80d02b0a9abe0457530576`  
		Last Modified: Tue, 04 Nov 2025 01:18:52 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ad72b9fbbf02071b57042a8c7999e3885e79ceee07b73ec2f6976ab10cb7468b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0736db63fe5aa9feccc372e1dbc13e8483f2d32250d7b09e6de0cbb8c9d6a7`

```dockerfile
```

-	Layers:
	-	`sha256:34ff739bf11057f5c55455eea78640e147c67c4d75940b8fe503f36f86769d9f`  
		Last Modified: Tue, 04 Nov 2025 10:28:55 GMT  
		Size: 3.2 MB (3173535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a35589327f984106b7e1b0249503c87f36ce24759bd3ec4fdcd8a53e8db237e0`  
		Last Modified: Tue, 04 Nov 2025 10:28:55 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:5f126f829a845f90a79c63505d39e21617d417b2cc6d65f209ee0a16a940f197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6ed5b208ca305e1295c6fa53aa31facd806a5d67d24104c5fb0d39020ecbf8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1762202650'
# Tue, 04 Nov 2025 01:19:49 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2528dd148b36df470732f8eb1cfdb230a730e032a76eca2a67e06418aa90966d`  
		Last Modified: Tue, 04 Nov 2025 00:20:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7df5e1135c56b98ef321591b1f814b331ba598ba67b93771605ea303b474859`  
		Last Modified: Tue, 04 Nov 2025 01:20:49 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b4c78ba1f23b9d8cbb528a2d3e83ea3f1bdec9e7f7a8e455e110a938fe292f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0201a99de425e4e98bf4253366107d6c083d4dc1dac789eb0588c5fe4605d7b8`

```dockerfile
```

-	Layers:
	-	`sha256:717678815fbcbc772143e2182cb1ae8f648db492f4ccd1f9c44be47825fbbc73`  
		Last Modified: Tue, 04 Nov 2025 07:29:41 GMT  
		Size: 3.2 MB (3162347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f0e8d750da6bb9fac0ddc80a0fdafdc65eb9d0630d591e30bf5874eb693b91c`  
		Last Modified: Tue, 04 Nov 2025 07:29:41 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:e240680d0a9a15e1cd72096b8f3a7fdd214fd7b80df204cb7324395c34b2142f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49352519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc65df6e4cdaf608d63622b338694a97a1f6b09a5eb8bef449c375b427ed9ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1762202650'
# Tue, 04 Nov 2025 06:42:02 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:93643b56a8f62c9c311b0ff7993136ac2cf19e53c5963289069de8747aac449b`  
		Last Modified: Tue, 04 Nov 2025 00:17:29 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd817e59f24e308e0fff17fd9d2836dbf180faa92775c5617572ac82cd2dfef`  
		Last Modified: Tue, 04 Nov 2025 06:42:17 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7db23c1567b8a04a1c5666db43c7fd1c1f7f3e104cbd75cf0edf1eb8944ffe6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72ab73785b7826b8fa611457493e7ef467f658b5214bdfdbac33b6d47f839f2`

```dockerfile
```

-	Layers:
	-	`sha256:cd948e220dbd02beac1821ecd5f1f93265d519163079167d0bd5b8ccfcc6ece3`  
		Last Modified: Tue, 04 Nov 2025 10:29:02 GMT  
		Size: 3.2 MB (3171471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a7d41e840f11e2ec1967032eccd888626d6b75dcb36bed1d30d7d616a1ca205`  
		Last Modified: Tue, 04 Nov 2025 10:29:03 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
