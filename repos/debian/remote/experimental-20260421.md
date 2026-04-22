## `debian:experimental-20260421`

```console
$ docker pull debian@sha256:764d38c393dcc3f034ddd51e02d23c3be3db75cecedc733a5d220139ef4ab0ab
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

### `debian:experimental-20260421` - linux; amd64

```console
$ docker pull debian@sha256:7ae5630163357de51938f5d6a735e471c9d6810e14297b9b7c5ce9138549ee2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48670805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6375c1583f16d2431544b8d0256536288a26c8d91ce8ecbce742a6351bdb2fd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1776729600'
# Wed, 22 Apr 2026 01:15:42 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:da1b39412060ddb62e7201c79b442133c0f4a701d2cd10e846eb8d608ef00909`  
		Last Modified: Wed, 22 Apr 2026 00:16:57 GMT  
		Size: 48.7 MB (48670584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a15e1423f34d994db0e73a59f38741ec659944cdabb4cc55a0fa5965aba4f4e`  
		Last Modified: Wed, 22 Apr 2026 01:15:48 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260421` - unknown; unknown

```console
$ docker pull debian@sha256:961ec5b96f210b2fc777961708fadec4b5c91cb995a979bb80c6b51ca69782eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6b3d68be75ba3b2a5d80e81410663a0bbf86ad914437088a06d5ba1bc1671d`

```dockerfile
```

-	Layers:
	-	`sha256:678dde4067b053736de5addae94b4aa63b0b1b62d421dbf75662e6749bcba4f4`  
		Last Modified: Wed, 22 Apr 2026 01:15:49 GMT  
		Size: 3.1 MB (3145547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3bcd4a008846e77f3f05f9e0b17248b222a68fcb74103d6f16a0c3a7bb153a`  
		Last Modified: Wed, 22 Apr 2026 01:15:48 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260421` - linux; arm variant v7

```console
$ docker pull debian@sha256:501256738b563d9b2823e9565dadcbef7a9d89f8557c02eb567151a73b4a465f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45607612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04b840847f8e084f4f652465824a04c9ddff3c704aa04cfad43a5e316f85566`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1776729600'
# Wed, 22 Apr 2026 01:15:48 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:8f4d0f64c416981efdadc732b77011349b8c4e03b427d794bcca746622a8fb45`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 45.6 MB (45607390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43118519c15c3a62870ac931cf476423481d521095ceceeaae1307a0030d2cbf`  
		Last Modified: Wed, 22 Apr 2026 01:15:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260421` - unknown; unknown

```console
$ docker pull debian@sha256:3b912854665956ec914deae6969fa0eff4772d93957ecdf6f7cfd2373e54b0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae77b3bb240d1d74b8d50f2b68eb51e2536097ca84d0bfe878330453e39d9ee6`

```dockerfile
```

-	Layers:
	-	`sha256:64344f8c4a981edf6d314de820dd3eabcbbf0e923a2b8571967622bd736df7ee`  
		Last Modified: Wed, 22 Apr 2026 01:15:55 GMT  
		Size: 3.1 MB (3146917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e30426a4804ea6a9b9bc66a2e40af692a1d7cef5f841276b21ead900e430b6f`  
		Last Modified: Wed, 22 Apr 2026 01:15:55 GMT  
		Size: 6.2 KB (6165 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260421` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:974e034b3c5266700e5352c9be7aebeac2c049c0fb7927b16ddc546b907df38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48711597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8a1e0cd2eae14d55f547c4e5d0dc731f724ef49a969d89248d50fe2b5c4728`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1776729600'
# Wed, 22 Apr 2026 01:15:46 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:c6b5ac29527c0f10c387962282d51011fba88600d0f076d2a4a2cb9c3f4f7be3`  
		Last Modified: Wed, 22 Apr 2026 00:16:40 GMT  
		Size: 48.7 MB (48711377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5b8dcaf4d757a34808321c10de7c40f084c797951535fcabf387a81ae689e5`  
		Last Modified: Wed, 22 Apr 2026 01:15:52 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260421` - unknown; unknown

```console
$ docker pull debian@sha256:18906823675b5788531fb4e4f6bbe0266f1355382f668420dc43d041e530bc8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcf70e82e765b6332933f079b583b5d83aa59289149d83ce141c449689a784a`

```dockerfile
```

-	Layers:
	-	`sha256:541b8c537cb88e2550d4f5919daeb9c734a17a048d1f6770b40c3f388a2cce02`  
		Last Modified: Wed, 22 Apr 2026 01:15:52 GMT  
		Size: 3.2 MB (3151509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ee29a444d86ffb130a3b4f4be8394c9994ee644f2a98b5de4d6bbaaccec8865`  
		Last Modified: Wed, 22 Apr 2026 01:15:52 GMT  
		Size: 6.2 KB (6181 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260421` - linux; 386

```console
$ docker pull debian@sha256:986cc510d27391931c474cf8ead10bb2539dcaed9d4998168d28fd95f7bea32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49978435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eddfc60c9e046ee184970d57d71c0e2986b5de61dfdd737f289248169a7fdac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1776729600'
# Wed, 22 Apr 2026 01:15:51 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:cd9e481a5dd715733e79008499f16ed10c38edb874e68816c67be5b48ac410aa`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 50.0 MB (49978215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90888da409796df90595c44c7920d4798c7528047e7d0c6ec30fcd969b418f7e`  
		Last Modified: Wed, 22 Apr 2026 01:15:58 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260421` - unknown; unknown

```console
$ docker pull debian@sha256:cce022fd65daec03186d24fb339e96513626653734e4f2154c21189ab92b3606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c44328cc00918e2b11b245a39da6ce1d414c809158ace261c362236ef93dc4d`

```dockerfile
```

-	Layers:
	-	`sha256:cd986501cb0403e4a030122bd0f81ae4f359d1e360d17bc6f5ee1601b32af925`  
		Last Modified: Wed, 22 Apr 2026 01:15:58 GMT  
		Size: 3.1 MB (3142741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a0ad6ccff5c6341139b998883df54d9fc98e61a8fb14e195b3c6e275d9a9be7`  
		Last Modified: Wed, 22 Apr 2026 01:15:58 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260421` - linux; ppc64le

```console
$ docker pull debian@sha256:c5f20648b6a6851217887f218e9768d970cb3bfb921f59717ab43b1861ca01ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53971145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5944738a848f4d614ba85a7448f13883a88292c20f3f8f66300eec356a63f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1776729600'
# Wed, 22 Apr 2026 01:17:08 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:d218915bf98aedeef44a0c653592adf66d72027e66c55115ae99e04cfeaf6990`  
		Last Modified: Wed, 22 Apr 2026 00:18:49 GMT  
		Size: 54.0 MB (53970924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73213c92ff8576a931db17b991581ebf19bd8e58ddcb5abb99aabd7e94a31aee`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260421` - unknown; unknown

```console
$ docker pull debian@sha256:f41acc4340dc7b129237ba49f24dbabdb3a0cddf7e1e1846856a4867cf0adcd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e3e4dd74d863796c05d5da34e50010a1bfaba373c0f3c11eda34ac2d92a318`

```dockerfile
```

-	Layers:
	-	`sha256:af2b077e84ad192786b4f4b1d7fb8dc00cffdf4f732bef67dc901001ed86d22b`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 3.1 MB (3149060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58b468b0ae8e21907133052f483a6d90f26da1f525acc85746fa6fd6d9a761d`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260421` - linux; riscv64

```console
$ docker pull debian@sha256:ad261cab43de8de32f406332128b862733ee1b4da8fc348ab70a5c26bfd5a970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46781469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9459399975fff29cba44d477965a91ec266b0df2b1cc2efb10504230c15e58e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1776729600'
# Wed, 22 Apr 2026 06:03:24 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:aa065db152c47374403e2d1b1f371335a923e0c816dc69e05b2688e8c4248547`  
		Last Modified: Wed, 22 Apr 2026 02:32:48 GMT  
		Size: 46.8 MB (46781248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0714021c07b608acc44f83d5aab47282ffd1101450c35d312992766feecf1b`  
		Last Modified: Wed, 22 Apr 2026 06:04:16 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260421` - unknown; unknown

```console
$ docker pull debian@sha256:bada1fa9c3eab5d1e2c020fe4f36ac6c9e9ff62c3973d281acb5266bbf8bd266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3143196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c35e7258212ed6e759f9fc503e298481fc5b94b27ddb0780c6c4e486da57078`

```dockerfile
```

-	Layers:
	-	`sha256:bfb5a868403ec0808a0cc93252e22a22506255ed6b6024aee32aa5c733e3e5f6`  
		Last Modified: Wed, 22 Apr 2026 06:04:17 GMT  
		Size: 3.1 MB (3137063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c94f5f079f672e46b479474091873100a38c26aa4d6c43c00720faba4d31916e`  
		Last Modified: Wed, 22 Apr 2026 06:04:16 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260421` - linux; s390x

```console
$ docker pull debian@sha256:5692a10ce1144d16e21d86e85d8e9716f2170175861050d3de27091d014e7da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48411174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fcb394f4fb9c103e1046ae14a0435c9745ab94ad57d1547326a5a698925bbf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1776729600'
# Wed, 22 Apr 2026 01:15:07 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:94cc507370142df8a6a6c11401d1d18650ae32fff6ae2bcb0d4e4840a1e93548`  
		Last Modified: Wed, 22 Apr 2026 00:17:14 GMT  
		Size: 48.4 MB (48410954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b2264f2100691a855189e3fae7b28d33acf32d60d1813fb8538deb5c6b4bd7`  
		Last Modified: Wed, 22 Apr 2026 01:15:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260421` - unknown; unknown

```console
$ docker pull debian@sha256:9d8e1b58da98f61fa329f0a29988b13e83eb8a22cc8891093607029569ab2321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bac0f3b56f3e0dcbb376d753b34241dcc9c6e29b938460de590cc3a010a82c`

```dockerfile
```

-	Layers:
	-	`sha256:b82725623ddbfb1cabb3ce0e671e951c5870626c8493cc86977a4aafb5329c26`  
		Last Modified: Wed, 22 Apr 2026 01:15:20 GMT  
		Size: 3.1 MB (3146998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b0ff32e27939189e699bd7a8c9881160f1a13ba76272de5c734056c06c3282f`  
		Last Modified: Wed, 22 Apr 2026 01:15:20 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json
