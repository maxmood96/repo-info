## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:a898d6958f737cb865443f7cf0d63518fa05e8f61345205c2664306b3a8d993d
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d4e775cb76782502bd02eece1eda4b0a8d55a4d3ee1dc17c14b09feafd209899
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73654654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bdfa4dad25173a03ab31b77b3e6e228879dd9ed3040b7767dff741d2e6ce27`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:30:28 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
# Fri, 27 Sep 2024 04:30:28 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:10:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dae9d245be83a876418da4287aadc60061be7b905df337290be90c8e2bd942b`  
		Last Modified: Fri, 27 Sep 2024 05:16:24 GMT  
		Size: 20.4 MB (20404612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:326c47ff85ea598c88a6373d582ef1c6de0eb3fc0b7f6a9fa9f59250ea5f813f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69564930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c238989bfbc727c388dd851fa69e387bedaa311f086ed31c2213d306af10bb1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:29 GMT
ADD file:4e733f6ab5ca47e96afa5484ac2356542259685b0f38d5370aaf3ff6efd60b52 in / 
# Fri, 27 Sep 2024 03:19:29 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2dab2d41b4d3c1013596d851ef68dd96a59ea71db4c50a8e9daec6977beb1e9a`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 50.1 MB (50141188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45409b0518e0782369823c9bfaead974fdd198f9b729525b7784d928cf3f7973`  
		Last Modified: Fri, 27 Sep 2024 04:04:32 GMT  
		Size: 19.4 MB (19423742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:087a4e515cf7a1f37454402410d12026217e390490710553bdd7b56bbe281d84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66427534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c64bff340794dad4d2c5fe7fde8be11e10f84ef198a2af322e27fbb2e8c5e6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:39 GMT
ADD file:7c02e68cb0d4c1b545df6c3c1548fdfbb0b8728190927f1aa0a481628eb80842 in / 
# Fri, 27 Sep 2024 05:14:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:55055767cac3db3f353667eecf5967bd4d61aaf6f68b845d1c472311762c6497`  
		Last Modified: Fri, 27 Sep 2024 05:18:38 GMT  
		Size: 47.7 MB (47656889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe7ba8ffc1ff9cdaa583c4b78a356d900036e41391f4ad532ea17ef7226ff6`  
		Last Modified: Fri, 27 Sep 2024 07:40:59 GMT  
		Size: 18.8 MB (18770645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8400ef23e2bfc1cf7961db7e7fc5cc365c21fc94bd265e5586c1ac7001d823c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73733338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaa242a8c35f491600ed256f8fa81f930e3e3971e3b401d781772eabee39a12`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:54 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
# Fri, 27 Sep 2024 04:38:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fc848450eda758c5f4c056230d289d3bacb82835760763661a9b5aebb3758a`  
		Last Modified: Fri, 27 Sep 2024 05:26:37 GMT  
		Size: 20.1 MB (20139073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7802476f80697b0d8d2e5d71ab473170f26b519bb144992d6add93dd482b2718
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75563583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6442f8185858decdddf033823e4bf8efbf0c130cc1fa8d22fd5c1d3018536d6e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:59 GMT
ADD file:b0f2319c396534f2fd08b2706fb1f0fd78e74e08c267d5e06e0eb0f82fe07ff0 in / 
# Fri, 27 Sep 2024 07:23:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:02:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:977268bcf0b2cba57760ad7ace3863e248276a9851a6938bfeda275ed37ec343`  
		Last Modified: Fri, 27 Sep 2024 07:28:47 GMT  
		Size: 54.1 MB (54077811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7fbbad98fe4fa8d720a3430a25da5207444dbe7555c066831aea5fea6901da`  
		Last Modified: Fri, 27 Sep 2024 08:09:26 GMT  
		Size: 21.5 MB (21485772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0c117689692b057acc8213bf376b412eff1499b594d99c9fdeeb8b793b8dd873
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72967287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e41b859b97c6e171049841788de1a97a82477edd39d6477efccc6dd4ad4862`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:16:21 GMT
ADD file:cfc638665fbd1de945c77faa66094fdc1c2a7a3e61a02e7558b48593a3569760 in / 
# Wed, 04 Sep 2024 22:16:26 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0fe676035759e9ba94505d30bcdda1c4551dcb03be9195f24905e870dce00126`  
		Last Modified: Wed, 04 Sep 2024 22:24:56 GMT  
		Size: 52.1 MB (52121073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb0177a8f9c1d11993a113ed4db6fe549ff6e3060d86438ab68826142d1fd2d`  
		Last Modified: Wed, 04 Sep 2024 23:16:19 GMT  
		Size: 20.8 MB (20846214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7dfe7f2474c97c8c5c6c60643147edd25a2275ef8d96ac019c47a72b54bd5c51
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80148788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9125d9685f5ce2e879b85d739962910d5e860f1cbd233aec7a11ac062aa49456`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:18 GMT
ADD file:61be8fbc8c48a038743e523ea5539b007c504e38025630b54f774464a5b21963 in / 
# Fri, 27 Sep 2024 05:33:21 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7d9882c6fe69b65aaa672267378b325d49eb761a1518c6646ba15eafea787b1f`  
		Last Modified: Fri, 27 Sep 2024 05:36:38 GMT  
		Size: 57.1 MB (57123161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5a7efb15e28989001836168c26f86cfa942d47c522ef07c07c02abbf8fb2a3`  
		Last Modified: Fri, 27 Sep 2024 06:05:40 GMT  
		Size: 23.0 MB (23025627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3215f819f7c134ef7f6419c2df43620029c30939b449a8d4cc7c62d3a946e8aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71500653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efed2f8783057bc14f79d6c2b2bd765819525f1d9769e0423b347a7d07e51f3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:42 GMT
ADD file:f7660b52d63bdf7c045c4722f75fe4e353e88b57bffc834348ad141ea0d12995 in / 
# Wed, 04 Sep 2024 22:25:44 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f9fbdbff518ec38d5367f0b03978c04c3107f39b06d2bb498f646b4903fd13db`  
		Last Modified: Wed, 04 Sep 2024 22:31:12 GMT  
		Size: 51.5 MB (51473852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea5ef465799bf40fb820e96c6cdb0b3ca4823cc42d2ef644d6b9684cb164fde`  
		Last Modified: Wed, 04 Sep 2024 23:07:16 GMT  
		Size: 20.0 MB (20026801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:32a8c0af96f9a31118c91a08bf2f2cf38dc4b986a325557d84203f43c7b6cdcf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74234173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9eee7a70ef8c4b7ebb8b8e5353eb05a0035489844aa9fbd353097589d36973d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:46 GMT
ADD file:5c5ad29b01b72e50aceb20af8172a88e23803553ed45c73a28a9a138856ba70d in / 
# Fri, 27 Sep 2024 02:43:51 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:17aa999733edd287bf5bd51ab2a58ef17211e311db82e8024e72304b5186e2aa`  
		Last Modified: Fri, 27 Sep 2024 02:47:37 GMT  
		Size: 52.8 MB (52808143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8d052710c80bb8f1ba5c4daebfc8ac149ed5b56a5185e5d6bd1a75f49bba31`  
		Last Modified: Fri, 27 Sep 2024 03:21:13 GMT  
		Size: 21.4 MB (21426030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
