## `debian:trixie-backports`

```console
$ docker pull debian@sha256:51d7d9a9c6bfd7376429294a7108e96f7cc00b2dbf350294a41ec6fd220f0377
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:4993ab80f563a183811f761c3157830871fce51241765c23e0d3c007d2778925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49284849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23b2e953cc5a239759d596b654804fce77b354b81afab839935bfce761caa16`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8df953ebdf8853121f13a7280dec9c17bdcc60a630eb6e817e6a46a114801a`  
		Last Modified: Mon, 29 Sep 2025 23:48:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:67fa301cfc58da052735638fd675a036f345a7b6935188f3622b98b65ecae2e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c16c231a2bb335c52c33c3e12b309b862dd905bb444fca0bf17df689e3212c`

```dockerfile
```

-	Layers:
	-	`sha256:d158d982e36056bec596693c942d51581ff544a533f08bd55c10d41e52f78ae8`  
		Last Modified: Tue, 30 Sep 2025 00:31:54 GMT  
		Size: 3.2 MB (3169970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb28dad81b929c6eeb6d4d6871e1e58bbb93fe5cbd33fc64111241724eaf280`  
		Last Modified: Tue, 30 Sep 2025 00:31:55 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b20b72e681f3b13e1ec3163a744ea8500ac2ac0808369028447e6b4eb26ff24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47448701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826db6fc540122cbddde77f516835416d5faa2e0ff833a83caf73d26abce937b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0096434708f67385cef0fbdd93979f2d8849a82842e1217f692977f3e6600333`  
		Last Modified: Mon, 29 Sep 2025 23:34:22 GMT  
		Size: 47.4 MB (47448480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edfb676e8f0266ffaae61aa410ef07643b746c5535a59ab794957814cb30b06`  
		Last Modified: Mon, 29 Sep 2025 23:52:37 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c69280ada0528e35879a40e7a0d9c5168e5af2373abc73a1a15673a5b8e5b830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b30830cef800e156fb189ec9bb6f429e21a6a444d02e69533dc3a33872bc84`

```dockerfile
```

-	Layers:
	-	`sha256:9b827e8ad9bd3f2b22419b375d45c8973aa5546f79fa303934fc5c5ba593565d`  
		Last Modified: Tue, 30 Sep 2025 00:31:59 GMT  
		Size: 3.2 MB (3172907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e289e1bf68c579ca1fac1e7f219aa31b5022b46a0fc111926d46bf2a8f35606`  
		Last Modified: Tue, 30 Sep 2025 00:32:00 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:87738b82d7823e6dad8d139976747090fa8024c1b856bd9cf02fdeddfeef2f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45716362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e94557b35ed0ae126eca1ff54304677fde754006fee3fad17eed766106170f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2bfc3e00e130950b6362e6dfd7b2fb6422153e64a38bdcb425f69c089f79f4b2`  
		Last Modified: Mon, 29 Sep 2025 23:35:25 GMT  
		Size: 45.7 MB (45716141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6246b6e7c2763c08ad7946c950c4fdcb60d317783f878783d5d85a3a8e58a60`  
		Last Modified: Mon, 29 Sep 2025 23:53:29 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6a346d323f035f3084d492198c6ecc2c158bb70b876b6d644490ccd2a1898953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f911a44e6ab82c6c185aac8e12ad8243d6acc0a70fdfed374f6af1ff33fc950a`

```dockerfile
```

-	Layers:
	-	`sha256:2659fc668a1dd253e57795033afe2d1f78fd2ccf7926220b2abd748419b90648`  
		Last Modified: Tue, 30 Sep 2025 00:32:04 GMT  
		Size: 3.2 MB (3171344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71676145055d57c18f45b537acf4bc218928d0ca94d30032b2be8e957c996110`  
		Last Modified: Tue, 30 Sep 2025 00:32:05 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:2288b18d33fe050793f9c19a92fff411c26b53c99f69d813c61b90aa67744d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49648917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9c0d6310794caa77d7447635da42301af04de4a223789ef10b6dae09e2dd7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d069da7215dcb47be91541b7e759b92a60ffbcf5e0cc4b5e6876e221c8942aa5`  
		Last Modified: Mon, 29 Sep 2025 23:48:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ceaaa8c6c7e8203c8d5cfb6c6fcce15b1792697b88988aa1a00338e7d5e932c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe55804cb44b23daa3eb7871a50910321838951064966f456c6b52ef5f6f1e0`

```dockerfile
```

-	Layers:
	-	`sha256:cb9622d927066b96b66eee03621bc3df1740071220495b1be9a2bb5e46bd282c`  
		Last Modified: Tue, 30 Sep 2025 00:32:09 GMT  
		Size: 3.2 MB (3171451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13ad098599ecb3dbe710f5dc520da5628901ad52648b1725a29923a8f2d6b28c`  
		Last Modified: Tue, 30 Sep 2025 00:32:10 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:d04a7f33ebea6c0d974dfb38d6564e7502f815b84619700f54e61103ff06c67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50800451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3333fa8a702400e8ac9c7566e06084c85d7203062cef5f3ea66f354cfb2d2c7c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f1c1f592b5569b5e2093c3107a48f2929b609f05af6d24c06d41a7ec1ae5e0e1`  
		Last Modified: Mon, 29 Sep 2025 23:35:36 GMT  
		Size: 50.8 MB (50800229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d069da7215dcb47be91541b7e759b92a60ffbcf5e0cc4b5e6876e221c8942aa5`  
		Last Modified: Mon, 29 Sep 2025 23:48:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3c5d2712d301f1df580c284bf47b94c143bb16f7c5cd3b4112590f8080c1c0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17cc7eb7e029464e8123e39bf5e01b56b3360af854f561071fa626a6955c42f5`

```dockerfile
```

-	Layers:
	-	`sha256:392c14c6226a8d9d0e0ff150d1e27677f7b93aeb279065f64d063b22dacd5953`  
		Last Modified: Tue, 30 Sep 2025 00:32:14 GMT  
		Size: 3.2 MB (3167173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce4f3146d558bc1e75b96046dda3dd37fef99c205167698b23108711f0873b3`  
		Last Modified: Tue, 30 Sep 2025 00:32:15 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:4a00ba346e9808dae90bde530e8e8d35a20532e436a58c13c28e6e3cdbaec31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53104656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4ddac24910530253979e1deb0437e203ef6b01b180a6d528a5292b2b29c266`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66d95f8d42c7a234997f80ccbad8dfbf679b3ed63e0a6be2c1fad00a2a53a2`  
		Last Modified: Mon, 08 Sep 2025 21:59:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b9d518ab49e2cf0468476c8bdb1f94dfb6c9fb111303b9bc2d68276ff4d699e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075c2b4e964d9415cdc5db9ccc51a6eeb6d2c650a221b3463a28c59f6cbccb6e`

```dockerfile
```

-	Layers:
	-	`sha256:f533912d0de0b42fbc55ac5365b1c18eb1139ac2c384806d2f63d62a053dbaea`  
		Last Modified: Mon, 08 Sep 2025 21:31:30 GMT  
		Size: 3.2 MB (3173481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056c9061ea207c5777c0e0425318bbdad8016eedca6cc8619e772995533f530c`  
		Last Modified: Mon, 08 Sep 2025 21:31:31 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:13727ca72e8514353c5fee2de23f3eec8095d84985a84194f06162b1f34622c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e10b205795d8faf4c63e311745a030a823cf4a6d45e083ef25d3ee64ab6fb6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:913254a25f5e448a50a1e74fa50f037e22f85cfe4d6a3c626f4b7405299b7c1b`  
		Last Modified: Tue, 30 Sep 2025 01:03:38 GMT  
		Size: 47.8 MB (47770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed2e1702e8a4470c5ddb19eccfcb7344e413a9d8d3d7083fdb257ae9c0f008a`  
		Last Modified: Tue, 30 Sep 2025 01:29:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:52571708f73762ba94e5855d7c0e9900bc23e34aef71507011bcb17d629ce902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942b9b657faa9c730c442e232dbbe5c83b86c22e6986e63026c2d2987db31eb8`

```dockerfile
```

-	Layers:
	-	`sha256:bc1e53880140b1c7f8e156ad4e079097a8fae5a8b5aa91b1ee777d85a48d824c`  
		Last Modified: Tue, 30 Sep 2025 06:35:03 GMT  
		Size: 3.2 MB (3162293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a251e44d05a9827117338f37315b583b548c19f71b56c921febd19e9ce2d49f9`  
		Last Modified: Tue, 30 Sep 2025 06:35:03 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:d7e41ca6243dcfa7754f85d6313484da03fcfb154361641299ed03f46ee1bc8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49351665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a155fdcbe054941ea8599c246a022ad47a50e42f5117e86790abd30fa03d7a00`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1922f4220aa812be8fb1d0e990a2333e94d2a390310b73d1baacf0c81150c09b`  
		Last Modified: Tue, 30 Sep 2025 06:15:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e1880c2e700bff9d54022cc69f77c3c5e1b21196a5abf802763665b2c5d58e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3f00cbee4fff278c2c3de5d4d8fb6e12d5310fa47e417d2fd6e354bf31763c`

```dockerfile
```

-	Layers:
	-	`sha256:a62a6195d1c36dafdbdf929d2d92b8d1bf5cf846065b93712410799acb4ba36a`  
		Last Modified: Wed, 01 Oct 2025 00:31:33 GMT  
		Size: 3.2 MB (3171417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1538499423f98f44a763358066d865a08df7820152b94a6d3d2eb8fc4c40404e`  
		Last Modified: Wed, 01 Oct 2025 00:31:34 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
