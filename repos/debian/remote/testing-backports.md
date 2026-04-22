## `debian:testing-backports`

```console
$ docker pull debian@sha256:e5791af8fbe8ddd26bcd2c62aca9cb7152fc302df0344809a1a914dee6a630b5
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
$ docker pull debian@sha256:9e9baafd1e6ad705cba4a71199966b1027be2b2556502ef8852bd861c239906d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48697871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf87be01880862e44ca00278fcd2d3c081ab489538f5c681816412ad4ed7dbf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1776729600'
# Wed, 22 Apr 2026 01:15:31 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:abac6300560e52d30e8863740fd61dd35f371fafec8988cf290ccbea4887753e`  
		Last Modified: Wed, 22 Apr 2026 00:16:46 GMT  
		Size: 48.7 MB (48697649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4305ccf45f13fb635370d2e8dc5453b91c22de16668e7ac35866e2dcb285ab7`  
		Last Modified: Wed, 22 Apr 2026 01:15:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e15922942cee1808a3977bf4c6a0b3e285d241d3239813bd752398c67dde3a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427d871d3b0da4f54b3b0fc947455f6fe396040fdf963d43e84f017154ecae0d`

```dockerfile
```

-	Layers:
	-	`sha256:ad5733b470185f6d1f591ec05a52be2e663fc9f892da1f7877b05c66d535f32e`  
		Last Modified: Wed, 22 Apr 2026 01:15:38 GMT  
		Size: 3.1 MB (3144424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb840412648d860b3d70a55b2db2a0267f1632a2c393bbf3f9f28f4a22e1fc3e`  
		Last Modified: Wed, 22 Apr 2026 01:15:37 GMT  
		Size: 5.8 KB (5792 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:0eed4bb68152ae7cc79a431b53fa1da1166f6a6228a22cb7110c76175a970dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45622355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577d2eb1f338941090e1c14d9ad36cf3cbce4f4c4de17c074dd3ab36b0f0a20b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1776729600'
# Wed, 22 Apr 2026 01:15:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cc58ca000cbe5f8100a66887fe4a78a7f18408863d4b871783fe724e67a1f289`  
		Last Modified: Wed, 22 Apr 2026 00:17:01 GMT  
		Size: 45.6 MB (45622133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975216c97eb0dfd531bb898bc3e6579610bf09ceeee5339c3cce1bae88834a2d`  
		Last Modified: Wed, 22 Apr 2026 01:15:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c5a0a050cc133a90ccefd5760860524d754dc3b1e5939cd6673d7459ad4b7568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b725c91f16469087c9ebb7b28a0aaee2a9a8e67f096d4d3e9e35658f623a2b40`

```dockerfile
```

-	Layers:
	-	`sha256:4646d7cd27dafcffd1415109c14468e8ed5d1b002120ae9efa832bcff0a8c18b`  
		Last Modified: Wed, 22 Apr 2026 01:15:10 GMT  
		Size: 3.1 MB (3145786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b145c9c7ee2ed9eadfbacd7d34b6284ccb951891e9577ec26ff0fc715915a42b`  
		Last Modified: Wed, 22 Apr 2026 01:15:09 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:68a60377f5a8c57b8a4f75e538e2eaea3fc65fa3ec1cecef9b00b8087f1f3a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48726332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a97c98d8ac9af3897e8e7ddedff4686b47dfa35908b138d551f1bd4467ee21`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1776729600'
# Wed, 22 Apr 2026 01:15:07 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bf17e2bd9d2bffe1d04cffd7317dcbb7a2a4c186c9dfb9d304256a390be3e654`  
		Last Modified: Wed, 22 Apr 2026 00:16:36 GMT  
		Size: 48.7 MB (48726110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f0885571673a03352fa4f87ec6e0d61866f084bd83dcfae0a42d787bd6d212`  
		Last Modified: Wed, 22 Apr 2026 01:15:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:21e74dadc15d9b4d552e602adfec653b1d5f5693a198c551e75170f821c34e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d6c5cf6475486343309ce58bb0f9c39a1f34c9967ace859eb932506a372c83`

```dockerfile
```

-	Layers:
	-	`sha256:355ba5add09d33a15116977bbbb6dac001c512975ab48cab66ee807d4c4b9659`  
		Last Modified: Wed, 22 Apr 2026 01:15:14 GMT  
		Size: 3.2 MB (3150374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00734268caa3b1dbaa033e8dee279b091fe14f945587c86a3176a04baf4da34f`  
		Last Modified: Wed, 22 Apr 2026 01:15:14 GMT  
		Size: 5.9 KB (5862 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:85109f1d8ea7baf6c1f0c121951d328fcb9dff77b91e31d7dc4b2cac6bf4d6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49982855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8f444c8072f06699a385f7e53f36dfecc15c4f9372103aa4af83ec504bf6d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1776729600'
# Wed, 22 Apr 2026 01:15:46 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:357989791f0e79f4822196bad9dabb96e004f9aa19efdca858f406c72349087a`  
		Last Modified: Wed, 22 Apr 2026 00:16:58 GMT  
		Size: 50.0 MB (49982633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4124ad317876f7f0de898c5436157d336eeaa4e342c66ecd089570190be2739f`  
		Last Modified: Wed, 22 Apr 2026 01:15:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:36c6031dcd4bfa2ae73f7abbdf9d41abcbb69638328afedb1379ee476470b817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3147401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584acd0e09f811a47db77b2d260e399ed5973e78ceb8aa83291397c8d24c7bb0`

```dockerfile
```

-	Layers:
	-	`sha256:2936fe56230d38998b6ee9790b3fa996ec3b54531328bb5119e35764a755d0fb`  
		Last Modified: Wed, 22 Apr 2026 01:15:53 GMT  
		Size: 3.1 MB (3141624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d775aa4a7d44188a115874ec5b55b935abddf7081c13c571802a04dd5010c78b`  
		Last Modified: Wed, 22 Apr 2026 01:15:53 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:d752750dd1cfa44867defaeb2dc341ae75c6ecb29933d53809a6f283463fb3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53984157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241341e32a6d295c66b9356215d0f8a01534e344a153b60b574eaa4ba0c0aa66`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1776729600'
# Wed, 22 Apr 2026 01:16:04 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f9b980fdc131af725c95a05efc822a28b18b0a63759873703360421929beda59`  
		Last Modified: Wed, 22 Apr 2026 00:17:44 GMT  
		Size: 54.0 MB (53983933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9b66bdeddb7620c2850ad50823347a03fedcf7967a1f8dbd5702a0cbb024c2`  
		Last Modified: Wed, 22 Apr 2026 01:16:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:782c4f7429306827fcbbb942f34003c2ff253a00878430a95d83a9b790f37d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93416be9b1bd02d2ec90584ca3a3de741f1112336c89f758492b813a8721090`

```dockerfile
```

-	Layers:
	-	`sha256:8432ef3b23e9352f758eee46d43d067a5a6f2fe6e392e882a62a230e70ce73e2`  
		Last Modified: Wed, 22 Apr 2026 01:16:26 GMT  
		Size: 3.1 MB (3147929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9721dd73eba5eabc2b8f12d41333304cf26a872ec0349ff3e19ffab19cb1131a`  
		Last Modified: Wed, 22 Apr 2026 01:16:26 GMT  
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
$ docker pull debian@sha256:d63257cbb5d64c07ca19442da8b9ae1db2d86a276891a2afc5d3a2e3b9feadfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48407827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23d524163556392ab5adc19a1ae14521d6733fe403bf2e311e9ee35ad0c1259`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1776729600'
# Wed, 22 Apr 2026 01:14:37 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7d15de2b1a4fc4a6aaea8920bf366a7c0eeaaf95efaa5bf45810c4f134cefa77`  
		Last Modified: Wed, 22 Apr 2026 00:16:42 GMT  
		Size: 48.4 MB (48407605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb678c0ecd0cc88914b678f5985249e90d83fc9e2711d73867083211d6fa380`  
		Last Modified: Wed, 22 Apr 2026 01:14:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:74df894fc9da1bcc7e6e808bd5980b2f2ef737d5ac95d94e08dfebf661e1e110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8072b783eff5df29d76bb8239847a6db25d685dc8648d901b7c4c4d25f233c`

```dockerfile
```

-	Layers:
	-	`sha256:91f1c1263d6356457f3f5a9af68ba4ea9c6e9ed861b279fdc6f5e683fa01b47e`  
		Last Modified: Wed, 22 Apr 2026 01:14:49 GMT  
		Size: 3.1 MB (3145875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c8b0023f648acd1884be4203b76c51adbc9e23370eeeceb92e7f26396a82663`  
		Last Modified: Wed, 22 Apr 2026 01:14:49 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json
