## `debian:experimental`

```console
$ docker pull debian@sha256:67606aaf8496071861dfeefc70319df03576ab5641e0cefdf2b350e13c803ecc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:3ac12a2a5310106169b0e4711a023eeb5b8b24064d5b87b99c61b849d9ba587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49658212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef8e3a823b886f267ccbe96ec8290927738f8d4cad8d2926e7eabfa509c339c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:ee21244e7fbeb55d12d482599f8e19a2f8ee5334f9406281ee95a823709cb8d4`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 49.7 MB (49657993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b9e6df6330952521247f5c0dda65c47ac43ff2fad0c8facd8e171f1340e142`  
		Last Modified: Mon, 08 Sep 2025 21:52:56 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:97b7d34e541444a986ae4484936e727bc0b5a67f05f845aa02d87b3747e96ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50dec714da2a730cc8c017a4fc81a714d3fa50422f1833112e2abfb582ab4ea1`

```dockerfile
```

-	Layers:
	-	`sha256:93cb19ec68dfef49deee8f6c453139992c04c7dfdd3e94e2506e49773c5092fd`  
		Last Modified: Tue, 09 Sep 2025 00:24:28 GMT  
		Size: 3.2 MB (3171367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d0beef7126964d0c2a0a282432c280c9d380df1854f6d0c337f4520565291ec`  
		Last Modified: Tue, 09 Sep 2025 00:24:29 GMT  
		Size: 6.1 KB (6144 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:b5568d4783a495e9294b63b9ffca0b64dcaca4da3012a7af824c2c47872ee420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d0b6e4e0d4c8cd2ab86fde0d35729925ecfa6c4ac275311d540046318aa991`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'unstable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:5113e810d9f7dc6709921d1550f4d1489e07f7d472b633c6197af505f3b8f027`  
		Last Modified: Mon, 08 Sep 2025 21:15:32 GMT  
		Size: 47.7 MB (47745324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2f9ca4fa34cebb5c03e864444fcb394e0b94eebeae05c80b6d31e95d2af4d1`  
		Last Modified: Mon, 08 Sep 2025 22:00:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:0c464dd174d1b4abf7a3abe405cce7e48bba97474334108017b04f390064e79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3384109e9f344e92172b3cb99a3ed01d5bd02289c2784f1fc7094f016aed5223`

```dockerfile
```

-	Layers:
	-	`sha256:9078bcc3df8f7beec45016ea3095a93c46bb23996af22518e923b3949046b7e1`  
		Last Modified: Tue, 09 Sep 2025 00:24:33 GMT  
		Size: 3.2 MB (3174329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:130d81b9ed8210738713ff9e330763203ccabb5c36502f015f601449d463a14f`  
		Last Modified: Tue, 09 Sep 2025 00:24:34 GMT  
		Size: 6.2 KB (6207 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:d840d410528ec7287d1650e19ef27f708ec7074bcba6137c2e7267e6f8bcb98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46006917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec41b06150b1b0e7568d04ee95526b7f5ab6f390c6f29989808d15fe430b09d6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:81f3b3935f8754c20363f4fdaab9fe4417eb104344ecb24228999e219f13575c`  
		Last Modified: Mon, 08 Sep 2025 21:15:33 GMT  
		Size: 46.0 MB (46006698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26fc8946329ca93ebf52e2fd6b3e3c223160fae034dfa818a9144690a538656`  
		Last Modified: Mon, 08 Sep 2025 21:57:06 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:6f4a3824ae51a3fc25f775892ca994c579f1080e2ecadc67f6a0df477ef21009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4d98532cd560dcea461d70ac26d91ccba42e8d215dea32cbf21525435e8317`

```dockerfile
```

-	Layers:
	-	`sha256:a07f3cb36005127ff9b06d6fb66a1447ea9b1f6d61cbe19016f669a4290c5a13`  
		Last Modified: Tue, 09 Sep 2025 00:24:38 GMT  
		Size: 3.2 MB (3172749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3e2e99f6e48161c6d63479d53770b9177aba3575f696726fea9cd6f4e5d4b5f`  
		Last Modified: Tue, 09 Sep 2025 00:24:39 GMT  
		Size: 6.2 KB (6208 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:086477a5883fed71b892b390210a51cb1fd3914deb614d294e71ba72dc672607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49934945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe913a5112fc3d70c8629a893826a0d5fbedb534456ac5fcd0dd359885388c7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:26211369345f2e4eab8ae868d64f60e39194183681480598cafd9f2639b61bb7`  
		Last Modified: Mon, 08 Sep 2025 21:15:17 GMT  
		Size: 49.9 MB (49934724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eae7c8f1ffbb9222645acefa50ad8a91dc9ff61afc69f6fca63c189e2c7557f`  
		Last Modified: Mon, 08 Sep 2025 21:35:05 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:b257a0ac26c29e160158ec23cd1775618953025f6385271249bcbb336174c159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e04b62f32245c5d9295e42758fcfa1b4a69358cdcfa28c29050cb98b00f8707`

```dockerfile
```

-	Layers:
	-	`sha256:a3f4aee3b6bba8a681af88b7f95cce4728b4720d9f5a928e8aaf6611d5c61efb`  
		Last Modified: Tue, 09 Sep 2025 00:24:44 GMT  
		Size: 3.2 MB (3172860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67ab40494d6f8f9d0ec0efff8acaef788678f32b71e3d3779609aff081adc64`  
		Last Modified: Tue, 09 Sep 2025 00:24:45 GMT  
		Size: 6.2 KB (6224 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:826fb5e990f68a3cafdaa5f152054b41c3a987f4f44cecf794aae9b665ab41e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51113837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15221e9cda4b217638d442a159d9794f6c3d39d8d3a6402a7e121256072b114c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:9bacb7a8dec2a0f7ca748ace8f537d21e44222334f0b6f1ba9eb1c3f9ae6a247`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 51.1 MB (51113616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec5507232f16f6489d8b889754f79de41061090720db1140ab53bd9f845a961`  
		Last Modified: Mon, 08 Sep 2025 21:58:06 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:45b3b1582e28ce1ca97014bf2f1dbbf05e411374ae72c91fc29772553912ef9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3174689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4066047406f00eef2d26217d56a9147ae8e71e74d1a0f507d9001fad2e672c98`

```dockerfile
```

-	Layers:
	-	`sha256:d2caab518976e11cdd9df7f804124995d54bbf1157d50877aed9301bab43280e`  
		Last Modified: Tue, 09 Sep 2025 00:24:49 GMT  
		Size: 3.2 MB (3168567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f06d746b55176d224a4c3f32ea7755fa7f4ef03524319227a405347f9d04bd7`  
		Last Modified: Tue, 09 Sep 2025 00:24:50 GMT  
		Size: 6.1 KB (6122 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:4ddf8f999a5fa56f4a4726374d923327e6d242293666777f6e0e7f060662cf28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49822484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586a3328dd03e6df31bf891dfbff5ca805a9416c1c980fdc4d5de6caceb9aeb0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'unstable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:86de560ae5dda166ef408413e1256c04ef23d08b5f38423cb7fb22b02d3db846`  
		Last Modified: Mon, 08 Sep 2025 21:17:08 GMT  
		Size: 49.8 MB (49822264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de89a616fa51f3247335396ef8b9d90604b109310b1b8e8e8eac4f18795f146a`  
		Last Modified: Mon, 08 Sep 2025 21:56:06 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:38cf2c32ddd3ab161f73024a863c09a5b7f4f278cc934f6685eeccd3d2570f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 KB (5976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73f081f91faf460cd4b62f8cd44acc315d95f298f1e165919c182684fd0b235`

```dockerfile
```

-	Layers:
	-	`sha256:2ce7abc0b83e054926e15c445a6e9f058aa225a468a115ce8ff479d2fb840bcd`  
		Last Modified: Tue, 09 Sep 2025 00:24:54 GMT  
		Size: 6.0 KB (5976 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:18b79cb3f70f0af21b51f59f0fc18efd51fc96016d2b2d6cf3c72755b858840a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53459016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e543dfc62c676f21f4b38a4e18fabbe367b04d2bd749c75ecb366db562e8854b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:f184de182b15f43d0d0377e0226519159f9bd7d80b4677f5e1514cdfe6d7f753`  
		Last Modified: Tue, 09 Sep 2025 04:54:11 GMT  
		Size: 53.5 MB (53458795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66332a9500bf6f3339a3fd593c1c0a52adf97cf04ad8c12bfe32705c52c8e6c`  
		Last Modified: Mon, 08 Sep 2025 22:03:11 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:101b0a711bc2a8c0c77fe11b66e8612ed6c7e67f65e6ad0e5d7a67e52d470d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3181056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b401536f10e0d7fc1f36dc3579828bca8245e9d9f9b276ff279279d1601249f6`

```dockerfile
```

-	Layers:
	-	`sha256:3519e4cd936da4ae99af15ae25eaac20c7a0d8a75d14f398b5b667ad9cde468c`  
		Last Modified: Tue, 09 Sep 2025 00:24:57 GMT  
		Size: 3.2 MB (3174880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36db31c544ca92fd840d0bc7add98fc463344649355afed82b8fdbd1aa89c051`  
		Last Modified: Tue, 09 Sep 2025 00:24:59 GMT  
		Size: 6.2 KB (6176 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:13634370752fa850bb0a6882a32f9f80a423322e6bbb635bf844f077a000f6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47776783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270c6c0b2dd0204f131e3b88f7c23b33ecadf619283b477b076f7855640e9d53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:49905211581fe3e61537fd9efcf132c0adce7bb2392c9b012120b155453a504e`  
		Last Modified: Wed, 13 Aug 2025 07:00:15 GMT  
		Size: 47.8 MB (47776561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ff468d20aea9d87e705a5ebb841265f164aac86014ee9715fe3f56ff5e68b2`  
		Last Modified: Wed, 13 Aug 2025 07:46:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:772baf43ca8d6604659403f6cd953829b01b01ecb336db7e5de75d1fcead3628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3166362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ff1a3d58ed6ea8e6782f2c97ebce23cdcbbfc6dcd1ff18fef04fb7e290ae61`

```dockerfile
```

-	Layers:
	-	`sha256:5d711f6f1fc5a077e7f394ba8560a973fcd6eeb5fd1e39d583065e93b648bff1`  
		Last Modified: Wed, 13 Aug 2025 09:24:05 GMT  
		Size: 3.2 MB (3160186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa476d480931b4b7d2f4336cceb429473a128dbb20d8de52ee81bd93b62eb398`  
		Last Modified: Wed, 13 Aug 2025 09:24:06 GMT  
		Size: 6.2 KB (6176 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:6a9705509db33039d1ff0610ea835e55b2611f7bec65bf005fddbba73421b21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49652261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e725abe87667818d38118a2044fad73626272fac68f8ae35a416fad21ec3546a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:cd75d0600873081600463c01ac825b23c5521f8796d0bf7c9b50cd7b6ee6a792`  
		Last Modified: Mon, 08 Sep 2025 22:19:19 GMT  
		Size: 49.7 MB (49652041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543e021bb4f38552ea1ff24dc649f01e29cae24093fb2fdce1bb4df82c6bd178`  
		Last Modified: Mon, 08 Sep 2025 21:56:08 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:d2d2cd37a1c7f86b486db259b450e3a8a9299c0da1adec3d4a70ba2f47229da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade6fa12f80e21ad2b4953e87aebf78ae1c2b058b9b39e6d744176b5e63ce138`

```dockerfile
```

-	Layers:
	-	`sha256:bbbe9d4ba69afddd57a8fa773133f2b9daff4b408ed48e21f0c9a7ad705d54ea`  
		Last Modified: Tue, 09 Sep 2025 00:25:05 GMT  
		Size: 3.2 MB (3172814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:846a4cec7b5b0ea8d5c360fccbb59bfcefa1f60f97ebe57b228238e01bf22a21`  
		Last Modified: Tue, 09 Sep 2025 00:25:06 GMT  
		Size: 6.1 KB (6144 bytes)  
		MIME: application/vnd.in-toto+json
