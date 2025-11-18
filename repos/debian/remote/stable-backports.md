## `debian:stable-backports`

```console
$ docker pull debian@sha256:0f0941217395195635f81e0c7a97766d700d1bac3fb23065cdbeb60597045068
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
$ docker pull debian@sha256:3225c6027ba5ed42bf8a5a65f32b0c42a19359f49c35ad56973850b1a6b489b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49289769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be541f329e686ae7bb08d73f74184e13b26589e939bec21de4a391c8a93bf9c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1763337600'
# Tue, 18 Nov 2025 03:57:07 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c160d5fc38f71c3f54560e28843a7d375d45eaa53a6dfb70212570a85d7c48b4`  
		Last Modified: Tue, 18 Nov 2025 02:32:44 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb7c8d4e89503406fe0667446981920436bec0a85b9570ded64a62b9f3df235`  
		Last Modified: Tue, 18 Nov 2025 03:57:23 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5306f601fd9d166bd1806b2e193a152f0944af5351ce0e4933c0595b0bd9ede8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c62a1f5c9bdb3d6b52bca94ccc5c926bf51d0795fb45d668d0a40c9284984e`

```dockerfile
```

-	Layers:
	-	`sha256:4ab0061c124699b1047ac0b9fa223c8411f6e839718021860aa5abd4928d4886`  
		Last Modified: Tue, 18 Nov 2025 04:31:25 GMT  
		Size: 3.2 MB (3170018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a373995ee1a79763eb105c1b374eec247af32fd66c0265000497bc743e428d05`  
		Last Modified: Tue, 18 Nov 2025 04:31:26 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:49e0f5e32e782974c83f288076178321ff54f7cc805d9fb54fdb447723e72832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47448976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70177b959d0e831cc1c10342807220d35a0aff284a34a6272141ebdabed13f31`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1763337600'
# Tue, 18 Nov 2025 02:17:33 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2612fd8f8491f32c4b81fe443aeddff05913276b67312fe29bef1a0e49957139`  
		Last Modified: Tue, 18 Nov 2025 01:13:24 GMT  
		Size: 47.4 MB (47448755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cdb31f5d024de5a7772b3642cc185c67d0bfeac71327cc572cdfde8da4ad9b`  
		Last Modified: Tue, 18 Nov 2025 02:17:45 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fd10ff2a7f93cf03733bb8d27569add1caac7b46f1ec7fd18a43f8858900bbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b9c790634941c77f3e184b51e8768eb00d4e8d3b8687d9d8f70cfc589d6195`

```dockerfile
```

-	Layers:
	-	`sha256:a62602bd1a7a7f072abad7357ec7f084956938b1897cdb99c20c3f79b642c014`  
		Last Modified: Tue, 18 Nov 2025 04:31:31 GMT  
		Size: 3.2 MB (3172955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88ff1db83bddf3f9d2437efce598984bab5628633f67b76e984655aa4df28782`  
		Last Modified: Tue, 18 Nov 2025 04:31:32 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b628e04d919a1e0025feb92d4dae334bec1ae8ef1f98cb933fb2ced418544a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45718501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ce2562062424c02bdeb6f56bd9c450b6179ef0403cacf87f61757268aea892`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1763337600'
# Tue, 18 Nov 2025 02:18:33 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f5fe416d4bf5bcfb708758a6d25d5c336315668631075af5812ab1a005ca7427`  
		Last Modified: Tue, 18 Nov 2025 01:14:12 GMT  
		Size: 45.7 MB (45718280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cce6f2ef5f1660c9a4c276bea16d5d8e8000ce12b11bbd428e31257652ec62d`  
		Last Modified: Tue, 18 Nov 2025 02:18:44 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:264580aaf84b571e9ef78b243b058b7603f20c4e1c546b814ff66cc83b82d19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c82b4dd93603cf52dac0d5e8d694ae8740481589061a96319f9ab8d51932b56`

```dockerfile
```

-	Layers:
	-	`sha256:2e749caf2e9ded6752fcf71178afe07825e944a0327f964d16aa84b9192e93af`  
		Last Modified: Tue, 18 Nov 2025 04:31:36 GMT  
		Size: 3.2 MB (3171392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9532a823556f78db65be24d58b1aa21530178eb5458e006f5f846efb67bb1171`  
		Last Modified: Tue, 18 Nov 2025 04:31:37 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:323dfc737e9e249b1892be67b1cb40e27b469f242d985ddd955ba2dc4563940a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49650454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf3222ac37c72a74f31132fc09f9666e59a6f21747c7cbba0f70ee5d4395a32`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1763337600'
# Tue, 18 Nov 2025 02:15:58 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5ae6899e942e1905a8a220a88793b6d7474f79d6b5dd16d45183dd615076a7aa`  
		Last Modified: Tue, 18 Nov 2025 01:13:06 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352a375272e1bcdbdaab9e023e58aed106e574e0068fc0d52f35afdab382e0b7`  
		Last Modified: Tue, 18 Nov 2025 02:16:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:24f402ecfc83091a0a56fd78c9e62a56b0ea9faf8f4bdef05a0b8e63ca233149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23fa081df0a1507b342a5d2b1cb97721aa3d63bc32edff3c08882e0e2268a84`

```dockerfile
```

-	Layers:
	-	`sha256:5c4ab712b8ffcec1c29f4ffbfeb8446b6996422e247dde6f45393bd640112e36`  
		Last Modified: Tue, 18 Nov 2025 04:31:41 GMT  
		Size: 3.2 MB (3171499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb5f6937b3f5aaaac79d8e1c2a74228511d055a2e329b1e4b3b1f6fa6dfb1245`  
		Last Modified: Tue, 18 Nov 2025 04:31:42 GMT  
		Size: 5.9 KB (5851 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:10acc3c9430504b768212a9a310849aa1a4c4ff6b36629893603bf5ef4928057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50801968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bfd938177cea99a404a0772deea28f3238b31f98bf1398e549164a4837e776`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1763337600'
# Tue, 18 Nov 2025 02:16:09 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f8be73040538d00d17fd7d8f11e461950a5c81f1b958275123e8d2a4f64d00a9`  
		Last Modified: Tue, 18 Nov 2025 01:13:47 GMT  
		Size: 50.8 MB (50801745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8050f5ca3762394a30d83463445580b8ac83516e1053ba3e55253268706c53b1`  
		Last Modified: Tue, 18 Nov 2025 02:16:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1074c0a8f55a73e0f467263a6d50b68574a1d5a3c60a705d8e9fdc3842859b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973caef3f6b3807622fe8e7b78199128c30abe2ebc4466e2c775e8e25dbd990d`

```dockerfile
```

-	Layers:
	-	`sha256:4454e2f6b42b6459005c481461c640823914cda107074c8879db2e0ed239e228`  
		Last Modified: Tue, 18 Nov 2025 04:31:45 GMT  
		Size: 3.2 MB (3167221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a138712eb3d0d4351a0cd254e94b78b1583eeb6f62925e94aeb2ef1c3ac659`  
		Last Modified: Tue, 18 Nov 2025 04:31:46 GMT  
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
$ docker pull debian@sha256:a77e0e08f896937469aa1a71fbb264ab6484692fcef71392ba441626e5ddaacc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49346236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6ba29e31c74f4470d4651a7e9293420fadce0bd694add11bd563248e502ab1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1763337600'
# Tue, 18 Nov 2025 02:13:20 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3a0c301a30ae17916447993faa87319010c0e6222a5c30eac3f5c06f5ec59507`  
		Last Modified: Tue, 18 Nov 2025 01:11:57 GMT  
		Size: 49.3 MB (49346016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2fb2a44d6b53c7f9c9d75eb3d1962fda44eacca21252c419f716af9f1a79c9`  
		Last Modified: Tue, 18 Nov 2025 02:13:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f12d1b46f138a67285be238e428f0ce5362d9df562e8b0204797c5ebc0c9da48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1085336baaae52eedcaaf5acb4cbfe6659d53e6aaccedc9b6443b16831b22af`

```dockerfile
```

-	Layers:
	-	`sha256:825735e21610a78818e196b8fb0deb28cefca558a3be1fbf5691be63dfa0c6fb`  
		Last Modified: Tue, 18 Nov 2025 04:31:57 GMT  
		Size: 3.2 MB (3171465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ac36b6ecf33ef94e94d5df8ced75443644e8c54c6029201f30c116a7295997`  
		Last Modified: Tue, 18 Nov 2025 04:31:58 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
