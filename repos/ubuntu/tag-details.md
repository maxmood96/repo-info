<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:23.10`](#ubuntu2310)
-	[`ubuntu:24.04`](#ubuntu2404)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20240427`](#ubuntufocal-20240427)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20240427`](#ubuntujammy-20240427)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20240427`](#ubuntumantic-20240427)
-	[`ubuntu:noble`](#ubuntunoble)
-	[`ubuntu:noble-20240429`](#ubuntunoble-20240429)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:f7904edd1cfddcba55c80059579ce1f5ccaf18a84d79751721726a5ba479310d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:20.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:cc9cc8169c9517ae035cf293b15f06922cb8c6c864d625a72b7b18667f264b70
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abc4dfd83182546da40dfae3e391db0810ad4a130fb5a887c6ceb3df8e1d310`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2ff7db5269022af324189ffb3ee686d05e33a913f4aee93aae77553a73b4a4ac
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23623322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d2e547d6406db6e822c4e4b87612d9306ac1db2e7ade8e61a0e1917135796e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:58:26 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:58:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:58:28 GMT
ADD file:648705eca6ad0949d4722f06be77e38518c38195f6aa605ceb301e2b576583a6 in / 
# Wed, 17 Apr 2024 17:58:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9a6fff73b326d5324045be533d975e22b1bc95d54f4659c6ddffa7cfed29e694`  
		Last Modified: Wed, 17 Apr 2024 18:54:31 GMT  
		Size: 23.6 MB (23623322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1fc4c6f9a232c4f4db6ab06bb5c92aa49f1fec4432e0a889ac6d7b130f31d31f
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25976141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7ada54560faf82e2086a671c8496121c800f952b92ec2bc76ec00c60098be6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:57:12 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:57:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:57:14 GMT
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
# Wed, 17 Apr 2024 17:57:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:935803725f5775642918295f3557fecf93003fde6403df6fcbb2379ce4795a1d`  
		Last Modified: Wed, 17 Apr 2024 18:54:25 GMT  
		Size: 26.0 MB (25976141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5ed609ddbf6b6fcdba35b7f88ea356bae47f2bee6e65fb9bc2f62fd765cff079
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32077044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a608a59ae9f90ecf8082c4dc897c6973d47b524356d864de82e03fe98e1fae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:58:26 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:58:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:58:30 GMT
ADD file:4b03eaec2f51a953c9ccc0a67500331d1c8e8184b6aabb40b8b988151cae02a7 in / 
# Wed, 17 Apr 2024 17:58:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b570306f252a15e55f4de029744967f9e5144d19ee7b38348a19357b1965b484`  
		Last Modified: Wed, 17 Apr 2024 18:54:37 GMT  
		Size: 32.1 MB (32077044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:88a3990f01d156a9cf839813b633b8dd046fbf17cb1d7fd35195275ba1361736
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26367744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29262bf367f64e6b82b3d83a07b5936bd5d4b50d802f0a3a706b5acf20ee1ac8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:33:19 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:33:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:33:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:33:19 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 13:33:21 GMT
ADD file:437329bc1595e1f595679a14cae312da49f4465fe0b6b7263e2831d77736f05d in / 
# Sat, 27 Apr 2024 13:33:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9eb4731ed147087570d62c01c9ee9f9f22b6d4bc2b0f1215688db1911a8c7cb2`  
		Last Modified: Sat, 27 Apr 2024 14:55:22 GMT  
		Size: 26.4 MB (26367744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:bf8ed9f43241e3413e07eb70bdbf4db00a57122674fab1024dc0a53e32369049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:22.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:2af372c1e2645779643284c7dc38775e3dbbc417b2d784a27c5a9eb784014fb8
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52882761a72a60649edff9a2478835325d084fb640ea32a975e29e12a012025f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:1d9e10849d346703aa823547c0466da1323dcb55704778eb50d9f8b111edf266
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26638183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3c049d6f24945a3c18783e6cabf222bb5df1910ca28af64c34775a1679325e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:29:44 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:29:46 GMT
ADD file:511fd2f076c60f46f9185a7e8c176585251f3eec5c08d6b4cb8efdb0a9bb53fb in / 
# Wed, 17 Apr 2024 18:29:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f3b420ffc3c77ff845194a1e5c28971de13891b8169612c7e0a8f23ec0ba0a9c`  
		Last Modified: Wed, 17 Apr 2024 18:55:42 GMT  
		Size: 26.6 MB (26638183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:984f7324c44c67df577958e874e7e438c67ff7bb6562129129405da98a388518
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27360350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ae71f2bc601e0e4b21b06dbc9a01fefa28569901196469921b293d716779b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ef8879b7897601a39e1de82a5f2c44f77b7ce9c9d504f735a3fcc247197bbbfc`  
		Last Modified: Wed, 17 Apr 2024 18:55:35 GMT  
		Size: 27.4 MB (27360350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:08ef29b26b32e8d902c6c51f53f8c7e01ca22176cb9493cb72fe257d08655dba
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34461311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d004706cff8045728fdb4cbdb37cf7e425c12bdd2aeb01d70e6e663448ae91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:51:23 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:51:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:51:27 GMT
ADD file:a6dad5ca890a7e93d717612d191eff2d9bbab6f9cef18c588630297bd6a61cc4 in / 
# Wed, 17 Apr 2024 17:51:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8735f03877b4ef190c5279652cd5a0a8db5ddb4170fd1fb1710abee9d2f811b1`  
		Last Modified: Wed, 17 Apr 2024 18:55:49 GMT  
		Size: 34.5 MB (34461311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:4b24be9d94475438fe8313d8772be9c94e7c89d4e2b2d2a7570dcb3a7f51ee80
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb33d4cf8418e4e1c97489979c96315f6771327c8f82b4bf602e45387a430fa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:52:56 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:52:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:52:58 GMT
ADD file:7d693ab3b1f45d4992a119ec94444efc96c176ad954375f3bc1299ab813a46a0 in / 
# Sat, 27 Apr 2024 13:52:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:01c7fcca5fd930108d469aeb9d86249eb7f2cdc75699dfa8dd132d9b5f55d29f`  
		Last Modified: Sat, 27 Apr 2024 14:45:56 GMT  
		Size: 28.0 MB (28000423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.10`

```console
$ docker pull ubuntu@sha256:431db664ea655923702ac110ec4d09bb63bb146b2e37ef8cc889831990ee5dd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:23.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:141d7b0a56d0bd0b876765c20b48ec40e1843a09c1d0c79aa5efee82bee21244
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27234007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd494f24c6ee4c536c1aa8b913be1fc699bf8d7d51911036d3671da8b36fefd3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:02:03 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:02:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:02:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:02:03 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 16:02:05 GMT
ADD file:870c43eadc01423c5bc11fc4422ee10b05cae0f50c997f8e380e0ed25c6c0b11 in / 
# Mon, 29 Apr 2024 16:02:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:56c566a8d234cbea1867522f63b812f51bb091866286e8f350f23a951171b9f5`  
		Last Modified: Mon, 29 Apr 2024 16:18:42 GMT  
		Size: 27.2 MB (27234007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:5df962bf62a7d0ece2200f3fd4427a707c4a0612279568ab98f3c9ac92fd3e01
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24888954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b006a6e04b9773d4390c9e5af30114f3056d4b8db54c7c44bbe01d422b34b107`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:08:51 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:08:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:08:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:08:51 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:08:54 GMT
ADD file:f07b1f2c0ba7dbff20c2f89af95625b7160c10dd0b56c8ce400479098ff75d9e in / 
# Tue, 16 Apr 2024 12:08:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b3c603a20ac30fbf108a364f97b3fdbfd692ee1c1b2597567218e72db6eaff94`  
		Last Modified: Tue, 16 Apr 2024 12:46:43 GMT  
		Size: 24.9 MB (24888954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:4627f4a72bfc36475f6b0e7fa6f8865d75a165d47d437ad386168f3be107f989
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26414813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c1de4085ecee82c5f3f244ee7797d92808e34c4de513b5bd68fa46f6b2ad06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:36:32 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:36:32 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:36:36 GMT
ADD file:2a859c5d715743469a5a33d7b6038db94be34745cff1d5f681ed1d3d0e5931a6 in / 
# Tue, 16 Apr 2024 12:36:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b78e311e28b3f037f6cfc8470f0dfa0c1d89160a34d0dadefa10b3239d33dfe6`  
		Last Modified: Tue, 16 Apr 2024 12:46:37 GMT  
		Size: 26.4 MB (26414813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ccc5e01ef699b4e4ed576499c885c727667a2df98ae5e8af8006b18a5513315b
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31365049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60663f39f12fa270dee6f0356d34f06facdae5daed954433b6b1733405b0e94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:36:34 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:36:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:36:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:36:35 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:36:42 GMT
ADD file:d101590827db35fb306467a12041319349f48362c5708f20a992cacfa084f678 in / 
# Tue, 16 Apr 2024 12:36:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:42e56421b7ba4fdaf4a5c3dbdfde02f434b638fcb84d80270dec2b3c9f4b0ca7`  
		Last Modified: Tue, 16 Apr 2024 12:46:49 GMT  
		Size: 31.4 MB (31365049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:47c6b893ab777ea2f23f010efa7af2b964ec6d3e04409dbc421e5cf06b9cfc45
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27332110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070b853442b94c5e9ad49f3224ce745ad43cb333eeb4ea19788f224c4da22aa1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 15:49:35 GMT
ARG RELEASE
# Mon, 29 Apr 2024 15:49:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 15:49:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 15:49:35 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 15:49:37 GMT
ADD file:76b6235c926b9bd628f27161f73913d479e584c2035eb7185806b814f4e96e14 in / 
# Mon, 29 Apr 2024 15:49:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e5f6811577ee1a4f42b07b0ef1fbbdd8a4cf7b470ee3ea89de99f370a57bf832`  
		Last Modified: Mon, 29 Apr 2024 16:19:08 GMT  
		Size: 27.3 MB (27332110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:24.04`

```console
$ docker pull ubuntu@sha256:1402edee0a57e2a79eb26417e928263d9f4a60bb29c18d470171aae3a6303d25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:24.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:d21429c4635332e96a4baae3169e3f02ac8e24e6ae3d89a86002d49a1259a4f7
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28867545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3dc08bfed031182827888bb15977e316ad797ee2ccb63b4c7a57fdfe7eb31d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:49b384cc7b4aa0dfd16ff7817ad0ea04f1d0a8072e62114efcd99119f8ceb9ed`  
		Last Modified: Mon, 29 Apr 2024 17:08:44 GMT  
		Size: 28.9 MB (28867545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c94d54dd82aba50b58c698accfc4a0a849955ba93f3a1de76353326caf2e9229
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26109958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cfdfc5de64a9bf2322886c5eeb80e1da07abc070d02ca1ffbd429bc3f0782c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:03:39 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:03:42 GMT
ADD file:158f9c2033bf15aea7323a8fc02ed64bb41784f98f36b5faf68a959346a86757 in / 
# Tue, 23 Apr 2024 22:03:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4163275920c38f5bf1c5e40b38598dba06a2fb1edd701aa7fcb16be1cad2a2de`  
		Last Modified: Tue, 23 Apr 2024 22:26:40 GMT  
		Size: 26.1 MB (26109958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d55bf48d8900628edec854908273b6adc4003a8fa4f43aa48f3287899f859d39
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28012692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07db2ffa22daeb428e1b654f77b0bb60c3368c2d391c77c4d3f379d982669084`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:03:43 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:03:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:03:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:03:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:03:45 GMT
ADD file:61020b87bc980abd05e75207205df7ecca6ea7023b3a5e804aabded0eebbf2e7 in / 
# Tue, 23 Apr 2024 22:03:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:67c893392cd92a994ecf5f35ecd3eba2631838f68b751dd27dac25a9e8a736cf`  
		Last Modified: Tue, 23 Apr 2024 22:26:33 GMT  
		Size: 28.0 MB (28012692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:8ea7c2024af7c23083fdd313080e7765036a7a00e87cd004a2213433dddb2b17
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33490376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db75cc60d4de04f10e12664827c4024c2a622a22985023ced8b4bedba66d9c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:16:12 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:16:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:16:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:16:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:16:16 GMT
ADD file:7fd16485139d3989a1a5565c0d7fb14bb79403891eb470189d51dac672fd641b in / 
# Tue, 23 Apr 2024 22:16:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c84264c6c2e73f5dbe8fd6afdcd17c6c94824d50c386190238f88f29f3cc059d`  
		Last Modified: Tue, 23 Apr 2024 22:26:46 GMT  
		Size: 33.5 MB (33490376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:31e02f893eaf7729befc0e21920e63b968bffe76760943a6f56fa1c7f3abb055
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29165121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ddac1146e91c07078f0becc2472c05513ee6f3b42c467cbe1176bc7a8bcd99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:11 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:13 GMT
ADD file:09121ba3a412b610ce92684a3218535826bd353b73e98bc8efe44ad9b4233d0d in / 
# Mon, 29 Apr 2024 16:38:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d450eb1572800c4118ae87f5fd5ee2a6fa067b00be1e578fcfee7725ca35a70e`  
		Last Modified: Mon, 29 Apr 2024 17:09:10 GMT  
		Size: 29.2 MB (29165121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:f7904edd1cfddcba55c80059579ce1f5ccaf18a84d79751721726a5ba479310d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal` - linux; amd64

```console
$ docker pull ubuntu@sha256:cc9cc8169c9517ae035cf293b15f06922cb8c6c864d625a72b7b18667f264b70
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abc4dfd83182546da40dfae3e391db0810ad4a130fb5a887c6ceb3df8e1d310`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2ff7db5269022af324189ffb3ee686d05e33a913f4aee93aae77553a73b4a4ac
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23623322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d2e547d6406db6e822c4e4b87612d9306ac1db2e7ade8e61a0e1917135796e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:58:26 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:58:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:58:28 GMT
ADD file:648705eca6ad0949d4722f06be77e38518c38195f6aa605ceb301e2b576583a6 in / 
# Wed, 17 Apr 2024 17:58:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9a6fff73b326d5324045be533d975e22b1bc95d54f4659c6ddffa7cfed29e694`  
		Last Modified: Wed, 17 Apr 2024 18:54:31 GMT  
		Size: 23.6 MB (23623322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1fc4c6f9a232c4f4db6ab06bb5c92aa49f1fec4432e0a889ac6d7b130f31d31f
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25976141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7ada54560faf82e2086a671c8496121c800f952b92ec2bc76ec00c60098be6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:57:12 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:57:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:57:14 GMT
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
# Wed, 17 Apr 2024 17:57:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:935803725f5775642918295f3557fecf93003fde6403df6fcbb2379ce4795a1d`  
		Last Modified: Wed, 17 Apr 2024 18:54:25 GMT  
		Size: 26.0 MB (25976141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5ed609ddbf6b6fcdba35b7f88ea356bae47f2bee6e65fb9bc2f62fd765cff079
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32077044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a608a59ae9f90ecf8082c4dc897c6973d47b524356d864de82e03fe98e1fae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:58:26 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:58:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:58:30 GMT
ADD file:4b03eaec2f51a953c9ccc0a67500331d1c8e8184b6aabb40b8b988151cae02a7 in / 
# Wed, 17 Apr 2024 17:58:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b570306f252a15e55f4de029744967f9e5144d19ee7b38348a19357b1965b484`  
		Last Modified: Wed, 17 Apr 2024 18:54:37 GMT  
		Size: 32.1 MB (32077044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:88a3990f01d156a9cf839813b633b8dd046fbf17cb1d7fd35195275ba1361736
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26367744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29262bf367f64e6b82b3d83a07b5936bd5d4b50d802f0a3a706b5acf20ee1ac8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:33:19 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:33:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:33:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:33:19 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 13:33:21 GMT
ADD file:437329bc1595e1f595679a14cae312da49f4465fe0b6b7263e2831d77736f05d in / 
# Sat, 27 Apr 2024 13:33:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9eb4731ed147087570d62c01c9ee9f9f22b6d4bc2b0f1215688db1911a8c7cb2`  
		Last Modified: Sat, 27 Apr 2024 14:55:22 GMT  
		Size: 26.4 MB (26367744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20240427`

```console
$ docker pull ubuntu@sha256:1e64dee1a07808b81f58f798e41f0d6906e67361128aa358c7ba619a2e848af7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; s390x

### `ubuntu:focal-20240427` - linux; amd64

```console
$ docker pull ubuntu@sha256:cc9cc8169c9517ae035cf293b15f06922cb8c6c864d625a72b7b18667f264b70
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abc4dfd83182546da40dfae3e391db0810ad4a130fb5a887c6ceb3df8e1d310`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240427` - linux; s390x

```console
$ docker pull ubuntu@sha256:88a3990f01d156a9cf839813b633b8dd046fbf17cb1d7fd35195275ba1361736
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26367744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29262bf367f64e6b82b3d83a07b5936bd5d4b50d802f0a3a706b5acf20ee1ac8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:33:19 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:33:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:33:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:33:19 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 13:33:21 GMT
ADD file:437329bc1595e1f595679a14cae312da49f4465fe0b6b7263e2831d77736f05d in / 
# Sat, 27 Apr 2024 13:33:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9eb4731ed147087570d62c01c9ee9f9f22b6d4bc2b0f1215688db1911a8c7cb2`  
		Last Modified: Sat, 27 Apr 2024 14:55:22 GMT  
		Size: 26.4 MB (26367744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:bf8ed9f43241e3413e07eb70bdbf4db00a57122674fab1024dc0a53e32369049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy` - linux; amd64

```console
$ docker pull ubuntu@sha256:2af372c1e2645779643284c7dc38775e3dbbc417b2d784a27c5a9eb784014fb8
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52882761a72a60649edff9a2478835325d084fb640ea32a975e29e12a012025f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:1d9e10849d346703aa823547c0466da1323dcb55704778eb50d9f8b111edf266
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26638183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3c049d6f24945a3c18783e6cabf222bb5df1910ca28af64c34775a1679325e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:29:44 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:29:46 GMT
ADD file:511fd2f076c60f46f9185a7e8c176585251f3eec5c08d6b4cb8efdb0a9bb53fb in / 
# Wed, 17 Apr 2024 18:29:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f3b420ffc3c77ff845194a1e5c28971de13891b8169612c7e0a8f23ec0ba0a9c`  
		Last Modified: Wed, 17 Apr 2024 18:55:42 GMT  
		Size: 26.6 MB (26638183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:984f7324c44c67df577958e874e7e438c67ff7bb6562129129405da98a388518
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27360350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ae71f2bc601e0e4b21b06dbc9a01fefa28569901196469921b293d716779b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ef8879b7897601a39e1de82a5f2c44f77b7ce9c9d504f735a3fcc247197bbbfc`  
		Last Modified: Wed, 17 Apr 2024 18:55:35 GMT  
		Size: 27.4 MB (27360350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:08ef29b26b32e8d902c6c51f53f8c7e01ca22176cb9493cb72fe257d08655dba
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34461311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d004706cff8045728fdb4cbdb37cf7e425c12bdd2aeb01d70e6e663448ae91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:51:23 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:51:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:51:27 GMT
ADD file:a6dad5ca890a7e93d717612d191eff2d9bbab6f9cef18c588630297bd6a61cc4 in / 
# Wed, 17 Apr 2024 17:51:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8735f03877b4ef190c5279652cd5a0a8db5ddb4170fd1fb1710abee9d2f811b1`  
		Last Modified: Wed, 17 Apr 2024 18:55:49 GMT  
		Size: 34.5 MB (34461311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:4b24be9d94475438fe8313d8772be9c94e7c89d4e2b2d2a7570dcb3a7f51ee80
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb33d4cf8418e4e1c97489979c96315f6771327c8f82b4bf602e45387a430fa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:52:56 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:52:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:52:58 GMT
ADD file:7d693ab3b1f45d4992a119ec94444efc96c176ad954375f3bc1299ab813a46a0 in / 
# Sat, 27 Apr 2024 13:52:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:01c7fcca5fd930108d469aeb9d86249eb7f2cdc75699dfa8dd132d9b5f55d29f`  
		Last Modified: Sat, 27 Apr 2024 14:45:56 GMT  
		Size: 28.0 MB (28000423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20240427`

```console
$ docker pull ubuntu@sha256:d8e65fb6ec33404669de367632cd41a537322bf4e3d8610e129191799ec6b5e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; s390x

### `ubuntu:jammy-20240427` - linux; amd64

```console
$ docker pull ubuntu@sha256:2af372c1e2645779643284c7dc38775e3dbbc417b2d784a27c5a9eb784014fb8
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52882761a72a60649edff9a2478835325d084fb640ea32a975e29e12a012025f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240427` - linux; s390x

```console
$ docker pull ubuntu@sha256:4b24be9d94475438fe8313d8772be9c94e7c89d4e2b2d2a7570dcb3a7f51ee80
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb33d4cf8418e4e1c97489979c96315f6771327c8f82b4bf602e45387a430fa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:52:56 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:52:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:52:58 GMT
ADD file:7d693ab3b1f45d4992a119ec94444efc96c176ad954375f3bc1299ab813a46a0 in / 
# Sat, 27 Apr 2024 13:52:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:01c7fcca5fd930108d469aeb9d86249eb7f2cdc75699dfa8dd132d9b5f55d29f`  
		Last Modified: Sat, 27 Apr 2024 14:45:56 GMT  
		Size: 28.0 MB (28000423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:1402edee0a57e2a79eb26417e928263d9f4a60bb29c18d470171aae3a6303d25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:latest` - linux; amd64

```console
$ docker pull ubuntu@sha256:d21429c4635332e96a4baae3169e3f02ac8e24e6ae3d89a86002d49a1259a4f7
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28867545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3dc08bfed031182827888bb15977e316ad797ee2ccb63b4c7a57fdfe7eb31d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:49b384cc7b4aa0dfd16ff7817ad0ea04f1d0a8072e62114efcd99119f8ceb9ed`  
		Last Modified: Mon, 29 Apr 2024 17:08:44 GMT  
		Size: 28.9 MB (28867545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c94d54dd82aba50b58c698accfc4a0a849955ba93f3a1de76353326caf2e9229
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26109958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cfdfc5de64a9bf2322886c5eeb80e1da07abc070d02ca1ffbd429bc3f0782c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:03:39 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:03:42 GMT
ADD file:158f9c2033bf15aea7323a8fc02ed64bb41784f98f36b5faf68a959346a86757 in / 
# Tue, 23 Apr 2024 22:03:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4163275920c38f5bf1c5e40b38598dba06a2fb1edd701aa7fcb16be1cad2a2de`  
		Last Modified: Tue, 23 Apr 2024 22:26:40 GMT  
		Size: 26.1 MB (26109958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d55bf48d8900628edec854908273b6adc4003a8fa4f43aa48f3287899f859d39
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28012692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07db2ffa22daeb428e1b654f77b0bb60c3368c2d391c77c4d3f379d982669084`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:03:43 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:03:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:03:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:03:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:03:45 GMT
ADD file:61020b87bc980abd05e75207205df7ecca6ea7023b3a5e804aabded0eebbf2e7 in / 
# Tue, 23 Apr 2024 22:03:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:67c893392cd92a994ecf5f35ecd3eba2631838f68b751dd27dac25a9e8a736cf`  
		Last Modified: Tue, 23 Apr 2024 22:26:33 GMT  
		Size: 28.0 MB (28012692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:8ea7c2024af7c23083fdd313080e7765036a7a00e87cd004a2213433dddb2b17
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33490376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db75cc60d4de04f10e12664827c4024c2a622a22985023ced8b4bedba66d9c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:16:12 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:16:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:16:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:16:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:16:16 GMT
ADD file:7fd16485139d3989a1a5565c0d7fb14bb79403891eb470189d51dac672fd641b in / 
# Tue, 23 Apr 2024 22:16:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c84264c6c2e73f5dbe8fd6afdcd17c6c94824d50c386190238f88f29f3cc059d`  
		Last Modified: Tue, 23 Apr 2024 22:26:46 GMT  
		Size: 33.5 MB (33490376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:31e02f893eaf7729befc0e21920e63b968bffe76760943a6f56fa1c7f3abb055
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29165121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ddac1146e91c07078f0becc2472c05513ee6f3b42c467cbe1176bc7a8bcd99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:11 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:13 GMT
ADD file:09121ba3a412b610ce92684a3218535826bd353b73e98bc8efe44ad9b4233d0d in / 
# Mon, 29 Apr 2024 16:38:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d450eb1572800c4118ae87f5fd5ee2a6fa067b00be1e578fcfee7725ca35a70e`  
		Last Modified: Mon, 29 Apr 2024 17:09:10 GMT  
		Size: 29.2 MB (29165121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

```console
$ docker pull ubuntu@sha256:431db664ea655923702ac110ec4d09bb63bb146b2e37ef8cc889831990ee5dd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:mantic` - linux; amd64

```console
$ docker pull ubuntu@sha256:141d7b0a56d0bd0b876765c20b48ec40e1843a09c1d0c79aa5efee82bee21244
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27234007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd494f24c6ee4c536c1aa8b913be1fc699bf8d7d51911036d3671da8b36fefd3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:02:03 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:02:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:02:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:02:03 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 16:02:05 GMT
ADD file:870c43eadc01423c5bc11fc4422ee10b05cae0f50c997f8e380e0ed25c6c0b11 in / 
# Mon, 29 Apr 2024 16:02:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:56c566a8d234cbea1867522f63b812f51bb091866286e8f350f23a951171b9f5`  
		Last Modified: Mon, 29 Apr 2024 16:18:42 GMT  
		Size: 27.2 MB (27234007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:5df962bf62a7d0ece2200f3fd4427a707c4a0612279568ab98f3c9ac92fd3e01
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24888954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b006a6e04b9773d4390c9e5af30114f3056d4b8db54c7c44bbe01d422b34b107`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:08:51 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:08:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:08:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:08:51 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:08:54 GMT
ADD file:f07b1f2c0ba7dbff20c2f89af95625b7160c10dd0b56c8ce400479098ff75d9e in / 
# Tue, 16 Apr 2024 12:08:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b3c603a20ac30fbf108a364f97b3fdbfd692ee1c1b2597567218e72db6eaff94`  
		Last Modified: Tue, 16 Apr 2024 12:46:43 GMT  
		Size: 24.9 MB (24888954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:4627f4a72bfc36475f6b0e7fa6f8865d75a165d47d437ad386168f3be107f989
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26414813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c1de4085ecee82c5f3f244ee7797d92808e34c4de513b5bd68fa46f6b2ad06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:36:32 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:36:32 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:36:36 GMT
ADD file:2a859c5d715743469a5a33d7b6038db94be34745cff1d5f681ed1d3d0e5931a6 in / 
# Tue, 16 Apr 2024 12:36:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b78e311e28b3f037f6cfc8470f0dfa0c1d89160a34d0dadefa10b3239d33dfe6`  
		Last Modified: Tue, 16 Apr 2024 12:46:37 GMT  
		Size: 26.4 MB (26414813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ccc5e01ef699b4e4ed576499c885c727667a2df98ae5e8af8006b18a5513315b
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31365049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60663f39f12fa270dee6f0356d34f06facdae5daed954433b6b1733405b0e94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:36:34 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:36:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:36:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:36:35 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:36:42 GMT
ADD file:d101590827db35fb306467a12041319349f48362c5708f20a992cacfa084f678 in / 
# Tue, 16 Apr 2024 12:36:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:42e56421b7ba4fdaf4a5c3dbdfde02f434b638fcb84d80270dec2b3c9f4b0ca7`  
		Last Modified: Tue, 16 Apr 2024 12:46:49 GMT  
		Size: 31.4 MB (31365049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; s390x

```console
$ docker pull ubuntu@sha256:47c6b893ab777ea2f23f010efa7af2b964ec6d3e04409dbc421e5cf06b9cfc45
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27332110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070b853442b94c5e9ad49f3224ce745ad43cb333eeb4ea19788f224c4da22aa1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 15:49:35 GMT
ARG RELEASE
# Mon, 29 Apr 2024 15:49:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 15:49:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 15:49:35 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 15:49:37 GMT
ADD file:76b6235c926b9bd628f27161f73913d479e584c2035eb7185806b814f4e96e14 in / 
# Mon, 29 Apr 2024 15:49:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e5f6811577ee1a4f42b07b0ef1fbbdd8a4cf7b470ee3ea89de99f370a57bf832`  
		Last Modified: Mon, 29 Apr 2024 16:19:08 GMT  
		Size: 27.3 MB (27332110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic-20240427`

```console
$ docker pull ubuntu@sha256:a24a8225d97e111f8ff41bea82e70c3357aacc40a47c528b4539f04165880177
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; s390x

### `ubuntu:mantic-20240427` - linux; amd64

```console
$ docker pull ubuntu@sha256:141d7b0a56d0bd0b876765c20b48ec40e1843a09c1d0c79aa5efee82bee21244
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27234007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd494f24c6ee4c536c1aa8b913be1fc699bf8d7d51911036d3671da8b36fefd3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:02:03 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:02:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:02:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:02:03 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 16:02:05 GMT
ADD file:870c43eadc01423c5bc11fc4422ee10b05cae0f50c997f8e380e0ed25c6c0b11 in / 
# Mon, 29 Apr 2024 16:02:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:56c566a8d234cbea1867522f63b812f51bb091866286e8f350f23a951171b9f5`  
		Last Modified: Mon, 29 Apr 2024 16:18:42 GMT  
		Size: 27.2 MB (27234007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240427` - linux; s390x

```console
$ docker pull ubuntu@sha256:47c6b893ab777ea2f23f010efa7af2b964ec6d3e04409dbc421e5cf06b9cfc45
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27332110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070b853442b94c5e9ad49f3224ce745ad43cb333eeb4ea19788f224c4da22aa1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 15:49:35 GMT
ARG RELEASE
# Mon, 29 Apr 2024 15:49:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 15:49:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 15:49:35 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 15:49:37 GMT
ADD file:76b6235c926b9bd628f27161f73913d479e584c2035eb7185806b814f4e96e14 in / 
# Mon, 29 Apr 2024 15:49:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e5f6811577ee1a4f42b07b0ef1fbbdd8a4cf7b470ee3ea89de99f370a57bf832`  
		Last Modified: Mon, 29 Apr 2024 16:19:08 GMT  
		Size: 27.3 MB (27332110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble`

```console
$ docker pull ubuntu@sha256:1402edee0a57e2a79eb26417e928263d9f4a60bb29c18d470171aae3a6303d25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:noble` - linux; amd64

```console
$ docker pull ubuntu@sha256:d21429c4635332e96a4baae3169e3f02ac8e24e6ae3d89a86002d49a1259a4f7
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28867545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3dc08bfed031182827888bb15977e316ad797ee2ccb63b4c7a57fdfe7eb31d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:49b384cc7b4aa0dfd16ff7817ad0ea04f1d0a8072e62114efcd99119f8ceb9ed`  
		Last Modified: Mon, 29 Apr 2024 17:08:44 GMT  
		Size: 28.9 MB (28867545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c94d54dd82aba50b58c698accfc4a0a849955ba93f3a1de76353326caf2e9229
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26109958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cfdfc5de64a9bf2322886c5eeb80e1da07abc070d02ca1ffbd429bc3f0782c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:03:39 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:03:42 GMT
ADD file:158f9c2033bf15aea7323a8fc02ed64bb41784f98f36b5faf68a959346a86757 in / 
# Tue, 23 Apr 2024 22:03:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4163275920c38f5bf1c5e40b38598dba06a2fb1edd701aa7fcb16be1cad2a2de`  
		Last Modified: Tue, 23 Apr 2024 22:26:40 GMT  
		Size: 26.1 MB (26109958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d55bf48d8900628edec854908273b6adc4003a8fa4f43aa48f3287899f859d39
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28012692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07db2ffa22daeb428e1b654f77b0bb60c3368c2d391c77c4d3f379d982669084`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:03:43 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:03:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:03:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:03:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:03:45 GMT
ADD file:61020b87bc980abd05e75207205df7ecca6ea7023b3a5e804aabded0eebbf2e7 in / 
# Tue, 23 Apr 2024 22:03:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:67c893392cd92a994ecf5f35ecd3eba2631838f68b751dd27dac25a9e8a736cf`  
		Last Modified: Tue, 23 Apr 2024 22:26:33 GMT  
		Size: 28.0 MB (28012692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:8ea7c2024af7c23083fdd313080e7765036a7a00e87cd004a2213433dddb2b17
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33490376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db75cc60d4de04f10e12664827c4024c2a622a22985023ced8b4bedba66d9c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:16:12 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:16:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:16:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:16:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:16:16 GMT
ADD file:7fd16485139d3989a1a5565c0d7fb14bb79403891eb470189d51dac672fd641b in / 
# Tue, 23 Apr 2024 22:16:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c84264c6c2e73f5dbe8fd6afdcd17c6c94824d50c386190238f88f29f3cc059d`  
		Last Modified: Tue, 23 Apr 2024 22:26:46 GMT  
		Size: 33.5 MB (33490376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; s390x

```console
$ docker pull ubuntu@sha256:31e02f893eaf7729befc0e21920e63b968bffe76760943a6f56fa1c7f3abb055
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29165121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ddac1146e91c07078f0becc2472c05513ee6f3b42c467cbe1176bc7a8bcd99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:11 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:13 GMT
ADD file:09121ba3a412b610ce92684a3218535826bd353b73e98bc8efe44ad9b4233d0d in / 
# Mon, 29 Apr 2024 16:38:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d450eb1572800c4118ae87f5fd5ee2a6fa067b00be1e578fcfee7725ca35a70e`  
		Last Modified: Mon, 29 Apr 2024 17:09:10 GMT  
		Size: 29.2 MB (29165121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble-20240429`

```console
$ docker pull ubuntu@sha256:4044130df74b1007f0924d1e66ee888bbcb2d1b548a1ed74bd2c3ca81f01fee9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; s390x

### `ubuntu:noble-20240429` - linux; amd64

```console
$ docker pull ubuntu@sha256:d21429c4635332e96a4baae3169e3f02ac8e24e6ae3d89a86002d49a1259a4f7
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28867545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3dc08bfed031182827888bb15977e316ad797ee2ccb63b4c7a57fdfe7eb31d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:49b384cc7b4aa0dfd16ff7817ad0ea04f1d0a8072e62114efcd99119f8ceb9ed`  
		Last Modified: Mon, 29 Apr 2024 17:08:44 GMT  
		Size: 28.9 MB (28867545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240429` - linux; s390x

```console
$ docker pull ubuntu@sha256:31e02f893eaf7729befc0e21920e63b968bffe76760943a6f56fa1c7f3abb055
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29165121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ddac1146e91c07078f0becc2472c05513ee6f3b42c467cbe1176bc7a8bcd99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:11 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:13 GMT
ADD file:09121ba3a412b610ce92684a3218535826bd353b73e98bc8efe44ad9b4233d0d in / 
# Mon, 29 Apr 2024 16:38:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d450eb1572800c4118ae87f5fd5ee2a6fa067b00be1e578fcfee7725ca35a70e`  
		Last Modified: Mon, 29 Apr 2024 17:09:10 GMT  
		Size: 29.2 MB (29165121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:1402edee0a57e2a79eb26417e928263d9f4a60bb29c18d470171aae3a6303d25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:rolling` - linux; amd64

```console
$ docker pull ubuntu@sha256:d21429c4635332e96a4baae3169e3f02ac8e24e6ae3d89a86002d49a1259a4f7
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28867545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3dc08bfed031182827888bb15977e316ad797ee2ccb63b4c7a57fdfe7eb31d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:49b384cc7b4aa0dfd16ff7817ad0ea04f1d0a8072e62114efcd99119f8ceb9ed`  
		Last Modified: Mon, 29 Apr 2024 17:08:44 GMT  
		Size: 28.9 MB (28867545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c94d54dd82aba50b58c698accfc4a0a849955ba93f3a1de76353326caf2e9229
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26109958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cfdfc5de64a9bf2322886c5eeb80e1da07abc070d02ca1ffbd429bc3f0782c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:03:39 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:03:42 GMT
ADD file:158f9c2033bf15aea7323a8fc02ed64bb41784f98f36b5faf68a959346a86757 in / 
# Tue, 23 Apr 2024 22:03:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4163275920c38f5bf1c5e40b38598dba06a2fb1edd701aa7fcb16be1cad2a2de`  
		Last Modified: Tue, 23 Apr 2024 22:26:40 GMT  
		Size: 26.1 MB (26109958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d55bf48d8900628edec854908273b6adc4003a8fa4f43aa48f3287899f859d39
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28012692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07db2ffa22daeb428e1b654f77b0bb60c3368c2d391c77c4d3f379d982669084`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:03:43 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:03:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:03:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:03:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:03:45 GMT
ADD file:61020b87bc980abd05e75207205df7ecca6ea7023b3a5e804aabded0eebbf2e7 in / 
# Tue, 23 Apr 2024 22:03:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:67c893392cd92a994ecf5f35ecd3eba2631838f68b751dd27dac25a9e8a736cf`  
		Last Modified: Tue, 23 Apr 2024 22:26:33 GMT  
		Size: 28.0 MB (28012692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:8ea7c2024af7c23083fdd313080e7765036a7a00e87cd004a2213433dddb2b17
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33490376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db75cc60d4de04f10e12664827c4024c2a622a22985023ced8b4bedba66d9c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:16:12 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:16:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:16:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:16:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:16:16 GMT
ADD file:7fd16485139d3989a1a5565c0d7fb14bb79403891eb470189d51dac672fd641b in / 
# Tue, 23 Apr 2024 22:16:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c84264c6c2e73f5dbe8fd6afdcd17c6c94824d50c386190238f88f29f3cc059d`  
		Last Modified: Tue, 23 Apr 2024 22:26:46 GMT  
		Size: 33.5 MB (33490376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:31e02f893eaf7729befc0e21920e63b968bffe76760943a6f56fa1c7f3abb055
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29165121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ddac1146e91c07078f0becc2472c05513ee6f3b42c467cbe1176bc7a8bcd99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:11 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:13 GMT
ADD file:09121ba3a412b610ce92684a3218535826bd353b73e98bc8efe44ad9b4233d0d in / 
# Mon, 29 Apr 2024 16:38:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d450eb1572800c4118ae87f5fd5ee2a6fa067b00be1e578fcfee7725ca35a70e`  
		Last Modified: Mon, 29 Apr 2024 17:09:10 GMT  
		Size: 29.2 MB (29165121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
