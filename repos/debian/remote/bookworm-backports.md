## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:f58e2440904c8baeb714e3e99cb649f4c6e7141c0bf00673d9e8b432df856503
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
$ docker pull debian@sha256:e0d784936586deec3d6e1a25b44f9bb870727d25a2797da0117c488faa05109a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49575920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5125a24d1813b3d74f3e2403913002c259a5e32f3be3d516383fd73589f838`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd7862def039651662d87f12add7f89f91621661f6dca4d05a17066c0798b1f`  
		Last Modified: Tue, 12 Nov 2024 02:01:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:75aae1d46c5549818c20198db6e070c526f1ea60f0ef5190a6f28c43e7d63768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afdfb525022140e5487735726463463b4669483b87b46ab9c1beabb2e8fdc73`

```dockerfile
```

-	Layers:
	-	`sha256:c3357b02d740d20379a58f2c7134e5f9e6af15ff856cb23c3214b84583ee20e6`  
		Last Modified: Tue, 12 Nov 2024 02:01:47 GMT  
		Size: 3.6 MB (3624282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2173d50d67655a4541bb752c8cf1780883a32c262fa42f3f5c9e4b87fac73e8`  
		Last Modified: Tue, 12 Nov 2024 02:01:46 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4f756123c12b9eaa7a93ccfe3b780cbcf092e929f9ff5f4667c5922f58c9d74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47338971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc16fc9c8b1a65e9e9a89190127af59766ba74b42b3f34cc5c944f9fdc46bd9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:895d07844c9c09054971f530ffd0794c329a785344079a01ce24e3d51727407e`  
		Last Modified: Tue, 12 Nov 2024 00:54:43 GMT  
		Size: 47.3 MB (47338750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f6cb02093ce689b2678764006cb5d389b5857d8358027e34813f8b8bd26465`  
		Last Modified: Tue, 12 Nov 2024 02:01:12 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1426c8143b02f291ef00665ab4b91179ef23f565725725ac1580446ec597b9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3d233218e765bd8dae4eeb13aeba7000ffbe0217a51177c1f3a1aca276b432`

```dockerfile
```

-	Layers:
	-	`sha256:93be4471c9a88c83e3cefbd65d0bb2b672404c036e655155e50d692e7abf8f04`  
		Last Modified: Tue, 12 Nov 2024 02:01:12 GMT  
		Size: 3.6 MB (3624482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb9e90ced14fabc6d4986a166710eb53afa3142a3eec1b98ea752711042498c3`  
		Last Modified: Tue, 12 Nov 2024 02:01:11 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:7ccfdb8d85d42e67dcf0d0a777b2c4bf3e97670cd7d95a39c447c0f14e687ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45150787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9304d143ce8175cc899eb289e00dcc6e0dde7546381aa7ca1652f31fb289ca77`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacb9abaacbf1d7ddc31870e63c90f91deeb7992cbecb0d83984166aea54bb51`  
		Last Modified: Tue, 12 Nov 2024 02:19:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ac3498ec91d227c3bb1de1357ea51db44140c7eee1cdc7359736f4d4cbc59a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5e485aa11bb73dcd85f3c78cf6ccb33957a64947ddb11c9d7142aa4dbacffc`

```dockerfile
```

-	Layers:
	-	`sha256:ef81dec41d35f84bdad5b26c271b4f46f33bf85a09085ed96a8768106daab793`  
		Last Modified: Tue, 12 Nov 2024 02:19:53 GMT  
		Size: 3.6 MB (3626460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bfae01325cf4f241363baeb8c2456d7e8cd67e5615bd4b97446fd887c806d65`  
		Last Modified: Tue, 12 Nov 2024 02:19:53 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b226cf16a63b057f5b373f64b6c688fb83fabff06868db911ef0c4b1e0b5068d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49587426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca8790503ad28423cb6f9666e7f98ba711cc824bed4facf93d1d4b9271275ae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c809fd028bc4c536cf538904fdd90eb7d84e7d11ae9a2d461e89e2687288bc36`  
		Last Modified: Tue, 12 Nov 2024 02:21:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:317a0bb9de231e92b3c6d5ec8e1ac263ed4d0e9456bb233fc75b10e3014f8474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d810490258f5a1fdf16a2c50046e43b41e14d12030ac19355c5f8548c7888eb9`

```dockerfile
```

