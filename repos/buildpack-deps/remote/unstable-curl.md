## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:540356d430734f32c5b2223e2e04008a77cfa396b80ab956ec85edc7b123b3a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a2788682f53c727debe5159f58c17bf9701acd5840a056d3ef008eaf0e5bb00f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73800876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6970ba6285920f38361def9c7b603339b3423d9f562fc26d9f1d7886a34bdf5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:df0497091d0cfc8e931a73bef35cfd57d59f19322fcca6f87470d3b532a9d8c8`  
		Last Modified: Mon, 17 Mar 2025 22:17:40 GMT  
		Size: 47.5 MB (47542630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cd1ca2661836ac2dcfb48519e1a1fcf2b3ddbc182b83cfd451a37cea0328fe`  
		Last Modified: Mon, 17 Mar 2025 23:14:04 GMT  
		Size: 26.3 MB (26258246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d2f2eccc24a5b2ddab2fceb30638c789f54b7447e18f08374242ddde0f58cc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a295e4bfb28701e01e4f3d26b39dcc901231a9fd3a5fa6c00b291e0b9bd0ac`

```dockerfile
```

-	Layers:
	-	`sha256:041540c465b22579a880d623d4aa1a046ca288aa298f06374f3b7647b8ec0051`  
		Last Modified: Mon, 17 Mar 2025 23:14:04 GMT  
		Size: 4.0 MB (3958975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5013f7ddbf9e169be5bdda59b289a6f70b1babf8f7f725348d90af0cacda1e6e`  
		Last Modified: Mon, 17 Mar 2025 23:14:03 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:74ee3ae850668f4ab9f67bd38bdcafda91c3a4b19739b94642b4c724da6a1733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70726670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87af87a2047241d546d31d75affdc36ef7f718a94138322e581f4642f04ec25`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:181ed5745a356167f17446082e0f91fa4520dec07c3cc08122f73d6e68f0ec6f`  
		Last Modified: Mon, 17 Mar 2025 22:18:17 GMT  
		Size: 45.8 MB (45764033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce18890e4323b22dabb2af5cd6dd6ee47e0cbe22914fe96ed5ec5652746adc9b`  
		Last Modified: Tue, 18 Mar 2025 03:09:17 GMT  
		Size: 25.0 MB (24962637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a71070e5bcdc852fe244126e9c62ef57839ba1c57645a021b1ffe1ff633478b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d166e0d9fa2a6e206b9b5b937212848b29ebfa58eb8fa5c190ef3d9275d6ab`

```dockerfile
```

-	Layers:
	-	`sha256:3cd8aa89daccfc89d6695a3857f4d9f42e785b4de79b6dff2a21e21a3ae48961`  
		Last Modified: Tue, 18 Mar 2025 03:09:16 GMT  
		Size: 4.0 MB (3967238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb61975362d879917019afefc1c213d4b362c258867f698b50a5b4aecc9b06e1`  
		Last Modified: Tue, 18 Mar 2025 03:09:16 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:344efb702f263fdad9f06ae0295455f7ae572134496f8e0a84e7a9b6a206f398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68090001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1fc3a45a6b234b832b523ff41cb5d9b50274d4ed8941e8d686ad67eb002b7d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d0067c75852db589ec6309ccaa1c2e508a0e7bb3c58863fcadae19a1c1537e18`  
		Last Modified: Mon, 17 Mar 2025 22:21:44 GMT  
		Size: 44.0 MB (43957597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80d864355272bf90fd1144966fdc99f539dd4252af76ad0a5d7e1ee868d856d`  
		Last Modified: Tue, 18 Mar 2025 07:22:02 GMT  
		Size: 24.1 MB (24132404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:90676ac2c05f4f29273975284a630e6ced1af93b8e2f6bf573123975b9fc4a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3966692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5f32958cc258ae84a4959494deb96420119fc2d78baed6e2af56318433a60a`

```dockerfile
```

-	Layers:
	-	`sha256:66c72c3fa3016a9e4b5c0c7140a6cbbf68845d68154b9ca21df7168859b07b4b`  
		Last Modified: Tue, 18 Mar 2025 07:22:01 GMT  
		Size: 4.0 MB (3959828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:413a02c2c6251fd3f6c15084d2fe255da619cdf6f8bdd886e6d390f7699eb8c1`  
		Last Modified: Tue, 18 Mar 2025 07:22:01 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e0a79d6117c9935f18e569d78de330360580909620a96a04b57489d8860041e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73614780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7779d33f7a6753e050f7f107c50bdd2128ceec27551b83678fbb13e737aa1a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:94a031aaac55d50c4495d8888a65973ac1a320a931aa0e73e9fb6cef43e2efd2`  
		Last Modified: Mon, 17 Mar 2025 22:20:15 GMT  
		Size: 47.9 MB (47916898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9c585ccfb21ec8756fd9ca6b5b83f6e36d0003a2342f6f55b3087ee0d0f4c`  
		Last Modified: Tue, 18 Mar 2025 04:59:39 GMT  
		Size: 25.7 MB (25697882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2154524886d4e7cdef9df8e98923d1b79dff22e4711e465ed3a186fc415a7f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4baad0a2d57c80cd4480d899593b5e45ef9834d11d715386d0f41504d8be4b9`

```dockerfile
```

-	Layers:
	-	`sha256:0f0a3e4ef445b032851edda759c1355e8e3739747b848d9b68adda1e4d859df2`  
		Last Modified: Tue, 18 Mar 2025 04:59:38 GMT  
		Size: 4.0 MB (3960506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58ecf11ae61bc5fae9cf9c825dd3e8497e25ec7842f102e89031f14fc8e138d2`  
		Last Modified: Tue, 18 Mar 2025 04:59:38 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:97cfa441b941ce843b8e64821979dd906d34484a60046cf488a84aefd3a2fffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76259470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9782a0d783450d496881db896b052813aba2f4f816bf2076a9eecec8cb7cdf35`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f3d6c6a3aa49b126cd200d7ce5830c3bb8ef015d44bad711b523cd3cad501611`  
		Last Modified: Mon, 17 Mar 2025 22:18:06 GMT  
		Size: 48.9 MB (48863161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888eee8ccf6b7f4f49c878caf4a23b48de26dc0c12d38b4a0f13ce0b7214d834`  
		Last Modified: Mon, 17 Mar 2025 23:33:29 GMT  
		Size: 27.4 MB (27396309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:40aec232354a0e4dc6dbe28dd5bb7cdf894ea6fcda423cc2b0d54dbaaa1a92a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9774c6726c6676f3f7b0904397f4397aaa8238d00549a9fb2d32f34da395c345`

```dockerfile
```

-	Layers:
	-	`sha256:36109c4c900d01e2580194f48655821fb4ccf5a7303e2ba5400da6b080790598`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 4.0 MB (3955385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f145bcbaeb32ba813657130e55b66ec23eb53395c50ff744887aa2eb4f8730a`  
		Last Modified: Mon, 17 Mar 2025 23:33:27 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6c3ca0ad841c52259fd887c0572f59bfd0445e6ac9da8f5e6d416ca0c3a344c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74033130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963787c310e6b99d79b42a1764cf4ad30ab2420e932f2df9514c82405a485e46`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e12542a0a53bb97cc352ca7ce416a009a12137a70b8b9c3e736be4923c559ab0`  
		Last Modified: Mon, 17 Mar 2025 22:20:29 GMT  
		Size: 47.8 MB (47750847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e581beb347f24f554e5f2cf2d1525cb47adbd2ebd171f2c46bd47fada5257b`  
		Last Modified: Tue, 18 Mar 2025 16:30:23 GMT  
		Size: 26.3 MB (26282283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ded2e064764c7f819dff9b437ad76654f86d031b6c47a680201f120259bb34ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7a577a66283380e62d1db51a9c7874c314b43736d7dc85529c91da39fb2f09`

```dockerfile
```

-	Layers:
	-	`sha256:fc0a991b63b5eb5577c103b83ceede9ee7b8c09b2dcde9815f66eb28e8ff2c1d`  
		Last Modified: Tue, 18 Mar 2025 16:30:20 GMT  
		Size: 6.6 KB (6637 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bb6b86896c67d51995414fc2a0a4e717b3e8798e9743aa517fd2a669f7b1895b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78995589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92cbc73c2d28c0e0f2936abe9fe4b552f4293cff0cdbb79391471d22890b85db`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4f7ad9881f20bb4c15e9c02d5c71121438e0f80af4492bc3595dca35345480d6`  
		Last Modified: Mon, 17 Mar 2025 22:22:55 GMT  
		Size: 51.2 MB (51201856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277e01a580518b309bd39ae29e17784505bd4ae5bf702764ef69018aabfb218e`  
		Last Modified: Tue, 18 Mar 2025 00:01:23 GMT  
		Size: 27.8 MB (27793733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f7f48a5adad28de33790cf6f78ac6ea19615526c32739b5fa27b7f1ef0845afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3975080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f66fc6098c02f5204694ea301086576254b5c2e0fa449761285ee217f8ec2d`

```dockerfile
```

-	Layers:
	-	`sha256:452708de4beb26a55b4584447c6dec5edcfa4d5ae225708d8fdff722c4a11c27`  
		Last Modified: Tue, 18 Mar 2025 00:01:23 GMT  
		Size: 4.0 MB (3968244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:305ce59fb16d8a1bf8e3d1bd7e1877de2177a7fc0b931c35a45833ac54919149`  
		Last Modified: Tue, 18 Mar 2025 00:01:22 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3b9b2fd3533da866c837c75eee0ede5ec295ef3f85a042cf22282f21f60cfd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71644189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a86500e3980bbb8e2d40c73dffa31fe4ee6445549690611a83716b859b8766`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e088c063eb399e547ca6ed33d1ebd46f19289743d98703ba83311c2214184834`  
		Last Modified: Mon, 17 Mar 2025 22:34:26 GMT  
		Size: 46.1 MB (46065424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a540c8b69cf893a7a0a6c436d4761b79fd51f1845aa5b66555a58dc019b8cea8`  
		Last Modified: Mon, 17 Mar 2025 23:27:02 GMT  
		Size: 25.6 MB (25578765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3a08400d4064ed554996ee7dff984b86b75fec2c5ba9b107ee71ab7ee87f5d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3957146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3718beb8abe6420d927e2baf23ad5888b5c5ac89cabdf4d666abe84a9945608a`

```dockerfile
```

-	Layers:
	-	`sha256:2732bac4576e50f6de3fd4f4184d683a377d95fec291369d34b5a38ca3eec79c`  
		Last Modified: Mon, 17 Mar 2025 23:26:59 GMT  
		Size: 4.0 MB (3950310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99a010d31075b9e934746fa417abede9d2cdfdb5aef57765cf5bf370ce57fe4e`  
		Last Modified: Mon, 17 Mar 2025 23:26:58 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5bf4465f9269710d45b4dd77c307d8ea946abd79c3ed78de71808e39166460a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74974060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead82ff34dd0ffd7f338fed7f20842a6d1c629752e2bb297245cea708ba451c0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:18840c5918002e02a891410ac8cb796ccc166700f997d1063ab46da46dc721f8`  
		Last Modified: Mon, 17 Mar 2025 22:42:36 GMT  
		Size: 47.6 MB (47571368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d448240a5617efe437620dbc6c199b4b34036766dc8ba22365b81ef5e32d08`  
		Last Modified: Tue, 18 Mar 2025 02:50:47 GMT  
		Size: 27.4 MB (27402692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b7a7faadf26b4ea72e36fa14e3a66ae1372d285151ab35c7f0b17ff61281c6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3973522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f404a1ae108675ea73a6f15e7844b22c36b6b905abdbf7f1176b0dc52d694e9f`

```dockerfile
```

-	Layers:
	-	`sha256:8c259c35786d85c6666fa9747f4a4b3077dee9a87256adf79de5c641add12fe4`  
		Last Modified: Tue, 18 Mar 2025 02:50:47 GMT  
		Size: 4.0 MB (3966718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e9c11841aa41dd9070c9794c23f7fcaff0228c5274d332c62af7218c4ea2d2c`  
		Last Modified: Tue, 18 Mar 2025 02:50:47 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json
