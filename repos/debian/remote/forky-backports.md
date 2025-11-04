## `debian:forky-backports`

```console
$ docker pull debian@sha256:945d9ded9b8a2fd1a591a61c201617d8bced23b7680cced6ec823db80f587b49
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

### `debian:forky-backports` - linux; amd64

```console
$ docker pull debian@sha256:5c787b1090e186e1c33d3b53f57cb81c3c35c3bf947d4d3786c89b6117281c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48481587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c51a4ae991953bcbd3defc5d5cbacf6c66544c9c83ae80b6463070093e686b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 00:16:33 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:186ca733686ffcaca03fdc512b51c9498f39b93235775cf08154b1ff0b143901`  
		Last Modified: Tue, 04 Nov 2025 00:12:56 GMT  
		Size: 48.5 MB (48481364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44d60e3d83b80bafcd63d5d531ac1fa79056b549f833a9a767ef6d144446f22`  
		Last Modified: Tue, 04 Nov 2025 00:16:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:055cca928433a01927dcbca0475aa092b0443e8f2a7956f510a6c4677cbe62cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3135315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a01630c1fac596b0c7457d5493ab30c315b97a5f979aab66d77229dbe15351`

```dockerfile
```

-	Layers:
	-	`sha256:0c7757f11ca76fd59e87c3b2dfc05558349ce83915ab5e2b62e36fff646861ae`  
		Last Modified: Tue, 04 Nov 2025 10:25:47 GMT  
		Size: 3.1 MB (3129537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accb3174c512bc31d4d64a77798b7f9ed2ee0ea11b44cb0ca4813e20d293c40e`  
		Last Modified: Tue, 04 Nov 2025 10:25:48 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:05ddbe1911ee7bfa0d53a23713c32904bcfae9a3e681c0e92a4c180c05c0aefd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44987872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196c556c3fb888787945569ed1e6b4aae82bcd64d197859a655c1717eef62cae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 00:16:19 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1a3f9ca9ddd6f8d1ee0ddc59ad7ed9255992d14a1e28dcd6f3a00557f6d1c188`  
		Last Modified: Tue, 04 Nov 2025 00:12:42 GMT  
		Size: 45.0 MB (44987650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782e1184a8da02daae326876f3ec33a58e5f7bc46ddbfda866c31346886ab0fe`  
		Last Modified: Tue, 04 Nov 2025 00:16:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:dd975465483ec5f5820518f44a6423cd631454011ad2e7d6749a014022143cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d5205140611a12e7fc0fafa0b5489b2fc8b787154dde4047d819e0756a825b`

```dockerfile
```

-	Layers:
	-	`sha256:39586a4aeb1cc5d06de2b2cbc5ad0b52c1dce070ec4458526638169594518dab`  
		Last Modified: Tue, 04 Nov 2025 00:16:26 GMT  
		Size: 3.1 MB (3130905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90af8d4a9434e3795dccc8fe7f1b1944aa316a751a61b442cfe92449d7367fec`  
		Last Modified: Tue, 04 Nov 2025 00:16:25 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:792c255ae627eacaced0fa011d1015b46e3bd722923063dbb085bbbb62939593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48583861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:848daf8a00608f236017727b07c9b91cc2807c2608aeaaa46c80d7613003eb2c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:17:43 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:52d2706ca00f3431b3c37b306b3eb6cc4989781e31180bfdf93c4dd4108e1e3c`  
		Last Modified: Tue, 04 Nov 2025 00:13:40 GMT  
		Size: 48.6 MB (48583638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774edee1144a797538b42d3c7fe9e45c5f1d6384473e61b892b57ba45e7163a9`  
		Last Modified: Tue, 04 Nov 2025 01:18:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3157b3ccea842b413443788fade20374393cccfdff7531817f00157abea8330f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8128bd520d065a0d85e2e63c65f774822878a16c5ab18a13c2981cfe8d66006d`

```dockerfile
```

-	Layers:
	-	`sha256:4ebb87e1cc988cc6a73f3951948e3086ed964730eb1d09b402a9f887bdd9bd69`  
		Last Modified: Tue, 04 Nov 2025 01:17:50 GMT  
		Size: 3.1 MB (3130378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26a7c10b8958e01ed7fa0e3b3bf52090d5779790b1aa552cded63ff548780bbe`  
		Last Modified: Tue, 04 Nov 2025 01:17:50 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:80b40fbd3ba0991d52fb8cfd22c08fe603131e110f8068a0932da6c1ceec08a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49809722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21dad5a61cd1218a513553076a57ef4148ac072bb78b15adf4c88aacc32f0d70`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:17:29 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bd86ecb6d3ac97cad4df6e0aeedefdf1790afb18f99112bd09ea68844e318978`  
		Last Modified: Tue, 04 Nov 2025 00:14:09 GMT  
		Size: 49.8 MB (49809500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a9ad61f516583dae0f4eb6f98db02e1ef1549a36e202065d0150bcf21ee5f4`  
		Last Modified: Tue, 04 Nov 2025 01:17:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e6a3e6c59c802a19cd4358e53c98d96ec464f67e19484ab7b7ce619e4322c775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca059d92471e702cceddb4c817cf8b780fd3d7c382740cb937a614877aa6abb0`

```dockerfile
```

-	Layers:
	-	`sha256:93f6c00ca72e07e912cf1e3a9b3af4adfec68c7196dce9745df073c4e4c40ea7`  
		Last Modified: Tue, 04 Nov 2025 01:17:37 GMT  
		Size: 3.1 MB (3126746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ae427eb0e94954e70d71b5e959dc6b85affeefb4280243571b25a693bc030d`  
		Last Modified: Tue, 04 Nov 2025 01:17:36 GMT  
		Size: 5.8 KB (5760 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:6425cc95d1ae65010be2a9a9bda54061b9452540ab14e3b00766bd54a23db20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53315462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d699cfe7f98864d7e457d98ff887cf6ae7ad1104245dac9cc1c5199c011341`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:16:38 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9422d47ff8508a211c5181db20a5b72bab47758f9bcd0687b05752ead1b35a5a`  
		Last Modified: Tue, 04 Nov 2025 00:14:32 GMT  
		Size: 53.3 MB (53315240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90a0262c729fe506b0910731b6394c72668d5493197ceac363a0d0488cb0347`  
		Last Modified: Tue, 04 Nov 2025 01:17:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:366ae5e156e4757b4e659e7613b0f109ce23fdb4428097519012e54cadec882e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddea961a3c4b6936eb21cc61a733f87f0c6932e983bf31b6121f6db31cbd7c1`

```dockerfile
```

-	Layers:
	-	`sha256:c457bae33f3451df6a02c04e7bfc75f4c403d4f82eb8a44b78d3484ecfd48145`  
		Last Modified: Tue, 04 Nov 2025 01:16:56 GMT  
		Size: 3.1 MB (3133026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dba6ba587f1a368af75817b0d878229e769259c0d7978f0a42525bfb797e49ac`  
		Last Modified: Tue, 04 Nov 2025 01:16:56 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:bd31f1a0f9417d523d70b80bcda53cd4ee8979aa7b615ed1bbe4014a9d719306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46791348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6894dae8e8ab629861fb6dcec1059a67039f705015d549cc0dbf292809d4d6ae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:17:59 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:81afe9ed9d72ebbd06999820f64e36aa62bc978725062b4cc32efc39c6a99213`  
		Last Modified: Tue, 04 Nov 2025 00:13:41 GMT  
		Size: 46.8 MB (46791125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf706f26189ec92bd8b1b973e142e9d62839cac2656e3c210a0f6c4338970682`  
		Last Modified: Tue, 04 Nov 2025 01:19:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:be7a7e5773769c10b18220a0d8629ff3406a6c62784bafaa265a047170012d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3360a9a5e9b7a38d0f536334ffffbd65592750ec06552934264dc3dc13843f`

```dockerfile
```

-	Layers:
	-	`sha256:1adb4e4fafdb387907e0316874c685c0e3f419ad26201ea9996d7f0bac4732f2`  
		Last Modified: Tue, 04 Nov 2025 07:28:28 GMT  
		Size: 3.1 MB (3121836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b5558d66ad2b4082167870128fd27e7e7a49869b27945952309683c0008e7b3`  
		Last Modified: Tue, 04 Nov 2025 07:28:28 GMT  
		Size: 5.8 KB (5803 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:0a41824a191ce1d5c0b3d3186dc4e96bbba9e914551228dbb57d40f4775a1c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48343286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63d394ac31ffc5cd971211bfb60a238dc975e655f89d7dd61838c167e29c221`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 06:40:34 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:aa89048d1c3c931b297cf2d408ea7138528530c43e452af625223e71f97282b3`  
		Last Modified: Tue, 04 Nov 2025 00:14:09 GMT  
		Size: 48.3 MB (48343062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0a62be9a1e0a60ed7eaa92972c892f1dd4072432b7c10a3b22e65eaeb5cb1d`  
		Last Modified: Tue, 04 Nov 2025 06:40:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2baf7cb6d4258c286627da7e762ca832323e9b18f416369ba9b7a44d29aa16c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ac72fc038c9d8000b7678c7b3ed039d525dca4fd1eb69b541efb9352bc9378`

```dockerfile
```

-	Layers:
	-	`sha256:58af562d7764045426fd302234b1314e02c5f0c191aa36c041d7b779f182d907`  
		Last Modified: Tue, 04 Nov 2025 06:40:51 GMT  
		Size: 3.1 MB (3130986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effca480b54a8bec54d287524178b57be37c0f3cd7f150df33bb609cd35cb282`  
		Last Modified: Tue, 04 Nov 2025 06:40:50 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json