-	Layers:
	-	`sha256:77f0e540bceeb9da29a6629287dc930f59ab007205721c985e513ab772642eed`  
		Last Modified: Tue, 12 Nov 2024 02:21:53 GMT  
		Size: 3.6 MB (3624496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9783bda289f874c6f3b0e72c930228071f306caf88b5065c83f8197a224fde3e`  
		Last Modified: Tue, 12 Nov 2024 02:21:52 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:832309683672fff4b64ea610893bdff9e30aec235ef04d2da9bcee2229c402da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50577272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e6d7d4c93cc850dc0313f767a0488162dd0cc8dd58632a9adabab6cbbd9c62`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2874a19de00923c5d4f3572480e03fb1a5b86a0704401c6b0d1ee7e21f9ec57d`  
		Last Modified: Tue, 12 Nov 2024 02:01:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e946f0578edc88d158500906232e62127e9f70e6c2d8f7e7da57243f29fab31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a5ef8f031d375d7df39d7282632ae57662cc3e2aa97ea5591fe02d43b6e153`

```dockerfile
```

-	Layers:
	-	`sha256:3efac3bc9cf2cab26a0035d4d8051051ac396e9dd344961e53ea24918a25f531`  
		Last Modified: Tue, 12 Nov 2024 02:01:47 GMT  
		Size: 3.6 MB (3621442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:489b9686e10f086938ce07b1201b82c7c9377cb6807cdcd384f445a1064e671b`  
		Last Modified: Tue, 12 Nov 2024 02:01:47 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:0fe1702638c2ec07257db9cf349e77fdcf7ea4c9d52e676680386f9fcdd9991a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49559405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62950a3d34cf3843f382497446c94f59d9337b560f7c392575a7b75d7d805aab`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:17191dc8a469e4ef93330c5c8402fa0c0761218a5fa02ad2db7b34508d0e995c`  
		Last Modified: Tue, 12 Nov 2024 00:57:16 GMT  
		Size: 49.6 MB (49559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23b15d2dc06385b29047c47f0a9ce01dcabb0ca88adc40aa4e885fb4f850a87`  
		Last Modified: Tue, 12 Nov 2024 02:02:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6a54fedb18ee59be45da5f2c702655da406f461e3d34ac6d7cced517a6615593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e8af4184cc508f1dc10feb192d02b3c4a3f708b932bafbd7c410a83ba199db`

```dockerfile
```

-	Layers:
	-	`sha256:1ce3010e42efcdc4f98dceb230cd986ca02bdb4f314d5e8526e36c0e17d052c4`  
		Last Modified: Tue, 12 Nov 2024 02:02:23 GMT  
		Size: 5.7 KB (5671 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:1dc2212c00534d5f49f682f51f6896a719e897e88e6d55f804480fdf1415fb44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53555496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb36e3485b9e8226bb9bf9891bb61fd80b602603686a2765e5839a34548a5db`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aea661fdabc2a77fdbade169e1651d8dfa79219e9dd1196b0931af7473343f1`  
		Last Modified: Tue, 12 Nov 2024 02:21:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bf17582d682a0662d96efba10dde7ff3b0954085a8be64de67db3e378f5b25bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5673aa3f3ee8086c01263b87b198595aae3df5a759c85e7dc636e5febbe8770e`

```dockerfile
```

-	Layers:
	-	`sha256:65b3882066c59ca5857bb181d2f053214e9c468319dfa5dbb28ee6e88fbeb396`  
		Last Modified: Tue, 12 Nov 2024 02:21:48 GMT  
		Size: 3.6 MB (3628541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7764bd97343905333cec2aba9a6e3137eaac29e042116afb85a7d04a185f9cbf`  
		Last Modified: Tue, 12 Nov 2024 02:21:47 GMT  
		Size: 5.9 KB (5873 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:7633dbaf76edd6577422bcabf3a6d9219263332e3ecbb426d6fe751406ed0bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47938912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15758e9c9a280d320d9ceda633d119d3a9288883d23094b8e546c4c6ab0026ff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916f15721d0adcec3f1c4147e5501ead4e55c8bfb5983fc52da1eacac05fd08e`  
		Last Modified: Tue, 12 Nov 2024 02:20:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:28bb2ad766da02bb18883f3caf4d307aed2eb0878da3545db682017aa22ba437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91d212f05efc0b857c85e13a98fa4abdec12510e1f94717e1df57a063f7a062`

```dockerfile
```

-	Layers:
	-	`sha256:b26f712f9f94ec0f446e8b67eadf430933afb55952acf8beb066779cd2969054`  
		Last Modified: Tue, 12 Nov 2024 02:20:26 GMT  
		Size: 3.6 MB (3624013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e068a58d50404bf897920b5a0c85d024e2ff87e010ba5bae09b8e6c770a1970`  
		Last Modified: Tue, 12 Nov 2024 02:20:26 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json
