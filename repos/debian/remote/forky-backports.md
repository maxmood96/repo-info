## `debian:forky-backports`

```console
$ docker pull debian@sha256:0182785ffe411ec4adee6fbea60bcd4371a5081116d6efe8dbb39ffb28a07a5a
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
$ docker pull debian@sha256:eae71d0aa5a9df1c079a5551b10cd1b80cf9736fe375b153bbba4b22888bdfb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48779498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636f836fe5b1b53f6e66e71c6ac8832b9d419ef4e06b4fc9a241ea864052af46`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:15:47 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5721d6b62cfc7a7bfa692b95ea547e4ea39b5e2bfe1bd3e1a88886f80c2846e4`  
		Last Modified: Wed, 10 Jun 2026 23:40:06 GMT  
		Size: 48.8 MB (48779274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86000a1bd71706eac6fc8f94d1e649d1c3352d0e0f985dc445d3f8e86dc4bb6`  
		Last Modified: Thu, 11 Jun 2026 00:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9bb871c78d37b9a7a600023a7dae21ddb940f411f83b8e9af576aaaa0234a7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3159748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fc101c292778a0d0251abfb7f81a102a02b00fc26d063cb7d367e75791c994`

```dockerfile
```

-	Layers:
	-	`sha256:cefbb0a54d1b075b449edc95b360767411204af31ab5283ebc463e571c71193e`  
		Last Modified: Thu, 11 Jun 2026 00:15:54 GMT  
		Size: 3.2 MB (3153970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43eb6d78b4df748d527d70b10364d8afc704388751c9eb6653bdf5add1b2f8c1`  
		Last Modified: Thu, 11 Jun 2026 00:15:53 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5961e52ff1562ab51f6ae711f9de57dbb8668a2a81bf2c3798806d0db1f29774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45676785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5886109bd8ab5641b377d62844475b86740433171948461398631bced9c583a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:14:56 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cd14977d91415ae0c2f3a09dcc1dbfa071bbc9d1eaf7ceed6655fe0e671e8d27`  
		Last Modified: Wed, 10 Jun 2026 23:41:34 GMT  
		Size: 45.7 MB (45676562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e4ca9f4e2f74a3a1f04a0d624b56b3a284a02f11e6f08922c1f189725887ca`  
		Last Modified: Thu, 11 Jun 2026 00:15:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9f2bdfdfb7440267d11cf04b415c832da2f3e1eae9b4c19e5d0574d77fbd3b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe62e101394a9a7023612d6c1c27a47d204f3b59021f0620d45933423627feb8`

```dockerfile
```

-	Layers:
	-	`sha256:13059db69679404ea13cb21f85aa707b83ee68edd3ed6acddb824ba7631bfcd7`  
		Last Modified: Thu, 11 Jun 2026 00:15:04 GMT  
		Size: 3.2 MB (3155332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c5b2b4afe558c0a0c2e4c04e77e7dd4fc7f98b6a5aa56850de1a17f121ea53b`  
		Last Modified: Thu, 11 Jun 2026 00:15:03 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:9c2aff946f8cbfb7e21389570e0b90706a82643d72f295a2edf69b158fd69e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48795830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4788ed687444c1c28bf82013a0cfb29b4b7e922fcff677b32e8297248b1368b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:15:59 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:dbdf5115192d6ba17e54d5f2d3cd16e18cba052a9281223f09caff8a3d00462b`  
		Last Modified: Wed, 10 Jun 2026 23:40:03 GMT  
		Size: 48.8 MB (48795608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6ff1817f5adf4de85d8d95d494ad64934d58ff9d17b3a96fe64ea0041a7bde`  
		Last Modified: Thu, 11 Jun 2026 00:16:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fb4449ee0483d268b7ddb0b5707ee559ea03bb6bede816d514cb50494fb8d7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3164486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d26979cf85c3c8508ad0e2e7be8760c8ba6a5f506396156953fed2de27b276`

```dockerfile
```

-	Layers:
	-	`sha256:e5ab075036c3685a9059b85e6388caa396acfb912cf74ebeb34204a2dc742113`  
		Last Modified: Thu, 11 Jun 2026 00:16:07 GMT  
		Size: 3.2 MB (3158640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e84f8f8f1b534180363dad98306990256078cae1d653974f785899f26cab84c7`  
		Last Modified: Thu, 11 Jun 2026 00:16:06 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:6ecc42022ffcccc59451db31509a9ffbf64151420a31761825c1e922ebba7dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50077034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15994bc111ee0c8c5118ac152bf673066e09dea05ef1c49b85b197b915c8aae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:15:38 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d6a4be7a6be3ed3c4d92863f22edf1e7aa21046c79f8c96f534040141953aff3`  
		Last Modified: Wed, 10 Jun 2026 23:40:24 GMT  
		Size: 50.1 MB (50076810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d6e2c2e9f03656684813b384e45404fa9f243f8eaa2c4c5b655976e53fea90`  
		Last Modified: Thu, 11 Jun 2026 00:15:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2b2db7b170ddd4f10c552f421521779591aa04ea4fa61a89949a163a21d5225c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ffb081227583d8194021024276110e79391fb1496c7abbb67740be9c106542`

```dockerfile
```

-	Layers:
	-	`sha256:cd36b63fa176d1327826bf961aca6ec903b0c8da3d69f157627ed85d656e0249`  
		Last Modified: Thu, 11 Jun 2026 00:15:45 GMT  
		Size: 3.2 MB (3151170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f2cac057d288555f2740116ea0862a53bff5f698c23d244252d90f2885d292e`  
		Last Modified: Thu, 11 Jun 2026 00:15:45 GMT  
		Size: 5.8 KB (5761 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:de1d032bc5313f25184eb42ab687b611e56ac704e5a43ad9a8468b937cc0cec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54103328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cc502481765104d85f9b9bfba9e257872f0677c5d1611798b424fc845888bc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 02:20:28 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a6e9fc5fff5ecef539442636839ebbab04ed9b3cd7caa39a93b1023297047494`  
		Last Modified: Thu, 11 Jun 2026 00:22:03 GMT  
		Size: 54.1 MB (54103105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c542a291414d3780f0c23c5d9f0191d1b122c18edf1d7a396ba4da9c1bfd7c`  
		Last Modified: Thu, 11 Jun 2026 02:20:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4fd7a90507af7ef0f1bd9c81a9eb10b023490becb17a3f799adc6b6098c81911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3163279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195a49add418c67be8020a5308c7fa9258344bc61a4fbd86091524f317d452ec`

```dockerfile
```

-	Layers:
	-	`sha256:1209eae08e3beae2108ab5129425d80da9fedd0b8547caa848d0b53182ad5b65`  
		Last Modified: Thu, 11 Jun 2026 02:20:47 GMT  
		Size: 3.2 MB (3157475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0256b66636d5322f36ded4b247958d2ba3d365e1016aff1d6508af70621b9caa`  
		Last Modified: Thu, 11 Jun 2026 02:20:47 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:22c088d91d03240989bdec7985064f619c470af28799220ccca404eacb067ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46868627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0fb55a9db2601048d2d269840011841871502e1fed1550d25949125f3f880f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 22:06:32 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6ed3cb07ce8ad88fd9ce6ed049f21f5d3412d5a91293105a260fd0d8e0631f44`  
		Last Modified: Thu, 11 Jun 2026 02:45:18 GMT  
		Size: 46.9 MB (46868403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b249d26af5bf6c628ef32b2c8e1855947a0a3953b926736ac6bc58f5c9034e`  
		Last Modified: Thu, 11 Jun 2026 22:07:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9a02dbf0dfca3961c9af8548ec0875563f4490f56b7238b7d8ea6be72495a073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d3f87807d74ed5153b007c1009dec78f8b5cca66bfafefae89f1efb5e2c854`

```dockerfile
```

-	Layers:
	-	`sha256:8deeeb2a3a9c5eaed5a3f3c5dc8e512ea0d649488427adba0fa0cdaa8c15626c`  
		Last Modified: Thu, 11 Jun 2026 22:07:28 GMT  
		Size: 3.1 MB (3145478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff4555e15573a47a43fca4f9f78b5ba827ef45fc06437fceee6a95dfdaba5bf`  
		Last Modified: Thu, 11 Jun 2026 22:07:28 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:c9a075042231051a6a7a8c8438549cfe3d1b794d3edda2cdfe990753d45a8250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48513330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a922172c87508252dc11d395e0a14a4b41286d10b385bfa3576064a3bb881527`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:14:47 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5198203a924daa24fe6af49f715c31ab29dfca39eea778fa09abc744d2bad231`  
		Last Modified: Wed, 10 Jun 2026 23:41:11 GMT  
		Size: 48.5 MB (48513108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc01ae4ad5d31bb0fe8a83ac9fa8ce184c38495e3fac1871bc17668860db89`  
		Last Modified: Thu, 11 Jun 2026 00:14:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c0aa1c756014e1f4e772d1a047c87f9060a3be0a2d6bde880a65dd8fb997adb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5da2405fa87dd993d678cf00b64c5cfb0f9a3d926fff5ca406aafae45cfb296`

```dockerfile
```

-	Layers:
	-	`sha256:653a8640c52d6545b769a1eede00eed35b63d4560215bcfb380cbbdd8c1448f6`  
		Last Modified: Thu, 11 Jun 2026 00:14:59 GMT  
		Size: 3.2 MB (3155421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df8fba8d12a0eabcd100dc4e4cb8c0cb7cab8dd96624096fe769598707325d68`  
		Last Modified: Thu, 11 Jun 2026 00:14:59 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json
