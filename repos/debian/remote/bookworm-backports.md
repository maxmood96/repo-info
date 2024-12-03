## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:aeec34fb4658dff60e6055859db0dfece1b4cfa0533e37d404416910355376d7
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:168f8873adeadc8f6bf74371a6e24b5ea1935673c4b462eeebfeb125fdae165f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48497434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8f0046e6282b39ac3efd38c708c4b571cdb9ea39c2e2d77a8670da052ca341`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630a787c08eeb21398a4fa27068454ae4302a6ca5aa4e1fe1e416f3624a6b9e4`  
		Last Modified: Tue, 03 Dec 2024 02:13:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6d81286e7395f9dfa3123409a826a7dd6cbc8bb2674cc6e61cf208f17a31ba1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7762277f7ca67688e46738c69122469836fa54cf0d3ead0478df9d61c253e8`

```dockerfile
```

-	Layers:
	-	`sha256:988ca56ed69c2c81f3250a4244d9fe06a6c5c046d4a1cc0f40272e6fb76e6c58`  
		Last Modified: Tue, 03 Dec 2024 02:13:38 GMT  
		Size: 3.6 MB (3623034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:302d7e5084a9c72e8b095e38a6c6d31cad8f98c64f475c09c479f7412060a9ca`  
		Last Modified: Tue, 03 Dec 2024 02:13:37 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:677a7cc278258d7cc878c5ef9934e7e413e6ddeb976a8c12f67935257f5c799c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46024598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a127378dd8cea73f300d18a97b4e6f9d4439604ce3de4bcb31b21b7d22f9f03c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a8ab0b752e573ceb3480052f24bc5fe3f4f4665c13a338db39c1d51f749528e9`  
		Last Modified: Tue, 03 Dec 2024 01:27:04 GMT  
		Size: 46.0 MB (46024374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2a69028a6a54c88e3db7af45c1a14939271183e580666c144b27ada66cb926`  
		Last Modified: Tue, 03 Dec 2024 02:18:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:742de0afbf46f4a39b5f16644c51cfd4cc6ee6aedddc2613858a8c34dfaaf5ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f721bb0bcaf6ce72adcdd147f9cbbbfcfba2d3205a24955dc6de78d85066172d`

```dockerfile
```

-	Layers:
	-	`sha256:50fa7e91255d8e9f4bffd71722d0f103d1abd0c1b386b874e63a8719b5810f97`  
		Last Modified: Tue, 03 Dec 2024 02:18:46 GMT  
		Size: 3.6 MB (3623234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d81bfbca0da9eb4bcf0cf1fee5f2427f2baa3c9b0f06fa5ba84f25f3578c9607`  
		Last Modified: Tue, 03 Dec 2024 02:18:46 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:48b17f9c88e32027c0279da92462e4b2363f229b5b6c3266dfb9cbba7362704b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44200331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81012ad3af4d58782013c33bcd26178c39f396951d69ad89ec2e5fdfde9ad85c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4d43724a324f138c88a78ca6df0a39ab6868bf1f121eb974439c5a51284e1ac2`  
		Last Modified: Tue, 03 Dec 2024 01:27:59 GMT  
		Size: 44.2 MB (44200109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ac0c151c82cd62872f9a8a2fd16b2560d4e928b3b6e1d00039aabab2c1b87e`  
		Last Modified: Tue, 03 Dec 2024 02:18:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d10cb2432fe347197a18b7d59c58bb71635bf5cbb8562477098dc3036576921a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71897b5e7b9d21b3362dd0c7743e66051316adeb1fe5c6e256912c30479528e2`

```dockerfile
```

-	Layers:
	-	`sha256:5678a0850a15fea1d2953643d3c4e3a9cd269b682925e412d9101617732ee4a3`  
		Last Modified: Tue, 03 Dec 2024 02:18:50 GMT  
		Size: 3.6 MB (3625212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ce63d1ab16ea26a37d44b32bced8d44f336b16721f85a67b580dccb5538adc4`  
		Last Modified: Tue, 03 Dec 2024 02:18:49 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8992b9df91d53dc1fd61e046b5de092358d243409fce0d7f2c390af0624ea448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48325905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1104d247d122b35bc52ed7fd887acd73cc9e34da7bc0c83ba38637c584eaba3d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1d4b95342265172bd62f1f897cd03bdd2b0ce77c669423ab39d52a5c51bba5`  
		Last Modified: Tue, 03 Dec 2024 02:18:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:cfe5026c9e0f401d2254908ec83eff808903658bc388f0642b2597d2fb3cef1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44538613051182a9258a033baa6d4fa7a22e0019b8098bed10e38e2c4a7beacc`

```dockerfile
```

