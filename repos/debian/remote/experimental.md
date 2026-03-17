## `debian:experimental`

```console
$ docker pull debian@sha256:523440ffd5879fdb9f7a6d1c8687b6d2ebf28fb85be6569de2a0cb9536231070
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

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:35d8facf53da488ef01d303a59d76121e3f1ceb78c2f22900c4fc56c6a119405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48676696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f87e2f7440a9a60de66a4dc32d977c1c03a4064dbd5c5f85e2ae1030111a5ca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1773619200'
# Mon, 16 Mar 2026 22:16:10 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:cfc223668840e4554c4b291aec25d995636c5a89103c549d3691a5e614ea9ed0`  
		Last Modified: Mon, 16 Mar 2026 21:53:23 GMT  
		Size: 48.7 MB (48676476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149673f36b57452f7bb9211551dea4c692bf882333715e06ecd21969c8e0df0`  
		Last Modified: Mon, 16 Mar 2026 22:16:16 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:49fd6ce39cfea7777afba8c3129086ea194bc1a12c52a719670879ab5f073fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5216a26b1de944cbb398cf994ec35e99a18f4c06cfe84472cb2f8f702c5d11`

```dockerfile
```

-	Layers:
	-	`sha256:643b326d78ddce327ab57ec87e968e06edf8007353bd9e1cf9f8772643cb9b26`  
		Last Modified: Mon, 16 Mar 2026 22:16:16 GMT  
		Size: 3.1 MB (3143654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d08804d16c954afa76eec8fced83e46483b32349d000f9ea538e95179ab22e84`  
		Last Modified: Mon, 16 Mar 2026 22:16:16 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:7035c75786fffcf080b6da9b6924e840da5293b222853cd2f8f2f62d16d8cce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45603845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac4239beb7e3d9a271d3e445da9384c9a2cec91ae64d1ac913f3d4c1a7a4e92`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1773619200'
# Mon, 16 Mar 2026 22:17:12 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:09e5fd54319e994e5baec34bc03f8923753056949907de6b31f0ce3159b2ff4d`  
		Last Modified: Mon, 16 Mar 2026 21:53:28 GMT  
		Size: 45.6 MB (45603625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275f4cbd16e4902fb0a646e98d390d7adaffdb3683a7256a66fffee7428f0881`  
		Last Modified: Mon, 16 Mar 2026 22:17:18 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:53cfd75489d8194fa3737fd497a38913e95be0a2d9e4ff674bb65620493c5ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e88f102a204098ef7171051a43f8c45726818f4c6c2d0e507ca17052c2076e1`

```dockerfile
```

-	Layers:
	-	`sha256:87df22efbc76d82eb0ae8608b87f6b8a87aa22ec8d264e77fb51545b31caec9c`  
		Last Modified: Mon, 16 Mar 2026 22:17:18 GMT  
		Size: 3.1 MB (3145024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79178be528d9e682690ee4b5f2078b7c689f17ccba694933ed9d5055ed872810`  
		Last Modified: Mon, 16 Mar 2026 22:17:18 GMT  
		Size: 6.2 KB (6165 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e4bb934c814a1b0941ff9f8a90e6e9c1632e0c07942d6faf4523ab6be0a17b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48715401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7370614948ba08d37d09b5843051e34fc085d70d23c5c5d254e35cde78b6d3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1773619200'
# Mon, 16 Mar 2026 22:17:57 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:7fa31052ed8a124b0628f97e9fa73c8910c84f8de7f6377e87fc12cf50334c57`  
		Last Modified: Mon, 16 Mar 2026 21:53:07 GMT  
		Size: 48.7 MB (48715180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa68959fada88ce7b08f64641872705ed313f64c454941a484a60b86d35c9e6`  
		Last Modified: Mon, 16 Mar 2026 22:18:03 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:96dc7d36669450ac99d481445f8bf2859c1682151acf675fa88b58725edc9be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05081ecf90e5219795019aeaf4777e3662ab7aa0e0414b74c6ed3497f1fb109c`

```dockerfile
```

-	Layers:
	-	`sha256:b59921427fab3b7152b2bc4192ceb2821648c4184ce3d932b2293a8b44ad3ffd`  
		Last Modified: Mon, 16 Mar 2026 22:18:04 GMT  
		Size: 3.2 MB (3150432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:519b1e59ddc792972c908ce1eda2b664621be3cd3c6e82b82b25d40f789b20e5`  
		Last Modified: Mon, 16 Mar 2026 22:18:03 GMT  
		Size: 6.2 KB (6180 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:19dfba6424fa4fe68866c7f94d1911ee31b8d335b7d7c1912be6a245322773a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49948272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b644d42ffe92fc5737dbd7f09c9bb2586763aa7a706bf84bdc59342432be23c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1773619200'
# Mon, 16 Mar 2026 22:16:18 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:23bd81842bd2e41342eebf41cac5fd13309708f77e14c2493a81b4fa44d3d380`  
		Last Modified: Mon, 16 Mar 2026 21:53:41 GMT  
		Size: 49.9 MB (49948053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a98d88d01756894869e6afc1e598baabf78c38de99eb135153cc65a9f7289fd`  
		Last Modified: Mon, 16 Mar 2026 22:16:24 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:bcbef68a4ef2b33228fb93cbe00622145d725c484d3b21f4f36cfff138b5e8d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0109032bc17dbaab4897387bbcdd6716acea294fac6991b9c601d741fbb582dd`

```dockerfile
```

-	Layers:
	-	`sha256:c183eb792d1f325ae294f06a9f0cc675ad4af30f6faafa67bc38056769277275`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 3.1 MB (3140852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ab2fabaa0d7b23058907c4c6bee2d063c9b1aa73368bc146c93cec23f66201`  
		Last Modified: Mon, 16 Mar 2026 22:16:24 GMT  
		Size: 6.1 KB (6078 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:746548af2b0ac94f5cf5fd27a858af22ecb16fe15273a4b07afa6bb19e6cb470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53933892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb9f5b62e1f4cdfc8fd16f28bc273ee26057b3a6013a62954010aecea2e3f63`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1773619200'
# Mon, 16 Mar 2026 23:35:47 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:b5b3abb54c5cab76595727b3215e0e22a8e84b1ae57f88ccc753da6dd21d587e`  
		Last Modified: Mon, 16 Mar 2026 21:56:23 GMT  
		Size: 53.9 MB (53933671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46690670eec55d6bea6d68a52ab8f21e8b794ce1ae806cf7b3893fac043d7e40`  
		Last Modified: Mon, 16 Mar 2026 23:36:06 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:e9a2f7f6409d78496aa1ac7bba23b2ca61f0c8f9e712ff76dbfecbdef5f32233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bd142097012e3942e62d64d9183fdbe392d810357990eff9e9c45734bf7458`

```dockerfile
```

-	Layers:
	-	`sha256:185a574a997b52adfd056debe9adc92f63f4727cf86f462f5f9906d93239ca80`  
		Last Modified: Mon, 16 Mar 2026 23:36:06 GMT  
		Size: 3.1 MB (3147159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9427519fa00e894a890e7589c53587f619f1c9b42c112b315fd6b305459fddf`  
		Last Modified: Mon, 16 Mar 2026 23:36:06 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:2df7a57d6f16bab4284503b71a9657cbdb6162a7c8042c886b09f1b978971ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46778573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec757699659cbf6844d886439095c346f9f822c78702a66f1296b6bfc2e5862f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1773619200'
# Mon, 16 Mar 2026 22:53:12 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:81d92818197dfe294c5f4d68c4bc0c99caf37505beb78439cac363781fc160a2`  
		Last Modified: Mon, 16 Mar 2026 22:12:37 GMT  
		Size: 46.8 MB (46778352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c46f8a0d2d67df442af18d9a7037a4b64fb91efba38b6aab14f82fa01bbbe26`  
		Last Modified: Mon, 16 Mar 2026 22:54:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:5e49826e13eea443ac85af17eaa517f0968fdb5da0810a5c57e57dfde7b8f740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3141295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4cb3209bbbe5b9aed40c98b8bd7bcf8ae787e4daa9bcde34b7a886dd6fbe335`

```dockerfile
```

-	Layers:
	-	`sha256:b6158e9dfd2df1b733376d1bef5da99ebb1d02f51521a78f0e7575952d154531`  
		Last Modified: Mon, 16 Mar 2026 22:54:05 GMT  
		Size: 3.1 MB (3135162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a71b4ab95ecc309e9d00a26f2379e505aea4804939cfc69a379efb013f2f43b3`  
		Last Modified: Mon, 16 Mar 2026 22:54:04 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:ba8986d7c6651c4baba9594f2b1d3e47f8438d0dcf5706378b93516d6d74dba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48373463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c22d3c0ed927a2796b7e009411dd15819b7a8c5f3ca0cf4e95dc69023021b99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1773619200'
# Mon, 16 Mar 2026 22:15:59 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:0b89b04671a87477c5e352dd0ae37501d272923b8177302e0847c436d967cada`  
		Last Modified: Mon, 16 Mar 2026 21:53:08 GMT  
		Size: 48.4 MB (48373242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0077e6f50d2b9b09519725335ccb4a44f531bf54c98c4d8a6210a017177d7a53`  
		Last Modified: Mon, 16 Mar 2026 22:16:11 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:4ba6be4a5b593258d65bf3aab216e3613a0a32aec9d80eeabd103a62b7c0c92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2962ac19a6ec1de4c8a08d7848e46b438a67e11574ef1e1b523c1a579701cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4408ae9af1fbe4ab39e96a1f318eb3febdcd6c74cdccaf2a1edb0f723f2b1b`  
		Last Modified: Mon, 16 Mar 2026 22:16:11 GMT  
		Size: 3.1 MB (3145105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2be6f964b526fff79043f836bf8027991f8f6beeeddb0c91118938931a47fefd`  
		Last Modified: Mon, 16 Mar 2026 22:16:11 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json
