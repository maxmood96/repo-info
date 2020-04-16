## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:800b40b6f463a78e37d6a913c3047f4bf8325e772b4d0b1515b78da4b9a42215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7f7f185300585e2de635f25e390588673c87d450a424e57b25d257c57e6acaee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125787750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9d81d9cf55a0acc03e455d864a0d8a3638b84abf1dd1c7e25cee850612bcb4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:22:48 GMT
ADD file:7562f01f4040e4f21a40337301dd14e4377f3d101bd0919a96ae05bff37d7087 in / 
# Tue, 31 Mar 2020 01:22:48 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:05:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:05:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 02:05:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:616821eae326bcd1b2974181d172e5949f2c8c091398159b63b0f483913be88a`  
		Last Modified: Tue, 31 Mar 2020 01:28:20 GMT  
		Size: 51.9 MB (51949680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c04e796c39db97cc83b98c665f9d3f60b53540de3aef972a49131d996b2aab`  
		Last Modified: Tue, 31 Mar 2020 02:11:44 GMT  
		Size: 7.9 MB (7930362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e38af22482c0eee10c6177e3f57aebccdca1c6f4050aa653ba0fefcffec7507`  
		Last Modified: Tue, 31 Mar 2020 02:11:42 GMT  
		Size: 10.3 MB (10297863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14b2afe7eba2a0d3afe523ef0cfbd8492e331f5114b35c8cc6dbee1c196889d`  
		Last Modified: Tue, 31 Mar 2020 02:12:00 GMT  
		Size: 55.6 MB (55609845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:df855b373b550990f4cc96490ba5bb78a4990530e899424aabbf4f27b2027111
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120680161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e92421e033f34973310df40b327d1fe5c87dfe874247a50a6515310994918d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:27:39 GMT
ADD file:a797b22ab77042681c9442f161cd9c34b230f5e897a7c038c5e619cf0e8159f3 in / 
# Tue, 31 Mar 2020 01:27:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:35:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:36:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 03:37:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9a071e689ab0273b55b5ea6cd2f8c7f83096ceff8fb3d7a616e059804c29d70c`  
		Last Modified: Tue, 31 Mar 2020 01:35:22 GMT  
		Size: 49.9 MB (49891269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e955f774e68fb041a9d50840f6e6c139bb7aa9f26aaeaeffed32316761a69b1`  
		Last Modified: Tue, 31 Mar 2020 03:50:06 GMT  
		Size: 7.5 MB (7512962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97a6ee6cfc96be92a20ec0b7b805e4c521d088957adbd612a4252a4f45ed15c`  
		Last Modified: Tue, 31 Mar 2020 03:50:06 GMT  
		Size: 10.0 MB (10008505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571262e91f17243db435c188e3873071be5aae97276bad3f0a2e436bd99b555e`  
		Last Modified: Tue, 31 Mar 2020 03:50:31 GMT  
		Size: 53.3 MB (53267425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:94638f3bf517d750e4d53247b1648732c732bd8f4900689ab4e83ecd69dbda34
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115519587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d24b4edf6d5fc1a0456923a64b389b3889f82e3f0a5ace623d48eebdb71bcf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:50:55 GMT
ADD file:fdbba631aa2e54ebb3f3a92627367ce7e2e6efb1157a884945e4d69c360073ea in / 
# Tue, 31 Mar 2020 01:50:57 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:49:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:49:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 03:49:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fc5c37e59a5331bf2b56343097ed41f57f5df3c898439059baccb2d6dfbcb203`  
		Last Modified: Tue, 31 Mar 2020 01:58:45 GMT  
		Size: 47.6 MB (47626226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c70a792a98ea8510fe5ed73c7568e177f2c055525cabdeec63f3b252f9785d`  
		Last Modified: Tue, 31 Mar 2020 04:03:18 GMT  
		Size: 7.3 MB (7253641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f4973145ed34075ebb198eb399df21ca2d3d039494b853c612c0848fb447c5`  
		Last Modified: Tue, 31 Mar 2020 04:03:18 GMT  
		Size: 9.7 MB (9672910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f44d80d06a7a6f1d0a37e8ac63f05264d98ae04e13c146e3610e0bd40c8d930`  
		Last Modified: Tue, 31 Mar 2020 04:03:40 GMT  
		Size: 51.0 MB (50966810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:27e8d8dc1b437dc09aeed258b3f2f8561f41c4afb593b7030aafe53442f5145f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124806681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4880de8f07be75d1391865240af7a0a98c55755fc0b3204b8d79010f1e680db2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 02:06:41 GMT
ADD file:89d1d53ca595aac3a67a5b8b833603f2f27cb35fff838b1e022c7b8d9ab52c27 in / 
# Tue, 31 Mar 2020 02:06:44 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:37:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:37:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 04:38:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d022a4286a83893fda6e1ecf3f90454f2247ecc550aae515cf06acb929d6340b`  
		Last Modified: Tue, 31 Mar 2020 02:13:07 GMT  
		Size: 50.9 MB (50882731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07eb75dbe1288fca2b2cdf0cce2fd4c6d5eba054268b57545b206b8cfd35061d`  
		Last Modified: Tue, 31 Mar 2020 04:48:14 GMT  
		Size: 7.8 MB (7805629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fd428992877f78dcb767e9cb28893448835f9ea1a1b69a22f9f68485bc7bca`  
		Last Modified: Tue, 31 Mar 2020 04:48:14 GMT  
		Size: 10.3 MB (10294206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d231c2f2ceb2cf79f1aab709a30d6085011d1af257ceeb61f7f18e233bcf7e8d`  
		Last Modified: Tue, 31 Mar 2020 04:48:39 GMT  
		Size: 55.8 MB (55824115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:70f397880c21bdadbb05fdda14dcce696e36c25ccfe16427ee9978c83eab5453
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129449677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b893a07ecaefb695d1b319012713e2afc351ca1d6e8a5a57d31b341b48e075`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:41:56 GMT
ADD file:af11f81927371cc0ed957aa36f4036c71c73a0b79ab27523cf0d49d8e0260041 in / 
# Thu, 16 Apr 2020 01:41:57 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:31:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:31:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 02:31:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1cf4ce40baf558f42709af03658907805f477c72b1b1a39869aef429cd35cd3c`  
		Last Modified: Thu, 16 Apr 2020 01:48:16 GMT  
		Size: 53.1 MB (53130042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dcc2dce5f80bcf713e09688ddce4e707509747c60ac5dcb21b50ba63fa26bf6`  
		Last Modified: Thu, 16 Apr 2020 02:39:42 GMT  
		Size: 8.1 MB (8110058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b96fa002b78190463928c6db889856164ede953e0bbc48a860d1856d448dd69`  
		Last Modified: Thu, 16 Apr 2020 02:39:43 GMT  
		Size: 10.7 MB (10657287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7351fce1761580c1a90469f6a39ce4b504f9c1b1c46ac9de64a36b5067846200`  
		Last Modified: Thu, 16 Apr 2020 02:40:03 GMT  
		Size: 57.6 MB (57552290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fb8d69aaeccae37fe1ed7f927f5d4789339ec417ab036e956b705a146f50a171
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136161370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407ea49622cca7cec0c09a9740e4a16cdf9e62d2ce4677c6534675e76ddb85ed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:34:16 GMT
ADD file:8f010ac42180d1a69abeb831a2cf65af2b505dc37ca5566d1f8e0af98223a68d in / 
# Tue, 31 Mar 2020 01:34:25 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:32:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:33:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 03:35:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a96cc3285dca9557b63f3a1daed7cabe2c2e3fd70599474a054f37ae9105c6c`  
		Last Modified: Tue, 31 Mar 2020 01:48:49 GMT  
		Size: 55.8 MB (55834936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616d46070d2d79dda9e6b725a456cc523fced90f731b94a80fe3b63dcbb34f63`  
		Last Modified: Tue, 31 Mar 2020 04:04:16 GMT  
		Size: 8.4 MB (8354814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30854a2a0cd6b68888c600cb3b15000ac47d6f0a9bb3ccafda003ddeebe996f`  
		Last Modified: Tue, 31 Mar 2020 04:04:16 GMT  
		Size: 11.0 MB (10975756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371525c676a3a79f437345a7eeb988835dfceaba7ee6c5cd16e3e63ca520fd21`  
		Last Modified: Tue, 31 Mar 2020 04:05:16 GMT  
		Size: 61.0 MB (60995864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:125e455dd3fcd6d56ce6c4302cdb387e0021e7ba69aaa96526c915e386b0b3c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123299289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cee77f2b515d74f062725ea776c7796ce9d2a6f09a6e28da1ecce901614ddde`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:42:56 GMT
ADD file:1d96a73c9c03d31b0a60aa6b4e0215085afcdee6dc39954655798110c12c223f in / 
# Thu, 16 Apr 2020 00:42:59 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:01:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:01:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 02:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3633d30b569d7f8e4addec62b3bb5c460572eb82d6568a9bc40a9f189dc4bdcb`  
		Last Modified: Thu, 16 Apr 2020 00:47:02 GMT  
		Size: 50.6 MB (50576543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275dfe1709bf7bfd1a7e225a7b974994148dca503ef21f837a74970529f9eb01`  
		Last Modified: Thu, 16 Apr 2020 02:07:15 GMT  
		Size: 7.6 MB (7600071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae5ff7d1251f85fd4f476599f4408381f4e029ec36f4f1b66a96e89b921e7a0`  
		Last Modified: Thu, 16 Apr 2020 02:07:16 GMT  
		Size: 10.2 MB (10183857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686e996ff9bb08017109e59fc8068db8d4300aea3359952891468365b7d82d4d`  
		Last Modified: Thu, 16 Apr 2020 02:07:29 GMT  
		Size: 54.9 MB (54938818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
