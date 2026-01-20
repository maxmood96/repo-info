## `debian:rc-buggy`

```console
$ docker pull debian@sha256:ef9d0706209afb99784a07830910c9a44daf78b4f8b746e2f0215a0804b36b1e
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
$ docker pull debian@sha256:6f6733b0c923e0135f82bd2bb2c836ebf3148606acade01df8817b70201db16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48842174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09a4d0083397fe1ca30300e9cc5f0fffc72ef8c7f41f6fac615a72a4e767a09`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 01:16:44 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:b2184fb6462644b6acf50283df065d3d00ff827c80b1fe7de520944b5c1333b4`  
		Last Modified: Tue, 13 Jan 2026 00:42:32 GMT  
		Size: 48.8 MB (48841950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238cda1746df37b6ad30c1205373da5ef9794065ecbfd2707ff37d749053a59f`  
		Last Modified: Tue, 13 Jan 2026 01:16:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:3f4ac857c011c498150bc23d16a6f38cb9c550dbbda017341581a0654125008d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b35796e4d3b22ee45d578407c59af0f9ba10449d4655b7bf86db86111e63f5`

```dockerfile
```

-	Layers:
	-	`sha256:db006d01a655d0588321f2b222fae3dc6ca7a16a3d35f4a510f221f5ea63268a`  
		Last Modified: Tue, 13 Jan 2026 01:16:51 GMT  
		Size: 3.1 MB (3143132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b63ea18bb348a3375db4b5e245d8a822e0d7752a928b59b0ae6c0db98e11b281`  
		Last Modified: Tue, 13 Jan 2026 04:26:15 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:32 GMT  
		Size: 45.1 MB (45124955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4364015b83d4ed7b814b390d3fe4eadb29a69d486be30d2621b894934d17e165`  
		Last Modified: Tue, 13 Jan 2026 01:19:32 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:26:19 GMT  
		Size: 3.1 MB (3144508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf0af063a946f5e6845033d060248b6f1e18c6b777dc044d07bae0fc52a7082d`  
		Last Modified: Tue, 13 Jan 2026 04:26:20 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:16 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:26:24 GMT  
		Size: 3.1 MB (3143985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f95804aec5e2d96e4cf05a8ff224b654ebf93295794e60780bd340542d114e`  
		Last Modified: Tue, 13 Jan 2026 04:26:25 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.9 MB (49943816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8008f64b189a87d4290abb9bd7eb8ffc6689adb6c8a763524369e4cc41c6f6e0`  
		Last Modified: Tue, 13 Jan 2026 01:17:57 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:26:29 GMT  
		Size: 3.1 MB (3140331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b640e3b056d2e0ca3fe7bbd75b29c562d1487a53b3889427e1b193123ff85b`  
		Last Modified: Tue, 13 Jan 2026 01:17:51 GMT  
		Size: 6.0 KB (6034 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:35a371c774511c0eb980bbdc041cf11bd6b03ba943b41fe1e191bfdd7a1d9084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53525660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abdf3211451fb5a0601e9dd7c7e5318ffaeaf8a276c3c5a105bdb981052e28dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 23:27:18 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:3fc9cd4fe16c3d17cfa9014c31678a58aad75101c0db66189ea08efe999c1a84`  
		Last Modified: Tue, 13 Jan 2026 23:17:59 GMT  
		Size: 53.5 MB (53525434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec1b2a61af2b05c42115e7ee4b997d0558480dbd8d3b6e743622b05a1680460`  
		Last Modified: Tue, 13 Jan 2026 23:27:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:cedd3c87891ca8a959696cd57d7aff71f1eb24b1f7e143efbaff8a2a434891ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425f7616f8396ec77fa233ed30bfbf4229cbd8266a9c9d8d2c5f4b9f96e95664`

```dockerfile
```

-	Layers:
	-	`sha256:5337c65c813dff7494155e1ccac2371d21da8448cd9604df6eb903fcf64c1c7b`  
		Last Modified: Tue, 13 Jan 2026 23:27:35 GMT  
		Size: 3.1 MB (3146641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f213daa7508106219209ec7f42a1f45a6a9e4274bdf07f2ca9da62a704d5833`  
		Last Modified: Wed, 14 Jan 2026 01:24:35 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:04:34 GMT  
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
		Last Modified: Wed, 14 Jan 2026 07:24:28 GMT  
		Size: 3.1 MB (3134636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92cc42e916d1d837dd2cb6d59554a6bffc1d151f3a9208bae946f36883d502d5`  
		Last Modified: Wed, 14 Jan 2026 04:14:04 GMT  
		Size: 6.1 KB (6088 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:469dd654782b02839750d19909da4c8fa52af78a3f568603c8089f0cfe4e3a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48388856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5652d6d9d3f00ad301b50111c1eb926f6f02f15c2c61424dea2804503585d9cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 01:16:08 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:1e9a1f6e22461ab2a7c3b148cd7fd0131848ded4c904183b11402001b4c02c1f`  
		Last Modified: Tue, 13 Jan 2026 00:40:59 GMT  
		Size: 48.4 MB (48388631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d11b535d86bf19d19af6c9147967e5d763dd55e79e40f663c9cd590798c4291`  
		Last Modified: Tue, 13 Jan 2026 01:16:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:26bc89b3c73cdf5f537fac59c45fd24fd2ac5b22d6705b794d3a1373afd3490e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af12639b988dc277f21569e49bc27b5c7f269339c1e1d05fe2343b54dceefa4`

```dockerfile
```

-	Layers:
	-	`sha256:f75248dab1786ccf066da288c88d4dffa593ebe7e384b57c5c8b2350bb595141`  
		Last Modified: Tue, 13 Jan 2026 04:26:36 GMT  
		Size: 3.1 MB (3144581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c5c3aa5dd5d923bb587e5ae59a4d380ff7bfd102ee4fabfea35d04c3a2ec613`  
		Last Modified: Tue, 13 Jan 2026 04:26:37 GMT  
		Size: 6.1 KB (6056 bytes)  
		MIME: application/vnd.in-toto+json
