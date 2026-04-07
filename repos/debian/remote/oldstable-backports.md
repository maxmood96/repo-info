## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:c850ebb2711e4dede58418bf5f7b0eb48c14d0211e8d257cef8ed528ffb8ca3e
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:97fd4a7d789d14dc73433bef21a237adb8c5033edbc50e87863a68b3a7c5a692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48489048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94260908ba3ffa4afe190b11397853afe44e727ea1bdc82e3a80149057b577d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1775433600'
# Tue, 07 Apr 2026 01:16:51 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:88271bc52b49f49686ae6803fbda3c4eaacce7c659aca148d4e0a0406b2ebacb`  
		Last Modified: Tue, 07 Apr 2026 00:11:43 GMT  
		Size: 48.5 MB (48488825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327f19c45668bde5d1b041a44bef7d28b63e3feec42d20cdeff74127d6f31a04`  
		Last Modified: Tue, 07 Apr 2026 01:16:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f81255c3c77065113b4569833de0e12cedadfc1068b078dc694631289f02e58a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da5e61ae4b647dfdbef93932833813d922426660614ac161785164913c1b8db`

```dockerfile
```

-	Layers:
	-	`sha256:461ccc48aeb024d0392ad73d8cb156dc52526c532b0c886304bb62afb67e6a3e`  
		Last Modified: Tue, 07 Apr 2026 01:16:58 GMT  
		Size: 3.7 MB (3734076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6be05becb6bc08834493ae9a45887833e7e120192d20604801cde292ffd9d30`  
		Last Modified: Tue, 07 Apr 2026 01:16:57 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:f5d35bb392244cd3e8367d42a59a08b53d433a3c5a0458f32862ab625ee099ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d501722ed9666e959c0d92273a6f0883f5f16e5aa6e3837273697589fc539e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1775433600'
# Tue, 07 Apr 2026 01:32:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:193b03692450e7cace4d0d2ca1fdfa555e6b02853e20cbcc770433394c1fdf06`  
		Last Modified: Tue, 07 Apr 2026 00:10:35 GMT  
		Size: 46.0 MB (46021671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f944245394f8cdaed87fa8ca28cfdc08c0b64bace0616257322f34f3823a23ee`  
		Last Modified: Tue, 07 Apr 2026 01:32:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8ae45feb2d9b6edce3ade30837824c045b8392be35b038cf758aace57f7f5d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68e7ea14110a93ed36884aa40a6f51886d824466ec72d4bac35dd772acf7907`

```dockerfile
```

-	Layers:
	-	`sha256:1218a6ed74ae952424afaad2bc5e581888ebe20680e3b5b9d71ede44a14c4f7b`  
		Last Modified: Tue, 07 Apr 2026 01:32:17 GMT  
		Size: 3.7 MB (3734277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:156e41a0cc9b730937de748b20ea962eefee4b9a1b4b3c40c9809c034b4c93b7`  
		Last Modified: Tue, 07 Apr 2026 01:32:17 GMT  
		Size: 5.9 KB (5865 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:00490893b5209daa84103864c37b769c8acb4424fce14fac1342bd78f4ad8d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44208047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5c23fe5b13fdbc186fee02481b9e6eefbeb04bc6dbd0674bbb6cfc5d8011c7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1775433600'
# Tue, 07 Apr 2026 01:15:55 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:71e882d179b8b0c8b17f097c46ae85003cdc6266340934668bff3ba51ecf0195`  
		Last Modified: Tue, 07 Apr 2026 00:59:55 GMT  
		Size: 44.2 MB (44207822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326be300d4944044e5835d67704cba9eb00a4cf2e0751c9bca4b3ffee7d10c08`  
		Last Modified: Tue, 07 Apr 2026 01:16:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a59d846c999f4fe2d6202cbcd41bed84c466fe537384ca37ba2ba50217420595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c80446d63aaa80ba276dc7580d4a5e974889395c86b7e427a2e978bd199b87`

```dockerfile
```

-	Layers:
	-	`sha256:ac3a81d957918d86173d11f999a7b185ff7382d3cb15a343436199056781f5eb`  
		Last Modified: Tue, 07 Apr 2026 01:16:02 GMT  
		Size: 3.7 MB (3736255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67b29dfbd135c1ff899b46ea6bca5de8727697b8f4d8cf8f339e4bd37f0d427`  
		Last Modified: Tue, 07 Apr 2026 01:16:02 GMT  
		Size: 5.9 KB (5865 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:9ba84a649fdafc065ba4c09fc5ab39db8df9b64ecc1f98589cd22d3f54c4a45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48373493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840ca6528513414801b4049964cab3d3e25feef87b70cd8f3e0878781919502f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1775433600'
# Tue, 07 Apr 2026 01:16:08 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9d50b0d2a880ca5bb2a3b65859ac33b11cd7600513db70ccf929bb522a7c6453`  
		Last Modified: Tue, 07 Apr 2026 00:11:25 GMT  
		Size: 48.4 MB (48373268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9cdafa5e4000d590426a4f3a55e1935a534cab332861ef5e4cae4ff730c8ec`  
		Last Modified: Tue, 07 Apr 2026 01:16:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7f2ad9e0a5a81f8551f8ebb24abe2d32494905db48c42b646e39408f2a0b9977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd284f609f912a60151cd95c0e281b2c005311a9d050e01739e23fe30e4d4bf`

```dockerfile
```

-	Layers:
	-	`sha256:bfc53e7a8d29040431b684dd3d62401f6a257c71a2bb7775d4cdf6c2c9c0d224`  
		Last Modified: Tue, 07 Apr 2026 01:16:15 GMT  
		Size: 3.7 MB (3734291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f667184e82ee562c2f5eebbf38e89da8407516bd620528c3e0961e5d40f40858`  
		Last Modified: Tue, 07 Apr 2026 01:16:14 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:734c8360b46cd2759272019708588c050901f2be6bc39d1e649642a86a9e01ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce404188828baf5899deda219d6dfb88fd12271c4b4071b9d1758eb99bb35b1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1775433600'
# Tue, 07 Apr 2026 01:15:45 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ac7efe00f580ac8e3b05db2c37237fe430575ec0c60c4d9e964da81fee650aaf`  
		Last Modified: Tue, 07 Apr 2026 00:11:44 GMT  
		Size: 49.5 MB (49477920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1178e823acfd31c92b4a0019a972746b6faef6178c48abed99a61fdf9261dec`  
		Last Modified: Tue, 07 Apr 2026 01:15:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4a582907dd2284430dcf87b5e4321c2c4feab4121f12784a59c1a982d3d191b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ffe5d1a72476d70f3e48a5f7433c4d9bf4636b08f5430bb5998037d25be397`

```dockerfile
```

-	Layers:
	-	`sha256:5645c2efc7581127022735a7a6a277a9dc42503eb5416117516e8e7e99d03c49`  
		Last Modified: Tue, 07 Apr 2026 01:15:52 GMT  
		Size: 3.7 MB (3731272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c96004c6a7bd7412cef4c4688a1cafb2b1d62cefcd694871abccc6972a064146`  
		Last Modified: Tue, 07 Apr 2026 01:15:52 GMT  
		Size: 5.8 KB (5792 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:774639003cea2745d4dae0bda3391b090f1ebf52f68d22fdb1df1573bb7e9edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48782823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09736c1d96f0b3a23f1ce76d69a578c7aa70f54fc22b7cef55b0942c1257e81a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1775433600'
# Tue, 07 Apr 2026 01:17:45 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:05a4c50c00c243357131097d0e94dc4c137acdc9909390f71d99531a165b1605`  
		Last Modified: Tue, 07 Apr 2026 00:10:36 GMT  
		Size: 48.8 MB (48782598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea332914caea561e2d657ef7590f204d62014fc55657f897940e58b92699c482`  
		Last Modified: Tue, 07 Apr 2026 01:18:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:456ac48e10aa2dcbd26f1792b5bae453d5bb8c86010318dd5461ce1488291c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82e8762759302461612fa835f0fb903fe9089d665c5b1bdfe3d8fd2fecb5530`

```dockerfile
```

-	Layers:
	-	`sha256:eadb86f544fdacfcb8cf9b1c36242f0a1f2c8a5fcbe4b1fb79c98bfd4207ec27`  
		Last Modified: Tue, 07 Apr 2026 01:18:02 GMT  
		Size: 5.6 KB (5634 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:3346d2dbff44735e94613fd038b71f316779ee96e0b0a13e7a5c995b5d217694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52337168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80af212379fe7ee600411a7c3e564868eb08eca74dde5447f8173a33dd6d2a4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1775433600'
# Tue, 07 Apr 2026 01:16:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b5a9429b3c324961270f24408bbe430f24d57c979ee7a32f4336735c85553d9a`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 52.3 MB (52336943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654d60bafeedc1fc1c53e85dd10e3820cca613c507f96140371fa2d8a599dca2`  
		Last Modified: Tue, 07 Apr 2026 01:16:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:949433bae96dd3ca07ce81f84bde02fe49a7883e46baba3ed279ded1af72fdd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8da4c8d1d00f6314025282d3c7a826fd8ce676f1c29f7fd6ee486eca57c457`

```dockerfile
```

-	Layers:
	-	`sha256:65f60c0905aacb93ebf392b022732fb6e4078ab605fe1ae969e1eef83418579f`  
		Last Modified: Tue, 07 Apr 2026 01:16:46 GMT  
		Size: 3.7 MB (3738434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d30174c5d52e9927a0bfeb88827858ab7926df122282b1e2e3dedfb10ef2843`  
		Last Modified: Tue, 07 Apr 2026 01:16:46 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:c167ddcb015f3233a9f41ce46227ca68bef37ba0545459fbcd549f883977f3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47148315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb7b0077b5fb832db5267f80bb64878300c3a5db86159fb945e915566237537`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1775433600'
# Tue, 07 Apr 2026 01:16:17 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fae51c3279c5f89e0883966bf3acfd921bb62f77b471384a9910e0913d9d35aa`  
		Last Modified: Tue, 07 Apr 2026 00:11:49 GMT  
		Size: 47.1 MB (47148090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75a25c4f0d9f1bcee3d670f4fdaf923c2c82c3096135c8ec7bdeec078390659`  
		Last Modified: Tue, 07 Apr 2026 01:16:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:eb406e36467b503c7e5cf6d66f7d8c4a1f4ac687dc16c5c3b1706dadc41ed74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a85a30d9fd553cc80675c94582e91ac15c082fb7194e05cb782601eee39d7e`

```dockerfile
```

-	Layers:
	-	`sha256:0200b7b2765ce7ea0551e338ded56e6e43cb8b1eac03db965feff8b7de193365`  
		Last Modified: Tue, 07 Apr 2026 01:16:33 GMT  
		Size: 3.7 MB (3730914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0893e57a7e60269ab3528eaaed2bb99a469b859fd7b5e19a993e60b46178b656`  
		Last Modified: Tue, 07 Apr 2026 01:16:33 GMT  
		Size: 5.8 KB (5808 bytes)  
		MIME: application/vnd.in-toto+json
