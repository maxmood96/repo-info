## `debian:experimental-20251103`

```console
$ docker pull debian@sha256:eb13eedc2e04126f74debb3f5dd50bff5b70ea053aa23b71079e6fb853f32c2e
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

### `debian:experimental-20251103` - linux; amd64

```console
$ docker pull debian@sha256:abe77d4b9bd332ae90755ff840c1a71010855ce842bec926793e5f33463560a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48485863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2a70fc4fefcb61d2b03a8ad1b0a3ef9f23e7193aeb450ea3a05a01cc37911b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1762202650'
# Tue, 04 Nov 2025 04:03:19 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:7a726d77a015ad71107356506f94f5a87e9e8aa9fd6057716048e3243a263cba`  
		Last Modified: Tue, 04 Nov 2025 00:13:32 GMT  
		Size: 48.5 MB (48485642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5aaf1cc5fe913601f1b04d7404c458e097d231063bbd59db6161d2f1ac2a940`  
		Last Modified: Tue, 04 Nov 2025 04:03:32 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251103` - unknown; unknown

```console
$ docker pull debian@sha256:182d242a7737d490ca1b9d17aa947ce8ddb28ba31b8f3a137c4e8e04ad5b8102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3135960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4551d4afc1b0c25c229f257b5e022b525e49396b3bcd6ffeeb020a14fe08296`

```dockerfile
```

-	Layers:
	-	`sha256:2e6d7d83671cd815b5daa1256cce97b7e854bef014b69a1a46bc7bfdb5e15496`  
		Last Modified: Tue, 04 Nov 2025 10:25:00 GMT  
		Size: 3.1 MB (3129859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83a69ed9658c7215d938b09f261398bda75aae4a7101d82ae3cf1f3ab1f981b4`  
		Last Modified: Tue, 04 Nov 2025 10:25:01 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20251103` - linux; arm variant v7

```console
$ docker pull debian@sha256:05f56617f604bccbfb551b3f5edbbae158f8801fb196f8a017ef6184b68e8ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44990857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2c634615fc87202fc64e5270e25c41f84f8c14561d3bc0ba54583389e581c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1762202650'
# Tue, 04 Nov 2025 02:05:15 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:6e2dedc4b95a0ec190d73937c2dc8401c0c57aecb27703eebb3e000d6f438e88`  
		Last Modified: Tue, 04 Nov 2025 00:13:39 GMT  
		Size: 45.0 MB (44990637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac17041a65a531bb90844875fd501929ab8667d7e87704597194aeb65a0ca477`  
		Last Modified: Tue, 04 Nov 2025 02:05:28 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251103` - unknown; unknown

```console
$ docker pull debian@sha256:5e251e83b720ce2ca1601d62bdd5f2765a14d2e68459666b0da02932fcc3b96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3137400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19dc541d40c4717b870f122afba6ee92fdc73cf40db1c97ad29226feb28e8b7`

```dockerfile
```

-	Layers:
	-	`sha256:0c7b14147e66048edbf3e39c2b7c60259505b27976b4bf8a4b93e7c292a4b4ce`  
		Last Modified: Tue, 04 Nov 2025 10:25:06 GMT  
		Size: 3.1 MB (3131235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8adcbc12a738067d06c50f603617bb4e793cb3e7e462f411bc634815f88fb2f6`  
		Last Modified: Tue, 04 Nov 2025 10:25:06 GMT  
		Size: 6.2 KB (6165 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20251103` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:116b115ca8afb33610ee483e320e9b2d9523d527321788d8754701f872e506a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48586241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f6eba7ef6dbb1b06c89185b03b48ecf08d5f0644cd3d6480744c2ec1151075`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1762202650'
# Tue, 04 Nov 2025 01:18:20 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:6bfc3d21e1f3dbba0c6e0fc2dffaba306990257eb19ba8842445799e017db694`  
		Last Modified: Tue, 04 Nov 2025 00:13:49 GMT  
		Size: 48.6 MB (48586020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aa534d0ae286e6b350c05b82a774d74e13ccdbb3aafd235af0a01c702366fc`  
		Last Modified: Tue, 04 Nov 2025 01:18:33 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251103` - unknown; unknown

```console
$ docker pull debian@sha256:a300c06c0f1a2314437574864a26dcbcc8ee88424efc34ec0814476299d54be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a20c3d8faa9a174bc2dbb2afca2e8b1da20634296f56c7de343ff7b6b420347`

```dockerfile
```

-	Layers:
	-	`sha256:e383c0b9faae84fd90756f29812e7d30bd8e794455d05f873ed8488468fa70de`  
		Last Modified: Tue, 04 Nov 2025 10:25:10 GMT  
		Size: 3.1 MB (3130712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c8425dc464046eef5e27d75bcafe2e9f5045217b854db31c1d4678e80650086`  
		Last Modified: Tue, 04 Nov 2025 10:25:11 GMT  
		Size: 6.2 KB (6181 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20251103` - linux; 386

```console
$ docker pull debian@sha256:54ae422713b8e42b3982fb4d506f8d99d7ce080fc4eea360d74f55f0e6b719a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49809230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83ea58e585df7f29f89ec98ed391facffd04d7aa6fe71ac0f568d5be3fa8fcf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1762202650'
# Tue, 04 Nov 2025 01:18:06 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:81e1d2ff7f85522b0fb68382107c88c852290825649f19e628abb3ed45454b21`  
		Last Modified: Tue, 04 Nov 2025 00:14:03 GMT  
		Size: 49.8 MB (49809009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc53064de1bd54080a74c8ba7c778d9332042434e4de2215d0611eb1babc8305`  
		Last Modified: Tue, 04 Nov 2025 01:18:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251103` - unknown; unknown

```console
$ docker pull debian@sha256:2332e748dad7d9ec3cc5a2513bc89863aed8002ba8712f175c9499983171586d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbee020bfea647e77353e3c9a289d14b3a7450628f8e2554303f248036d2587a`

```dockerfile
```

-	Layers:
	-	`sha256:77c67d621dc5f172c233daa391fa807bbbc535fa22b9b7e0bcc098d2aeeaae45`  
		Last Modified: Tue, 04 Nov 2025 10:25:14 GMT  
		Size: 3.1 MB (3127063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6129dad22873c24973765a15dcbf7f3f1abf726c5e5a8f85ea9f5da014306bf8`  
		Last Modified: Tue, 04 Nov 2025 10:25:15 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20251103` - linux; ppc64le

```console
$ docker pull debian@sha256:2589c42184ebf1cb0354ee1a47ecb8c2115b9a064a5677a4eac8783cd2ebb8b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53318223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f597b3ae10b5d691274f91d43b765dda9be1618844b8c262c34af458e7209e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1762202650'
# Tue, 04 Nov 2025 01:20:44 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:895ccc77361020669ee6b7ccc47221bead830a2124c37e9918f00c10dd75df8a`  
		Last Modified: Tue, 04 Nov 2025 00:21:33 GMT  
		Size: 53.3 MB (53318002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2382e663ce46dd030681311d273932bce2bad97e80bd5b82ed3ece05ef2413b6`  
		Last Modified: Tue, 04 Nov 2025 01:21:07 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251103` - unknown; unknown

```console
$ docker pull debian@sha256:045ec2b4e230e722011c6c4e61f3ea21f5f5b3f1a05a83c8b6b0a3da991d6c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3139487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3a32b8665ba15e81dafa578cfedba862d7eeb434176db0cb41c1afec114e0f`

```dockerfile
```

-	Layers:
	-	`sha256:5c233f341de60562a6b14641ed709303def93b62bd0e81b5e748974ec475cd77`  
		Last Modified: Tue, 04 Nov 2025 10:25:19 GMT  
		Size: 3.1 MB (3133354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1c8839d7ea65ebe9b67ac15114e0c111581dfd5c2da592520ae924a8a8fb68c`  
		Last Modified: Tue, 04 Nov 2025 10:25:20 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20251103` - linux; riscv64

```console
$ docker pull debian@sha256:dbc99e94eaf2916f4b07e620497663044f28cd329cd52bdcfb1c99c8cca083b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46794483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900d851b92f21bc27aba41df6a5c037631e5069dbbf5752c3936bce6d3afe30f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1762202650'
# Tue, 04 Nov 2025 01:25:16 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:5ce854dd87e3899c0d57c1835e481664836dfe75977d3564c7675f6f1ba1ced9`  
		Last Modified: Tue, 04 Nov 2025 00:31:19 GMT  
		Size: 46.8 MB (46794263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961e6869944b29d41dab954188f29c3f15e94e9477d231a1d6eac2e602035cfe`  
		Last Modified: Tue, 04 Nov 2025 01:26:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251103` - unknown; unknown

```console
$ docker pull debian@sha256:49a4a583a4dbba391386136b0bdac4d1bfe1544011d52cd17c789c330f11fbf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b6da0c16a8f6ac775eea9330c00cb029c8e0745fccf92537e43e9d697d6982`

```dockerfile
```

-	Layers:
	-	`sha256:9829ff021fac7e623a1c72c7711e52f5176a0c2ec8110731589160d5e2fef698`  
		Last Modified: Tue, 04 Nov 2025 07:27:53 GMT  
		Size: 3.1 MB (3122164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fd6cb624db078091ba0d61cfb54b87794f69e1e17d4a3984938fae73040f97f`  
		Last Modified: Tue, 04 Nov 2025 07:27:53 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20251103` - linux; s390x

```console
$ docker pull debian@sha256:a6ce86f16b421c71139e6a1314502a19c1daa7e03f98571f914d1312f033e029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48346667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818202d2009e4f0c76a3297010d897618e96066984269c523266475aebbea195`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1762202650'
# Tue, 04 Nov 2025 06:44:07 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:b654a051e447a9448bcbec96e305a6712fc268fe33ed0bdddeef8d9d7a2a13ad`  
		Last Modified: Tue, 04 Nov 2025 00:21:03 GMT  
		Size: 48.3 MB (48346446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e93623c87818d47fded019442cfc8aa2d78ec1e42accea3f52a3bf6bc9d9e1`  
		Last Modified: Tue, 04 Nov 2025 06:44:21 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251103` - unknown; unknown

```console
$ docker pull debian@sha256:52bfee544c923dd739cbb42b808844a1892f17d90114ff23455137e60d358957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3137409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9650596b942f9b01d2bdb938917edd3f31dd56f548f23dff5d539d0aa88e20`

```dockerfile
```

-	Layers:
	-	`sha256:7314c2bce0a411f9218ea01ffed8fcf953ecd86731248c787ac80f3df117a399`  
		Last Modified: Tue, 04 Nov 2025 10:25:28 GMT  
		Size: 3.1 MB (3131308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da3bafd2f66f7f25a0d7a9d88fd9c98fb007a2cc071bab139c59d9d8800340d1`  
		Last Modified: Tue, 04 Nov 2025 10:25:29 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json
