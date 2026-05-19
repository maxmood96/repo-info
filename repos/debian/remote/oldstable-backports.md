## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:317ceb817aad9f947da8bd8d0f1d9da21e857d07f2e6ae09d45277b6dcd2b1a2
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
$ docker pull debian@sha256:c67ad963c8905d73ae8f2db764c0958951202cb4638213b594255cbc12183c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48495667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ad42495cd692d187a47810d3770e90bbe8686546c6af6213176f4ba879dabb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1779062400'
# Tue, 19 May 2026 22:58:32 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:643c2323c86bece59ee00ac9d3da1a1b5c16dedb4de6131310f7ad5e266ef9a9`  
		Last Modified: Tue, 19 May 2026 22:37:14 GMT  
		Size: 48.5 MB (48495442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0b76c3db64d2b098c369b520022ac27768bda1de335baf61acb4dbc5be7054`  
		Last Modified: Tue, 19 May 2026 22:58:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:504db58262614c4d079bba391ecd5659f89144681e6a2aff8922b5b12808e032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3b205c273a0feac585467bba4e3ea48a5cdf2002fff584256e22fc61eee4df`

```dockerfile
```

-	Layers:
	-	`sha256:d7965be32bec8409b242e4ba3b9a777efea6e82b6867ab78d8ecc6296cee6ca9`  
		Last Modified: Tue, 19 May 2026 22:58:38 GMT  
		Size: 3.7 MB (3734094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75d3f94febd435e8b29f48f166cc96a5c73bd645e4ab3b16a8e5995deef40464`  
		Last Modified: Tue, 19 May 2026 22:58:38 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4d05c80f65815b3003d476bad66a4fe68ec975179aad90bf6102507f9c20c2d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46029735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2ccabb5bba9cd635b3791af8360ff0f74546103e6cdd1c205820b62d88ced8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1779062400'
# Tue, 19 May 2026 22:57:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:281f140543b558756b8a936026e20a3cbf5c1a170ec70aaf12ce08620cd740e5`  
		Last Modified: Tue, 19 May 2026 22:36:34 GMT  
		Size: 46.0 MB (46029510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb5a9a50c1611a2670e14bfc6f501e78bcc876ca034d213cc9f75aba1b3338d`  
		Last Modified: Tue, 19 May 2026 22:57:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:db90572b5ee39a1c2ab036318d9d5575473e80c3b76b40a317320bc5b1d3e52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb68fdc492fefef013516b876ac10725e6221b8f7cc2ab2905ef977c550e882`

```dockerfile
```

-	Layers:
	-	`sha256:1c8d3e064b6a28c6b71cfe803134abf31a0201faf796d1a86d9be36360c8e230`  
		Last Modified: Tue, 19 May 2026 22:57:17 GMT  
		Size: 3.7 MB (3734295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15b766867064548792d51ea2bb853b7a54d91b523a5942cdc65b5b545124d17`  
		Last Modified: Tue, 19 May 2026 22:57:17 GMT  
		Size: 5.9 KB (5865 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:509919a9953f99284b81dd97a1b58c973acd63c1b80600a710d3271a5ff8a53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44209388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eedf5b528fc1afab0454a352dcd064bb89f4751548b0231ef9334225986d377`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1779062400'
# Tue, 19 May 2026 22:57:26 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bac55ef1ceb1de5900c74d4e3dbbd7aad8ff8b7409930846f572278172297820`  
		Last Modified: Tue, 19 May 2026 22:36:46 GMT  
		Size: 44.2 MB (44209163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a78c36d6b99cb29cbc380729ab28ea32446344f9d790ce234f2ab951489d93a`  
		Last Modified: Tue, 19 May 2026 22:57:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:279e398ee99631606dc65ffda971505481de5217da91b86e299f6f47c7654572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02a9be88bded6b5d107336d589fe786b16b0f0def0ff75f86d265f4b3ea93d7`

```dockerfile
```

-	Layers:
	-	`sha256:8d265f8695081af27c45b032d7294c12d8e87495b1ec2cbed58c179f1784a8cb`  
		Last Modified: Tue, 19 May 2026 22:57:33 GMT  
		Size: 3.7 MB (3736273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16e19bb65573ba8f1f7cf9cbe08a7094095aae4ac7261d5453e4e720966efa9f`  
		Last Modified: Tue, 19 May 2026 22:57:33 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:896e3e3af7a93e521ebf964d0642d3a4374f40e55e132397c30010622b743c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48379666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c76f99e89e71857e96b9a754b6cf156c3cd97370cdf9618077c03128679b56`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1779062400'
# Tue, 19 May 2026 22:55:45 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:09135b457bd79c8bf923f2e627f2756b8dbf70fd7f4639c987bacf4107c32210`  
		Last Modified: Tue, 19 May 2026 22:36:19 GMT  
		Size: 48.4 MB (48379441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fd7b237cbdae9f6aab0f8bd9142e1284b13f0d070ab292335b02aff7307d6d`  
		Last Modified: Tue, 19 May 2026 22:55:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:515bb71d9ae8f60c873d6a4f00d6651318eac4762562a0a171931266070dd2a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8885f93358b8ffef2b2ff65e7d531b093b9b627d24a9ffef6e89759d671748`

```dockerfile
```

-	Layers:
	-	`sha256:05b2969f2f9d465388cf18d1150335d98876488b43aea6ba6fe75e1cd8eaf0a1`  
		Last Modified: Tue, 19 May 2026 22:55:52 GMT  
		Size: 3.7 MB (3734309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13da4b1328fd226314cb776ddb60d439a7638fe305201bcf4311ee2d3b5a597f`  
		Last Modified: Tue, 19 May 2026 22:55:52 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:5449258d97468bc3db3ef6f054d8404e9bd895e02e45bf6d34d097ba71786053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49483349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03abd5568d6d3f120435cf53f00b8ad0cb1e5b9cd47c6790f761adbdbdf0a401`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1779062400'
# Tue, 19 May 2026 22:57:49 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:619445a9580d0f80100143f9659b80364b979d13219503638e5a68be8eb375a8`  
		Last Modified: Tue, 19 May 2026 22:36:50 GMT  
		Size: 49.5 MB (49483124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6fdf5aa77b81474dea3c1138de141fc03879e3023f233c80c1416fd3df0fcc`  
		Last Modified: Tue, 19 May 2026 22:57:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:dde49fda2e73f28de8156d68c2f0a49863027f3aa5a598e4dcb2a8e414ed0792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b19576d4785732f91e1eb145224dc386a913e747b02180efcaf7503791081cd`

```dockerfile
```

-	Layers:
	-	`sha256:25b749004dcb8672fc46c31a17a6df1acf17443eefd83c23cdcda89ffddc0ae4`  
		Last Modified: Tue, 19 May 2026 22:57:55 GMT  
		Size: 3.7 MB (3731290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf4bb8de205a2e37420c83c02af07e17e54f1a9528cba33627f683a2bae6096`  
		Last Modified: Tue, 19 May 2026 22:57:55 GMT  
		Size: 5.8 KB (5792 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:506ff4eff235dd84fbbd267ce0b6470acffd2e9369b11b122b6d318807cf5757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48786470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b8ed343fe7e4840373a565e44adc753ac1349633b4a03d1639e49b67a63633`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1779062400'
# Tue, 19 May 2026 22:57:34 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3f76c8dd8026b2ba3f9b7d0df9f5fd9f64614b7bfea44ef67e469bd747cedf61`  
		Last Modified: Tue, 19 May 2026 22:36:15 GMT  
		Size: 48.8 MB (48786245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7cc7a49c12320b15628d3febd11a48f234d3bce5b18c23e0d77a4fbc695829`  
		Last Modified: Tue, 19 May 2026 22:57:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0e91397f9e8bf0f9473b222bd06aca2caef6e17c2d9173cbd1619ce552d59932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c56c43ddb7459af487f613156b2bcdc6b2c537bb01f316a39de12c50bd7c6a`

```dockerfile
```

-	Layers:
	-	`sha256:df47f0e21540a44377b5287f4da56c90cff937c7a0d4267f8d0d1465f6eb1ba9`  
		Last Modified: Tue, 19 May 2026 22:57:51 GMT  
		Size: 5.6 KB (5634 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:c905e733ab63f1185ddae0827a17c97e44b4670a6079a734e52240ad3a064c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52340431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ec3c7c8c9a113cd4daa9743c6a45a65619afb1bdd6257bbc3647f9b9937ff7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1779062400'
# Tue, 19 May 2026 22:56:03 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:965e5732b0fc2b11c43946e18092bb1263fe840327cf5e5dc6ce639276a5acb8`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 52.3 MB (52340209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96fbe54a81134e8ffa4d2024fac1342267d660b98712e11cd30a828c7044991`  
		Last Modified: Tue, 19 May 2026 22:56:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:859530b39225d58309aa42901a77f7a8389b5d494f9f9bf2cb044f700ae75870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22eb2e9091b82b039d790561dd8e05901fdd7a7cce1ba25759bb9bec1c612fa`

```dockerfile
```

-	Layers:
	-	`sha256:28a0c9b47cdaf097ce7a29eb7b33e91bb2777410cdce25e1963e7dfa370c09b5`  
		Last Modified: Tue, 19 May 2026 22:56:15 GMT  
		Size: 3.7 MB (3738452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:933937742e2e858750397f304d4abfee4a3d4294f9f1f6f6ed3473562f4f8516`  
		Last Modified: Tue, 19 May 2026 22:56:15 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:bdd57410af4cbd188ab5601d0513df289f1eb846d3b0c1862c831408028033d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47155824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6232e9913e0a2c08bd2cad429c375afdc0e4b1ff92fcff84ad986cf3299ada`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1779062400'
# Tue, 19 May 2026 22:56:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cd9c48d47f40ef4e27c3565effe11c07cf68151495618bab7ec689503a70b867`  
		Last Modified: Tue, 19 May 2026 22:36:01 GMT  
		Size: 47.2 MB (47155599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c0097dbea42daca25e9c807e97e9f56b0b22b907dd75ca399671ec5e079e6a`  
		Last Modified: Tue, 19 May 2026 22:56:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fea4c0e8935d9f070076357828fc53fa4a84fb60f7a72a09b336a6e15450a3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4dd28dda985c99500c5d6557b3b040a56ce7a6bebce83bd0d94e17d2bcda79`

```dockerfile
```

-	Layers:
	-	`sha256:87305446029ca4c0f989746154f2615cfad3d68a2d6583f53c1c039d1c7ac4ce`  
		Last Modified: Tue, 19 May 2026 22:56:22 GMT  
		Size: 3.7 MB (3730932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d01dd5f8e7e0e5a99baa5642f412f91770874e3cea266c25950563b3216e9777`  
		Last Modified: Tue, 19 May 2026 22:56:22 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json
