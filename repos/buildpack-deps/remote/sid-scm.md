## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:f12de483c34a7ddc9d021936475a0433b663acd108b94d0c4e9fbb541f68c740
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
$ docker pull buildpack-deps@sha256:84bf66b1fa99892160d3ec742ea4dc743df694f9dd3a620241419c5024da3646
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129338846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa4eda296a398179e2e4633d1bc19af0b9649d7a462a15eff7c9113dd86a064`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 00:41:33 GMT
ADD file:013e2e45d880a5e5d3c8ac0fafc140790ca1cefd17f2567b30509c07e6bd04d9 in / 
# Tue, 31 Mar 2020 00:41:33 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:22:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:23:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:23:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6b4a325a89fc0cab2f3ade12182ef3b2b0d777b725c55ef166a7d8e1d80d7425`  
		Last Modified: Tue, 31 Mar 2020 00:47:26 GMT  
		Size: 53.1 MB (53085713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da8b75e1598f9c9c1768e28dd5414741333f37655c91c43cf6d35fd9a2f8e0d`  
		Last Modified: Tue, 31 Mar 2020 01:31:35 GMT  
		Size: 8.1 MB (8108721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6053a7232909f13050253bad2d64e10fc1f0cdd4d248a794a99c4f71ae186c1`  
		Last Modified: Tue, 31 Mar 2020 01:31:35 GMT  
		Size: 10.7 MB (10657222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540a37aecc444b244c1b92d817cbd18b62937c7a451261c81a129ebee7d922e6`  
		Last Modified: Tue, 31 Mar 2020 01:31:57 GMT  
		Size: 57.5 MB (57487190 bytes)  
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
$ docker pull buildpack-deps@sha256:f122a24abf200ebce46efe03cb21a1c29c16cb3c97db0283453d4583031fa9ea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123196397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40475846f7806e02e9ca34d11f8c48a2e1e57051a2f1e1d43e369c0a7604854`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:09:33 GMT
ADD file:416f205dbbd8311318e69b6a4cd3d5426df0bc88ee4293cc800980d9d95e85fc in / 
# Tue, 31 Mar 2020 01:09:35 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:23:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:23:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 02:23:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:14bc63db6ec21658b800879387ad1a9200b09e59912af2bf8c5fe175da9e5ec6`  
		Last Modified: Tue, 31 Mar 2020 01:13:18 GMT  
		Size: 50.5 MB (50546013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4527654ed18a1f30bed3dfc69b5b6b62d0dd0d886de936b12dc43261ab235c`  
		Last Modified: Tue, 31 Mar 2020 02:29:31 GMT  
		Size: 7.6 MB (7597631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76af75185df23fadda1aa1fce4299d7f85ac601bd6d2e00a3a54023456b0581`  
		Last Modified: Tue, 31 Mar 2020 02:29:36 GMT  
		Size: 10.2 MB (10183863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e51fa7629c7a4c3615d5a8fbc92d2dd9d5a1cc4b2af9704ba63068c647a3bb`  
		Last Modified: Tue, 31 Mar 2020 02:29:49 GMT  
		Size: 54.9 MB (54868890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
