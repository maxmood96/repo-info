## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:6558cf50b7208094416618f89f7e3ad64cae2c48e601c2d39562359020ca0397
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
$ docker pull buildpack-deps@sha256:da6fdb925b5de7f3beaaf9f7138cfab36ec0cbfdcdabf72cdad10c36ca194511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127859410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290b778918d3f0776bc82777549e9e66202608ae29931c36c3a39cb680f69433`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a052304c7554ffebe70b582d4e2eb7d1d61098f5f96c8c9603940278d081561`  
		Last Modified: Sat, 19 Oct 2024 00:58:30 GMT  
		Size: 19.0 MB (18971211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfcca10ec23fe707cc08f7ab790838065704861f60c0f678095482cc25ef593`  
		Last Modified: Sat, 19 Oct 2024 06:40:45 GMT  
		Size: 61.2 MB (61228559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9757a6eef12d8e4457f63d8128b0b8c16a0230cee675ce2af94935916d16c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea98d047064758984f353ad89edcd13307d0700c40c376b60bdac9d397af66c`

```dockerfile
```

-	Layers:
	-	`sha256:7a93cf475e613ba4986581169e51da296f5eab2d1af2eec23ca1a4ebddd8c326`  
		Last Modified: Sat, 19 Oct 2024 06:40:43 GMT  
		Size: 7.5 MB (7486524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20c2dfc26ee7918a49826fed2ffc0d36d6dd4dab8b3cc5d2ec3b13523d04f02c`  
		Last Modified: Sat, 19 Oct 2024 06:40:42 GMT  
		Size: 7.4 KB (7386 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3b629d663679a2b2b40868852c5dfbda509fd66bd6f901cdf256592706f0da24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140280895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6f779d0370a31853b4d9b6ad68485f28d2bdeb59641df30882b6ee54f6a915`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b74f65518d0117b47b1d80b0bf8981ebb7ddb04cdeeadd261af699b6e5d50`  
		Last Modified: Sat, 19 Oct 2024 01:12:15 GMT  
		Size: 20.4 MB (20382473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b125c1d7d6d0668d3d31049e15ed26c5f15741a45a407eab00423ec50972be12`  
		Last Modified: Sat, 19 Oct 2024 05:20:09 GMT  
		Size: 66.3 MB (66298697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:981b9d0b27672f9ae58a479116f2d44a4372d329f9e65910623c50857c7f2012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7499825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83b16a06a55282321f67d9ada42e21d02d811ecc3a3fc386acf84684d93a15b`

```dockerfile
```

-	Layers:
	-	`sha256:e31fe82ca59e0b11c21807625cd32304cb7c70ed6c502b0b98468e11df80130f`  
		Last Modified: Sat, 19 Oct 2024 05:20:07 GMT  
		Size: 7.5 MB (7492419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859f0a00775cceb04089b3a21a3466d9b86a3ba87b410318a08e54198cb54287`  
		Last Modified: Sat, 19 Oct 2024 05:20:06 GMT  
		Size: 7.4 KB (7406 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull buildpack-deps@sha256:69505418e2f16418896bfbd47bf5990e615e43e539795a7343b693ab3fefcbfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152062495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d9cc630724fda513523a563038d51b567be8858d61db84360b0480b76603af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7d34de8e15cda6686099080e64714532070b3d06a451fa9d77a5716745974490 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8299bac21377f71d4bbd00f3075290f241c45c39e6a9a76012dbff5b62d14e88`  
		Last Modified: Thu, 17 Oct 2024 01:23:55 GMT  
		Size: 57.1 MB (57126645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739c73c116650c722a140d5e98dc4d5b306e6daaa1f611e7f00699c828890445`  
		Last Modified: Sat, 19 Oct 2024 00:58:55 GMT  
		Size: 23.3 MB (23314858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888fc73ea70716bfd3afc5289dca8e001895bc72345d7defb80ef4274358afe4`  
		Last Modified: Sat, 19 Oct 2024 04:10:18 GMT  
		Size: 71.6 MB (71620992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:091947bf09abd557140c76ccc13c579c0bb566a957f213ac4199ad7c0b96ec62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072b1bb8073ec496b02f75e62dd6bc2ca92d82db16e29cf66cfeef186b98d497`

```dockerfile
```

-	Layers:
	-	`sha256:9a4d7b382551912c219e859278693e28ae0f33f686b14245a858b2574bd45057`  
		Last Modified: Sat, 19 Oct 2024 04:10:16 GMT  
		Size: 7.5 MB (7492964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b4ed94ce213d59bddff9f794ef0437815f2d5fc19ff6ff307e2969652c6e64`  
		Last Modified: Sat, 19 Oct 2024 04:10:15 GMT  
		Size: 7.4 KB (7358 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cb2e75552a2d042a659ba547ccb0609e06f697798884a74c6805ee8b1ab38d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141797604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9b44ffe80f44627eca35eaa520ed53a92ed54585062c43ba93198f9ec59a05`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3816f9124671541da45f7e11a0a925de47e719482f5bcd085247ecdcb8c613`  
		Last Modified: Sat, 19 Oct 2024 00:59:12 GMT  
		Size: 21.7 MB (21656188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cc2aa2fcdc4addb1b596c3dbc6f3699d60107644fd49f54f3050356c21437c`  
		Last Modified: Sat, 19 Oct 2024 03:48:52 GMT  
		Size: 67.3 MB (67332572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b270aaa7768e4a2d159ff7b5f42829b62c59d4ef131517f86c9ae12564beddae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942bb4de50d03290e36368d5b3922ed61f5adbe88b45bdc98fe4f5ece352669e`

```dockerfile
```

-	Layers:
	-	`sha256:be9cc770647715d3212ab0a996c38d93ff0e416f9d91de05c1000fc1ed5dc2b7`  
		Last Modified: Sat, 19 Oct 2024 03:48:52 GMT  
		Size: 7.5 MB (7486926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd9a3268144974562f1606345489a7a1d2317d957179ab65d447e065d5173d3`  
		Last Modified: Sat, 19 Oct 2024 03:48:51 GMT  
		Size: 7.3 KB (7326 bytes)  
		MIME: application/vnd.in-toto+json
