## `debian:testing-backports`

```console
$ docker pull debian@sha256:27344a475dfc698fa42342382fc93ef0fb2b3bf991eec26b7918cb4ff8b41307
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
$ docker pull debian@sha256:44a8e750e64e6c092d5dc920602933f777f28932549c852746791d90f48fb670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50051257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:237862a278d1cb8bbd94330f2e54b5918f17ea9ae1ef33423a2ad9f5891596be`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1782172800'
# Wed, 24 Jun 2026 01:14:44 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:997fcd5cfd1d79c54a799ef1275b4e551794304b0dd4257811d1c2a741181727`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 50.1 MB (50051034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f07dccc220e57795fbe54b50dc0b4d0e1b957555679733b13f0aa6d5ff44952`  
		Last Modified: Wed, 24 Jun 2026 01:14:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f89b8d34ce5cdcca3b5967918fdb89563530af93a59f58ddad27fc54a18fd6db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797e6548f3c5db3ac737b3e7371c5bf8d11d6aeff05bed79016d3b2b7d14860b`

```dockerfile
```

-	Layers:
	-	`sha256:17c449d7a39b926faf20f5770df9b271eb92d7d45a009e9d1d5169ca4b516894`  
		Last Modified: Wed, 24 Jun 2026 01:14:50 GMT  
		Size: 3.1 MB (3147921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d50ed9949bcb1bd2a6dec63f1fa0f7e6dcf753f7418844131559966800cddba`  
		Last Modified: Wed, 24 Jun 2026 01:14:50 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:28f9cf8f6e389fca943b8dc030ee10bffcc5ee157f82bf1370d224763513fbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54079253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc17a96abd9457eab425c4196de9441582f506a5258776205a7d526b79163100`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1782172800'
# Wed, 24 Jun 2026 01:15:02 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:edc739abe003d71e29f51bd3f67a0748257a233f97beb886321f5f660e6cbaa8`  
		Last Modified: Wed, 24 Jun 2026 00:30:03 GMT  
		Size: 54.1 MB (54079031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fcc96aa82b7a61d2bf6c027af34cb9712953ca9cd5f4064f57346210c3c572`  
		Last Modified: Wed, 24 Jun 2026 01:15:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9e775ce157ba50e6d0cf728694c504901d20a952d7da103855500c567df6b452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3160034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642d199c1045e9adfc190c9d7326aa17cfcafcf872a6b3314a7444bc81b7a4c8`

```dockerfile
```

-	Layers:
	-	`sha256:46bf505c03db0d03793eb2b886e767337fa5ca690897900a955622766eb4ab03`  
		Last Modified: Wed, 24 Jun 2026 01:15:17 GMT  
		Size: 3.2 MB (3154214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e54e5df05e5a6e355efa7a6fa1041f7a98856fce4086032318bbdf5b535da311`  
		Last Modified: Wed, 24 Jun 2026 01:15:17 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:2cf04e8acad8cfa0048a6d5803e41c5693ad924e1f05b9c0bbebd5ee4590d34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46868628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222c7ce8386201f694dc62567a6ec91072b7d862188574fab3d907806ab7bec1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1781049600'
# Thu, 11 Jun 2026 22:10:29 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ac4a55378c030d05c280a7f850c25ec5ea06b66e587bea222cece96b927588bc`  
		Last Modified: Thu, 11 Jun 2026 02:55:57 GMT  
		Size: 46.9 MB (46868406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f66a369ea243ebc7929b7826f54e7607fc477d3895a8687aad7de4a432ac02`  
		Last Modified: Thu, 11 Jun 2026 22:11:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d10e6913cecdff6a365a8b86f8164031e3fda9d13df269e80867b016838f8f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c06663aa892535632769aa1b9c8b69af4f7344bf4a42b3246196a64083beeb`

```dockerfile
```

-	Layers:
	-	`sha256:9aa246f59b388ab1708d955232537814e19edb7679b5309f44e306515f7bb9fa`  
		Last Modified: Thu, 11 Jun 2026 22:11:24 GMT  
		Size: 3.1 MB (3145482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a4c82c3d9dba222496a66a288de76cceff3cdac62e6e528e2b747454bf8c9d`  
		Last Modified: Thu, 11 Jun 2026 22:11:24 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:16cfe06192b515e2980303b37695cef3579478a8aaf37a7a391947d60de76435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48492061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92eb6e904483d37b01a5a49c904ea20cb50ea9a9ba07af11184fad20dc21b522`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1782172800'
# Wed, 24 Jun 2026 01:14:25 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:55f193d6691f14cc10d6580d69d5e9df4cd7390a771f2807ff18665a2262556f`  
		Last Modified: Wed, 24 Jun 2026 00:28:16 GMT  
		Size: 48.5 MB (48491840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd612fe16d38dacb644958cb75bc8689c2930162cb66a8e5cc083857162e4ca`  
		Last Modified: Wed, 24 Jun 2026 01:14:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f6f186f2ed267deb19398dd212cc4f59a11b3bb99335e085cb16708afe6bfff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205518027e61d2aa3b9eb1ba3ed96427f9cb9173c076003af91077ff5e66c4c4`

```dockerfile
```

-	Layers:
	-	`sha256:663de8de09173d08f6e3ee6db53d41dbe9681822caec674442f2ddcb4fb3cd36`  
		Last Modified: Wed, 24 Jun 2026 01:14:35 GMT  
		Size: 3.2 MB (3152168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1445b31fd8336cc3ec067be4f9e4cded583adfbf8f7a4e05aa92fda86202468f`  
		Last Modified: Wed, 24 Jun 2026 01:14:35 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json
