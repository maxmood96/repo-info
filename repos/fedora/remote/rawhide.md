## `fedora:rawhide`

```console
$ docker pull fedora@sha256:0b01a7e0060195a46f0f32bc63bb0bbf114554f76a55409977ac98b626ffb5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:rawhide` - linux; amd64

```console
$ docker pull fedora@sha256:dfb26a5dbc30de897f86e60870a4b4000c7733545e866fd1c03637a931b2d4e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57682335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3276af7c7b76155193e85ec889dfafa3fd1653c7933007b56a0c9f3309071913`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 18:00:32 GMT
ENV DISTTAG=fRawhidecontainer FGC=fRawhide FBR=fRawhide
# Mon, 29 Nov 2021 20:29:08 GMT
ADD file:c2931c9c66bf5ab1f82c9dc9c12bfd0848c39318b4829067fc512332aa4aab25 in / 
# Mon, 29 Nov 2021 20:29:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3b1d0a681b8e8ced1876a5930548a88f190d2f8b9d2c70a65fc5310396c91bc1`  
		Last Modified: Mon, 29 Nov 2021 20:30:20 GMT  
		Size: 57.7 MB (57682335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:a2d49da0fb0cf905fa60b62c3f4d672a7bc15ada13976407f403a903e9c799a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57404615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1562ee981bb1c9cf936fa851eccd48e33f5f1cddd8ee3bcaba8b453466e82d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Nov 2021 21:12:33 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sat, 19 Mar 2022 19:19:54 GMT
ENV DISTTAG=f37container FGC=f37 FBR=f37
# Sat, 19 Mar 2022 19:19:58 GMT
ADD file:45b140b6bff51b337f97328705ea18d044afe7296544d671030d94aaa9ddbe6a in / 
# Sat, 19 Mar 2022 19:19:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3d8d377c7244dec052dd9d8842d162a4b68e98db2772f0d8ca69de62ac54dc0e`  
		Last Modified: Sat, 19 Mar 2022 19:21:21 GMT  
		Size: 57.4 MB (57404615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; ppc64le

```console
$ docker pull fedora@sha256:4a510d07d9aec6c493b4f13357d8311a41d2aae246c311f37cbb4e2e67dd9be5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62980449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cce92b36cbbb639daa3774e25944168aa7a7ed40f32309fd8421fd7137425ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 23:32:50 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 04 Oct 2021 19:40:57 GMT
ENV DISTTAG=fRawhidecontainer FGC=fRawhide FBR=fRawhide
# Mon, 29 Nov 2021 20:33:31 GMT
ADD file:be08ca3f825838838256ab8aad40238c9a808f382fc03c57f90160ee5ce63fc9 in / 
# Mon, 29 Nov 2021 20:33:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:710ac37497921380d46eeaca9894776ce53491e6470e8f1110d07a06e1f59921`  
		Last Modified: Mon, 29 Nov 2021 20:35:17 GMT  
		Size: 63.0 MB (62980449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; s390x

```console
$ docker pull fedora@sha256:84fb0572e7ebd3f2847d5d69eef533625ba5514b591fcd28a40c0c393f4e3140
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56287802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2b607837d5b8ececeb22e8104ca9ad6ab1229ed572e1ad7de466cbfdeec7cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sat, 19 Mar 2022 04:31:50 GMT
ENV DISTTAG=f37container FGC=f37 FBR=f37
# Sat, 19 Mar 2022 04:31:54 GMT
ADD file:4352aa085a28d5f4122af5f6b05ef11908959125b902e64a3fa0212749142bba in / 
# Sat, 19 Mar 2022 04:31:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ea4a4864b69be6130a159b80d50689823b28038ade6df5cc107718068e755115`  
		Last Modified: Sat, 19 Mar 2022 04:33:07 GMT  
		Size: 56.3 MB (56287802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
