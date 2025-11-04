## `debian:testing-backports`

```console
$ docker pull debian@sha256:f387cc8f2683615f654682e7ab6a09350a8bf54bf9b74c361480a6d61727abd7
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
$ docker pull debian@sha256:9f7da11c9a4db39bf049745a2b96c6766657ef846dc758bcdf1c963bcc60e6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48481584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490f6081f25063574b480bffc14d20aef802736ae709a9023092a628a0d6b16d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1762202650'
# Tue, 04 Nov 2025 00:16:36 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:90f44b176643572e0370d1172f54e2db1950b1b69536cab5f222f4cf55cff73c`  
		Last Modified: Tue, 04 Nov 2025 00:13:16 GMT  
		Size: 48.5 MB (48481362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c746055b2aae46edca4deffd143c65df24416817d37870d09f4335f99a7df4`  
		Last Modified: Tue, 04 Nov 2025 00:16:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bec3fe605ed15e8ffb1a043f3e71c2545264d0546896ac7b25ad90373417df0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3135335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facfb713739a91cde81ab8871849a63d6ad96bcc2cf85ad043edf1f1784896f5`

```dockerfile
```

-	Layers:
	-	`sha256:2b750864fedd91422ab7d817c0966d804f08dc41ac50bd6a6fc33f97eed6ed1d`  
		Last Modified: Tue, 04 Nov 2025 10:29:28 GMT  
		Size: 3.1 MB (3129541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f30054f3508d37dbdc6da5540335059bdbfb41bf20029c1a0f82f8a38fd47f7`  
		Last Modified: Tue, 04 Nov 2025 10:29:29 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:19c81f3884eeecadbf6bfa5d60dadd57241827d07d079f8bf67f8186847707a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44987871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963f15729ad8909c7b91e94a85da4ec0cd60eda821bbcfe6139134ba2c77e90d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1762202650'
# Tue, 04 Nov 2025 02:04:57 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0c2631ed92bba3d58ca5d004f036082287176b8e59f0c30e92ae658fcbc7cda4`  
		Last Modified: Tue, 04 Nov 2025 00:13:53 GMT  
		Size: 45.0 MB (44987648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0feed4cfd4390610fe63088cc57ea3383e9d491e25f72c097194239c695f280`  
		Last Modified: Tue, 04 Nov 2025 02:05:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:293094dde05603d35425bf773a452dc4d6a90ef086588cb5c72e4cb8f3ebfa0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378065996bef3575f9075a9501de3aa389fa87c0322709d736d5b730e996b901`

```dockerfile
```

-	Layers:
	-	`sha256:21023e7bfb32b3cdd6c3d4cbf8934904d019205ae5f594d7462a88fc53890752`  
		Last Modified: Tue, 04 Nov 2025 10:29:33 GMT  
		Size: 3.1 MB (3130909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2370e85333c6f80247ba356d52030c310bef8c545b0f05cf3fe513cb91077fe2`  
		Last Modified: Tue, 04 Nov 2025 10:29:34 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:2362e704347b137018f2b82dc4701b596aa8baad2adc398cd10e41429f7a962a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48583857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889778641feec0eb05e75230d4c20e688c643a003aeb1cb835e6d16e64c401e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1762202650'
# Tue, 04 Nov 2025 01:18:12 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8fe74ebf733f4a2b673fce2a29ff282e87d98a36ff2897bc5c237fab3f805191`  
		Last Modified: Tue, 04 Nov 2025 00:14:31 GMT  
		Size: 48.6 MB (48583636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0b484f903d53216bb7c1f656580999879d2ddf4588f7cee9a73148fa04aadf`  
		Last Modified: Tue, 04 Nov 2025 01:18:26 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:08681039312f218f63b1f28fac1a843e89d54df0b726c981028e1454d424fc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be03c3264edd8cca30ba0f750d24310eb6324ef9e033bfe3c5b47d318d589c9e`

```dockerfile
```

-	Layers:
	-	`sha256:a5bedd6fe7f984ea9dab514c269e1c7bb5ee8da6aa0ebcbcadc9522fa8ef07f1`  
		Last Modified: Tue, 04 Nov 2025 10:29:37 GMT  
		Size: 3.1 MB (3130382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e56338479dcc886398b227cac45f43656bd4b1a6199793d602acfe7561f81d92`  
		Last Modified: Tue, 04 Nov 2025 10:29:38 GMT  
		Size: 5.9 KB (5862 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:54c03aa238edb7c816807a7aeff6f0c58ae2d6233ea97712e8a9a66f01487e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49809718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d79f9665c9a95f5f96d18ed0853381a18cc074eacebbb785a6e5329714f641c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1762202650'
# Tue, 04 Nov 2025 01:18:29 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b2a108875f3224d2636140c6e6a6b157d29d25df61b5e30bfad48c53e6ef18a8`  
		Last Modified: Tue, 04 Nov 2025 00:13:44 GMT  
		Size: 49.8 MB (49809498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b1fc1af09969a1db50f76171910777f22f37c46a5da9e6b16d363c1e64b743`  
		Last Modified: Tue, 04 Nov 2025 01:18:42 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ef07560f02300e2a5fa925d49e38555e6c0d142d47a0124aa464cdef95577f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150302603e813dc010068a0dd54d11016513a2b20c0f26387cbe8813e79148e0`

```dockerfile
```

-	Layers:
	-	`sha256:020e1f6c454ae9cef1ecc5847eb323ccf77f957192bbcd48f7ccaaf7222ec650`  
		Last Modified: Tue, 04 Nov 2025 10:29:41 GMT  
		Size: 3.1 MB (3126750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fed806ead77d36c4fb427653219e7e3d7c44b26a43f5cd7836d8e8a57928561`  
		Last Modified: Tue, 04 Nov 2025 10:29:42 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:8258c68adfdb812c2e5399f7178f55a60b099c5345cbe641a29bde364a135fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53315460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc07b349a4ad2f3be6aa925e24af0f3ac1b3f564cfe1d1757d8d72e8dc87729f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1762202650'
# Tue, 04 Nov 2025 01:19:02 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:174727ec3d50f4bd692245f2ee33064dc9c22375cca6dc7eda65e345ac6d4927`  
		Last Modified: Tue, 04 Nov 2025 00:19:09 GMT  
		Size: 53.3 MB (53315238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fce8170373de8db877e8afdd5cd08294602a82b36d099078436b037256d5bd8`  
		Last Modified: Tue, 04 Nov 2025 01:19:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:632c95d93fe68ed0be457a9ae7cc164a09675f859d44b3b7fc201d1bfc73bdd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580026f109bfe22a6e641eb3d6a5ce92769f95764449626c0ea1e77cbd4e0337`

```dockerfile
```

-	Layers:
	-	`sha256:fbb390ab2cbec1c8f23621243e7db2c297c772d4a03cecf67e45a7713bdd050a`  
		Last Modified: Tue, 04 Nov 2025 10:29:46 GMT  
		Size: 3.1 MB (3133030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ef8b230ccafab662ebfa649b878daa9b3885837d97821eea97dee6255d0b7ed`  
		Last Modified: Tue, 04 Nov 2025 10:29:47 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:2bb0c74841c0edca86abd64d431db715ebd131936bcd0654ee2cb82cf40c397f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46791344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7787ac7cb78a2fbfa4c917089cc9b882ce68fb6291dcc5dc4bc280ccd0fad7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1762202650'
# Tue, 04 Nov 2025 01:21:38 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a3c633bd5a8a638b091323ca9232090c97b6cf727820f884e36ab020bdcbcd4f`  
		Last Modified: Tue, 04 Nov 2025 00:24:17 GMT  
		Size: 46.8 MB (46791123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d01c79ee2370649e5004a7e14fda3372d3b2814882bf5ad70cc31e37fbb07bf`  
		Last Modified: Tue, 04 Nov 2025 01:22:38 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6ce6485d05b891be07c778412972709e51cc9cd3dff74dda128e8f4212e8730d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cccdd60d0557a488fff9ab1d0092eec83c0f6712ad62946314d09a8df2c68f6`

```dockerfile
```

-	Layers:
	-	`sha256:b97b630296b7b40610db9d13540319f3e760a878ac15809e520dbe4cdee23d4e`  
		Last Modified: Tue, 04 Nov 2025 07:29:55 GMT  
		Size: 3.1 MB (3121840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3baf77c90c93a2222ae4e8c8a0b67f8bbfa48c8049f365a0f301a82e4b370c54`  
		Last Modified: Tue, 04 Nov 2025 07:29:56 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:ca3fee9aa1317deb96e1901e3509a79a15f53f6363a6831fe45aee2cdf34d98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48343283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59b28ab144eb97aaeaa5c39fbcebf6f61695bca3d775bb5ff2280f3f1505f0a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1762202650'
# Tue, 04 Nov 2025 06:42:40 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e99c0da2e97fc60ed941b2b64ad1209d58000b6a2e554be98962ab3f543525bf`  
		Last Modified: Tue, 04 Nov 2025 00:18:40 GMT  
		Size: 48.3 MB (48343060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38caf475179f5703f67d64f0b5daea5f7de3b953d1e03f96675bd084091b7cc9`  
		Last Modified: Tue, 04 Nov 2025 06:42:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5cf698e0c10efcf3be017496cf06874b8efab33cbc87870dd4394750eb589c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40853b12090f86f2b3d3817822a9b4dd642761aa8da29ee1e1e376b5070a6c55`

```dockerfile
```

-	Layers:
	-	`sha256:2eba15cd86435051041397e0a41b8e5ddab2792bcd555a09f3e4b5fd800c5214`  
		Last Modified: Tue, 04 Nov 2025 10:29:53 GMT  
		Size: 3.1 MB (3130990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e44e37c645bcbb92da641a264907ef5acd91a71f94604265080196911c608f`  
		Last Modified: Tue, 04 Nov 2025 10:29:54 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json
