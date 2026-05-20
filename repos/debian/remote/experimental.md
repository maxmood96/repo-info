## `debian:experimental`

```console
$ docker pull debian@sha256:c048c2f272ce321aa04f372faa07e3dc0a93c88c4730769d2fdd855a5276cc78
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
$ docker pull debian@sha256:1784cc81c44a745d1287aefdf4b9a3e7ae9256ea193ecb88882c913d2f70f15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48712234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd198404aac39a8d23645cee6634fc5bae1626c2549eb15c0bb2f3466dfa6df0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1779062400'
# Tue, 19 May 2026 22:57:54 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:2c1764546ba7d52677a89ed0413b302a754153e54c216b3222678f39f0859f06`  
		Last Modified: Tue, 19 May 2026 22:37:10 GMT  
		Size: 48.7 MB (48712013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae082a07432959531e66cced786aef3af17efbd9ef49218e3cd6bbe9835f65c`  
		Last Modified: Tue, 19 May 2026 22:58:00 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:ad7c84237cb00ad7aff7943f2fc2ae1761925f13247a9f40704ab749b009688d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d933fcfbbf67e6cc63ec231eb8e105a33b4400bd594596fff1c9e47f91adb41`

```dockerfile
```

-	Layers:
	-	`sha256:bb7895e1fa95f7ca517e559e643971eda39fecf5329e2b9d8c0a3ec380eb2490`  
		Last Modified: Tue, 19 May 2026 22:58:01 GMT  
		Size: 3.1 MB (3145088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ec852126f5408a367aafea7b0526f09b5750eef190a1e1a72b24200c890212`  
		Last Modified: Tue, 19 May 2026 22:58:00 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:042e989ab781f86ad3db724cc10c9f4e129fa8cf917d0088a7202ebf296d4fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45619182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c29af930785884177739ab7f516acb075a1ee3d06e4394bd28f123c27493b9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1779062400'
# Tue, 19 May 2026 22:57:53 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:6e73c1b86a758025c60376ff9fd0387cdd2ae718ca62196324dd07acc0c9f410`  
		Last Modified: Tue, 19 May 2026 22:37:03 GMT  
		Size: 45.6 MB (45618960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb804e27a6e2ca95039fe06be7646a3a688b72f93561591e2887dcd03af134c`  
		Last Modified: Tue, 19 May 2026 22:57:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:a27a667e46532c044b7d0f42cb52e35dc11414e591a97c72fdfbc35201233228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29cf4bf0261f0d199f4566b66c905b15997d891d1f69a674dc068e0c485d8ba7`

```dockerfile
```

-	Layers:
	-	`sha256:1c935aa7875bf5997656ca85370c6888674b9ca6bcac0f1a9b7abb84ef9ea639`  
		Last Modified: Tue, 19 May 2026 22:57:59 GMT  
		Size: 3.1 MB (3146458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93916629df9e27658a729e37b1f198bd1277c4f22b5b2bbaa8166faad1683559`  
		Last Modified: Tue, 19 May 2026 22:57:59 GMT  
		Size: 6.2 KB (6165 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d5f23f60d31090de6e9ce43518480c30b6d84301cd24c63b9125b13d62079f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48737839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff78cfa7323ba3a79f038e7d12dc8469725073aa399dbb0cc6078385cad83c9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1779062400'
# Tue, 19 May 2026 22:55:49 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:13c76dc53f5ee08af670ee52efaa266c3eb8abdf31a83a78161d45771206c865`  
		Last Modified: Tue, 19 May 2026 22:37:03 GMT  
		Size: 48.7 MB (48737618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7414d57eed1a337a5f7730cbd90d7eb698c1d2fdf3f297288e1d9fd562b7c4`  
		Last Modified: Tue, 19 May 2026 22:55:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:c647d5d7803df521d99899a47b4c1fdb77587640d65e53408a3c81efd24f8141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94cefed3ac0fccba0781c693dad2895337aaf47440689d3a2ef5ef16bf9b3e28`

```dockerfile
```

-	Layers:
	-	`sha256:e63e738967f45832bb7eae9f703a49859880c8d62d4983c34698b866bce8877e`  
		Last Modified: Tue, 19 May 2026 22:55:56 GMT  
		Size: 3.1 MB (3149770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e1561d38ab95bc60611c1da6c0b6ca657bdaa8d0def89ab0108ddfca4859433`  
		Last Modified: Tue, 19 May 2026 22:55:56 GMT  
		Size: 6.2 KB (6181 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:fc08fd94abb236d562f8841cf61a45c2376afa70b7c9e5be50eec1da90f1379d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50016226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cda89d196ff31569b8cbdd247906c0056633c48b70bce1d1b0c21f3261078f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1779062400'
# Tue, 19 May 2026 22:57:57 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:701ac252208df8a6246f2e260522bee1b1ff14b6e413ce817ab4281cfa97f01f`  
		Last Modified: Tue, 19 May 2026 22:37:26 GMT  
		Size: 50.0 MB (50016005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c5e6b5053e5eae283fed396dc8fc5fc5ed43bcbe11d42fcb9509c3e11e0ac`  
		Last Modified: Tue, 19 May 2026 22:58:03 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:eaf027b493e03072c6ac9bf4209a6c645a16674fe44b7c198235a4aee7ee2a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d413b2ef9793bb52a9ac9ad81397020ea077eda9717413e9c1857cee440c2328`

```dockerfile
```

-	Layers:
	-	`sha256:aa371e128c698a6641593a0a422bb367611158c763e709d440016ca4a772a26a`  
		Last Modified: Tue, 19 May 2026 22:58:04 GMT  
		Size: 3.1 MB (3142282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:445beecc1cf337f8a5c5687b2659a6dff207bbce05186cf6f6ecfccf4a6e18e2`  
		Last Modified: Tue, 19 May 2026 22:58:03 GMT  
		Size: 6.1 KB (6077 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:cdb40bda1238ef0a19d9f352784d09131b0ada6de591ff6bce57b9ef64ff8d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54046345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b9c788dda710cc0f085e39a048fe3d596e678a1c8256888a756f8f48a5cbc5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1779062400'
# Tue, 19 May 2026 22:57:04 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:5fb3e51e629b9b77693ee34f09383fddd90920c519939c0ec2de16443e35e990`  
		Last Modified: Tue, 19 May 2026 22:38:25 GMT  
		Size: 54.0 MB (54046126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573d857f3fc84133b6d173c214fc28ae0df40bf22a9419ff7000024236aa7c3a`  
		Last Modified: Tue, 19 May 2026 22:57:15 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:b2738a6d7ed2efa33a133b0561aa61c5055d5f8651577225e3cb67e7050b891c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e36b952c3f4fa65af991926a82f5825a12c5f09c1768c559f9cd5a2fd1e773`

```dockerfile
```

-	Layers:
	-	`sha256:f261d563fcb8523cf038a4f5744fef2cd8fb9bb39eb778a6840003123b85d5a7`  
		Last Modified: Tue, 19 May 2026 22:57:15 GMT  
		Size: 3.1 MB (3148601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b6e539a90d901113c5feaf5459906d9edcb2213bddf835d6c60e251725db4a3`  
		Last Modified: Tue, 19 May 2026 22:57:15 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:4c536bfb5d2ae1fe33ca3a1e32d18cad7d6da1b64178ed1ae3261175eca40723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46808624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d811e962272fc901e6063883f0ad6566180ed4fead1c92e0b8c3ad6330f2e1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1779062400'
# Wed, 20 May 2026 01:51:34 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:264b7e246f55401df2641332da5222b4151dd5e20f90673905a68e536c2c7798`  
		Last Modified: Tue, 19 May 2026 23:53:23 GMT  
		Size: 46.8 MB (46808399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3b4a5f0d7e0fa808917ffd1916d2aa2e89b5424d3a27657da705adf3bda970`  
		Last Modified: Wed, 20 May 2026 01:52:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:f70f804651e651cfb14d1d3890ccaab56c7bf88473e7ccf7f83176045d2ee0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3142737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54be87d815ce6f21e5a67bd3cd48dad33b635ceacf465bb8e3d3e51a3121f93`

```dockerfile
```

-	Layers:
	-	`sha256:6cb6b404d598312588e6b160ea232c3ce31b95f381d91593572d093affbc6efc`  
		Last Modified: Wed, 20 May 2026 01:52:26 GMT  
		Size: 3.1 MB (3136604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66fb6f43a1ed917cf83009fb97ce0b53b6ca71a5e932fe2b186b2cf8c406d8b2`  
		Last Modified: Wed, 20 May 2026 01:52:26 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:c78ad74987c006eff56b1b49eb82ed08ba0a0bc15efd6723238467564c26f52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48454473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29266708b0977c94877fd418384960573d39f4a9ebc50d764ee6331895626721`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1779062400'
# Tue, 19 May 2026 22:57:02 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:1f1e42b892b93d6773c4ee06b88ec5db06fbed8427a24f32ab05f6ab69243188`  
		Last Modified: Tue, 19 May 2026 22:37:10 GMT  
		Size: 48.5 MB (48454254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e515dbc76fc78c315890fa7b0c296ab33d741e5a95fe384aeeb1f53c86f2c4ef`  
		Last Modified: Tue, 19 May 2026 22:57:13 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:9fb135310f27b43dfc3d76da758ee699c2e9429435798d4f350b0205f3972d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5912c1fba38d6c033be3d676a9ee8a279e14382f05f1f17428108cd7c6596309`

```dockerfile
```

-	Layers:
	-	`sha256:96ad314848d8bad1c617876301b215c195218f93483e22a01aea0e76caaa410f`  
		Last Modified: Tue, 19 May 2026 22:57:13 GMT  
		Size: 3.1 MB (3146539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55cd0e2eea5610db797b10d4e25a1e36a4b3fa1fcdef65c643ac742277832155`  
		Last Modified: Tue, 19 May 2026 22:57:13 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json
