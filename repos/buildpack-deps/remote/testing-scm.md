## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:6774ea1a783f4f0ae05bd6cf7773de625ea972be3425df3518e08457ca8093bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:585656e13819d78a14d2e7038d5589af3eb6ee746bd30c82af2f8f043cb6aa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140117994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb3148837dc0db0a85a6b1d6b04ea41f0888a3c7bf61c285769d5ae575e85ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38f31efba20d2de2a38e9be5393dc31cf8ee1b44853ff5d87cddb66164a6614`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 20.6 MB (20643097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6a86195a6ac634586ab2d95656285880bf44bc989315a1a390e89fab37bcb2`  
		Last Modified: Sat, 19 Oct 2024 02:06:34 GMT  
		Size: 66.2 MB (66236156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3ea20d5bba8eeb2e736601c4ce114c361ac3fd03f83fef30075d024149db987c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e878cfa426f7d6f801ecbbd4da423790a35e9bb7f34a8518dceca0b05684c7f`

```dockerfile
```

-	Layers:
	-	`sha256:716f9e78031d3606e499bc4442ab01887e9daa138a84cd6040598b8b55e62485`  
		Last Modified: Sat, 19 Oct 2024 02:06:33 GMT  
		Size: 7.5 MB (7485854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b2b2da54ba360e1746e997c125c6c346c80274f7fa7c490be56551d6f15d1f`  
		Last Modified: Sat, 19 Oct 2024 02:06:33 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d37244e77642358ecbd8e02f932a2b902759f4e78f883342dd90c58bbbe8d718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133522236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c554071c074e0f5662cb4bfd4cfcded5ab8352625767fff7ca547532bd761ee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:010709d78fdc05933a72549f7cb322633ad7dbe3d97bfcbda0aa10337118fb24 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f9250cc0718983393b852e9ddb20839b610fbab7fa648abee09b726c74343ff5`  
		Last Modified: Thu, 17 Oct 2024 00:59:25 GMT  
		Size: 50.1 MB (50146097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5571697784adcbe29d963579310eec564ff21e0a1805050b884b9a866946b3`  
		Last Modified: Sat, 19 Oct 2024 00:56:34 GMT  
		Size: 19.6 MB (19643438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e345c83b2739677a81bb65e8b14bcf4b74047ea7c75729f3715016f0c7c8e4f7`  
		Last Modified: Sat, 19 Oct 2024 02:57:55 GMT  
		Size: 63.7 MB (63732701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:00d18a1cb21b84828374be7fe1569f0476ca91ce608c97e03e32e76273476c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e31d4e7fafe882a373e7a7298f5ea1647b1dbad6b13ce047d5cad2aedc3856`

```dockerfile
```

-	Layers:
	-	`sha256:20ca6cafe1bb36aec82c18a4b5ccdd308f9b10df0fa623351c59a932487d23de`  
		Last Modified: Sat, 19 Oct 2024 02:57:54 GMT  
		Size: 7.5 MB (7486766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c289e55fa61eb9c6049628f33edc91f1f20e240525f00e07e32498727c00d77`  
		Last Modified: Sat, 19 Oct 2024 02:57:53 GMT  
		Size: 7.4 KB (7386 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7066697a91a60d58795b2dd1699ae8b9951013f80a080391f83686cebb637d54
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127867058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf8200bc2a2bc7388ab86d683b382038f7813763c843e631c234a14bd75d738`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:05:25 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Thu, 17 Oct 2024 03:05:26 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:34:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b14885f9520938c577e16ecdfccbd10cf46510a9c0149d0d479ccd879d93d6`  
		Last Modified: Thu, 17 Oct 2024 03:40:06 GMT  
		Size: 19.0 MB (18974054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbebaaebd3fa818b1b4bafe8e7f26090da3811fd6c155b2f7f73dc8875a3a905`  
		Last Modified: Thu, 17 Oct 2024 03:40:26 GMT  
		Size: 61.2 MB (61233364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c91745059177b9c9ad8fb87b88908d8b89088446c5f8218182e1b847016d5859
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140290757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9abd2ff50f4249f751e5e2c3ba9e16c83bcdde940957f0a880f1786823d540`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:13:19 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Thu, 17 Oct 2024 01:13:19 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 04:34:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc979a58041d0ca8e5deac6b7852b9a756f65c5fde4ed5a01b9ab02ba82ff2a8`  
		Last Modified: Thu, 17 Oct 2024 04:38:39 GMT  
		Size: 20.4 MB (20385295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7f53239df6d74ac78e3ea17ce45a2e39dfce24b675fc31f8f4d6cf9bb4b4e1`  
		Last Modified: Thu, 17 Oct 2024 04:38:53 GMT  
		Size: 66.3 MB (66305737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:618815a42dba3ef78d1bb1de67f7ec2120dfdaad4720867753833cf4630f498e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143872452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e030da0121eee0eeab55546bdd08ca40bf003cf82e576562069a02c56e0e8dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5c3ffdc80062869321bb7433b1adb7b34816c3fba871dc68884bdb4115b512`  
		Last Modified: Sat, 19 Oct 2024 00:55:05 GMT  
		Size: 21.8 MB (21754592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86cb3c57ae9f50b2cf4f508d0c23399cc9692dfc7336323d593f363cb71e400`  
		Last Modified: Sat, 19 Oct 2024 02:06:45 GMT  
		Size: 68.0 MB (68040402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9008ac0613d41a0c2c395978561fe3ab8e18ff11ef7a1e577f10639da50b0e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3243a0416ab3c6b119ec1cf4e4e94ebdf31c3c374bc98f9b50e32fe11750e5`

```dockerfile
```

-	Layers:
	-	`sha256:7200b6a54740017d2b112c3bdeb08ad5b7011927790105fe36431b2f1e85f597`  
		Last Modified: Sat, 19 Oct 2024 02:06:43 GMT  
		Size: 7.5 MB (7481278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e262c25f641beedd8d9a8f58c64c13dd27c10bf508ee4c52904493950f448c`  
		Last Modified: Sat, 19 Oct 2024 02:06:42 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:78d50bdb37e5bb8ce65015b943145de8356d61c7bf9ac0d2b70b5bb19d61592f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138151112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c40a1f4ab862506927452bfc655b5b498b376a47d0ebbd5c7fe468eb7a88db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bde6977c24ffe15c007c6606184010ccb92606e6158cbd76d8e770997debfa`  
		Last Modified: Sat, 19 Oct 2024 01:01:31 GMT  
		Size: 21.0 MB (20966640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdea9feeed917171d6d06a6129bb34f0f75c8fdb0fc8f9755f248adca6eee285`  
		Last Modified: Sat, 19 Oct 2024 02:14:28 GMT  
		Size: 65.1 MB (65056004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:81190818ed7d83b0f92ee66dc853e7c6f22b9535d8e52f4f00fcfdc4354973ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f37bae74959741f2259d72bed0704bd028bbb2ff4414f68912774344bbdbf3c`

```dockerfile
```

-	Layers:
	-	`sha256:c02dd3eab5f5e9db4c0f38c6e763e61d6cf4e72819705f3060c07ec5c7819c76`  
		Last Modified: Sat, 19 Oct 2024 02:14:21 GMT  
		Size: 7.2 KB (7159 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:416d68c7a6ea996450091adfc2ad7659fe479b8592d3deb58962a40a976088ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152071022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a632aee26b4b1f0c77d9eea17429ff8bd4d62ccfc6a7c47e2034dda6e1ffa5f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:20:15 GMT
ADD file:7d34de8e15cda6686099080e64714532070b3d06a451fa9d77a5716745974490 in / 
# Thu, 17 Oct 2024 01:20:18 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:48:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8299bac21377f71d4bbd00f3075290f241c45c39e6a9a76012dbff5b62d14e88`  
		Last Modified: Thu, 17 Oct 2024 01:23:55 GMT  
		Size: 57.1 MB (57126645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbcab475561b983c55c4a069685bc4edb3857233ed2831996472141939c0d16`  
		Last Modified: Thu, 17 Oct 2024 01:53:43 GMT  
		Size: 23.3 MB (23316051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ae8e30c2b54262517c9a764062e90b5c337fd1a1089c9cbf94ea5050e659bb`  
		Last Modified: Thu, 17 Oct 2024 01:54:02 GMT  
		Size: 71.6 MB (71628326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4092e136e316706611e3fe5fa99da9c6cabe42ae013f7299d619ad4f8b8a3552
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141805274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b6c9ff4c72451df23ef7ace56e7a671b1e27f39121b289a02c061aa4ac6b1c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:48:13 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Thu, 17 Oct 2024 01:48:15 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:45:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:45:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e49835389a5b3be307cfcaee824ac271d1c990968ebef582d739387fe8cd1a5`  
		Last Modified: Thu, 17 Oct 2024 03:50:19 GMT  
		Size: 21.7 MB (21658714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba0166b7d6671ccc810cbc6335bc33f3a6c82e87668bb0dee7a3abc097ff3d1`  
		Last Modified: Thu, 17 Oct 2024 03:50:34 GMT  
		Size: 67.3 MB (67337716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