-	Layers:
	-	`sha256:b7aae2b5f60a6194e34bc4e3ee2acbcc27af0af7a9f01cf9be4d8682ad9df79c`  
		Last Modified: Tue, 03 Dec 2024 02:18:19 GMT  
		Size: 3.6 MB (3623248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:925784a71a11a2042ee75ae97bcde4e20bd56125b0a292e0729f20c964cfeafb`  
		Last Modified: Tue, 03 Dec 2024 02:18:19 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:b3969945b0b03cf1dab60bb4cdddee7f4190a01855d2c241d83937aa97980008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49476375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2a529eca1185c46f9082a9a31dfe35b7aa5b4187acb74685bea779da778669`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fecd35afc246c14ed8e0c351eccb1c06bd2222f8f1f0a273cb8567b6deedc0`  
		Last Modified: Tue, 03 Dec 2024 02:13:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f56b4a6973c3cf4be39e7b807378ac1ace498258079de0a6d0cf4b233e03f9f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36e35ba632b350b0ecb276ead95f06afdb544b29e569ae04dcbe0a0cd76dafd`

```dockerfile
```

-	Layers:
	-	`sha256:fdb480f63104df8eb60b07727def662502220b6767eccba4835ad511fb1158ca`  
		Last Modified: Tue, 03 Dec 2024 02:13:43 GMT  
		Size: 3.6 MB (3620194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:292456e58e443c150923856c245054c6754a5446ab7c2daf43c9c6a2bcb108b3`  
		Last Modified: Tue, 03 Dec 2024 02:13:43 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:48e23fbd55807c8358c37d7c0fa6d7331742920e0118a31fac5055d1d177f0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48772069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e538775f1f8e9a2444af7796faedd8b02a8c59ad69dd8f6870fe049a0ca5ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8f7c3140f4f3af477253c748b229283137cca4214e1c3df21109b821f9227620`  
		Last Modified: Tue, 03 Dec 2024 01:27:53 GMT  
		Size: 48.8 MB (48771844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b382531b6222cdf3d2fecf6c742948d8a9c852f9fc9f388193c800f0e7521b5`  
		Last Modified: Tue, 03 Dec 2024 02:17:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:65c83a966a0624fc5b47cfb140f905a466c576d56719e9aa6c737210e5e0e0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddc0bb9b453fe238286138c1cf59f2528e58c90d2402e351ce2e139169ddfcd`

```dockerfile
```

-	Layers:
	-	`sha256:76cf57f6bc20c888ce74eabe3876928d2eabfc91be191f93c9bff102980d0efb`  
		Last Modified: Tue, 03 Dec 2024 02:17:05 GMT  
		Size: 5.7 KB (5670 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:72a2234e32f8d1ae42cfe5258dd91433d449abeb42464e514c002557b4187253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52328446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae443762a6a842af1f09e58932afbb78c61dc2e342893ffe32436aa6b2780b62`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9d81e003d78e52254b243d1b76ef3da341384f870b7f6d6f77002e08623610`  
		Last Modified: Tue, 03 Dec 2024 02:15:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3e48ad5d55c727fcb872e0c3bf4a9d87e28f82c82311f07b7e62a21a5a241301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6744562a256fdaad60f5623724f8308866af6437e7a6a99f452f28ffe89e2c06`

```dockerfile
```

-	Layers:
	-	`sha256:a96e00b5f558bb1aebbc04e4ba6715d07fbe9121085e6a3c1ae476a1d181ce67`  
		Last Modified: Tue, 03 Dec 2024 02:15:50 GMT  
		Size: 3.6 MB (3627293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:572d6941def87e1384adde03253a8b571b077ebe25c0c62c721b8727b0cf3f7a`  
		Last Modified: Tue, 03 Dec 2024 02:15:49 GMT  
		Size: 5.9 KB (5873 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:93087fd3601acb0bd0db297bbbdac87a606dc0cf529b03135c7e23a8aa986d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47149992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27be83afcf70e567515d21c69486cc8e1d351a5e657aaf45283c77fe7d721a5f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:53a5c0dbd93a4a7f540e18bbe49ba3d7fadaa390ebbce009c756e34c5b1ae048`  
		Last Modified: Tue, 03 Dec 2024 01:27:55 GMT  
		Size: 47.1 MB (47149767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad7b0114f36579db2299a3d2bc85febe53d9bf501d2b6bfb5d8c1ca3cf3d90e`  
		Last Modified: Tue, 03 Dec 2024 02:13:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:03f2c0c5b4433752d642b374d30f8ee5d5e928e5cb68c91fc0a90b4ebd0705a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6dfe4e8a968b71b233a19936d8a3dc6078858e1de6d2f60af31cd95278a953`

```dockerfile
```

-	Layers:
	-	`sha256:8d8e95de1e10826bbd113f04cf660852660aff0decc64b5cf1e58875650da457`  
		Last Modified: Tue, 03 Dec 2024 02:13:39 GMT  
		Size: 3.6 MB (3622765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234a9c5913a3c2f59c8e1b98b6659c2a6ca4a23138f3c43fb73d1a1a57f74f11`  
		Last Modified: Tue, 03 Dec 2024 02:13:38 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json
