## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:ad56a1d2b0dafda9c766d8961f1fe445118fddceee4fdc37c3e651d8e7216c4b
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

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5da2c6eb7c53486c42b8bb740f8a6249bb8ccda0e5a905a27cdb29f2aa06f6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73744444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785772f8604a6dfc2be54bf1ebe4d5c8fc3121abb1a624419103339ac5236151`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b312498eaedc471a9ee574437ddcf442ef14eadb9305c2ea1c843f2af922d473`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 47.5 MB (47513473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307579de8afb457f38a2a818765fbf595dc7bca2e9022efb29cd9a1e5c6b6b9d`  
		Last Modified: Mon, 17 Mar 2025 23:14:00 GMT  
		Size: 26.2 MB (26230971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:93816f807a1931cb60f78c038eeab9e87214ceecf45081215096bc1fbc60cda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3970438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9475aa39e4b87ca3b445ff63827e6188e668a220a243dcf0b88b724808b1c90d`

```dockerfile
```

-	Layers:
	-	`sha256:a631ceedf3d33875e0b039ea490799558db6e7e3047ab485eedb1479a281aa29`  
		Last Modified: Mon, 17 Mar 2025 23:13:59 GMT  
		Size: 4.0 MB (3963618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ada97a6b692853cdf2918e67ad2354fccbf575089be3db7c7a3da49c0eff36d5`  
		Last Modified: Mon, 17 Mar 2025 23:13:59 GMT  
		Size: 6.8 KB (6820 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8f229be78533695f2b01838c909094820a711d4a9b6da18c9c01d8bb85d7e041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71834099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c34124109b78cf2b6e174aec34114f77e2300c1bbbc37ee87e50c5a79c4e789`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:131ae520a4eaed5ef3f8bfb62695032fc5b0cf09159cb958245abf1bbddef3b8`  
		Last Modified: Tue, 25 Feb 2025 01:33:17 GMT  
		Size: 45.7 MB (45706841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2cfbb99d11f866136a1de25d46d555105f60a1f7b061aaf7d89155339ee129`  
		Last Modified: Tue, 25 Feb 2025 05:17:32 GMT  
		Size: 26.1 MB (26127258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:771b1bc7da51b672b9e4b8fb5ff74caf4775ef963f5d20a317dd579cf51f2cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfbc7363dea40509fbd47c84726da57f51935453b4c4fb70e1fab2a885d69be`

```dockerfile
```

-	Layers:
	-	`sha256:c3c7bec1128a438c70d24a30d1717cb462a04c85c8c1466f900c6d4297dc825d`  
		Last Modified: Tue, 25 Feb 2025 05:17:31 GMT  
		Size: 4.0 MB (3990809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7c0ed172c31310db2c3124d65aad5ba829d4da5234e93f3d4001644ab0f46e3`  
		Last Modified: Tue, 25 Feb 2025 05:17:30 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8c844b9f3d0cf203e944fa57031c8232be27515e6339cac98bec7134e0b1ba70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69181570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cc20f04a9f28d645fdbd4a9aeb3f85307e752144294469b6b653040a08462c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1268bec7b6bf92bd5fc4d4120fd51b9bde5a9c50d4b8a8decb59fbe4a53da6fb`  
		Last Modified: Tue, 25 Feb 2025 01:33:55 GMT  
		Size: 43.9 MB (43903193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe307003fac8d59260832b7e5476d782c0d94c51fc746df3d40b574a8cd73406`  
		Last Modified: Tue, 25 Feb 2025 07:18:31 GMT  
		Size: 25.3 MB (25278377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d44c218c94a00152a9a98f11e6561b7a9956ba15903b65df09cc676bfdd9cba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2853be4af73e3581e434f66ef64aadc11fc936331bd025d9ee2968b0dbe29449`

```dockerfile
```

-	Layers:
	-	`sha256:f1788d96e00421b0ceb3ae4c75db7ba3ee286b669e4089847c374a1e35d8a87b`  
		Last Modified: Tue, 25 Feb 2025 07:18:30 GMT  
		Size: 4.0 MB (3983399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420eb896b5f05bf72bb258c5219094d71dc763131f00d66d741d3c906235da4b`  
		Last Modified: Tue, 25 Feb 2025 07:18:30 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:302310fcb56e2ef2e166721c0b1709c36fbd66f6bd03430681d79b0eab01f592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74740734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9ccb614d37086a3252f07b50d52f4011406bf9eeffdaf1082d4895dfffab68`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4febb367456c7cd84b8043b3b3b3c93073aa9439fb54961fd46a9370758fe523`  
		Last Modified: Tue, 25 Feb 2025 01:33:49 GMT  
		Size: 47.9 MB (47858532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f249b42e8ca4f2ab0a926162c24ad19731e17ebec889633ecab6f0a37257460`  
		Last Modified: Tue, 25 Feb 2025 05:43:15 GMT  
		Size: 26.9 MB (26882202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:01f1ec51610eb6b9c7db1c5d37d823354745c7c3f06ef0db9ef50970679c735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f495175603d95bc0144f0801a04627c2e831fb811c03474d5abcdf5b3e716ba2`

```dockerfile
```

-	Layers:
	-	`sha256:8169d87f65c15a10837c0e0316d8c54b4d04d20864d1a9939d67e50b5465e4e6`  
		Last Modified: Tue, 25 Feb 2025 05:43:15 GMT  
		Size: 4.0 MB (3984077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:535cfbc57e7fa30dc4ae5333fc7fcef55f5ba2f3e55d118903d5a2041dc932ed`  
		Last Modified: Tue, 25 Feb 2025 05:43:14 GMT  
		Size: 6.9 KB (6901 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:da9f0c53295e6566a8d19a1a64a71b8a5453d0c3bf858d96d1362c5fedd084e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76211779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891c78e20a492fdc81bd5da4d132e732961a0e7afbb1e2f0cee44b8fc0c066fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7f35c21acae2ef6b77873a46c174f1da0b28fbc4ea787b7f5bb3bd79c145883f`  
		Last Modified: Mon, 17 Mar 2025 22:18:02 GMT  
		Size: 48.8 MB (48831362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2417ac61f214f6f239ee6ce6ccf4e9a29aead09dd8338aeca7ca8645adc7a0d3`  
		Last Modified: Mon, 17 Mar 2025 23:33:10 GMT  
		Size: 27.4 MB (27380417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9ea64fa99e55d87f01ed297b29d22a83bf129c9adf003850cdc3520e62ffbff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3966821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283b6dbd59ff45b83da52a51fefddc0ec339fdbd75c43e6453debcaae7f2ba39`

```dockerfile
```

-	Layers:
	-	`sha256:6e429ffb84a43f6e4f0d2a0cb7ac83faeb3e30351be75268e0bc9f8258fdbfb9`  
		Last Modified: Mon, 17 Mar 2025 23:33:10 GMT  
		Size: 4.0 MB (3960022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90be2039126102bdd95c57f4fa2e33741923d3455735fd78b51d7f09ca70edc7`  
		Last Modified: Mon, 17 Mar 2025 23:33:10 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:57cfa2e917d5697190b3170744133b4e20ecd7dd47098f032cda15749323623d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75151253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38758c38d1de0d744d39c24288e66aae427d05c54d20753969162d2a99aec5f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b3018c8b96b9ba22f17940c42dddfbfef3058b787c07b7ccd94c52adb65aa552`  
		Last Modified: Tue, 25 Feb 2025 01:33:17 GMT  
		Size: 47.7 MB (47684440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d568a834d28f352d6c862c921a5a1525795a3ba966e684f287dc047fc5a62e6a`  
		Last Modified: Tue, 25 Feb 2025 20:40:18 GMT  
		Size: 27.5 MB (27466813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1bae52ff6391b44aa8410d26e721daf9fe993165321ec420036feb2e1830b07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6534c4437b73e8ea74e5fd31d76d8147caa6f298827dbc68233ce7820ed6ea87`

```dockerfile
```

-	Layers:
	-	`sha256:5dc5b7dff11b6f827a05b816c97fe982f01749ce26f32db091f5da4e399a4a88`  
		Last Modified: Tue, 25 Feb 2025 20:40:15 GMT  
		Size: 6.7 KB (6654 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7b1158a1ec6a61db1d9370c72173b789c3416211360bd5679a1b9866a29c8e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80147875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2891972b26f3d78e67d74b03fc14ea53c2f1b650602db0698cfe0251e023a229`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ea3e230c71f31965fdc8d0bdc4e71749c73ddb97789439e708ba01bec0516b7`  
		Last Modified: Tue, 25 Feb 2025 01:34:02 GMT  
		Size: 51.1 MB (51131291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7136b138a9fbadd117790fd6473b3c1516b6ff1b1b1e5e321ff71f2a2c4c08c6`  
		Last Modified: Tue, 25 Feb 2025 04:34:33 GMT  
		Size: 29.0 MB (29016584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:59ab33c6d69ca74e8bada3143400b82227893657d0eac5d97c493f45738d89a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c56668a96d1a0780c777b1d8a2785f652f3f95f8de436baa2d7f5c8b02b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:64800b663f1c764868477f33b530157d92e817dff12f93a144e393fbd6ef29ef`  
		Last Modified: Tue, 25 Feb 2025 04:34:32 GMT  
		Size: 4.0 MB (3991833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4287831e1e8e54dfa2124acebf7438381b568bab05c1f486a703bd4ec377a45`  
		Last Modified: Tue, 25 Feb 2025 04:34:32 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0b9a8e3bc285c720c3a0448fdf1721906dcceb45a34214423ce4e959a4f5b42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71610889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3112e5dd6cd8998062f7b4e2db6101bf48abfa2a3292e1df5244b043e180eb97`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d3a862dfbe73fb2b7bec94b343e4db0ecf112c748843a5e8e692909906de0788`  
		Last Modified: Mon, 17 Mar 2025 22:44:58 GMT  
		Size: 46.0 MB (46039032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbdbedb7310f3378a7d67fd47bc9c813ba967f6e7c89fad6232cc927a627505`  
		Last Modified: Mon, 17 Mar 2025 23:23:24 GMT  
		Size: 25.6 MB (25571857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6cbadd1baf1b0c61139fb56d0c53197ea01415f4261b16cc2fb30fa8195bf597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84c25fdc4f59e6ea86b4524bfc957e7c74a57ab98b307a63b98dc6a5b115984`

```dockerfile
```

-	Layers:
	-	`sha256:edba7dc75e9d8e268f4cceb94c5a4ff2eb3aa523f320e80d96ce1692a266943c`  
		Last Modified: Mon, 17 Mar 2025 23:23:20 GMT  
		Size: 4.0 MB (3954177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:111f505f358931cbcac881d4b04905cfd658cb0b7f9f67d52474ef6b5ff4095c`  
		Last Modified: Mon, 17 Mar 2025 23:23:19 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8ed01bc7a03531098cd6f408377c7336a7534f981a488d48a9269483f6f4438e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76116397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82df6e34dc335d3f4a50c408dcc7f52060d439944fa03ca167995d033dcc7212`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ab0460cfb129d20515573ff27552b94c41a5822739be2d7bf548df5315225ee2`  
		Last Modified: Tue, 25 Feb 2025 01:34:35 GMT  
		Size: 47.5 MB (47508261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ec199ac309750ebc4bdf20cce23eb64ef847d0a7c63d2075c1e80b9a8017dc`  
		Last Modified: Tue, 25 Feb 2025 04:05:59 GMT  
		Size: 28.6 MB (28608136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:407eb3c7c939808f061754255cdf557aa1630839f83fd3e8fabc0bc8cb616217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a357f9cc36eb6cde6b9bb8358bd17a1be209a6a36723290add6b2da240775d67`

```dockerfile
```

-	Layers:
	-	`sha256:e1578435a5544e8d5dad9fe4381e1ea273ee66e7c43084d0dee991aaba9d7e41`  
		Last Modified: Tue, 25 Feb 2025 04:05:59 GMT  
		Size: 4.0 MB (3989519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46822171c85a53f4d4d3365568c0dcb182a9f73f44777ce529288d81e69faa4f`  
		Last Modified: Tue, 25 Feb 2025 04:05:59 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json
