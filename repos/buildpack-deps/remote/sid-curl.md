## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:bb021af4a6ed072eeae8386791161e470202148474a95c3baea4823e2801329e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:caad2aca24ca403a1973910e2f4791f36b7b3e5fb425af6a7770bd22e9d221f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76600977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd25a8ea97d2b2f86521600ddb5e57db254046cacca05377c30858cfb434fb0b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:5df7677e65add6d6a9ff681d686094447da195b4999a1f7cff2192740e38e1af in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9fbbc539fc86b3c511f2260d35b9cf5ffb90638ed287142abafd6e1e4bdffbf8`  
		Last Modified: Sat, 30 Mar 2024 20:54:42 GMT  
		Size: 51.5 MB (51500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a99bf11f4d755d4745d428a5f8e59469920e4fa2dbb6384cd2d8b4155e6ee0`  
		Last Modified: Sat, 30 Mar 2024 21:42:41 GMT  
		Size: 25.1 MB (25100684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cde303353e0557e4632fe6d4d3b1903636b16ed4c2f0dd2efdfde0c49154af97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72590238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099267525a60ae8269b784db17b8d89fc4883cbb22c185e879571bef8b17c008`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:36 GMT
ADD file:cd2edb4c012f30c27d706f9d77429a6159628b9f9825990e5ed53fadf0dd1f2a in / 
# Sat, 30 Mar 2024 20:51:36 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:803f1fb1440883aa3e0e25bfaee63bd45d691a63416fe58ffa21737aa458dded`  
		Last Modified: Sat, 30 Mar 2024 20:53:32 GMT  
		Size: 48.7 MB (48683606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4adcb1bcec984aff86f15319a4ef9bf43bac660d2c31fb398102ad3cc6190d3`  
		Last Modified: Sat, 30 Mar 2024 21:19:45 GMT  
		Size: 23.9 MB (23906632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7bb08393ddc9172f1653daee17542d08cfc7f31b1408c85caafcf52c575dacda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69422843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9ac916505f84bfb509eb3477762a21c71698e5f1db222611903011b9f4437d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:42 GMT
ADD file:0ac8f97579d9f7611b866966dd5fc34fcfa2144355ba39b31883284475bb2585 in / 
# Sat, 30 Mar 2024 20:52:42 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:24:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0e8b88d91442c01c97d07c620eba463296206c34b7c84ca5b992728b1cf4bd11`  
		Last Modified: Sat, 30 Mar 2024 20:54:52 GMT  
		Size: 46.3 MB (46295373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30834b6bf99a6286a5001978342fbaa380b0ba46f9fb0df977b164e1e3bea295`  
		Last Modified: Sat, 30 Mar 2024 21:30:32 GMT  
		Size: 23.1 MB (23127470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:13c28b84072c7e9d0bbb7ae510977c4d4e0747b52c234125f78d1b0aa91b20c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76206390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed51ceb4392ad24e0551894887ea30ccfd611cb6440074a774b34a4e8c6e1812`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:01 GMT
ADD file:0431bf12596e1a5c3a0d8d282912373bfc2669375b5302333bbd39ecebd1e167 in / 
# Sat, 30 Mar 2024 20:55:01 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a4a3e98356da458ec5973da971b31825c760cc233f97a317c13cc7d3cf704a6`  
		Last Modified: Sat, 30 Mar 2024 20:56:59 GMT  
		Size: 51.4 MB (51377212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c3484d93fd537ed2435acc265bea31f7a3701955afec657d7cc9501a506f91`  
		Last Modified: Sat, 30 Mar 2024 21:42:50 GMT  
		Size: 24.8 MB (24829178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cda0b4ed2c65d325d0edf15b4d5e8459bef2d4f5a27a1a8bd4d71cdf281e16b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78567250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13648a0fda94cb4145326f4037c8a9e7272bba5fe7754a9f298e9c2e5c1fadaa`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:47 GMT
ADD file:5c0cc8b80773608ad255427432daa6a4ea6c6d1257178c16e9fde71fe5f2c803 in / 
# Sat, 30 Mar 2024 20:51:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c8e6f721d25b23e18d050c75bbf87b16883b01f37acac5142a881b7006f7696`  
		Last Modified: Sat, 30 Mar 2024 20:54:19 GMT  
		Size: 52.3 MB (52279241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d21e3778f3e12a5abf7a2295be5a05142eaad46fa3793baaf32a4f9d5145082`  
		Last Modified: Sat, 30 Mar 2024 21:21:23 GMT  
		Size: 26.3 MB (26288009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:72e4be73652e8dc05458a7b54e9e9a1d8dcb15e658eda60002b5eb0a590beebd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76152427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b14909d446d42857d16c65a888f02ae7df059ba4b435fc88fa7069cd1fd2ef8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:54:42 GMT
ADD file:3fab027e6d739287e4b7349292c885c809a65c14845b5d292aebb3844ce27682 in / 
# Sat, 30 Mar 2024 20:54:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cbe55b4cce02b94dd21e3b65d94bdb65a4b1119288ec18dec4cbfe762dc19adc`  
		Last Modified: Sat, 30 Mar 2024 21:01:00 GMT  
		Size: 50.6 MB (50600834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195f963513fde292fd81669591d3906b0da2c957d9712fccfa5e3456c15942a0`  
		Last Modified: Sat, 30 Mar 2024 21:46:20 GMT  
		Size: 25.6 MB (25551593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:44b879235275c23ac4ea8f634435b73cdfbed488c37f0b59f1863bb04790b8c6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82654894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404ee2989f40b8bf1d782733ee67a4d51f809eacb777913582e8a8d508df5aa0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:03 GMT
ADD file:2bc730d62ee0ff93ea46112c42f75f01e2e6d04449beaf198c5ae6fb388ddd07 in / 
# Sat, 30 Mar 2024 20:55:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:35:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b6224779f10a25b25659a091e0036b5df62f6e69a0c2fe4dc52a3341dae37615`  
		Last Modified: Sat, 30 Mar 2024 20:57:40 GMT  
		Size: 55.3 MB (55287220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fe9d1bcfdfd6cc666707508081610ef2a537ca8a7a9e722c61d540ccb99bd4`  
		Last Modified: Sat, 30 Mar 2024 21:45:19 GMT  
		Size: 27.4 MB (27367674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:bec0eb25faa85054bdacab8da9d9d50138c42aaa16df08715df2110d680cf979
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74482043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f100f56d88dba8d99909f4819951fbde0a33ce797e908064862c52abc53caf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:1794cba0a957e1827904ac718c197ffa00b710464d3140140303007e1771a90b in / 
# Sat, 30 Mar 2024 20:52:17 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16e4421a3b562748342089caab583089b0a176e505692af61640bf0a5aad09c0`  
		Last Modified: Sat, 30 Mar 2024 20:55:01 GMT  
		Size: 49.7 MB (49699884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418fd4dbd9609ca7faf0abe9ea6267b25c79eed962f75cf26a985c129d246a50`  
		Last Modified: Sat, 30 Mar 2024 21:27:33 GMT  
		Size: 24.8 MB (24782159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b1495b19a1aef63cffb7ed02e326d62ebe3f7a8302e9dc9078de88cdb0138cec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77423194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6080271906badcffc8ea612ac576254148c13a27b420400e2e28096aaf192f4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:02:33 GMT
ADD file:5d186ec2d875f4307a34d264914243316106515ef9072abb7cf5e80c252da588 in / 
# Tue, 12 Mar 2024 01:02:36 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:21:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ec6259c8a823fea482e8e351d24e5f493bd9f11e76074191518e50ac63335314`  
		Last Modified: Tue, 12 Mar 2024 01:22:34 GMT  
		Size: 50.9 MB (50889351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d95670fd7000d49d11835682e227fc4e48c87caf6a3e9e49895a14def51b2b0`  
		Last Modified: Tue, 12 Mar 2024 02:49:09 GMT  
		Size: 26.5 MB (26533843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
