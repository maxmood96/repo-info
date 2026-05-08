## `debian:experimental`

```console
$ docker pull debian@sha256:09f21784f02ebf972d9e1b60a9344d534f3d95159caaaef3bbfacda38cbe1f25
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
$ docker pull debian@sha256:cd925a551a6f6635e4c7f9387b9d92958d2e80e238c853c63231d94e89848ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48702464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef6c4586373fe788d7b4a66f58abf6bf8c5f58f8c787f2102710d01aef44dd8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1777939200'
# Fri, 08 May 2026 19:14:56 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:6396b26de0b91f8b165418fb54ccd7fc8a19d22afbac9a702ade122937484427`  
		Last Modified: Fri, 08 May 2026 18:24:17 GMT  
		Size: 48.7 MB (48702243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d4ab74447b9187621481f74d1f691d9b066cb517c9b50bf06b0176efb18aca`  
		Last Modified: Fri, 08 May 2026 19:15:02 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:b9ca4ffce8e205600ca83f73c491457e17ff64984a8cee6fcec3dbef0ac20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3303febc66c889f49e135359b4481f9ceaa26ac009b1f497100917402431d70a`

```dockerfile
```

-	Layers:
	-	`sha256:99930479a5693059ace89ba3ee1a1514611f71a54df5c5e5895fdedff6b18423`  
		Last Modified: Fri, 08 May 2026 19:15:02 GMT  
		Size: 3.1 MB (3147175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c33f4f0bb55d27067400ea3af222ac36a2710860dc35062eada3a776dd706e49`  
		Last Modified: Fri, 08 May 2026 19:15:02 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:e971859670c235782f5659d51153e482e1d9e26edebcf13fc6fed355b123e275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45610202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e5e34978a9f185b819de19f832c4fe049d4faf500b7036fe299cb24fe57600`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1777939200'
# Fri, 08 May 2026 19:15:16 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:95a0fb8ecb9b3a040443d9d42bfd6f5d6bf2d44509006fc02ced5500767be45e`  
		Last Modified: Fri, 08 May 2026 18:38:05 GMT  
		Size: 45.6 MB (45609980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52941f840eca54803a6ca062f75985742b600640664fb922e3c7fd776975ab66`  
		Last Modified: Fri, 08 May 2026 19:15:23 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:ccdb506a2ba8aad8a86c0351fe1b5d38a8262c9771a51654a55431ce3aaf2b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3dd4dfe744e009d08cd29c0e2a67ec1edc854f3ed6358a4a2f9b0cf27dff85`

```dockerfile
```

-	Layers:
	-	`sha256:b71111a631c46417991d170a9eacf1c5a9e2f4160b0b6aa7867b6f9a00ce1710`  
		Last Modified: Fri, 08 May 2026 19:15:23 GMT  
		Size: 3.1 MB (3148545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19f5cf30645fed9fbe47fa18aff5631f8060196685b96b6dafc3419a33bdbcfd`  
		Last Modified: Fri, 08 May 2026 19:15:23 GMT  
		Size: 6.2 KB (6165 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1e8d39f03f480d543b4ce94fad96ebfd0192cbfff0fecb58edba52628b04be0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48734378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520bca7bce276f3e5ef14372ad59856a73f02d1c330136b6515000587f4550a5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1777939200'
# Fri, 08 May 2026 19:14:36 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:0c561a829dcb1c26ebf7569797890e356231c0be0daebe6aa1f319a083bc3a8b`  
		Last Modified: Fri, 08 May 2026 18:27:06 GMT  
		Size: 48.7 MB (48734157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08dd024340e5a70e69a0e25cd4c2237433d2981fbf011bec15e2118f29ed4c0`  
		Last Modified: Fri, 08 May 2026 19:14:43 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:74bc175d6c87be05655a41a13821dddcbf44c0b34ecd799dce291c7cb53e6f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3158038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9938687b8389d7c9b1721bebf63416dc424cdfccde9b55b1001f3d49e33c3c57`

```dockerfile
```

-	Layers:
	-	`sha256:14ee98ee2778823c683f7558afbc4b86022630a53b086da04d67092087315144`  
		Last Modified: Fri, 08 May 2026 19:14:43 GMT  
		Size: 3.2 MB (3151857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76af18ffb984c25a8a49264b6e019ab6ad9611e376d74fe6ff82c5a5eb1d623f`  
		Last Modified: Fri, 08 May 2026 19:14:42 GMT  
		Size: 6.2 KB (6181 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:8e1a8bfc9e2d949adae21192a370b4d3708807b7b7eabdba30d8fc85bc7e5877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50006940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474a95919240876c897239580ebe6fc017c850db65d29eb88ba49845eafa78d6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1777939200'
# Fri, 08 May 2026 19:15:36 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:87dce434f6fd31d0fcd3a3e9fc57c3bc357840591b02665be5ee57b522ee8114`  
		Last Modified: Fri, 08 May 2026 18:33:03 GMT  
		Size: 50.0 MB (50006720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808b263eb88077429274730c8b1d5608c7cf6b023ef8796596a344be3adffaf6`  
		Last Modified: Fri, 08 May 2026 19:15:42 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:15edad41e0cf5364e32a3a5529d50702877126cead9b727c8cbefd464457ee0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b273559156db8e27d3d78048d3cf0a143c440055d7b705686b2a4a0b0665cf`

```dockerfile
```

-	Layers:
	-	`sha256:11ea52ff319b93af640f4f009c13d991b39e1da613905445059140c5e411f824`  
		Last Modified: Fri, 08 May 2026 19:15:42 GMT  
		Size: 3.1 MB (3144367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42339f07daec9545d4c21a9f8c570f37bc8b384573ce224d512e52fa51f56e7e`  
		Last Modified: Fri, 08 May 2026 19:15:42 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:f3af864c57ada7df5b2694f18a568ea95141fa8d080005a5a885f00f50f6e044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54028301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2c875f21997afeab493e73168044c06c2b41bff407d458099e339ea5276ad9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1777939200'
# Fri, 08 May 2026 20:20:35 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:a5ee333694ea08c826f3d66de9df09e9383e241afde30213ce04505d8142670a`  
		Last Modified: Fri, 08 May 2026 19:47:24 GMT  
		Size: 54.0 MB (54028083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8a8d726a590f34756ad982d4cc4141065bdd5fe3e69f19f3f287d8fdcb1ee9`  
		Last Modified: Fri, 08 May 2026 20:20:49 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:bc65e0d4028226cbfa6cbd44184783eed458ca2141235934b51f757f8be95c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9423728253c1bc66b4b0fe30dd4ab5e50dc9b5fb481ce8d0768cfef4195d2ffa`

```dockerfile
```

-	Layers:
	-	`sha256:3863e4e07dd5cbd532ac6e67caa17971bd23b6f758d3f6664c78b68409935d72`  
		Last Modified: Fri, 08 May 2026 20:20:49 GMT  
		Size: 3.2 MB (3150692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:138eba14db08f73822c5bd17321b9f10b46094a79998db04bd6e2ef6ad50155b`  
		Last Modified: Fri, 08 May 2026 20:20:49 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; riscv64

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

### `debian:experimental` - unknown; unknown

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

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:c203222f4ab79a2d0506abcc656a536c7d349c4ad1d5be13633848061dff01a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48444302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b518591d98bdc0e0e5b41114746690916e78f9bfc85d9def49a0ce89ffe7f08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1777939200'
# Fri, 08 May 2026 19:14:42 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:7ac2dab051078fefb660e71626199f1aa70a1a5a3bb1c5775ffce3312f00a6d8`  
		Last Modified: Fri, 08 May 2026 18:29:22 GMT  
		Size: 48.4 MB (48444081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012ef96c9a1f6d400f42bba22eca2b55047b119f815cb8e0e5f54871d92319ab`  
		Last Modified: Fri, 08 May 2026 19:14:52 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:0168835fc6a8e759eba81155d27c024fa364f31393623c69b47b751576ee7451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108b3b8319ddc457644fdfa1715179063331b7d154c77b1bee0d1fe07d463d59`

```dockerfile
```

-	Layers:
	-	`sha256:e4994d31d5636fa6e5c23a8fb7e3ac1ecccdf5600740280ab9cebc0d8f828c5f`  
		Last Modified: Fri, 08 May 2026 19:14:52 GMT  
		Size: 3.1 MB (3148626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b32ed1093029514ab9ad82c6ebafc8ae2b1b3ee7b55d2af7792578412b6b5d5`  
		Last Modified: Fri, 08 May 2026 19:14:52 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json
