## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:8b7510fb13d5e08e7c39744b3177486ec87b31f272c15d2de421be0929e7abb1
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1edc3c13d07945e7f48e3751699c3787ba7311cf2e73194b401c1852592f390b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74241363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4749af358deb69d2559ebfa9dc7d95ed096464a8caa7d607943289795d2dbe96`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2aa53e779a14a678b6be0553334055853528ebc9774eaa3e69e5fd71326114f8`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 49.0 MB (48967949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505e1c0337e142d28ab6c58fa7e5bf319287c629af695b520d6eb278c386eca`  
		Last Modified: Tue, 08 Apr 2025 01:24:25 GMT  
		Size: 25.3 MB (25273414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1d5b0670b6f2ea040e8bf3d615384c2ee3e09e7d4ecc2823c17322ed859d3539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c36c5886035f02fe6b1a812b79bdf09beabb6b6fd5d52fdc26514fc4a9f38a4`

```dockerfile
```

-	Layers:
	-	`sha256:ccaf6a3ed903ed7e66d3c0e65224304271aad99b34b7d740d00c80d5daaa44a0`  
		Last Modified: Tue, 08 Apr 2025 01:24:25 GMT  
		Size: 4.0 MB (3978433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e30698ce4837d1320f9694ffbb7e1fce558dde1c98c371f517a2ba0ff33478`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v5

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; arm variant v7

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1ab715a4c1292947d892e9c5ea768b492e73142f247c0605146cc23fb4d0d016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76774859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743cd08777d274c7f35922cb4fe74f67e7ecdb6bcd7dfb00b9184eb42c00ea58`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a0f0bbaf0e5a890ab90a12e5df307c321a3344fa0accfb31dc895fe008c16f85`  
		Last Modified: Tue, 08 Apr 2025 00:23:19 GMT  
		Size: 50.5 MB (50476501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686927d82bc30ed67f20e1ddfb9d146b7acb12e90c947c73db07541c131a8cd5`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 26.3 MB (26298358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4040f394cc4fec7de07b3ac3f1c21095a5a44b54b60144ac54de24b4f179eeed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3982268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6458115f46696dfce93210a45717c34faca044267ef77101171728fd3d6f02e`

```dockerfile
```

-	Layers:
	-	`sha256:d303edf3c6b17ac93c21bf6527826dad879864d5337cc81ac114a2bbc1a441a3`  
		Last Modified: Tue, 08 Apr 2025 01:24:19 GMT  
		Size: 4.0 MB (3975486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d506016603db48e2104954f1c11f60d54106d69186e6e6456a1d8e0f93e14259`  
		Last Modified: Tue, 08 Apr 2025 01:24:18 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; mips64le

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; ppc64le

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:793dcbced553d90aeb352501b5436f13f7edc9c5b2d252623eab8bb432b685da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72093002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16071853fa5c0f0a66f7dd2e3f445559233ed16e5fb7e34031165a212a9d9cd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9c53dca7ad1a1783f586e5e01ac8c6a23808333e74dea8e73cb813fed1a625b5`  
		Last Modified: Tue, 08 Apr 2025 00:25:11 GMT  
		Size: 47.5 MB (47479327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffe0734c1595d1fe0c36013a6078b10a14e39d1128a06575271e9a043d41f2a`  
		Last Modified: Tue, 08 Apr 2025 01:22:05 GMT  
		Size: 24.6 MB (24613675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c50726997d95485856a2a7c6b9fc4baa5eb66fa38a838786c2b432830ba56da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3977911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ac8be7dbe286f41c4d12f2623fe57b15fae6f3003237e1b43f10de76995c6c`

```dockerfile
```

-	Layers:
	-	`sha256:a4013f0174a24261e61a84e9876e1bebb4ed266306b9d9bc2763e6ebd59c98d7`  
		Last Modified: Tue, 08 Apr 2025 01:22:02 GMT  
		Size: 4.0 MB (3971075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aac204f78c07a5722f6540540af32faa5af7a031541162e159a070af6ea5416`  
		Last Modified: Tue, 08 Apr 2025 01:22:01 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:33b23bab04106e23161204a3311ed81600e2bc7d55a2c4d1de07f0af6153d603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75507631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d69f1cff51a744ed05918ee35d6a5c969de0dae4e7968233a7f02cdd3aab6a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4724dabe4aa05329c356a033beb752bf4d3d8e15762c4c9025e18f8b74f6a65`  
		Last Modified: Tue, 08 Apr 2025 00:24:40 GMT  
		Size: 49.0 MB (49047465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b70d32a5e527bdaaef0ef8d058290901aa64df97cc259e7f2fd2e845c51227b`  
		Last Modified: Tue, 08 Apr 2025 03:45:05 GMT  
		Size: 26.5 MB (26460166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2856b0f32493e95349154b2d89a3a01c96d1fbfcc4a2bf0525b4e631b9fe0743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9679e829b8c0e580620cd2db8b2b5daf6624746ed25063a3fe251d25b133f9`

```dockerfile
```

-	Layers:
	-	`sha256:3cc60fcac6da30b40c43c868cb77f40e4bf3edbed51a39a07f727cdfb21a97b3`  
		Last Modified: Tue, 08 Apr 2025 03:45:04 GMT  
		Size: 4.0 MB (3986048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76bd30a8baee6be9cc435f687208a0e2ba6f1f7157f39731326dc009deb3e309`  
		Last Modified: Tue, 08 Apr 2025 03:45:04 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json
