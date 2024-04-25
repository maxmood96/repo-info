<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:23.10`](#ubuntu2310)
-	[`ubuntu:24.04`](#ubuntu2404)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20240416`](#ubuntufocal-20240416)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20240416`](#ubuntujammy-20240416)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20240416`](#ubuntumantic-20240416)
-	[`ubuntu:noble`](#ubuntunoble)
-	[`ubuntu:noble-20240423`](#ubuntunoble-20240423)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:21ae67bf44d1d0a53ecdce48742c766e44aea4d16e18a3b88a3888eddaf782b5
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
$ docker pull ubuntu@sha256:cc61ae337f89ec395bf1d0b13c6f58ee834e3fc57b0de67694302bb637294300
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c9e106c9d9e28be2a5b7177b6079722213e2f76f15033f9614688024faf69f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4477f8fe99ebfd23fa06d28a2fa42eaa05d726926afc0a055e1ff2b612b7a293`  
		Last Modified: Wed, 17 Apr 2024 18:54:17 GMT  
		Size: 27.5 MB (27511740 bytes)  
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
$ docker pull ubuntu@sha256:34f7a6bf809a048bb7410596b3e79fe528d8db555037cdcc0fe6cdd28f81ebbf
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26367492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dc3614d906854005a159349657f6197981c2c8e153cd9a19f172859a8b3c59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:38:36 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:38:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:38:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:38:36 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:38:40 GMT
ADD file:da0ff0dbc934fe8a302da2a67ea8c5ff869d6bfdd919e1e1956c06f0cf34caf5 in / 
# Wed, 17 Apr 2024 18:38:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:58b877bf9e274878a32c49b69f298edbc9918ba172b0c63d20847cb5b82ce8eb`  
		Last Modified: Wed, 17 Apr 2024 18:54:44 GMT  
		Size: 26.4 MB (26367492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:6d7b5d3317a71adb5e175640150e44b8b9a9401a7dd394f44840626aff9fa94d
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
$ docker pull ubuntu@sha256:e8ac95e1b49f06d0533601ed1eb609d9b553f38cfe39f295868604ea83ee4d6d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437ec753bef37f94b7426428201feac1ed99190eacafdab558c4f626808cde04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e311a697a4031e52691ab1b5a8c325a448280fef9fc03d89dd97ab40f4245bce`  
		Last Modified: Wed, 17 Apr 2024 18:55:29 GMT  
		Size: 29.5 MB (29534028 bytes)  
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
$ docker pull ubuntu@sha256:d96bd8afa1b8a4b421a25b9416e5e94a7a4daf34911fecba0f800dee20a7b289
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5501c0751b2671b9937354cb3da8546e92da8ca3f677e9c0634bc73c440b0ff4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:42:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:42:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:42:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:42:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:42:34 GMT
ADD file:f721f8e69988c4a423ddfb143b1001213ba52ffe029e8623c2f62e210d611fbc in / 
# Wed, 17 Apr 2024 18:42:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:69f495792ca5ae69cb97986c54ee9f3fe805a53ca9f2f710b9ea60e20d0665ce`  
		Last Modified: Wed, 17 Apr 2024 18:55:55 GMT  
		Size: 28.0 MB (28000323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.10`

```console
$ docker pull ubuntu@sha256:bfae41cea51761ae450db6080b586a8c35334c756b511c06b393ae565a34cab4
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
$ docker pull ubuntu@sha256:7c151867cb4361e2c3ef67292aa1381158e279ed5a938bf3cd94b0902cdf271c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27233855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6dfff70ab08e6e729605dab23db47e63318ad5d4bd3755f81ef61edc36338b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:05:34 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:05:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:05:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:05:34 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:05:35 GMT
ADD file:e12b21146377229efd13935eb949a5d74cf2b246efc163ed315734630be3958c in / 
# Tue, 16 Apr 2024 12:05:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1039cbbd4ddd89f4a92572c9d25ae65572b3a23e6639b098d4d5037486b11b92`  
		Last Modified: Tue, 16 Apr 2024 12:46:30 GMT  
		Size: 27.2 MB (27233855 bytes)  
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
$ docker pull ubuntu@sha256:6a8c9e2452486e9af2f9d341f526e36b92ae153773c6f3d2bf075fef525e820e
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27332278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d60ec45481f4b29c95a39c6fb32f115c3ff9ad35d1fa78898f4a947380d5abf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:37:06 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:37:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:37:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:37:06 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:37:12 GMT
ADD file:bcaae6745c5074969da19bc7c697ea513ed4123bd3a263300b0dd2d86c419d62 in / 
# Tue, 16 Apr 2024 12:37:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb37a35236685ddfbba3beeca31d9aff06067e3467c97a9723710161595363b9`  
		Last Modified: Tue, 16 Apr 2024 12:46:55 GMT  
		Size: 27.3 MB (27332278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:24.04`

```console
$ docker pull ubuntu@sha256:562456a05a0dbd62a671c1854868862a4687bf979a96d48ae8e766642cd911e8
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
$ docker pull ubuntu@sha256:28a2b328825ac02db5c29d9356bfba80ba6c4b6ebfcac5a91a4656fa3453775a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28864706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de52d803b2245ea6d6b4235e43533dc5a70ea3837c0db840603d0b828d42266c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:00:11 GMT
ADD file:019ce26ec491bab156f6a15e93164ae5351fd38c7fff11d00c69c18e31e9dde3 in / 
# Tue, 23 Apr 2024 22:00:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fdcaa7e87498b7e172f808aa62dfb30c533563cb3e474262835357118da1f260`  
		Last Modified: Tue, 23 Apr 2024 22:26:27 GMT  
		Size: 28.9 MB (28864706 bytes)  
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
$ docker pull ubuntu@sha256:50bf9a282f4cd5d16ca4f05f8d55d01e4a3416b626a8af08126de109647e7b9d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29163278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ee08a3647dafdc0e67cc85666d8d77e924fd673256e7483f8a61df083899f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:59 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:01:01 GMT
ADD file:a8f6a75bd4e0f37e8479b0e5c1fd1ab287398559996948607323ac5831f29411 in / 
# Tue, 23 Apr 2024 22:01:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:079354fd34419cc993e11413ed32f193311de47dd426438ef91ac660e3e58e99`  
		Last Modified: Tue, 23 Apr 2024 22:26:52 GMT  
		Size: 29.2 MB (29163278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:21ae67bf44d1d0a53ecdce48742c766e44aea4d16e18a3b88a3888eddaf782b5
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
$ docker pull ubuntu@sha256:cc61ae337f89ec395bf1d0b13c6f58ee834e3fc57b0de67694302bb637294300
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c9e106c9d9e28be2a5b7177b6079722213e2f76f15033f9614688024faf69f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4477f8fe99ebfd23fa06d28a2fa42eaa05d726926afc0a055e1ff2b612b7a293`  
		Last Modified: Wed, 17 Apr 2024 18:54:17 GMT  
		Size: 27.5 MB (27511740 bytes)  
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
$ docker pull ubuntu@sha256:34f7a6bf809a048bb7410596b3e79fe528d8db555037cdcc0fe6cdd28f81ebbf
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26367492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dc3614d906854005a159349657f6197981c2c8e153cd9a19f172859a8b3c59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:38:36 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:38:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:38:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:38:36 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:38:40 GMT
ADD file:da0ff0dbc934fe8a302da2a67ea8c5ff869d6bfdd919e1e1956c06f0cf34caf5 in / 
# Wed, 17 Apr 2024 18:38:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:58b877bf9e274878a32c49b69f298edbc9918ba172b0c63d20847cb5b82ce8eb`  
		Last Modified: Wed, 17 Apr 2024 18:54:44 GMT  
		Size: 26.4 MB (26367492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20240416`

```console
$ docker pull ubuntu@sha256:21ae67bf44d1d0a53ecdce48742c766e44aea4d16e18a3b88a3888eddaf782b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal-20240416` - linux; amd64

```console
$ docker pull ubuntu@sha256:cc61ae337f89ec395bf1d0b13c6f58ee834e3fc57b0de67694302bb637294300
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c9e106c9d9e28be2a5b7177b6079722213e2f76f15033f9614688024faf69f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4477f8fe99ebfd23fa06d28a2fa42eaa05d726926afc0a055e1ff2b612b7a293`  
		Last Modified: Wed, 17 Apr 2024 18:54:17 GMT  
		Size: 27.5 MB (27511740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240416` - linux; arm variant v7

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

### `ubuntu:focal-20240416` - linux; arm64 variant v8

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

### `ubuntu:focal-20240416` - linux; ppc64le

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

### `ubuntu:focal-20240416` - linux; s390x

```console
$ docker pull ubuntu@sha256:34f7a6bf809a048bb7410596b3e79fe528d8db555037cdcc0fe6cdd28f81ebbf
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26367492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dc3614d906854005a159349657f6197981c2c8e153cd9a19f172859a8b3c59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:38:36 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:38:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:38:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:38:36 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:38:40 GMT
ADD file:da0ff0dbc934fe8a302da2a67ea8c5ff869d6bfdd919e1e1956c06f0cf34caf5 in / 
# Wed, 17 Apr 2024 18:38:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:58b877bf9e274878a32c49b69f298edbc9918ba172b0c63d20847cb5b82ce8eb`  
		Last Modified: Wed, 17 Apr 2024 18:54:44 GMT  
		Size: 26.4 MB (26367492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:6d7b5d3317a71adb5e175640150e44b8b9a9401a7dd394f44840626aff9fa94d
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
$ docker pull ubuntu@sha256:e8ac95e1b49f06d0533601ed1eb609d9b553f38cfe39f295868604ea83ee4d6d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437ec753bef37f94b7426428201feac1ed99190eacafdab558c4f626808cde04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e311a697a4031e52691ab1b5a8c325a448280fef9fc03d89dd97ab40f4245bce`  
		Last Modified: Wed, 17 Apr 2024 18:55:29 GMT  
		Size: 29.5 MB (29534028 bytes)  
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
$ docker pull ubuntu@sha256:d96bd8afa1b8a4b421a25b9416e5e94a7a4daf34911fecba0f800dee20a7b289
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5501c0751b2671b9937354cb3da8546e92da8ca3f677e9c0634bc73c440b0ff4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:42:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:42:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:42:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:42:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:42:34 GMT
ADD file:f721f8e69988c4a423ddfb143b1001213ba52ffe029e8623c2f62e210d611fbc in / 
# Wed, 17 Apr 2024 18:42:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:69f495792ca5ae69cb97986c54ee9f3fe805a53ca9f2f710b9ea60e20d0665ce`  
		Last Modified: Wed, 17 Apr 2024 18:55:55 GMT  
		Size: 28.0 MB (28000323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20240416`

```console
$ docker pull ubuntu@sha256:6d7b5d3317a71adb5e175640150e44b8b9a9401a7dd394f44840626aff9fa94d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy-20240416` - linux; amd64

```console
$ docker pull ubuntu@sha256:e8ac95e1b49f06d0533601ed1eb609d9b553f38cfe39f295868604ea83ee4d6d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437ec753bef37f94b7426428201feac1ed99190eacafdab558c4f626808cde04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e311a697a4031e52691ab1b5a8c325a448280fef9fc03d89dd97ab40f4245bce`  
		Last Modified: Wed, 17 Apr 2024 18:55:29 GMT  
		Size: 29.5 MB (29534028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240416` - linux; arm variant v7

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

### `ubuntu:jammy-20240416` - linux; arm64 variant v8

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

### `ubuntu:jammy-20240416` - linux; ppc64le

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

### `ubuntu:jammy-20240416` - linux; s390x

```console
$ docker pull ubuntu@sha256:d96bd8afa1b8a4b421a25b9416e5e94a7a4daf34911fecba0f800dee20a7b289
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5501c0751b2671b9937354cb3da8546e92da8ca3f677e9c0634bc73c440b0ff4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:42:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:42:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:42:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:42:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:42:34 GMT
ADD file:f721f8e69988c4a423ddfb143b1001213ba52ffe029e8623c2f62e210d611fbc in / 
# Wed, 17 Apr 2024 18:42:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:69f495792ca5ae69cb97986c54ee9f3fe805a53ca9f2f710b9ea60e20d0665ce`  
		Last Modified: Wed, 17 Apr 2024 18:55:55 GMT  
		Size: 28.0 MB (28000323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:562456a05a0dbd62a671c1854868862a4687bf979a96d48ae8e766642cd911e8
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
$ docker pull ubuntu@sha256:28a2b328825ac02db5c29d9356bfba80ba6c4b6ebfcac5a91a4656fa3453775a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28864706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de52d803b2245ea6d6b4235e43533dc5a70ea3837c0db840603d0b828d42266c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:00:11 GMT
ADD file:019ce26ec491bab156f6a15e93164ae5351fd38c7fff11d00c69c18e31e9dde3 in / 
# Tue, 23 Apr 2024 22:00:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fdcaa7e87498b7e172f808aa62dfb30c533563cb3e474262835357118da1f260`  
		Last Modified: Tue, 23 Apr 2024 22:26:27 GMT  
		Size: 28.9 MB (28864706 bytes)  
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
$ docker pull ubuntu@sha256:50bf9a282f4cd5d16ca4f05f8d55d01e4a3416b626a8af08126de109647e7b9d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29163278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ee08a3647dafdc0e67cc85666d8d77e924fd673256e7483f8a61df083899f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:59 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:01:01 GMT
ADD file:a8f6a75bd4e0f37e8479b0e5c1fd1ab287398559996948607323ac5831f29411 in / 
# Tue, 23 Apr 2024 22:01:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:079354fd34419cc993e11413ed32f193311de47dd426438ef91ac660e3e58e99`  
		Last Modified: Tue, 23 Apr 2024 22:26:52 GMT  
		Size: 29.2 MB (29163278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

```console
$ docker pull ubuntu@sha256:bfae41cea51761ae450db6080b586a8c35334c756b511c06b393ae565a34cab4
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
$ docker pull ubuntu@sha256:7c151867cb4361e2c3ef67292aa1381158e279ed5a938bf3cd94b0902cdf271c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27233855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6dfff70ab08e6e729605dab23db47e63318ad5d4bd3755f81ef61edc36338b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:05:34 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:05:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:05:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:05:34 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:05:35 GMT
ADD file:e12b21146377229efd13935eb949a5d74cf2b246efc163ed315734630be3958c in / 
# Tue, 16 Apr 2024 12:05:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1039cbbd4ddd89f4a92572c9d25ae65572b3a23e6639b098d4d5037486b11b92`  
		Last Modified: Tue, 16 Apr 2024 12:46:30 GMT  
		Size: 27.2 MB (27233855 bytes)  
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
$ docker pull ubuntu@sha256:6a8c9e2452486e9af2f9d341f526e36b92ae153773c6f3d2bf075fef525e820e
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27332278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d60ec45481f4b29c95a39c6fb32f115c3ff9ad35d1fa78898f4a947380d5abf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:37:06 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:37:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:37:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:37:06 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:37:12 GMT
ADD file:bcaae6745c5074969da19bc7c697ea513ed4123bd3a263300b0dd2d86c419d62 in / 
# Tue, 16 Apr 2024 12:37:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb37a35236685ddfbba3beeca31d9aff06067e3467c97a9723710161595363b9`  
		Last Modified: Tue, 16 Apr 2024 12:46:55 GMT  
		Size: 27.3 MB (27332278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic-20240416`

```console
$ docker pull ubuntu@sha256:bfae41cea51761ae450db6080b586a8c35334c756b511c06b393ae565a34cab4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:mantic-20240416` - linux; amd64

```console
$ docker pull ubuntu@sha256:7c151867cb4361e2c3ef67292aa1381158e279ed5a938bf3cd94b0902cdf271c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27233855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6dfff70ab08e6e729605dab23db47e63318ad5d4bd3755f81ef61edc36338b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:05:34 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:05:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:05:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:05:34 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:05:35 GMT
ADD file:e12b21146377229efd13935eb949a5d74cf2b246efc163ed315734630be3958c in / 
# Tue, 16 Apr 2024 12:05:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1039cbbd4ddd89f4a92572c9d25ae65572b3a23e6639b098d4d5037486b11b92`  
		Last Modified: Tue, 16 Apr 2024 12:46:30 GMT  
		Size: 27.2 MB (27233855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240416` - linux; arm variant v7

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

### `ubuntu:mantic-20240416` - linux; arm64 variant v8

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

### `ubuntu:mantic-20240416` - linux; ppc64le

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

### `ubuntu:mantic-20240416` - linux; s390x

```console
$ docker pull ubuntu@sha256:6a8c9e2452486e9af2f9d341f526e36b92ae153773c6f3d2bf075fef525e820e
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27332278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d60ec45481f4b29c95a39c6fb32f115c3ff9ad35d1fa78898f4a947380d5abf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:37:06 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:37:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:37:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:37:06 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:37:12 GMT
ADD file:bcaae6745c5074969da19bc7c697ea513ed4123bd3a263300b0dd2d86c419d62 in / 
# Tue, 16 Apr 2024 12:37:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb37a35236685ddfbba3beeca31d9aff06067e3467c97a9723710161595363b9`  
		Last Modified: Tue, 16 Apr 2024 12:46:55 GMT  
		Size: 27.3 MB (27332278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble`

```console
$ docker pull ubuntu@sha256:562456a05a0dbd62a671c1854868862a4687bf979a96d48ae8e766642cd911e8
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
$ docker pull ubuntu@sha256:28a2b328825ac02db5c29d9356bfba80ba6c4b6ebfcac5a91a4656fa3453775a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28864706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de52d803b2245ea6d6b4235e43533dc5a70ea3837c0db840603d0b828d42266c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:00:11 GMT
ADD file:019ce26ec491bab156f6a15e93164ae5351fd38c7fff11d00c69c18e31e9dde3 in / 
# Tue, 23 Apr 2024 22:00:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fdcaa7e87498b7e172f808aa62dfb30c533563cb3e474262835357118da1f260`  
		Last Modified: Tue, 23 Apr 2024 22:26:27 GMT  
		Size: 28.9 MB (28864706 bytes)  
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
$ docker pull ubuntu@sha256:50bf9a282f4cd5d16ca4f05f8d55d01e4a3416b626a8af08126de109647e7b9d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29163278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ee08a3647dafdc0e67cc85666d8d77e924fd673256e7483f8a61df083899f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:59 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:01:01 GMT
ADD file:a8f6a75bd4e0f37e8479b0e5c1fd1ab287398559996948607323ac5831f29411 in / 
# Tue, 23 Apr 2024 22:01:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:079354fd34419cc993e11413ed32f193311de47dd426438ef91ac660e3e58e99`  
		Last Modified: Tue, 23 Apr 2024 22:26:52 GMT  
		Size: 29.2 MB (29163278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble-20240423`

```console
$ docker pull ubuntu@sha256:562456a05a0dbd62a671c1854868862a4687bf979a96d48ae8e766642cd911e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:noble-20240423` - linux; amd64

```console
$ docker pull ubuntu@sha256:28a2b328825ac02db5c29d9356bfba80ba6c4b6ebfcac5a91a4656fa3453775a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28864706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de52d803b2245ea6d6b4235e43533dc5a70ea3837c0db840603d0b828d42266c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:00:11 GMT
ADD file:019ce26ec491bab156f6a15e93164ae5351fd38c7fff11d00c69c18e31e9dde3 in / 
# Tue, 23 Apr 2024 22:00:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fdcaa7e87498b7e172f808aa62dfb30c533563cb3e474262835357118da1f260`  
		Last Modified: Tue, 23 Apr 2024 22:26:27 GMT  
		Size: 28.9 MB (28864706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240423` - linux; arm variant v7

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

### `ubuntu:noble-20240423` - linux; arm64 variant v8

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

### `ubuntu:noble-20240423` - linux; ppc64le

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

### `ubuntu:noble-20240423` - linux; s390x

```console
$ docker pull ubuntu@sha256:50bf9a282f4cd5d16ca4f05f8d55d01e4a3416b626a8af08126de109647e7b9d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29163278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ee08a3647dafdc0e67cc85666d8d77e924fd673256e7483f8a61df083899f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:59 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:01:01 GMT
ADD file:a8f6a75bd4e0f37e8479b0e5c1fd1ab287398559996948607323ac5831f29411 in / 
# Tue, 23 Apr 2024 22:01:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:079354fd34419cc993e11413ed32f193311de47dd426438ef91ac660e3e58e99`  
		Last Modified: Tue, 23 Apr 2024 22:26:52 GMT  
		Size: 29.2 MB (29163278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:562456a05a0dbd62a671c1854868862a4687bf979a96d48ae8e766642cd911e8
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
$ docker pull ubuntu@sha256:28a2b328825ac02db5c29d9356bfba80ba6c4b6ebfcac5a91a4656fa3453775a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28864706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de52d803b2245ea6d6b4235e43533dc5a70ea3837c0db840603d0b828d42266c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:00:11 GMT
ADD file:019ce26ec491bab156f6a15e93164ae5351fd38c7fff11d00c69c18e31e9dde3 in / 
# Tue, 23 Apr 2024 22:00:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fdcaa7e87498b7e172f808aa62dfb30c533563cb3e474262835357118da1f260`  
		Last Modified: Tue, 23 Apr 2024 22:26:27 GMT  
		Size: 28.9 MB (28864706 bytes)  
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
$ docker pull ubuntu@sha256:50bf9a282f4cd5d16ca4f05f8d55d01e4a3416b626a8af08126de109647e7b9d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29163278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ee08a3647dafdc0e67cc85666d8d77e924fd673256e7483f8a61df083899f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:59 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:01:01 GMT
ADD file:a8f6a75bd4e0f37e8479b0e5c1fd1ab287398559996948607323ac5831f29411 in / 
# Tue, 23 Apr 2024 22:01:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:079354fd34419cc993e11413ed32f193311de47dd426438ef91ac660e3e58e99`  
		Last Modified: Tue, 23 Apr 2024 22:26:52 GMT  
		Size: 29.2 MB (29163278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
