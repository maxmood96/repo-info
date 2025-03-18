## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:98ed793fde2f673b32feda05321d6bfa8e17bb2d4c37101a9b545f59c7ea39c4
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

### `buildpack-deps:testing-curl` - linux; amd64

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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:126d37d6d10df132c25fe63e95ee99da19eead5c9f8e60571ecab888046af410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70694640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f225f120d8d054c68191211ad5d8910d443cd673e300cdfa082812caad1286`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:43d6e898d3a5beca16572b1a502b9433116891c583ecdbd0b66dccfd8af9e4fe`  
		Last Modified: Mon, 17 Mar 2025 22:21:05 GMT  
		Size: 45.7 MB (45737144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023a0e893b154d7d5e322d742da1db8537753d0cf777b8cb73ca869670a0c807`  
		Last Modified: Tue, 18 Mar 2025 03:08:29 GMT  
		Size: 25.0 MB (24957496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d2aadf98769a4638a508440ae1ed8bfafa9bc7982416a6625884a934008e580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3978762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73cdcf63b59ba1111705deff96d8bca68f00ffa910850e3a25d9cdbcf33ff283`

```dockerfile
```

-	Layers:
	-	`sha256:fcf6338a901175da227c1434a264821307dcc13623527d8ee5782c33e7892247`  
		Last Modified: Tue, 18 Mar 2025 03:08:28 GMT  
		Size: 4.0 MB (3971881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:183efb90a67a241d4c6a8a74a6a8dab0ea5b9784d3c58f308eae10af99079f56`  
		Last Modified: Tue, 18 Mar 2025 03:08:27 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - linux; 386

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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - linux; mips64le

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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b0804de94fd9bfc72d0af7b8efe7c7d7d245b97db6a389cca08f8001d369526d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78936095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e422c99cebdde0114fc3829984961cdad1f01b3d74a69bcf54909a01456e2b9a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:895a5f19953067f7b5f8d8697fd370f37def792e6b968ea95a15dd11594bc1a6`  
		Last Modified: Mon, 17 Mar 2025 22:20:07 GMT  
		Size: 51.2 MB (51162729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aeaa0f265ddf4206f6d845d5494e3733ac72919e3d0329859f2ce1f44f19c11`  
		Last Modified: Mon, 17 Mar 2025 23:57:42 GMT  
		Size: 27.8 MB (27773366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e9ab5fe6e5b89b6db3ba486a8945d4ee1cff6a0c7bac392163eb6106901f6bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ace8fb0f20bf2bd27b658f7d79d48743823c3bd791894100ec997e93cc0dd4`

```dockerfile
```

-	Layers:
	-	`sha256:62e996d1150fcbef2aabc02e6df37c3d34d05ddf22eb450b8960fe8fbdad988b`  
		Last Modified: Mon, 17 Mar 2025 23:57:41 GMT  
		Size: 4.0 MB (3972899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6606af07ca7d99fdfd2d6fa3fa19c9a29d9a24563631a43fdb01a5c16fddd514`  
		Last Modified: Mon, 17 Mar 2025 23:57:40 GMT  
		Size: 6.9 KB (6852 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e15e0e2ad56efc2cd11991bfea095fcde0bc8948f138ccc62180d54cdab3b278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74941319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afeee88ce08fa2146c4fadb350727ada91391f2e0f8a5929f1b5232671f7d7b1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d25d70cc33acfbb261e54e41a50ee310f48343b555ff5a724ee79cad7214fbf`  
		Last Modified: Mon, 17 Mar 2025 22:51:24 GMT  
		Size: 47.5 MB (47548830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74e201480524a9e7f1671230b2cae3b456d6d6a91a8a4a2b07140f308c08518`  
		Last Modified: Tue, 18 Mar 2025 02:48:54 GMT  
		Size: 27.4 MB (27392489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:153bc2ac0fc27bd164ae0b2b511d0a9757c28afb6ef3bace9baad500e19a9482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3977412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68e7bfbe7fadca7ea7e8127b2e3ed58e76788b9e5bc78d2954b95acd7c0c954`

```dockerfile
```

-	Layers:
	-	`sha256:a01c0c9d224c534886f7289dd1d0c97cbae424d01f1576a39442bb2d734b7011`  
		Last Modified: Tue, 18 Mar 2025 02:48:53 GMT  
		Size: 4.0 MB (3970591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de951a8340100b19d340693f1aa85e4caecd7fe5f542934c0acebba6ddd88958`  
		Last Modified: Tue, 18 Mar 2025 02:48:53 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json
