## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:c8545d9c828024316ff12d0c57c0d88e4a7252d8ad5b334d47077839aa508312
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:3859950a7e03f049b474d8f7ee6bfdb4f145c6fdde403e1fd4c6edc3e013dd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48494736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f28a9515d648dfabf3c2aeab08c3803da51589140638ce23cbbefc8abee1bf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd6ebd4509443684dda2389fb6a49448f53321962bfb8e8b2f39a28d76e0d9c`  
		Last Modified: Tue, 12 Aug 2025 21:10:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5c599fe4671b7f2146b778218ee431e8a7084fd854958fc4b894c0fbf91681e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc4f0d7b1e8b1783f8825811ca8cd6a91f8895bc144997670c48c1c21188a24`

```dockerfile
```

-	Layers:
	-	`sha256:efe7ccae6046ff9f8f77c7190129cd8485192e1fceb553cdfede41fbedaf1fc9`  
		Last Modified: Tue, 12 Aug 2025 21:24:58 GMT  
		Size: 3.7 MB (3726838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcac9963f4eee09e4027dbd9c6f91305c2187b268b455965032ffd48609ab1e0`  
		Last Modified: Tue, 12 Aug 2025 21:24:59 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:39b62a381e2ba5e2022b49276581dfa6b470b2ddd480476502b354f8462ddfc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46027460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62005fff8a7884aa1fbbe032c25c5b0d8b18fd32681eabd4ac332f8999c8220f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ea0d25317149dd26fe3fc21f7a1766f8528af12760c2aee4e2fa23834000897f`  
		Last Modified: Tue, 12 Aug 2025 20:44:49 GMT  
		Size: 46.0 MB (46027235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30957b92f0fd84360e475cd69a0e205e9b56253b008c41145f39dae30a8129a5`  
		Last Modified: Tue, 12 Aug 2025 21:09:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e79de317d14e063507c140a901fd1e32a7ab5c2a09deb53fe1280a23a44855a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccccb632ed141001542ab1e64f3992b0e2215818994af2d3f874804b976f033`

```dockerfile
```

-	Layers:
	-	`sha256:095c3ded53f9cac250ce989c3ec3e8712b0b7ccf55da5c461947d42e5b08152e`  
		Last Modified: Tue, 12 Aug 2025 21:25:03 GMT  
		Size: 3.7 MB (3727039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20100862532751d06f326c672aa7052505097fac1a35c6c0ceead2ea60ed8d1f`  
		Last Modified: Tue, 12 Aug 2025 21:25:04 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:beeec964b3017f9426aaf425eccc9120348e95e4c52f55d3ddf3c4373124a455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44209266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a5bd203e7e326eddf561f5ad08f62f068429e438c61a57a04e893f4a985422`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac26dec81a406b91e7ad3d11920472be22a80322302c52282872832ec486e77`  
		Last Modified: Tue, 12 Aug 2025 21:09:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a83e2381727282ce7916580f5c5a3884549041087713690f57a11b123fe6e39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3734916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10eb7e77bd2d93e3219076630625598db18d77fc330c0d2d54ea951ca94049e6`

```dockerfile
```

-	Layers:
	-	`sha256:cd558a12a0b80aa80dcc4f730fd25d8e3c14699b30473dc39e6db0a1a3d0dedf`  
		Last Modified: Tue, 12 Aug 2025 21:25:11 GMT  
		Size: 3.7 MB (3729017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3d1394a0372f1b3c3280629df2d6ee899af63b5c90aaa4982ff803c7192ec7`  
		Last Modified: Tue, 12 Aug 2025 21:25:12 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6ab7ac0aad0cc8ed5b2bb36ae8c5751da59eadcc23326f0d431b1ee61a3a92e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48342675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8841853aab997993d137df8c0523ba752b10fc9a6720c9721e7ca714f02b5eae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ee3d0c9e17063155bbb430a620539df1987483e4359a5198202a0ce0b4fbb4`  
		Last Modified: Wed, 13 Aug 2025 02:15:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a54fa80bf0f27202cdab3eb39047f7d9028d79289adb6113ff850bb0197275b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f089a7d1cfc5af3a02965c62dab03825caa11dcdf3b7825ec778024c8f5652`

```dockerfile
```

-	Layers:
	-	`sha256:427816309e8a65b9d91c4fccdfaf8f7a23cdd6fd7fdc37b8a7a085fc4cbe5b14`  
		Last Modified: Wed, 13 Aug 2025 03:23:54 GMT  
		Size: 3.7 MB (3727053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60e9e6a056d56f1a6c549669ffc17eb068d6eb805371425499e64802ee4469b2`  
		Last Modified: Wed, 13 Aug 2025 03:23:54 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:5b057f78ce7bb2f00e1eb83bbd3cf901381976099a12ecb660cb6d7e9b846d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae96c55db9872efa55e54fbd6f2ca3625256688d054f286b22706525fcb7849`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84148fd8f780fda45e38d8530874207c5571e13c6d8a42331111376d4df7abff`  
		Last Modified: Tue, 12 Aug 2025 21:10:01 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:97410d7e95edf270bc2a23c865e8021a2682f5fa2628a69664e430c616cbc423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be521ad6c2484f22b1a0c669ae15605679bd4e207630e7a92d82ce941da05c5`

```dockerfile
```

-	Layers:
	-	`sha256:6040c4262d95e00d59b72cf2450fa1fe1c691d019da3b260cdadc30a4806a324`  
		Last Modified: Tue, 12 Aug 2025 21:25:22 GMT  
		Size: 3.7 MB (3724040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d92530d9321263e6f7e3f6b608a02eeec26d2f7007c3200124dc24874d003a2f`  
		Last Modified: Tue, 12 Aug 2025 21:25:22 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:49c648fe345fa8a8347463cb56f446da61beabfc520c52a4130c1ceba05de3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48776879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b5644385178889f5b5b7adec1a439da6d99babf06d5bc5a1baaff97394edb7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:39ab9a968f454fda0ebffae415d31434cb4c4b3f4bb9da0e89f360bd60fa3275`  
		Last Modified: Tue, 12 Aug 2025 21:09:50 GMT  
		Size: 48.8 MB (48776657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc67c6fc63195be6c5431f334bf8b43dbd3ea5c1990b50565282c4bcc222d925`  
		Last Modified: Tue, 12 Aug 2025 21:14:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:dbdf3a868684b3d82fc2133a348ae22da46effb9398ce9f58b16ad7b2e1b6deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc481f6b4f6f16be0697ca574194d54f6e774ca8b0d2557bfc57eb2d92d921f7`

```dockerfile
```

-	Layers:
	-	`sha256:1c03b02032e971771b878006a87af02a05cd0a3475baeaed2340c91cdcede1b0`  
		Last Modified: Tue, 12 Aug 2025 21:25:27 GMT  
		Size: 5.7 KB (5671 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:447e15b7d686749378af67058e29cd5cb12606e3b801e8ca1b1bffc85c8762db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52338302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a51af68bc1b8c986cbc52cdfb0513b3d75718936075c24c7a2deb936aa5b23`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ddf8439d29402d104511e7f71462d95a7cc048520856a3741bf1df17aaeee3`  
		Last Modified: Wed, 13 Aug 2025 04:27:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b8744731ac8b1749bd9dc36926a80761e8fccc2e26564b35a8aed31de0ec13a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c227cbf9e2e2c62ac88e29ec28a9bb1ad054bea07b0ad2e1fb2a913cc4303c`

```dockerfile
```

-	Layers:
	-	`sha256:e698f9c9422aed99f6f8389f8c8cf7aeee37fb61c6d02e8e14d4636e7c95688b`  
		Last Modified: Wed, 13 Aug 2025 06:23:52 GMT  
		Size: 3.7 MB (3731184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6313f63e93d72fa56f4432a61db4bf8ce6ad374043ae397012f68ef27720c1`  
		Last Modified: Wed, 13 Aug 2025 06:23:53 GMT  
		Size: 5.9 KB (5873 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:d4b00672ce89f4497cc768a608df11e54833d8ca153adbbceb3e050b63e53e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47150091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2803727c1725047e2d85e029933890e763f8c87f121cfc2eabd03f497c2dfe7a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4854fd1b0a7338decd312828aeb5cc406af576b82945a482d4587f127a2978`  
		Last Modified: Tue, 12 Aug 2025 23:09:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6d55b95bf6143ee2ce1d44370283982d81c8e3d0084fa31bc070ef30d58f90c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c261db587acb8525e7bcb190c31945739e5a60ac9b945dd4ef3c3203cfb10ecf`

```dockerfile
```

-	Layers:
	-	`sha256:685de2c6173a38098c06236c7f420d61c8ca17b4edde71689b91d85e14cacad4`  
		Last Modified: Wed, 13 Aug 2025 00:24:40 GMT  
		Size: 3.7 MB (3723676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c9841c2faecc7c9122ddd21aa34d2ab831a64391aa0c5985d5f0c98e0b1dcce`  
		Last Modified: Wed, 13 Aug 2025 00:24:40 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json
