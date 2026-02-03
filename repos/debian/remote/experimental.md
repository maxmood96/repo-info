## `debian:experimental`

```console
$ docker pull debian@sha256:58884921f01a4f7c0127b16d27ce47a348318a742cbacc8877a1c13d99c85815
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
$ docker pull debian@sha256:cc357e63a86058b3123062730a80ff17caa0a7e3be0d9e9bcf18ed5fb70f92ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48654927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7d9a4b8b4e3b284d67f844b7e38bcf18465f8c1f5d24207be2e6ff53fe34f6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1769990400'
# Tue, 03 Feb 2026 02:15:32 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:5d328c471922b9c24eec6fe86b088870e4bf7f601f2dd72d0bf170cf0a5e1ede`  
		Last Modified: Tue, 03 Feb 2026 01:15:32 GMT  
		Size: 48.7 MB (48654704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f2c2d49322d97bac078c70b67b5a2e1886c97e3212e01960608ba15cd5954d`  
		Last Modified: Tue, 03 Feb 2026 02:15:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:ef7c31d739e7cbdfc939972bfc888bd8e9efa4fdd06387ced1477fe2d136de93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7509e513cbfcc20e134f73b9a71a7286e07c39e5b6d6304433fd80e8e692d485`

```dockerfile
```

-	Layers:
	-	`sha256:e0a81bc5bfcc06809cde997416831b7d3d0f7664fb263bfa664a68b09bdc9e5a`  
		Last Modified: Tue, 03 Feb 2026 02:15:38 GMT  
		Size: 3.2 MB (3150471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd4797138a4802a5a449ea0fac1c5327a33954d4aaf6039e45dfb7a818467d0`  
		Last Modified: Tue, 03 Feb 2026 02:15:38 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:d7ce67bca5069c3235ef05bdef238f7f40439654045a3fc589f45b1e94627160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45125182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf7c1e91e01c55ff0cb62216c6e013fa208b18b19293ecfb97fb61319dc1c74`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1768176000'
# Tue, 13 Jan 2026 01:15:16 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:25f8b8c05c313e5aa19fd75cd8eb0e8d59bbccfd54f23a1dba8c45ff7717b9da`  
		Last Modified: Tue, 13 Jan 2026 00:42:25 GMT  
		Size: 45.1 MB (45124962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d46489b7b9480bab773164ead408e88749c641d2c2f48563e2cc98523d0f68c`  
		Last Modified: Tue, 13 Jan 2026 01:15:23 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:a8550cbe2021f8c8c0a42bc255bbaa408b354d01accc6fa98a9b8fad8cb1889f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cafff2b05732f8f4f0bad8c7666dc6bbf480240608ed64f515013de33592a2`

```dockerfile
```

-	Layers:
	-	`sha256:a3c9e1b362f78612a1d1455fc313987dcafecc0f9e0c8a0874546c1ebadac1bb`  
		Last Modified: Tue, 13 Jan 2026 01:15:24 GMT  
		Size: 3.1 MB (3144524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868ef0cc8adee3959827bf05644cd38415d278975373f176d5d6367211c0cc41`  
		Last Modified: Tue, 13 Jan 2026 01:15:23 GMT  
		Size: 6.2 KB (6163 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:bf57d4ae1e91aaa1e567bb396b53606ad1a1107b847e39d2a31b0503ca674135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48824944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c85fa1ef8ee149aae7f702198d3ad6c682c4f2cb67c47ab1d49bba92acebbf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1768176000'
# Tue, 13 Jan 2026 01:17:12 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:a36821f44fb17f424807a0a0283bb021936ee48bb00ed8bd7e54ed7400a38cb7`  
		Last Modified: Tue, 13 Jan 2026 00:42:57 GMT  
		Size: 48.8 MB (48824725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023e919e23758c8fdd2a64336c9b5b9028eac766f47858e3a7a203a759b21c39`  
		Last Modified: Tue, 13 Jan 2026 01:17:19 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:e1f155afec88c0824eb5666f70cc43ef93e0496f01c9e2232e22dc6ea3e1e150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1a139a9b29feb83ccb56416f3a1d53b4f7999e9e931bbfcf2c9a2d7c9d0c3c`

```dockerfile
```

-	Layers:
	-	`sha256:6b2c1621cce08d319d201eabeff311dcb9dfc3571f237649ddece0d4f22e09e0`  
		Last Modified: Tue, 13 Jan 2026 01:17:19 GMT  
		Size: 3.1 MB (3144001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:699be2f0e5a18a5cd6e8d1071825340829cef0d0252a3be77c23fa13ec87c483`  
		Last Modified: Tue, 13 Jan 2026 01:17:19 GMT  
		Size: 6.2 KB (6181 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:7bdbb9411497bfd029317f36cfd4bfc4c466b5b982c79e040ccfec316fc41b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49944042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1d87ab4ab7700f641ce5ba281ff9adeaf13170772b835d5b95776c35eb4e47`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1768176000'
# Tue, 13 Jan 2026 01:18:04 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:6cc523c1353e2f7e3d9076701063b4820e209e699c3f43420df2e5422da80a8b`  
		Last Modified: Tue, 13 Jan 2026 00:42:59 GMT  
		Size: 49.9 MB (49943823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70295a80ece57a62edef8c29aeb93d9a58943f87dcd790ca673ef68b26b4b1bd`  
		Last Modified: Tue, 13 Jan 2026 01:18:10 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:701baf865f26404ef88eb9b0b33c6426d6c8926b8fb7cad6fb90875d9501e7e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1865bb59c2f963df1057c82df53b8d9331c08d4c740776fac1ba386c24900d`

```dockerfile
```

-	Layers:
	-	`sha256:eda1cf4db6393a3abf9649eb5e37fb80cbb592fe2057b9560ce3113f3b4c05e7`  
		Last Modified: Tue, 13 Jan 2026 01:18:11 GMT  
		Size: 3.1 MB (3140347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84817cef0c4347ef2b9e0c2439dd286a382f4306d1a8964b6cefe5ccb61b0df4`  
		Last Modified: Tue, 13 Jan 2026 01:18:11 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:b7e6ab7ae285ec084cd3696d38c6e74d2e8fb1232abe29de6fcb3dc59493025d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53584743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf987cefe99aae1f0a546ec45880105748ae5452e97dc52ff1c7041bc338c04`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1769990400'
# Tue, 03 Feb 2026 02:15:52 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:ac9478d372ab9900a4f99ed9d427a96a3de37a06833f433b4f9dcbb81db19679`  
		Last Modified: Tue, 03 Feb 2026 01:17:10 GMT  
		Size: 53.6 MB (53584521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e425367957ebad6dc87d076146bdf278a2c029badf97a481bcb3c3a6a8648b47`  
		Last Modified: Tue, 03 Feb 2026 02:16:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:ebc54fc5a65c96bdad416d239f4e8ac521800f61043a79fc03916b347f676ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3160131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df96465c72bd1c218dcc5bbad07c562447f47ac8eac07452ac75e690114b0a0f`

```dockerfile
```

-	Layers:
	-	`sha256:c1d136a22d6bcdcd763be53ef731dc7c158f0ee039fc719ef00dbe2a8ecbdd40`  
		Last Modified: Tue, 03 Feb 2026 02:16:10 GMT  
		Size: 3.2 MB (3153998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0abdad9353de66dd1cf4ee387c162240ed1d188703176c4742d1d96f7d9b6945`  
		Last Modified: Tue, 03 Feb 2026 02:16:09 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:834b6ab231089fb32193ee62e5410df70198c5b5bb9270db63c0ec578d06578e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46856980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10ff523d275d8eeea43cee931e7bca82158b5f747c951394555619be67087e3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1768176000'
# Wed, 14 Jan 2026 04:11:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:247c00c4e36f0aa85cff57992c0ca22b2bfb8e9809a678d7c62987521aaf3c49`  
		Last Modified: Tue, 13 Jan 2026 01:09:50 GMT  
		Size: 46.9 MB (46856760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1fcce0b2b45e441c3fc65fa5e4d8042fda66161b227f2170ae5d4c5d52a334`  
		Last Modified: Wed, 14 Jan 2026 04:12:12 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:9be8014c0529734e71d76a1c265bdf90887fd4dce05ed9184ae9068453b9f9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940498cd748275dec0720f9cae93238ef2504278611934b1818606e4160b57e1`

```dockerfile
```

-	Layers:
	-	`sha256:5eea785cd6c7f700e22ebe5b7172997c6d5a0300fc931914fa4af21481935086`  
		Last Modified: Wed, 14 Jan 2026 04:12:12 GMT  
		Size: 3.1 MB (3134652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c441d4ec7b63f0d40906541f59f5b4211f54e73710ea28b690b1d38854d625`  
		Last Modified: Wed, 14 Jan 2026 04:12:12 GMT  
		Size: 6.1 KB (6132 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:3b87610a949a9fa3a9dc85956d52405911a297d3b6efd31836058c63f4377603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48421418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f825f4c32ba5850e7ad1c61925bb666b84144273571e6e184d148f84b6a8f56a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1769990400'
# Tue, 03 Feb 2026 02:15:43 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:8a73935faa923da850aad16997bdc7c93e6f2998a9394fd1cac6755ff322159d`  
		Last Modified: Tue, 03 Feb 2026 01:14:18 GMT  
		Size: 48.4 MB (48421196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce13534a47666f9ad075307a5bb32e126837bf5367c3afdc149d535e2991f308`  
		Last Modified: Tue, 03 Feb 2026 02:15:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:26be35bdbc8de41658a128a71b52ba6fe1ecb1d7d6061198a26ae47d1ed172ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3158021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065b819aa492a473f6425e7454f90665320a4be8166a0078fb5fa58766dea00f`

```dockerfile
```

-	Layers:
	-	`sha256:3fc7095c7de702422b40901b2f243060cf67ed77de5f8c7b8b7dedd2772c7441`  
		Last Modified: Tue, 03 Feb 2026 02:15:53 GMT  
		Size: 3.2 MB (3151920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da51458d1cdd98e6acb26ae34259b8be9dbe6f12f10d28f6641b61e96182c6f`  
		Last Modified: Tue, 03 Feb 2026 02:15:53 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json
