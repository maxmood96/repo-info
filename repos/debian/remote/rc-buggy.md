## `debian:rc-buggy`

```console
$ docker pull debian@sha256:4f625fa08c3d94f90282da57ba5c17130b79a8dde07a0be36565ad1dfe2fff4f
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:de1044b51e1227216b6b6fd9fbbc05c742e35934080f0e477fd5309818b2bf8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48654927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfbbd5ad400fcbc0317a18a4398290b41e926d06062aac98329e7219fb30600`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:16:26 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:e5dc831051d738f5c1db4254dde56feb7c9e75e136e23995d896f1b6e1ba752f`  
		Last Modified: Tue, 03 Feb 2026 01:15:47 GMT  
		Size: 48.7 MB (48654703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99d954ecb5377fad694ee88e14ab59160fbb06d41a4611647250ef142ed8476`  
		Last Modified: Tue, 03 Feb 2026 02:16:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:005198b60c8cfed59f7f55066174bff364e9568dd76737cf6c2be681e96ce540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d885f701d38dce5547b8a68f8d7162a1c7060b0c401cfdc2ff09f6b5027438`

```dockerfile
```

-	Layers:
	-	`sha256:2c157522415cfbb7f6fd08f2aa1637169a016bf7f7aed48c8e1bdff8f995c473`  
		Last Modified: Tue, 03 Feb 2026 02:16:32 GMT  
		Size: 3.2 MB (3150455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73335ac57731f3724ddbb4b36defcbef0651aa5da400971d7037aca4394393f0`  
		Last Modified: Tue, 03 Feb 2026 02:16:32 GMT  
		Size: 6.1 KB (6056 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:4b94bbc4528de55ab2716bd751d56d4a9cc5c7841984cd06f5b44e229207258d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45125180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a738d4ecda070424d9ba386b0c3a192d4806372c150d82d2bd53ce5dba1154ec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 01:19:21 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:8b7f582255e583d8176a24d49b58b25ef2ab11e30f1f26c271dc02b42befa1ec`  
		Last Modified: Tue, 13 Jan 2026 00:42:25 GMT  
		Size: 45.1 MB (45124955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4364015b83d4ed7b814b390d3fe4eadb29a69d486be30d2621b894934d17e165`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:6f152d76057e21831705ec12e7be3410244d2dd372d412447ccc853dfc77178b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3e98edcbafe9abfd7f00839f559ff3fa231c195d2b09e4a00778c331024192`

```dockerfile
```

-	Layers:
	-	`sha256:8d361000b201c541762adbd40d323d114941cd561553c3d211c82c66fb320285`  
		Last Modified: Tue, 13 Jan 2026 01:19:28 GMT  
		Size: 3.1 MB (3144508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf0af063a946f5e6845033d060248b6f1e18c6b777dc044d07bae0fc52a7082d`  
		Last Modified: Tue, 13 Jan 2026 01:19:28 GMT  
		Size: 6.1 KB (6120 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:bb82c9e42dc6ba48e02c3c97940c01d97249134a5e334a4dd44c8d8458590e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48824943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33514ce4f108c467eee21f66f18af43dba760f0d77bf5321ba587d6b761f1dac`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 01:17:32 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:6d947e77c03f512510d8bed1eff4f80727f54732f6ae212199524bdf89493609`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 48.8 MB (48824718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458daca80ea8519490c804650eb1cff9d63cf1dc18721a99fdc4393637b9ffd7`  
		Last Modified: Tue, 13 Jan 2026 01:17:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:f8656e29bc4617685b4ca40a19fe70c12c61f061eff688bdbc4f9e9fa93bb6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fef67b69f51e1ab330d3c2ffbd5562dfc75fed8de2fea4ac252d63e235b45df`

```dockerfile
```

-	Layers:
	-	`sha256:ab1499a7d1f882046baebbc476026da37cf50a80c2ff127d536ec982e090a110`  
		Last Modified: Tue, 13 Jan 2026 01:17:39 GMT  
		Size: 3.1 MB (3143985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f95804aec5e2d96e4cf05a8ff224b654ebf93295794e60780bd340542d114e`  
		Last Modified: Tue, 13 Jan 2026 01:17:39 GMT  
		Size: 6.1 KB (6135 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:e4a68e2fdd42612ce500eff5749b9f696c80cc61180129e097527e7382de5e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49944040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df5f38c26b9982c232e655e0d03e2cdc44d032286fd08c4ce98453a6e8638f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 01:17:44 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:621ee2827046628793df0c5176988fc0eef90eb94ab1b862f17e074ba6064e3d`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 49.9 MB (49943816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8008f64b189a87d4290abb9bd7eb8ffc6689adb6c8a763524369e4cc41c6f6e0`  
		Last Modified: Tue, 13 Jan 2026 01:17:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:687deea13da4e4a86e6e2454e28feaee13854adf17ce67e3000085c6f1c20ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c901c9cfe9e590a4a9aa5d1a6c515d8c4ec48101cdc3c1f107a19020000cb9`

```dockerfile
```

-	Layers:
	-	`sha256:f405ba7bc1f19a7e0cee0b516946b7cf4a04912ad3d97dec058d8d0fafd23309`  
		Last Modified: Tue, 13 Jan 2026 01:17:51 GMT  
		Size: 3.1 MB (3140331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b640e3b056d2e0ca3fe7bbd75b29c562d1487a53b3889427e1b193123ff85b`  
		Last Modified: Tue, 13 Jan 2026 01:17:51 GMT  
		Size: 6.0 KB (6034 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:88aa7f84199979b63a1503c93f3754d33f7b0941133d6d331613ed5238ac96a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53584747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649511d2cbde1329ea56a710304bafd71257179c857e3df3a3cbcb3c4a05ecf7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:15:54 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:73480cc26c615330eccab26ce34bdcf83d5889a7e09a86213699bf4e4f64bc74`  
		Last Modified: Tue, 03 Feb 2026 01:14:38 GMT  
		Size: 53.6 MB (53584520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77de559c191148b9cdbe32045707d2f0d570c3b0aaf6b058e68b266223a39d94`  
		Last Modified: Tue, 03 Feb 2026 02:16:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:07c26ae71a24580ae0d32388ad3740f8cd8023f4e2dee9b5b49ac1aebadd947b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3160070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059ab8e0edd08ac971a13c7db65f01d9f95c9469284d58b1a9a0bf243608fb7f`

```dockerfile
```

-	Layers:
	-	`sha256:23aab2bcf96b19b37cbbd38e9dbeae334e15d792d635dba3b2d78c14db51c5b8`  
		Last Modified: Tue, 03 Feb 2026 02:16:10 GMT  
		Size: 3.2 MB (3153982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77ec91e073e4e01de43a8c6a0c15a887bc19e434add0cfc9e1a07884dd0b2160`  
		Last Modified: Tue, 03 Feb 2026 02:16:09 GMT  
		Size: 6.1 KB (6088 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:1f68b880d1bbdf03ff1b34aa7e72a54e50a0b3619ec404072dbe2af767e2a172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46856977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a412d27a8df43eddb3f988280ed8e36e1c71505a2955c88708fbb6908bac7d7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1768176000'
# Wed, 14 Jan 2026 04:13:10 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:3f1a05ef5786076b47fcd681b3f4ff2ab26c932b463a6ab7c885cf7684b1355a`  
		Last Modified: Tue, 13 Jan 2026 00:55:56 GMT  
		Size: 46.9 MB (46856753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f98fdaa99731cf7dbca7c09d326229882d57b4b385cbbfa855708f81e33d4e`  
		Last Modified: Wed, 14 Jan 2026 04:14:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:e640f0fea8a9d939da840b7f67a394cb06f44a59416ae474e8cb855f40370fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488e456510dc205e4ae0bde1fd310e46026dbce5edd0b54232487a3109f9d86c`

```dockerfile
```

-	Layers:
	-	`sha256:19269312e4aa867ffb098f29fbeb5f0322d35a722f9a4bf9754908b8e6febb91`  
		Last Modified: Wed, 14 Jan 2026 04:14:05 GMT  
		Size: 3.1 MB (3134636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92cc42e916d1d837dd2cb6d59554a6bffc1d151f3a9208bae946f36883d502d5`  
		Last Modified: Wed, 14 Jan 2026 04:14:04 GMT  
		Size: 6.1 KB (6088 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:80814439c8ddf011b7dca4ea3a34f9bfe6f5a230d1f135bc4884266602449fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48421422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bfbc52cf6c9077f03a0abd1dc1918c8715c7ff7c69d8ee1ac07557e29c9a76`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:15:47 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:3bfb68c2648b1088debcce6bc605d7ea6709b6f129c9ce647bf0a7c385d8350b`  
		Last Modified: Tue, 03 Feb 2026 01:13:18 GMT  
		Size: 48.4 MB (48421195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ed085441c7ed3ab9b413d2ec0139304cc5e823b0919848d1ca51d86e152a40`  
		Last Modified: Tue, 03 Feb 2026 02:15:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:6fa2a8bb599af27a37e0fa05af82474f1cf0ae276293c6199e349dc5933dba32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640668f32f42bdaafb7d9b1af1d1edb1e5c8c88942039dc2bf9eaa2a37c22037`

```dockerfile
```

-	Layers:
	-	`sha256:07947a60a122c6220993ad5eb1a2f3f980973319f4f738a39ca88d4368efacc8`  
		Last Modified: Tue, 03 Feb 2026 02:15:57 GMT  
		Size: 3.2 MB (3151904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744ba12348a3143072f2a5e7036016226dba31cba6a957ab622c15052f61ba1e`  
		Last Modified: Tue, 03 Feb 2026 02:15:56 GMT  
		Size: 6.1 KB (6056 bytes)  
		MIME: application/vnd.in-toto+json
