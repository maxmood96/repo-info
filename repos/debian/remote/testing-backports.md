## `debian:testing-backports`

```console
$ docker pull debian@sha256:2a6b22c262eaf868803e47dcc48919a9f6e477aa98acff572107876f3b0494e6
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:93987c7c23508d593af1a46398a773b08b457efe59c1820ebc14462afcd9e572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48622268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c834e3e3cdff94cb16191e527d7a6de1b7b2aefa2cbae9ae81ae2d2d3427e65f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1777939200'
# Fri, 08 May 2026 19:15:23 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:373e4a6ed208cabe06a1623397e69ef96eaf9f3acdd0cd879e26c8cc7c7d6be6`  
		Last Modified: Fri, 08 May 2026 18:24:00 GMT  
		Size: 48.6 MB (48622046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f708b5d92348005c299c6dee9e97bb45fb358edb6fdaab484c5060a346ae481`  
		Last Modified: Fri, 08 May 2026 19:15:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:381aaaa232b1c92d330162a999924d467281d201c1939e91ea827b80d45c58eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4616361fa4fe9241c2d19aa5abb0129b149b469b7d1e39ad9c1857c01e6c75a`

```dockerfile
```

-	Layers:
	-	`sha256:3c231d06eabf65d6c7e518bf4a31bee66e134e03ce1a59dd37a685270a988e88`  
		Last Modified: Fri, 08 May 2026 19:15:29 GMT  
		Size: 3.1 MB (3146857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb97105d95597caebcf2d54d093ab2f2d2fc45c657fd1f0ec9302af78f49232f`  
		Last Modified: Fri, 08 May 2026 19:15:29 GMT  
		Size: 5.8 KB (5793 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b2801d9489255045d4d61f224ab31f77357652204f7358d24782fe06f14c4c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45559878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9aae8d3aa7706948ba87621d3aec18002c5ee7e04d13cd50f235c240386843`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1777939200'
# Fri, 08 May 2026 19:15:07 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:eb84276eeca3f3198b7ce6172575d606e0f6778b3f4ddd06e63e68f7ac990a8a`  
		Last Modified: Fri, 08 May 2026 18:37:49 GMT  
		Size: 45.6 MB (45559655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00803b5d739e7608c217aa2570d2f08100baf9f5a43cbbad1d8eeafd3f1748be`  
		Last Modified: Fri, 08 May 2026 19:15:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fba2e87593427bafef9aa80637a0a9a48427a8c402fcb51ac1ecab74e0ae0f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf5e00f4a05bf1a287d27f32dd845ab2528783b8d94a755d8613a4f4cc4319e`

```dockerfile
```

-	Layers:
	-	`sha256:d0a84a5cc494a9e421ed848afb3663f5f88d18863b6486f6ca391dd5b0789046`  
		Last Modified: Fri, 08 May 2026 19:15:14 GMT  
		Size: 3.1 MB (3148219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea085d1b0829689ba054cc5674429751a4566989f1050953ae442e5ad8264566`  
		Last Modified: Fri, 08 May 2026 19:15:14 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f58e748d7205cfb671938a59d33e1ee7d32599a6e78d30fc800790a9e8d06624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48659976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9211b98cacb95cb7afd375fc30aca441ac6e306bb94165c639486e02a8ad035e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1777939200'
# Fri, 08 May 2026 19:14:56 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:54d8f68fe739cb25412100c57f7ac3d8c813d382e3c87d4a5b50e74ecfcf534b`  
		Last Modified: Fri, 08 May 2026 18:26:36 GMT  
		Size: 48.7 MB (48659753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724c2fbbc6f9530c302af04df409e6a05a4da099ae8e7424afb105f85e271830`  
		Last Modified: Fri, 08 May 2026 19:15:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:807614746a291bedd060117e35bfa732393c6968b3526bd1f51a029ad2ca28c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3158032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdafcfb9ccaa20cb97fc8cf1ac9ab21bcd0c2f0b487fa4246ff07f5e3be671e`

```dockerfile
```

-	Layers:
	-	`sha256:36e93aea1ec79f59744af82e937cb75f7853437e06d1ddbfacacaf36485f6288`  
		Last Modified: Fri, 08 May 2026 19:15:03 GMT  
		Size: 3.2 MB (3152170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de9a4d8cc1e3a2e52b6ede03b635cbb975dd79aebdd7fe805bc16dd5e0f4579`  
		Last Modified: Fri, 08 May 2026 19:15:03 GMT  
		Size: 5.9 KB (5862 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:7c970a0b8af357e260c58979f944f468d4160d146e9b5f4369c874fc4d5e6be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49924445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1c7024e5fe1347e88dbb74db3d719e0b8bf640f8b063ce2a5ae1081dc041ae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1777939200'
# Fri, 08 May 2026 19:15:17 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c4bf2344eb0d8b85c765c0311e4bb3914266eb017c58c61eef367588e929fbab`  
		Last Modified: Fri, 08 May 2026 18:32:34 GMT  
		Size: 49.9 MB (49924224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2736b63e8d962f538631cf1566ab2d0b6af45f229d7f0db5b4166a6bdd80294f`  
		Last Modified: Fri, 08 May 2026 19:15:24 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ea9a22e0a962b4df490065ea919b3ff6abf0ef17790696be8dbc0106503ccda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6f98e3f32b23265c550f7c8ac9a5544e95f02128d24f9851b2dfdb65071854`

```dockerfile
```

-	Layers:
	-	`sha256:8e43f0628b72e95c97319255f3f08a126ba49b386b6b86c7ad0449e5cab474c2`  
		Last Modified: Fri, 08 May 2026 19:15:24 GMT  
		Size: 3.1 MB (3144054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d918ff8fd5c1a6e6dd1bbd71267ace5b2128e9df5a605d724999f86fa6ed87f`  
		Last Modified: Fri, 08 May 2026 19:15:24 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ffa0f9171dbeb1b5066b0d77a99104462180457d933f71c073827527161d8f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53927201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2869c84c95bbea5cb415eca60bc907dbade89e922dfa8a83f5984822df058cf1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1777939200'
# Fri, 08 May 2026 20:20:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:72e33031a3b9159cc7f92066908f8a2ad8623d7374596d0e57926590024335c9`  
		Last Modified: Fri, 08 May 2026 19:46:28 GMT  
		Size: 53.9 MB (53926977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c905b733af6907ec287e562c75b6d625922f4807162e9cf77450d1d85bea2813`  
		Last Modified: Fri, 08 May 2026 20:20:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:05c919eb766af65fa01ef2839412c0c2ef08e7dca09a1fa999360a748e3aaa53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bbde691f7dd26a4dbf1d82fba514271725b819833863047edc33a937297b95`

```dockerfile
```

-	Layers:
	-	`sha256:34a9f2ff13d7e7e1f2ab737df3fde54aa8f4440aee48c2eb8a2884663a6009d6`  
		Last Modified: Fri, 08 May 2026 20:20:22 GMT  
		Size: 3.2 MB (3150368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f2ccc9358827f6cecb4412b1fb86fa719b2e61fab8b0e82ac6abd6c82527a9`  
		Last Modified: Fri, 08 May 2026 20:20:21 GMT  
		Size: 5.8 KB (5819 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:9a031b800322a831a4f24757acdd92f0de41310a6f2a48d56032655a798a6bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46771743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a048b946416d217b760818e86f26a78beded45d3c1161363916ba64d43a8b42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1776729600'
# Wed, 22 Apr 2026 05:59:18 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4c44f21b5df28caf1e5408af3b089559389c047937026366d530ccdda4a68b4b`  
		Last Modified: Wed, 22 Apr 2026 02:25:40 GMT  
		Size: 46.8 MB (46771521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5bc1a8601460c80942585b59383a7f1b558ef27a7dde9112b3b64985be3257`  
		Last Modified: Wed, 22 Apr 2026 06:00:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3cd6931bc5414e5914b5b6f5353ae282a77f27bfab6e1f030b5aa2461fc902af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3141751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f4a74cddd3434a1d2d3824711945a91338d2aee7f096b87dbbd8038180c54d`

```dockerfile
```

-	Layers:
	-	`sha256:2b0446fe0598a0b023cda9e63aab253ab9dec8d194accd9255bc19bc2d3cc020`  
		Last Modified: Wed, 22 Apr 2026 06:00:15 GMT  
		Size: 3.1 MB (3135932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd8b35b2e52107594871d5a16c5613bc5ce847f42f438e36bb9378c8ce057c0`  
		Last Modified: Wed, 22 Apr 2026 06:00:15 GMT  
		Size: 5.8 KB (5819 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:1f356c27a60247750b8fc44204e61eed35d2db5462825b29fea2e0eae846d4b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48373758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e33fe25e9b0c3292beb2f7c6e126ed9c4b71803d10b7d7957d98828507549c0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1777939200'
# Fri, 08 May 2026 19:14:14 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:151aa0262450548ce7c86e3829cd579ddfec1f6190a3c78d17553b497410dfa9`  
		Last Modified: Fri, 08 May 2026 18:28:52 GMT  
		Size: 48.4 MB (48373535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b61aab66b2f89c22156a54573ed55886f548e255e14adc995062fd98f534d4`  
		Last Modified: Fri, 08 May 2026 19:14:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:62c7c5ee871fd0db4ddd27c8dedf75e412c7c44f7a9420fdcc727817adf96b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78fe9c991d10a4bf32cc0e12b57438de13f3a7542c11c58e19561455765cda45`

```dockerfile
```

-	Layers:
	-	`sha256:8a082d232c593e949d224899e2168fd92c8db3b51177c73dd4d278abb76351b9`  
		Last Modified: Fri, 08 May 2026 19:14:26 GMT  
		Size: 3.1 MB (3148308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77eec4c57eb80c1a2bee1f46351cfc6d1745ea481283dfa0de2789f1f68ace27`  
		Last Modified: Fri, 08 May 2026 19:14:26 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json
