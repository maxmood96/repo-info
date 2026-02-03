## `debian:testing-backports`

```console
$ docker pull debian@sha256:82e24441bc9accd75ef11af1fe35c1857f9bfdd654b814b0d1c7f453b842fbdb
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
$ docker pull debian@sha256:b4dba44fa79a015fbf598cbafa23b83525da70fe5b64e9fdc937e957af37dd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48655962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9c3dc4ce410e1055a1f9230bc0653f1be768973cd8706266569f7981077bda`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1769990400'
# Tue, 03 Feb 2026 02:16:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5195bf09170e6f427c63401408925ebdcc18df14385049cc0921fa4e070abc9b`  
		Last Modified: Tue, 03 Feb 2026 01:15:55 GMT  
		Size: 48.7 MB (48655738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aeb5b6fac0721e70ff83131c0cf92062ce3201db242d84d8e6faef3d8c7d8c5`  
		Last Modified: Tue, 03 Feb 2026 02:16:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2c6f18a6efb24929fe99039c37135ef1024ea1679e8bd715357becbce9adc55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca473c0244c6dfdfd9c7fa8c11b29c518b825afa7265b0aeb732897fc5f6643`

```dockerfile
```

-	Layers:
	-	`sha256:3b26be81976499a28dc5633f7dc88cd6e0323f933f34a16e4144a9f7fee125cd`  
		Last Modified: Tue, 03 Feb 2026 02:16:09 GMT  
		Size: 3.2 MB (3150961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26973b037160741872bd240349349d5afc45c97d9b353c541d50482e13f2b4df`  
		Last Modified: Tue, 03 Feb 2026 02:16:09 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:81ec21bcef14f85f65a6782d88d4f858012f29c459573a46a8ea8cabecf7f69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45128725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d802ffbc5ed69dda32f29e495606b400cac3777439c6fbfeaf61f65ee146d2ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 01:18:08 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b52b83a8ae7e06dc9628b08b5ba1e89d1671fe275e5a1dad70de57feeb453db8`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 45.1 MB (45128503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611bb61db6d32fa947523e363731f4e7d623b0f38fc5a9376b7c2bcdc08c9402`  
		Last Modified: Tue, 13 Jan 2026 01:18:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fbda5f7bd486aa698cfb70c8f82221ea1d8eb36ed7339ff24e898ee8ea49c7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e86619d6f6192b1b5bc720413f9220dc2affa0f1003e9ec0fb23191e583d2e0`

```dockerfile
```

-	Layers:
	-	`sha256:190d7137c024b8565aad11d9c2f88f66790dfd366da222466d59c890f3ceaf0c`  
		Last Modified: Tue, 13 Jan 2026 01:18:15 GMT  
		Size: 3.1 MB (3143411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f62f50fc397c07f05ff45b376fd6fbec8c43573004c56945a8be12d7dd7ffbf8`  
		Last Modified: Tue, 13 Jan 2026 01:18:15 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4c05a128315a5a9141e0282f97c953a86a88a280a8511807915562c9b5462446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48821035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5abde4a2d47455dbb45cc5d309b14de677ce8749a4b0c85667e91f9c466884`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 01:17:11 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7bff1ad60177e8dd221d8df5866b0e7967fbd97f4eb69a5eb672bd24b7ffc9ba`  
		Last Modified: Tue, 13 Jan 2026 00:43:00 GMT  
		Size: 48.8 MB (48820814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67630b0a3b96fe8dfd739f8cd78d925902da72bce8f2906e2fb798ac73919517`  
		Last Modified: Tue, 13 Jan 2026 01:17:18 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:90a776a0b5876c0e7606bdd7f3b5f8000faf37f7ea8495782253ec1bf9cd7402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1697a641199649088b57b920c8d281e19dee86a4b6cced0dd35118910eaa179e`

```dockerfile
```

-	Layers:
	-	`sha256:824223458fdcd00e5c170d9c3c00420d3dab9b36935af9b8f95de63ba4e9cae5`  
		Last Modified: Tue, 13 Jan 2026 01:17:18 GMT  
		Size: 3.1 MB (3142884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:840a8f67ca1497379e58eb2b685fe129a77d8b7bee820a3bd1d9db6187c73e83`  
		Last Modified: Tue, 13 Jan 2026 01:17:18 GMT  
		Size: 5.9 KB (5862 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:ce5b3ebaa8699fb70055ab45f87c3e0ecba708e385985027f6f90708b2f41dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49944772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150c3736ad0b88acee9752ecf5c3210fdc84a1a7761ea5a5fe8e0d8fdd698fba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 01:18:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:65a17761f67102b9b31e6ba09bea12e37d10922372c16ce1a4f483d5e6df64aa`  
		Last Modified: Tue, 13 Jan 2026 00:43:27 GMT  
		Size: 49.9 MB (49944551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b62f140ed240e1b26a66dba73ea74702517cdaaa50f99df712aa5a8b443053a`  
		Last Modified: Tue, 13 Jan 2026 01:18:07 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e3f02290719b157b22c2b75fc179913e611f50c550d9b76113bde2f176bdf55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb5911b0e7095abbf588191e27db52c07ad498a7b04afea54a08b23852b3102`

```dockerfile
```

-	Layers:
	-	`sha256:f9acb89edd38f81458e28afa75ef5952406f801b93daf56d5d80abc2845dba4e`  
		Last Modified: Tue, 13 Jan 2026 01:18:07 GMT  
		Size: 3.1 MB (3139247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0b84d88df194e9609ff867d18548a1b463acd01204b4c67e01c64d829ace4d`  
		Last Modified: Tue, 13 Jan 2026 01:18:07 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f2d65d0a8ac7d2cad503f7ae2c4973243786fa3c0f599c630154510a509b00bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53582892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9230452c0aa9121a5a70e663c545c3cbc9c204fc9bb72f90b27707c4576d5f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1769990400'
# Tue, 03 Feb 2026 02:15:20 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1a1783231c3dd75846ddfd4277f3f207d78dec75ee1f53161099a048c12db614`  
		Last Modified: Tue, 03 Feb 2026 01:15:51 GMT  
		Size: 53.6 MB (53582668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4828c6891dfeb4ef0889a1b9dcc9f4a1dd627fa33cb7a8232e5156e08ef3290`  
		Last Modified: Tue, 03 Feb 2026 02:15:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c74cd72fa9c1fb7ad9a7bbb49b5c3824cf299ec87ff6ff7df80ceb443ef3d8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3160304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b39ff77f1a2d5e9fdbd9195ebddf399e5d0442ad7b3bad79a73ece219779d6`

```dockerfile
```

-	Layers:
	-	`sha256:6ac561648b9eda39d0fb18867cf944b36d19bbee15c2b5d5e8759b6859f6b00b`  
		Last Modified: Tue, 03 Feb 2026 02:15:34 GMT  
		Size: 3.2 MB (3154484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c294d0594236016888344d28c5255a99bb11d1dd67f78968fe06e8114e6ff4f`  
		Last Modified: Tue, 03 Feb 2026 02:15:34 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:fb3f274ed7839886023de45dc2e02c7fdbaef052f60338203d6fca695c8392a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46854688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868dd2984733b77251c787ed941b6b31341ab68d2280c7358f98a18d6fea2cee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1768176000'
# Wed, 14 Jan 2026 04:07:18 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:91e82f1d58406699b930594305527c53618f59da57e5326a595907e3493b82f0`  
		Last Modified: Tue, 13 Jan 2026 01:02:49 GMT  
		Size: 46.9 MB (46854468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895e2f7e7862637d229f9598e10597a1261ad3a4fbd1b8e34660be054d5f706b`  
		Last Modified: Wed, 14 Jan 2026 04:08:12 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:eeca3de25934e33c48334a219c81a6ed7497c2dbf5dee16f46cf2c5428f39e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3139361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c940681b5da64f7be4126ba2ff8167e8ceb76e21df52d370d7be2311bc6486`

```dockerfile
```

-	Layers:
	-	`sha256:eb8e91d8af3f130cba6082e1c93e4347b17a4220046c6896cc6a97f6d8d50dc7`  
		Last Modified: Wed, 14 Jan 2026 04:08:12 GMT  
		Size: 3.1 MB (3133541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f7710d291674518d0f94515c05703921690d4d88554ecc3e1ae239f4a7b92f9`  
		Last Modified: Wed, 14 Jan 2026 04:08:12 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:7a042ed704bbeadb38a07cece688f5d3c79e87258f62a991195518985f7aa7f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48429555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205eaa55ab56f13a9cdb78e8f2af2568ee60a9d5ca09a7317ef2543b4dd06c07`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1769990400'
# Tue, 03 Feb 2026 02:15:44 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:307dd5b030418664167d57cabfead401f56d4230a8297dc01ed7acc18877867e`  
		Last Modified: Tue, 03 Feb 2026 01:13:49 GMT  
		Size: 48.4 MB (48429333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd79bad1ad762151b8c7b086243ebd0e52cad48c8b8770a70730e59c0672e00e`  
		Last Modified: Tue, 03 Feb 2026 02:15:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3321ab52b828dc50d8860119c8ecd6d864460f204dde9ae122fa498bb1cea5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3158203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a1328352e2bcbeebf35d0d44b207da54fceeda85104f4c379bab545a3796b4`

```dockerfile
```

-	Layers:
	-	`sha256:553e74b41eb49cb895120ce9fce94ba2e4e33c65e01ffd1d0f31846e920d36e7`  
		Last Modified: Tue, 03 Feb 2026 02:15:55 GMT  
		Size: 3.2 MB (3152410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6efebee0847ad6a7750646df91d272977abf6e3f978b523ee0396ce017a976c3`  
		Last Modified: Tue, 03 Feb 2026 02:15:55 GMT  
		Size: 5.8 KB (5793 bytes)  
		MIME: application/vnd.in-toto+json
