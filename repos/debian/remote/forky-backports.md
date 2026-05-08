## `debian:forky-backports`

```console
$ docker pull debian@sha256:2f2cdbca2843a2f6777a1fa088984bbb28e161f0fe32024541aa9e349c54eb0a
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

### `debian:forky-backports` - linux; amd64

```console
$ docker pull debian@sha256:cb0b1c242b3b1c284147eb622eef222b260aa5ae02eb156005801f60c2ff2b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48622267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45bad5cfb9a2b6ae29d6ec0dba547df01d253d78720decd7116b6d5dbf1567c0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:14:52 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0e929ba940bb6645aaebb3cf3e1b30d0ccaa2f7d53cb82e57d451efa023dead7`  
		Last Modified: Fri, 08 May 2026 18:23:00 GMT  
		Size: 48.6 MB (48622043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2948f31aa257374fba848fe3ca74e3bf3c812da11cb95278910c984333d6a67b`  
		Last Modified: Fri, 08 May 2026 19:14:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f50983a36f4284aa3011010d45202dc513ca495f692251e7f5819b0c6cff8251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f55622b2ec7eb2eff55aec9341b004f7dc5486cb73e83c8d818b73dda39c0e3`

```dockerfile
```

-	Layers:
	-	`sha256:efc0305cc52e3c403583afc6da0d292dd054ea7c955adb664e3def3e24524cc8`  
		Last Modified: Fri, 08 May 2026 19:14:59 GMT  
		Size: 3.1 MB (3146853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64a5fc2d203e6684824e7c2314a28040f0e9ed4fbd116da24c01f6c0ed95b9fc`  
		Last Modified: Fri, 08 May 2026 19:14:59 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:fb06154e3a14075de9cb1c56ff7c01c064d310faf8d1b8e568f44fac28fa99a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45559876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6486e73de5a974e22c8b52cdb2dcfaf4b6113b46eae0cfc0cfa36dcc17bc8e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:14:38 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1d504d75b0bac1a71363cc538d085e2c22d8b451c5112cd1892dea705c788f73`  
		Last Modified: Fri, 08 May 2026 18:37:09 GMT  
		Size: 45.6 MB (45559652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a9dbb14277ee19e76aff2704b694af9bd598400c5e02310892a4f685237051`  
		Last Modified: Fri, 08 May 2026 19:14:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9511e88524e260eec14615b85b6da594bcb37e38a5a940f874572f081041507b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9c7f2fc89f10a103c64971b28d92bc3da0cf0b70a184bbf2c9c5d1179b7cdc`

```dockerfile
```

-	Layers:
	-	`sha256:36e2cc89579e0ebd1b9dbd6db47f8390f9faacc29793ef304e2fa9c83d3b2a05`  
		Last Modified: Fri, 08 May 2026 19:14:45 GMT  
		Size: 3.1 MB (3148215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38dbc088f4c8224dd77b7e8576027a47caacacd241349df8766595a30c85fa2d`  
		Last Modified: Fri, 08 May 2026 19:14:44 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:9fb9ccd3b1d20a14c276752dd04388c3401fd0b15d7b91e8dd484f552b180867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48659976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fce82072750e088cc465e9fe33d51a6ece0259b17aa426afbc792ca5eae75cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:14:39 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c3ba40fb7e0c033b95f4145478256aa8b70beaf3f8b8ad41dc909fdebc63a611`  
		Last Modified: Fri, 08 May 2026 18:25:22 GMT  
		Size: 48.7 MB (48659751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6063c1b97f4f919c38ddad7fc0312e9398c67024922abbfce9cddf4a09ca009a`  
		Last Modified: Fri, 08 May 2026 19:14:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:50f39992d977542b0c8aaa2e1d1957bb2eceda9ebef72e349404e03101657ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3158012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225483fa33a9e2dc4f23f62cb9aa5a9e52db23268e67810bf45c79868cb5ab91`

```dockerfile
```

-	Layers:
	-	`sha256:8128c30fc0fd35bef3f70ef4e908c598b320e3515bcb742fe4bbddf2bae8876c`  
		Last Modified: Fri, 08 May 2026 19:14:46 GMT  
		Size: 3.2 MB (3152166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca38291d4d713b2b13ba87fc5b059faa72e48c5eac500fe49622aa8dc04f3f0e`  
		Last Modified: Fri, 08 May 2026 19:14:46 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:a0b15ec703ecdd9e124b3d2b89f26d5f5cc7a9b3982cad438c729893f99c645c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49924445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2405b9ba6a571a0d807cb3c491d8a475baf55f846b5ae2fb03a0c8261848d432`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:15:36 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fe128ab7d9fa2ef88e1a5446e3be7ae6051e047d4c17dfb5871acbb83fbcb043`  
		Last Modified: Fri, 08 May 2026 18:31:14 GMT  
		Size: 49.9 MB (49924221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5de75c87321f0ac83210f4684dbfecbcc9626d5938acb5862ff6840c1eb586`  
		Last Modified: Fri, 08 May 2026 19:15:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1f14f9071696ad0e5b0e6302cee5484d4003437e531367fa34216526bdbbd8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e024761a0d4d21cb63fb3fd2a612dd812d1e98cb9f50c86d8cc9b40ab93ebe`

```dockerfile
```

-	Layers:
	-	`sha256:3ff661b9f1eea7d2ae6653d65abe826c5288774445dbdb38f2cafbd0fe361974`  
		Last Modified: Fri, 08 May 2026 19:15:43 GMT  
		Size: 3.1 MB (3144050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ce7183790b438e8249be51de1349af074551c9228b16334a90ab46056c04acf`  
		Last Modified: Fri, 08 May 2026 19:15:43 GMT  
		Size: 5.8 KB (5760 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f0b4c8409ffb602335863139cabaad41f08389d65a17f3dae4a4b8179f521835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53927198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586013c959c6db7fbf5fa8195ea872b38e4ba18edb61e8d4c71bf2b9ff47ae25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 20:18:28 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b0beeba61b823ca3e14a339f1111ae37331fca42dd43aff18c04950bc3c9921a`  
		Last Modified: Fri, 08 May 2026 19:44:35 GMT  
		Size: 53.9 MB (53926974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccfc5f1c6bade8724630e0e45bff0e7c7d908fed1b51123616092401442f745`  
		Last Modified: Fri, 08 May 2026 20:18:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:de471f0fbbb4f099eef2a62d16a3ad179965a70076055ff29e766aff656432d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b4ea2fe3f3fbb9c0231857d76debed80be3affcaa3ed159838fde2c3877896`

```dockerfile
```

-	Layers:
	-	`sha256:9dc9ecd35aa3cf767a9218c5db6ece25492dcc980cfeb4753cf8a4df477771af`  
		Last Modified: Fri, 08 May 2026 20:18:46 GMT  
		Size: 3.2 MB (3150364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28af33883d36a834913b8926f4cd11fb5dee0c8c7239bea8b43e6f98d67babdd`  
		Last Modified: Fri, 08 May 2026 20:18:46 GMT  
		Size: 5.8 KB (5803 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:bc4f3f0eccc6f1af7010f81235da244d6cd8e57b7d7fb56bf35788a25da96c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46771747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba503b185dd1fdeccb5e196740afeea4203f97d451cad6829d7ee6d8df027b86`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 05:55:42 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:04fb0dd36a6b62569331264b3dc244d1f567b4ad68c8c1b27f9d22978f421544`  
		Last Modified: Wed, 22 Apr 2026 02:14:57 GMT  
		Size: 46.8 MB (46771523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9dfb5ce5da29c7eb899dc5bb8267d2db95d4cee8224c3da3ef8362aa7c751f`  
		Last Modified: Wed, 22 Apr 2026 05:56:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:529dea12026d6331377885003b390d5f3691e8bb1c8a8e9421bc33dd4ea9fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3141732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1baf6641f6cb6512799a4158cc8f43c03a5fe044fc716c915820ebb2ee1af789`

```dockerfile
```

-	Layers:
	-	`sha256:6e7030fa9fa8577c9e789bad81e0605790e83b2a7b81bc6b5110ae986e2ec431`  
		Last Modified: Wed, 22 Apr 2026 05:56:36 GMT  
		Size: 3.1 MB (3135928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fa9ebf0b926727254d0f49148310018796cbb7637ed30be91f1826e291f9ebb`  
		Last Modified: Wed, 22 Apr 2026 05:56:35 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:23699bc36f5f6520fd56ae4d3645efd25bfe429b70647e539c1af5a34daae136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48373756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f169e0331132dbf3175a8e2a6da2cd672d9ec6ac36cd72e0135c265acc9ced72`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:13:41 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ba3092798c7b7e427c9591ec4f0d9efaf8a9b59416038e46d07c57fb149b38ce`  
		Last Modified: Fri, 08 May 2026 18:27:50 GMT  
		Size: 48.4 MB (48373532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1f0f0ee45a9b3ded1f8d0eb4c75742ebe1de0ce64af411b018c328756f1c21`  
		Last Modified: Fri, 08 May 2026 19:13:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:15d6fc9487fcda188008e9cd125d7c4d6b065baa348206b158d1e7c7e99b12c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff3aaaf3060c1d86f1d64be5dbfafcd3f02ac822611d6012a12b1900bbc03b3`

```dockerfile
```

-	Layers:
	-	`sha256:4e172eeda21a9a44690227f4df1833da4551a472be12f2659d40597a2df08096`  
		Last Modified: Fri, 08 May 2026 19:13:52 GMT  
		Size: 3.1 MB (3148304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aae3674d01122c2f2cdcfe2a1f288a5e916cbe3b1364c997fb09dcb7d7a165ad`  
		Last Modified: Fri, 08 May 2026 19:13:52 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json
