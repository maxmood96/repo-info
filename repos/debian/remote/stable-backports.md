## `debian:stable-backports`

```console
$ docker pull debian@sha256:da7eec5975e4359c5f7368a4b3ed1e690796340ddf61a673caf09c1525f4d17e
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:adc358414278341afbae62d772b5ade0f25d4f4517753fce4252acc3e2f4f5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49317342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4717c4180f8a2debedf876bfa23f91780acb2f6b3077b59e560f00069dafcec4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1781049600'
# Thu, 11 Jun 2026 00:15:53 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:76c1b568d783b0a559a2770aaeab50f23c7b7f3dd90364c64fba1639cd29c86d`  
		Last Modified: Wed, 10 Jun 2026 23:40:43 GMT  
		Size: 49.3 MB (49317120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b6ff084a7483c4db14a2315ae6dec0128b37205730bd5629f6df1df7754276`  
		Last Modified: Thu, 11 Jun 2026 00:15:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:998d0159a9ac6d987a20681f3a0b73d22f324985381540a99f3afbfae91a8f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a245ae97f4b28d3dee6fbea8cd4f8aef313290c5aaf592909c7571b168b93d13`

```dockerfile
```

-	Layers:
	-	`sha256:d5ec64458f85e9794e908a5b75a7cae83f5aeffda6acf7e6de4d425246e43353`  
		Last Modified: Thu, 11 Jun 2026 00:16:00 GMT  
		Size: 3.2 MB (3170955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45350d579edc56a0a82bb6c7dc8cafa10006b95a4784afcaf0588288e36da56e`  
		Last Modified: Thu, 11 Jun 2026 00:16:00 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:bdb3faffa6b3c4a419fcac0dbb62e62313f6337120b3fea328f2cfb777067864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47495032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfba61f014d28092ff605eabaa7c18bc728552f62c3726eb6de2fee2b9a6bb2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1781049600'
# Thu, 11 Jun 2026 00:15:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bb365e18e4a59d04337d032f20a4472965f1e2eee516ab699795c01ba82765df`  
		Last Modified: Wed, 10 Jun 2026 23:39:14 GMT  
		Size: 47.5 MB (47494812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb88decfb9149bffbd421d315e137396534dfe725a8138bef468bdc211fe144`  
		Last Modified: Thu, 11 Jun 2026 00:15:51 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ab6a4003887923c302864d59c5094e8f21e0ed7973c28a4b681cc316376519f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1037c1e8e296d510f86a9977d79afe7d936542be942e949815e6ffbf83231abc`

```dockerfile
```

-	Layers:
	-	`sha256:a7f49de777203be76460497080dc08901281d27634604e3982702dce04ea730b`  
		Last Modified: Thu, 11 Jun 2026 00:15:51 GMT  
		Size: 3.2 MB (3173892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7115e252cad6943d6213bb718bdc5c6efcc9f46088e7420e825a9f9c92d61ce8`  
		Last Modified: Thu, 11 Jun 2026 00:15:51 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ff1825e7bb08e0f43b8e26c29f729bb722b51a8350b3b44efa611f85ecf7844a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45748861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a6508ae31f474c16f44a8c7a24961ccb46a2ddfb9c08fedfa2c521d383e2ff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1781049600'
# Thu, 11 Jun 2026 00:15:45 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1465566b8e00c1e1105244e8396fdd6c02b3b7747ce3bdbf2176503872c00e05`  
		Last Modified: Wed, 10 Jun 2026 23:43:10 GMT  
		Size: 45.7 MB (45748641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8017d91ca9b91e6d3a29caa200ebf154d02ae7f6d71a003111d0b6d1cd030a2`  
		Last Modified: Thu, 11 Jun 2026 00:15:52 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5184a3714f66748712f92f5118643c7690219e0928b85dfe4533e5cb071aa91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ebacbd723507ac5256554ff057e7171bfc8ed407f01177d5e79c153f2247a7`

```dockerfile
```

-	Layers:
	-	`sha256:522a4e02324f704fda58967dbabdc847ce488c89898998175008e150b9560e27`  
		Last Modified: Thu, 11 Jun 2026 00:15:52 GMT  
		Size: 3.2 MB (3172329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8163f66e6be8f00177a495404c5401b5c883d7413ecb6956eeb93b5b08b28278`  
		Last Modified: Thu, 11 Jun 2026 00:15:52 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:906fe8cca4086c0e155c64df90e0599fed8e7970b2cb5595d1ceaf3374935a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49678390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6580d03e174fd964bdf941f5b747852fce719d18d03921e56ff55237f924ee4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1781049600'
# Thu, 11 Jun 2026 00:14:53 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:982e76ff0ff5fd68cde264ba90670e342dd29a01ef9d0559a2e682f70d2053aa`  
		Last Modified: Wed, 10 Jun 2026 23:40:14 GMT  
		Size: 49.7 MB (49678170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3425d0203c3d7c78e54b94659f07d2ef5a91fc57ce63bf07b5a61b24b4dd586d`  
		Last Modified: Thu, 11 Jun 2026 00:15:00 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c94294aba4824646f9630da336a6df5a12c8987e76bd4c204914f153e2847a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66bd703657f176ee05f149c9d81f65ee2a60d05084de62e3bb9e7326474c641e`

```dockerfile
```

-	Layers:
	-	`sha256:6b0865deabae9f0a54bd86ab342d7a60cc5f5fc0f0dfc53f422634ed4ba4b273`  
		Last Modified: Thu, 11 Jun 2026 00:15:00 GMT  
		Size: 3.2 MB (3171799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e6b53c9af198ba80e74fa8fc470f829e00dbb03d248791024973cb02c0d67cd`  
		Last Modified: Thu, 11 Jun 2026 00:15:00 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:396ae33eb158d3d870bf2cc2a9ffd6314bd6606fd2fd5c4503e5f711de168693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50835786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4877bdb5d813f971dd86967bdb92f551a67d588d558a5fa0712baf931a496b0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1781049600'
# Thu, 11 Jun 2026 00:15:56 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:55ebfa52cf28986bedeb6101a1d106a70705e0d12484904e391becd5b957d026`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 50.8 MB (50835565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22270c558ab4c4d81be98c20664cef635cdf56bce995b7dfedeff1b7a7c424f9`  
		Last Modified: Thu, 11 Jun 2026 00:16:03 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0b54024dcedb186fe27aae5f4a2e582c5a21115f3fbb65bf16429b06628ca443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029afbe7be3a54e89ff84950558e0e34c626ff2e9ac59aac7fe02d576bb154fd`

```dockerfile
```

-	Layers:
	-	`sha256:fb8c03c494c3de7b5d4ee426e9c36be737a7922757e9457c199ff0ad76929a0b`  
		Last Modified: Thu, 11 Jun 2026 00:16:03 GMT  
		Size: 3.2 MB (3168157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250b4bbae7dfbb543e3f5862b2a255669429028645df8367301b90cc3e2e9e11`  
		Last Modified: Thu, 11 Jun 2026 00:16:03 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:635e0c7b37d5e9d36dae9ab0afdfdde4798ce55e1e9400af12a62f4b3075297a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53138162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038c62d35f91222405dee5b1acd76e693560bd2634440376346118f5ad704796`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1781049600'
# Thu, 11 Jun 2026 02:21:03 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b014062169c676fa63036f0ddd3c7cc400ee3e37e3e0583b12accddc4fbd3192`  
		Last Modified: Thu, 11 Jun 2026 00:23:41 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d333b9d92f58b8a70154d9d2f6bd22c63be1f560ae52bf1c4ec66db54155507`  
		Last Modified: Thu, 11 Jun 2026 02:21:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1a41c0f7f9d13f360bfd7abc9ac6864fd1f84961f69eba453d384e6745619ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ac3c4d6d74d6922440dca810c51c4c72eca36b97f536917c5ace4f2404ac3b`

```dockerfile
```

-	Layers:
	-	`sha256:c514d9dbc270da545bb8084744a56481c8ea5ab877bea76bb5280d2643836762`  
		Last Modified: Thu, 11 Jun 2026 02:21:15 GMT  
		Size: 3.2 MB (3174468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:734b631aab1d78588337384ede4056b9a976aaf252a70d6a4b5bbafa502bc921`  
		Last Modified: Thu, 11 Jun 2026 02:21:15 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:2e0e08497acd1ebb0cec21ac2db1cf99f531b283c10154fcf182265638a9c79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47802755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310c1230a94f0340140abf318c4961dca37aa7f0d418349a489f21fd53f606ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1781049600'
# Thu, 11 Jun 2026 22:08:26 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8e8587ba31c7d2366e168db6284a9bad01ffdd923354b652e256b3c1d990522a`  
		Last Modified: Thu, 11 Jun 2026 02:52:24 GMT  
		Size: 47.8 MB (47802535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df6665c8fb6a2355bc7de96b354f90774e09697016ce72a9cf9e76804661cb3`  
		Last Modified: Thu, 11 Jun 2026 22:09:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:58d86f2a29f89e9e52fa251af6d6fd7c07cca6685803c5342835bcf09ebf6541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4a4008ffdc3ffed6345b8de72eaa34c91ac31433a6b64b973a71f010f42352`

```dockerfile
```

-	Layers:
	-	`sha256:a71645650f65b9e132e1b466d325b8f63861dfbed80652098f6471eca23b3209`  
		Last Modified: Thu, 11 Jun 2026 22:09:21 GMT  
		Size: 3.2 MB (3163280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a4ab347d0852ac18d16e92fb8a29ff04a9a0b35fff88bdbc1559b1560bac523`  
		Last Modified: Thu, 11 Jun 2026 22:09:21 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:fabcae581c584e2612aa146754c182b29cc99cb7706dff595769d191d19a27df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49386121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a1d17496ae04d28f137575167446258e35950f1aaadd9df2632dc91e6e2059`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1781049600'
# Thu, 11 Jun 2026 00:14:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4a2784e11b34a218320514b554121259d990c7a63e9648bb109a9bb2fbe792c3`  
		Last Modified: Wed, 10 Jun 2026 23:42:05 GMT  
		Size: 49.4 MB (49385899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9647d2aaf8cca33b395e495745e44274628a49967e9c44d1cc018d0e46b1d53`  
		Last Modified: Thu, 11 Jun 2026 00:14:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8d921e1cca40b4c7496195de19f3defb646fd10f24d5adbdca2932dcbc037cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302e8ebc8e797ecc305eee6918a3b6620dd62cec1400f072336a4d36ecc6324b`

```dockerfile
```

-	Layers:
	-	`sha256:4fcf4d4a5b9a8f206169dd14da38bde83815e0e84166a54fbcc67be1ca05c463`  
		Last Modified: Thu, 11 Jun 2026 00:14:56 GMT  
		Size: 3.2 MB (3172402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7751e83e4061960543b9c73f32d76af53115aef5dc239001fb1f125d279b2516`  
		Last Modified: Thu, 11 Jun 2026 00:14:56 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
