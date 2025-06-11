## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:b54fe157d902b67fed41c25ac29303ec3a6f6a62ffa349f1a82bfd32c46d3ad8
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
$ docker pull debian@sha256:aed916f2e624a5640374d4437fa81b15d1e229a7b02cf99fdcd2f7f12b9d8e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48494497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2002048e5d089373020007248e9902c92a75268fb906d1b2d7cef6829402f7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811f5a334632391e1ff3cf8c666f36628f53717fc6468d40b725be970a02e732`  
		Last Modified: Tue, 10 Jun 2025 23:31:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b3a1883d37a08375383dc316b73f3c52c1400449c78efdf83e34702d74a95f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5962abb4caec1c384601ad2e33c7c67b1f426dbb5a1eae008bd8eb68b0ea73`

```dockerfile
```

-	Layers:
	-	`sha256:f058bf6cab7f157bfe3251fed130f25ea86d67d1950190e9c2067a0f7586eec7`  
		Last Modified: Wed, 11 Jun 2025 00:24:40 GMT  
		Size: 3.7 MB (3726838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:988f7932db9b2180a869f8bc4e89fada3192dbda79efeeaa8990c96ae55e2e41`  
		Last Modified: Wed, 11 Jun 2025 00:24:41 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:fa7bfa1ab453f7918d0f3eb29f3bbfaf3b6243473b362ff02e2330cdc0c5c2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46026812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f8c38ef4e23d5ea059e55743020295e1851d441f34be3032e1fc5acd2ce5a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fe4bc1cbdee9e4aabbc6c58a2156f300e4c3158cfb501698b1878215892a8763`  
		Last Modified: Tue, 10 Jun 2025 22:46:12 GMT  
		Size: 46.0 MB (46026587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc70175ef74611489e17d5d7d30d53c2f9887d8ea58015c9a05f40593607c55`  
		Last Modified: Tue, 10 Jun 2025 23:32:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7ed0cfbf5e957f93516ae2967bc362a46f3d871ecaa8c1c8ea51fc0df52b2381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e4a3fc7d83d78cfccb2d98f4db4ecd36b72a3c16f70a790c246cf71e9b5eaa`

```dockerfile
```

-	Layers:
	-	`sha256:1e3480f60e1f20f6890f5619e83c919ace4cb4d404842bbe461367f20d942d58`  
		Last Modified: Wed, 11 Jun 2025 00:24:46 GMT  
		Size: 3.7 MB (3727039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b30eb1d04e85a725005814f020659f9307ee1f200f5fe8b41fc04a7d02424ba`  
		Last Modified: Wed, 11 Jun 2025 00:24:47 GMT  
		Size: 5.9 KB (5898 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b998be8347679bfd3a05d88d21a97c60fa2ffb73912bf48defa3099f62340773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44208435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede9fa658e407a7bdce6a77cf318f4b3530ecc59430207780f9c5a5a58a65ab3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635f8ac4cefa939441dc7ffad2e59ef63f2fd83fc6e98e2d5e46b4b61c18a93e`  
		Last Modified: Tue, 10 Jun 2025 23:25:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a0cdb44e282874983bf309bb0780cdb32a3f59ac7312406269eac7767710dfc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3734916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a51d8a8f49fa804637e8307309d25dae21278db0b701b9961852233182bcff8`

```dockerfile
```

-	Layers:
	-	`sha256:9285125bcb66ebc20059ffee53eeb4afc21470148f94859dbc26b51d34666c67`  
		Last Modified: Wed, 11 Jun 2025 00:24:52 GMT  
		Size: 3.7 MB (3729017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6445d8cae1602f75089712fb492b23ff9218c3906692391a3a5423bb534b3685`  
		Last Modified: Wed, 11 Jun 2025 00:24:52 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:99fa2b9be3ebd53bf9848596e1d355a1349bea6b7383404ca17406c98f8308ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48339077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94534f31c9f4a3e75388a53824a9b3edeb4cb56df692591a89dde817e6037ec5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cef1eea796c8fe72cbd24f3036366a5fbf5d0526a3ca867ad1b27e6d8e71650`  
		Last Modified: Tue, 10 Jun 2025 23:24:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:eb92c40c6721e575bb79660fd068da6681dd23e918268c1291deb54e67384edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3486065baa3fb92e583de618830802ff36e39c15bdf42058677c2d1ba2dbc44`

```dockerfile
```

-	Layers:
	-	`sha256:71b3521542c51abe91e4ee7439ad0829cb075498589fb05802aa545375351430`  
		Last Modified: Wed, 11 Jun 2025 00:24:57 GMT  
		Size: 3.7 MB (3727053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:979e709184424cf30647ef2fbfd274e37394b659e9f896f4fcccb20b1f3ec4e0`  
		Last Modified: Wed, 11 Jun 2025 00:24:58 GMT  
		Size: 5.9 KB (5913 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:cb284387fee2c86c1e4c307cb10ca8029a3cbbbfe1ab75fba211b5f0ee90e095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49477699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8956f72a4bc4ec0e2ec63c966c7ccfceaffea14669e94eb127dea6f4ef4e99ae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce76418fbb284b3633a280d345451d1f67153186bb5354f06aaf995c05176f4`  
		Last Modified: Tue, 10 Jun 2025 23:32:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:684ec1c434e127379a586ba3a379d787b9a9a512ec341a983f941e8e69579d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927dab22273070a9487bf4559dd4defe0414cf2b96c299ea6183767738bbac21`

```dockerfile
```

-	Layers:
	-	`sha256:b27e461f8ad6ce9b9c49d0e8fdaae60ed6962932a3c7e79314948957d4984c1f`  
		Last Modified: Wed, 11 Jun 2025 00:25:03 GMT  
		Size: 3.7 MB (3724040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94c6b872b8e8b8790a28b68790c0919f44d45ec974c05b8c4ac3a23b17c71b1d`  
		Last Modified: Wed, 11 Jun 2025 00:25:05 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:b3e208446aaf75802070c5c64a8ac91cd83fe5bd02b72ce6a43bb53dccad8dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48775825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d9e4a808313749f0e8dbb1622f502674628c2648c9aaa2a9ff4352c75b515b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:348f1ed415b5b1e1f9982a78ffeb15637cbc5b41f93b83724c5938c2c226a58a`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 48.8 MB (48775597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bee1d2a5fce9732032f7ca7e680b8b3e4cf52d49725c918ce47be79b0cb83c`  
		Last Modified: Tue, 10 Jun 2025 23:31:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:97f35f5e9a01661b84f618e843bb30276bf10b539a3be0254c8f1659fd9a145c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64f8b98d2abbbf537e4cb6808271db4e42af79fdeb8f49597e53af7dfedd758`

```dockerfile
```

-	Layers:
	-	`sha256:8f338f2e6a8f3f42f5209a69b41111070a0f271574dc318e4984f3a9a8053e95`  
		Last Modified: Wed, 11 Jun 2025 00:25:09 GMT  
		Size: 5.7 KB (5671 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:716323b41eba982ffc2b1ecf80f8bf6ca38d54de4d4fcdd30f3d50b1143b00b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52337580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8b7e41bd360f87eed6434031937ec2623796612f620c262cf248a6ea461353`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82cf0f4b4d52a4795d59593c7709b06c522037054068444987b57cff267c420`  
		Last Modified: Tue, 10 Jun 2025 23:33:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:db4fb1329e81d0e86aac8ad09d76085f7360d08a2f6fa999b51042ffff526c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5b3b899ba05f1675338ba7b60e4274f229e130ba75aef0cd152ff874167fd8`

```dockerfile
```

-	Layers:
	-	`sha256:7590b746bbadc7443fd577f890b69d2f56dd6de3935f1b03f98b8f2409547624`  
		Last Modified: Wed, 11 Jun 2025 00:25:13 GMT  
		Size: 3.7 MB (3731184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b5c5781dbf6fbc869833e33fb5283115b31d654f07b88fdae11966bf03dd4ec`  
		Last Modified: Wed, 11 Jun 2025 00:25:14 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:ddd4b2099a2f2ac8f652b420346183aeeca24345b7734eed684527e3051e4fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47149634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0a72e60db0c480c75e9241395dfeaf4bec1f9ad24ac523f4027765c3b6502c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:92d876c60c42d9677caf30587cba2266fe6860ddc50efdd0a6fcec154e589f76`  
		Last Modified: Tue, 10 Jun 2025 22:48:13 GMT  
		Size: 47.1 MB (47149408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48597a28441eac704427daecc2409b000ccac24c00c340cb7c38c59da5159b3d`  
		Last Modified: Tue, 10 Jun 2025 23:31:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:89f498824a4e31842a11777169d4e5719a1ee195b5991406950deb4c474d7cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b24331e73c4d403335decc73f4854c00b482204fee93134fca9aab8a9e627c1`

```dockerfile
```

-	Layers:
	-	`sha256:b92392ffcef059af5a49784ac2eeeb074fb4344d3076b33e552eb0c7b8bf6d81`  
		Last Modified: Wed, 11 Jun 2025 00:25:19 GMT  
		Size: 3.7 MB (3723676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7df782ce613d6833a4736ef4c3c8178bb31dcc8de7df1ae49944da47352133ae`  
		Last Modified: Wed, 11 Jun 2025 00:25:20 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json
