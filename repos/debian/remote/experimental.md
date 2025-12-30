## `debian:experimental`

```console
$ docker pull debian@sha256:3deecc1feedf484c5b901b90a45834c2e878e516f81d513938179fe26659fc0d
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
$ docker pull debian@sha256:f367de46dd3559593b5db08714377cb8b2b319c4215381b4c6437d7d19c75e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48821344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde2cf7861484472233c71d77af38e35b33d616f55755770367f2c91aa9e50b9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1766966400'
# Mon, 29 Dec 2025 23:15:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:347bbd8c29bc38e34228debd6364d80e7184750d6554ffcc3f848e1f145b9399`  
		Last Modified: Mon, 29 Dec 2025 22:32:06 GMT  
		Size: 48.8 MB (48821123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1583f5fe563a04220592f20615f9ff4ec1b2af2daa47866c626269c1cc2e36c3`  
		Last Modified: Mon, 29 Dec 2025 23:15:30 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:297bbde0bc4e615d11b58c6bbb4ea41474b3c9187140639a51e61a4a61485923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd2972a6497bd3825c9061ea071502f312c5d2d78898fa63f4780f546b10d34`

```dockerfile
```

-	Layers:
	-	`sha256:77e57b06297e2eef1c1c9756cac61c8f4832457d4b73ced6beca9a45c93ba1bb`  
		Last Modified: Tue, 30 Dec 2025 04:25:01 GMT  
		Size: 3.1 MB (3142361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d663d0fec2ca65ac1dca1b0447c1bae3e274ea707f5b37858f76f03506e620c8`  
		Last Modified: Tue, 30 Dec 2025 04:25:02 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:5f7bed9766a7f01eb8bd21248c5ee98b59a9a32aa3cfacbc765ab8d9ae39f2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45112723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b73d7b4e67eb6d3e45c807171c3483e0bc6e0cd759c86a339725daf7b9f57be`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1766966400'
# Mon, 29 Dec 2025 23:14:19 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:d8eb23e636ccdf9a41cfcf7c042d54d33a12bf4cae266b9bdc25b3e3e4335599`  
		Last Modified: Mon, 29 Dec 2025 22:28:12 GMT  
		Size: 45.1 MB (45112503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc3351aec56ceca57b95ededb066d9221108819ce563db63f9b15a1f892ee70`  
		Last Modified: Mon, 29 Dec 2025 23:14:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:3a5d7cfbfbc3b78462b30dc8af551fd95a980e994fa6830570bbd0eee0a94c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f152a5531225a4a3f351476cb4e4a43294d50e10d2f0a8850544929ac825bc`

```dockerfile
```

-	Layers:
	-	`sha256:1f9410f112e0dad93c255c373db0322d726e36d899864158f2e9b3defbba971c`  
		Last Modified: Mon, 29 Dec 2025 23:14:26 GMT  
		Size: 3.1 MB (3143737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c92672f19b345370bdccfe8560747476cf73f5fb7be39bf212a6b68d7ec12caa`  
		Last Modified: Mon, 29 Dec 2025 23:14:26 GMT  
		Size: 6.2 KB (6165 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f060aa80391d56f4879f5dd049050435785d8d010953b850d77e37e3881918c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48801255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3df84f8a17576d7a2cd7bf3b33d23488b1b04dddbf0d7dfa5ef58a53de4639`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1766966400'
# Mon, 29 Dec 2025 23:14:03 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:cb582f2c56919e9f0069f2bef686730425ad86d5ac592abc904e7dac0d90f4c9`  
		Last Modified: Mon, 29 Dec 2025 22:31:27 GMT  
		Size: 48.8 MB (48801034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65e0fa2575cea8aead8b5d50298540f5997c52dee6de6071f9f2f593e5f85cb`  
		Last Modified: Mon, 29 Dec 2025 23:14:21 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:98b87c9ded8a5402fb4ec3c46c869878f975b862a7d90843911018db35ef12c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28f72adca101da4384719ddde60d6a96cf51ea783ee57a857cceaa92f2ce528`

```dockerfile
```

-	Layers:
	-	`sha256:abd5dbe5b9649637845c4ec3637a2ff0cf1259b3893d003c8ceb58e54ac2db53`  
		Last Modified: Mon, 29 Dec 2025 23:14:10 GMT  
		Size: 3.1 MB (3143214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f2e11ab0bf065e5107750be2e98dadba315edc3caccec7e151250210a2b0f92`  
		Last Modified: Mon, 29 Dec 2025 23:14:10 GMT  
		Size: 6.2 KB (6181 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:0c020ea113ee3a1cc33322bc26c0747cf478bb09d2077e58ed95043860d0b14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49939371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3d30d33fd59cba5147c8f778ddf56ce3b75568a325972b4afff694838dae5d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1766966400'
# Mon, 29 Dec 2025 23:15:23 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:38ff80ad37e7d6d1e5ea7f338df05f56907f52cfc431a90fd7f00e5265f4e4df`  
		Last Modified: Mon, 29 Dec 2025 22:27:52 GMT  
		Size: 49.9 MB (49939151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f893ab10c52e078f4c5de8423cec45b688fbd813976902fc116e6166b7349c6`  
		Last Modified: Mon, 29 Dec 2025 23:15:37 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:5b9886d53ccdfb252dfd424e08d8e5e584115dd75fdaf2db8c924ee3a2de4030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00180d9fd3fd696172c86cf7ac693c380aaf38256bb953c615a7b6d8fe876957`

```dockerfile
```

-	Layers:
	-	`sha256:f0af5a4f2e05220e0170ddad6e11f9035d532a8ac615323f60050e1a36cf76d2`  
		Last Modified: Mon, 29 Dec 2025 23:15:31 GMT  
		Size: 3.1 MB (3139560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f41da1838164fdc8bde97084908c329496c7067624adcde31dbcffa725cb426`  
		Last Modified: Mon, 29 Dec 2025 23:15:30 GMT  
		Size: 6.1 KB (6078 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:5ed06e72c4db1fd89442ec78b15f15146d4f7e7f212b9101555365caf4ef9f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53505140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a0f0e14649a46b3d7ae88502663bd712c0a1972aa7cba9b2b74ff800260357`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1766966400'
# Tue, 30 Dec 2025 02:15:13 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:c1c1995f6a4c01edc5c3cc88d95b0e6d5c29a78edcef774e56563b0cc5b26625`  
		Last Modified: Tue, 30 Dec 2025 01:51:42 GMT  
		Size: 53.5 MB (53504922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b156e381927be682cb4558a4c099acc24e893ef758a909e861575478a8c4d27d`  
		Last Modified: Tue, 30 Dec 2025 02:15:30 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:72ecb7ec89a54e5238bdd098c78d1bafeae5ea36f5d0f757ffd9012ac81795f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6a6c6d8e341b6027ba8c6eccbd26aa95abb9c6e0039d440e77a4ba27623388`

```dockerfile
```

-	Layers:
	-	`sha256:7707d811233bb932d5a8a5aeac40e616e0bc727285d0ca5a0f2c932728d3e6b2`  
		Last Modified: Tue, 30 Dec 2025 02:15:25 GMT  
		Size: 3.1 MB (3145870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fbceaf7538127b1bad263e177bed2a8158de88731a77f5054b9ffd87a7acbd0`  
		Last Modified: Tue, 30 Dec 2025 02:15:25 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:c9c315813c4da7fa099eeaac172d8d5ed9b9be9162adaa75f1fb0cc8049737de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46843065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bda4006392b42eafa4277e7ba9cfb17986d8d406de712a5098ad3b0f3a3cf0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1766966400'
# Tue, 30 Dec 2025 01:25:48 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:2d8e64e51150f32281d8598b7f91d33cab4a9a2f8a00521eedfffdcf6c75c14d`  
		Last Modified: Tue, 30 Dec 2025 00:55:38 GMT  
		Size: 46.8 MB (46842845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a715e4f559f78dc11d9664e5240f01548be87ab63e4ec75896364e88217bd8db`  
		Last Modified: Tue, 30 Dec 2025 01:26:46 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:71fc7e2f5bb085de2e0c52b866eb7915bb834cfbdd77506375b3eb2e6b01cdb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3139998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c7c177aa41c5ecff02634b7ae281487b85ec5e8f64d082e4547788b8362094`

```dockerfile
```

-	Layers:
	-	`sha256:d0b9bc2318961eeded7de57b22c26e61ab24252e0e923c05fe4bd5a0b8775b4e`  
		Last Modified: Tue, 30 Dec 2025 01:26:42 GMT  
		Size: 3.1 MB (3133865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6160fb713e8b0a8168ad64d6d16e179fa0dbaa233b4a2eb9ee6b8261319c71a0`  
		Last Modified: Tue, 30 Dec 2025 01:26:41 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:388287af94b54d9867ae9c199f77ef1a2f0a704979622cf85b21726ce47ee571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48375580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab041c6c5862777974a6772162ba125ac42d97bb70d12c104c04907ec7a6c153`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1766966400'
# Tue, 30 Dec 2025 03:22:56 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:3be197e351af10470b9c435b59f0ea490c26ed188e178d50db3392edb18e57d9`  
		Last Modified: Tue, 30 Dec 2025 02:09:45 GMT  
		Size: 48.4 MB (48375360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6268adb8f469a01e957133deacf18252d6bd9bbbcc9ecd6337e5df624feb4b`  
		Last Modified: Tue, 30 Dec 2025 03:23:15 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:7702751ebe8de63d331f8c99ec87e8f0877f2daf0dcc772cff13e533ffcb29f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da676b0c5bd349cc050e277859ac3c8c797d6d4e2da438ba21a1d34d971f4817`

```dockerfile
```

-	Layers:
	-	`sha256:227e7d99e481cc31d6a3372b5724e352d0ba23f00eeffcf76c684024bd219070`  
		Last Modified: Tue, 30 Dec 2025 03:23:11 GMT  
		Size: 3.1 MB (3143810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:483c49ee5eb915d7bd904476df1b41b35035edf685a5b4051edc09f7857125eb`  
		Last Modified: Tue, 30 Dec 2025 03:23:11 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json
