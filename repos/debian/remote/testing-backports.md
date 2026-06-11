## `debian:testing-backports`

```console
$ docker pull debian@sha256:e7c5f4c6c02ffbaf113aefe504517a8b6595e4794152ea34b8ab9f42edf848c2
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:a2443bd954f707178d18dc27faba4b510d9d9251ab3f5afc7e796dfd0c6a4a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48779499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d780bf2c0838c8e28c321b87c78753ba012a2f7a5a1a809667fc16cb2c83fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1781049600'
# Thu, 11 Jun 2026 00:15:58 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9fcbe81726325315e419e96d2d3462a068d809512f102a51a6a2a820988cae49`  
		Last Modified: Wed, 10 Jun 2026 23:40:23 GMT  
		Size: 48.8 MB (48779277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d3911ef0963047ab164c9693303c30c49e89eae0cb7f1f06cfee5661760b6c`  
		Last Modified: Thu, 11 Jun 2026 00:16:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bc68eb9cef2d6db24604639589791d1fecf149ee960989b74d43768b590bb1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3159768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d31cf4b7b54a859aa5b688eb4384447ba310bc2efe6dc0a9c4c9298c4ba51f8`

```dockerfile
```

-	Layers:
	-	`sha256:3293c3bec70f94ab5e4f0db154532d0bf776ccd559ba65b0747400b85547fff7`  
		Last Modified: Thu, 11 Jun 2026 00:16:05 GMT  
		Size: 3.2 MB (3153974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2200d39580961ec5f5df47c66315fbef3626fd4f7735280bc04782141fe40e97`  
		Last Modified: Thu, 11 Jun 2026 00:16:04 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d1df9268810f318eba70ae2f9ecd364dc9e95e9a9d10a5ca7131c5c934bae1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45676786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b50384d67834c9f5b78057a74881ac29b90fc129b6ee3def81e776961dc27d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1781049600'
# Thu, 11 Jun 2026 00:15:17 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:abd05c63c4e563f690f1b36bc71dc45c5635c07510515880c6282d4df1f8b1ae`  
		Last Modified: Wed, 10 Jun 2026 23:42:33 GMT  
		Size: 45.7 MB (45676565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af4fe6f2db0f7558d2530d01e5c0b4467b3395c5b3d8c78f23cac494f300824`  
		Last Modified: Thu, 11 Jun 2026 00:15:24 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:41107e2b10ffaab746adbbf38c5282fa74c9bdbd3b6e00c9047297d555606875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2308620c3d9858728b00d85bc235332a107de5a18ea27e3bac1e76ab76338780`

```dockerfile
```

-	Layers:
	-	`sha256:8321adcd79ea4fbaec9bfefee4ef03dd9ab773546c0c4067416abdd76f75d979`  
		Last Modified: Thu, 11 Jun 2026 00:15:24 GMT  
		Size: 3.2 MB (3155336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e9e2b0b84669cda2209341b37cd3e60418073ad476941e78e8d656fc564935`  
		Last Modified: Thu, 11 Jun 2026 00:15:24 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:166dd31cfcfc29058e4af1a5fb2d284b32d5e60e9fce2a8b5f5a7050da364656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48795829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9958435486d7cb413a68716ec0a9fe7952ac755b282ae24bfea09da08bf8e8b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1781049600'
# Thu, 11 Jun 2026 00:15:13 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0ac2de9040ad910c5f209871a68d1fc648dea0542b3e6b1dad4c36549fff6879`  
		Last Modified: Wed, 10 Jun 2026 23:40:15 GMT  
		Size: 48.8 MB (48795609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f78a20bfc13b2440352d56f96eeea8c9ef3b64f50f259ba4408118049029514`  
		Last Modified: Thu, 11 Jun 2026 00:15:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9b1db81defc6d3d499469a7578cebb62e687b36889da7cb7ef653d683374b2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3164506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a03237da79b21ffb8cbd13b02d59c8ddedf8523aafaf81d8a8a8b3c70a05f8`

```dockerfile
```

-	Layers:
	-	`sha256:3f42cec0d524fbe2faaa36985f380bd3756a45510e9a4e36d7d56b66607cffa8`  
		Last Modified: Thu, 11 Jun 2026 00:15:19 GMT  
		Size: 3.2 MB (3158644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8abbf89648439f330f1361c659539a04614e6781e2746c19e914d7305527c689`  
		Last Modified: Thu, 11 Jun 2026 00:15:20 GMT  
		Size: 5.9 KB (5862 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:21d3f33194a0f824739bc0469788ed9cc88f3500b731ed91d2d0442237d27308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50077034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf90befda46dff439b3a11a2984f08ea5ff8eee17a2f5b38e507eb64ff9ba137`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1781049600'
# Thu, 11 Jun 2026 00:15:56 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d202352e18eebe30161de45b828011b4a789f9365749eabf5ec01f2a07689a5c`  
		Last Modified: Wed, 10 Jun 2026 23:40:28 GMT  
		Size: 50.1 MB (50076813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67401bd06d80b3696235ddac9f2b6df782b9dc1fae436620ee300ab3acea3ff4`  
		Last Modified: Thu, 11 Jun 2026 00:16:02 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:59af4ba5e436b9579b1c1e8cb701c7e1044e52d270f25d28e1abcf168302d4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7370bb58c81f8f3758f33d0d403f14905344bb8850591977b1ddda864527af5e`

```dockerfile
```

-	Layers:
	-	`sha256:70122a6e60c39b78c733acf1ba1d9894a70d9d47816be52f48573c0ce36f531e`  
		Last Modified: Thu, 11 Jun 2026 00:16:02 GMT  
		Size: 3.2 MB (3151174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0effaf03c1da13e92dfa4dd717130e72a90e4a9e5e53240de278ccc63354714`  
		Last Modified: Thu, 11 Jun 2026 00:16:02 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:3fde66df63546a91aa4d5cb648603c74aa675dc31be34d4084187a2bf1932112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54021507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f1d92d8a9979c09874901f7f95b12f2e557d3cf34c6e9e7bd197cc8ded2e43`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1779062400'
# Tue, 19 May 2026 22:56:38 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a896bf8623032a9b4075e6319b6f84fd18fb93674032660f124004714d68a5b6`  
		Last Modified: Tue, 19 May 2026 22:37:32 GMT  
		Size: 54.0 MB (54021284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b278cbc22a5f8684efa93c350e845bf08327018f8b49f6229f125feb53650e`  
		Last Modified: Tue, 19 May 2026 22:56:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:76708087c34a3308018c73d4c54b246d2d0d73c6101590eb2978f75b6ecacad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aca9df18bc19a6eb62ca640926047e3e1452605fae4a46be197360241e550ac`

```dockerfile
```

-	Layers:
	-	`sha256:6220a69e5301243265b563005ea4c144e7836fec417f085085a04b19f37ad5fc`  
		Last Modified: Tue, 19 May 2026 22:56:51 GMT  
		Size: 3.1 MB (3149757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9cc8a70d449878780459b973584c4ad4139ee3aa172e080adcb6fb6763c5134`  
		Last Modified: Tue, 19 May 2026 22:56:50 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:10b163ee4dc3445dbaf1f897ed6be4118d041d68084e2523c610cc601e4a03ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46833413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fb27768cdf51ac6e555788e318a150a5915421b66773b4ac3842bf41a547b3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1779062400'
# Wed, 20 May 2026 01:47:56 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:612adadf0063fc0d0780b5c5f6efeac492aac518a4614c14f4ea5ff21a649186`  
		Last Modified: Tue, 19 May 2026 23:46:24 GMT  
		Size: 46.8 MB (46833190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea72aa88b01894b72ff8f06103c02b7afdd03799ddd7758cb0216504afb02d8c`  
		Last Modified: Wed, 20 May 2026 01:48:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4c687d2baac3dfe208550edb6f8cf827405042940af6a5b43055b1be684c5789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3143579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9980a7039deaf8aae3c56f8a9c164c6b5644ad7f065a60a7a5df16d43c34f6`

```dockerfile
```

-	Layers:
	-	`sha256:c78026ed543f9b62b01e99abe7bd59028bf8c6091faa155e445f36edecd0c4da`  
		Last Modified: Wed, 20 May 2026 01:48:51 GMT  
		Size: 3.1 MB (3137760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11bb1c911d37e0f34cd7cfa176e1b7f8ec2b450bce124e2a95c375d974a7c949`  
		Last Modified: Wed, 20 May 2026 01:48:49 GMT  
		Size: 5.8 KB (5819 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:7499cfd94cc3aa3ffba492f1b153f05273bb1fcff43be0d95d261c5ec3fa0713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48513332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1faa309ed15481d18ece17365629bd20ae5afb6e282252199f2ff2531183ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1781049600'
# Thu, 11 Jun 2026 00:15:46 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d7126aef2aebb51829b0047dfcdb7ebc424e9fa253eef97b8d7aaa7471f6f16c`  
		Last Modified: Wed, 10 Jun 2026 23:42:13 GMT  
		Size: 48.5 MB (48513111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5ebfebf7ecb70290f4943735f781442cf5483275924a252a6c1fe7f8dd282f`  
		Last Modified: Thu, 11 Jun 2026 00:15:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b97f9626c67d2b16d11a8f73c717d0d9f5c7690dc97e7a85faa6e64cd64b3204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b82dcfb826d7335de2d4529c3ffff73512989146fa48bbe6c1e8f659c65285`

```dockerfile
```

-	Layers:
	-	`sha256:b610c6d9ae972cf9a0107202c43a3bde47f02f58426670769f0972ab928462a4`  
		Last Modified: Thu, 11 Jun 2026 00:15:57 GMT  
		Size: 3.2 MB (3155425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:238d008f86fab99d6c63236bb7db5c45b5776d7e4409976334fe7efdf72bd0fa`  
		Last Modified: Thu, 11 Jun 2026 00:15:57 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json
