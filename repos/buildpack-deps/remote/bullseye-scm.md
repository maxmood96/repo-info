## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:c59f4b616760aa5f19641a6d7091db6a3e9a795233ca93a1f3dede6f0b6c243a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2de01d14c23c27a0aa8f7daaa81d270f5ece0d2da06b6c974ece241cf647b37d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125450362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ff236d5953f579716fa68e791140c9a3800929d7159cae8810c3517ff48688`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:11 GMT
ADD file:54b23fc0b4b728c85082d50693e314d74e46329004bb55a97f43fea46c497dd2 in / 
# Fri, 26 Mar 2021 15:20:12 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:51:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:51:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 05:51:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:efee637ec1bae521f17fb8d92548c288e3396988c475551b8774c0d08c01c70f`  
		Last Modified: Fri, 26 Mar 2021 15:26:18 GMT  
		Size: 54.9 MB (54867948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0666f582e314627706e5e9fe66995fb84f633adc4b7b51e0ebb2a1d3f0678e38`  
		Last Modified: Sat, 27 Mar 2021 06:02:20 GMT  
		Size: 5.2 MB (5150446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff7141fe7ae560896fd2c43b0f6b628c5deed0a1e88d53e9ec72109e60c8533`  
		Last Modified: Sat, 27 Mar 2021 06:02:21 GMT  
		Size: 10.9 MB (10867044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670868a9f541b0c094771e75bfec22db184771c8090eae2be1e34a7cbf54c640`  
		Last Modified: Sat, 27 Mar 2021 06:02:41 GMT  
		Size: 54.6 MB (54564924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fc0a96c8059bcbfd4bd01013f1f32bc836a7d3467c3d9c7eba0e7d58243121a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120348805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0e82882eb21c312386e36a474e5d40af96374a3c21f7f569b6200bfe90f4de`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 07:50:33 GMT
ADD file:1b779b19b47bb1848292d2bf671b599eb9041626b747d8016817e0c7d46ff881 in / 
# Fri, 26 Mar 2021 07:50:38 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 09:04:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:05:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 09:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d8d862331f8860c127d174052922618c93a166777e5b776e8b08e87702af28cd`  
		Last Modified: Fri, 26 Mar 2021 07:59:08 GMT  
		Size: 52.4 MB (52404525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6864d5c0a91a133802b130cddb5c9fb77329c250e4f5d77c05e96188cbcb31`  
		Last Modified: Fri, 26 Mar 2021 09:25:47 GMT  
		Size: 5.1 MB (5060013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0cf03c5e0e5a428fa3a5789c4793210e762dbfb24e1f688a878754fe9ada6`  
		Last Modified: Fri, 26 Mar 2021 09:25:48 GMT  
		Size: 10.6 MB (10569895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1985045f60a052a5d3b4e89129ae9f03ece21620c4b057aa105c0c78cc5775a4`  
		Last Modified: Fri, 26 Mar 2021 09:26:11 GMT  
		Size: 52.3 MB (52314372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:895671b64d35c1257769edc7bf65f4e503a02b13978c4926c661e67a3e5d5c39
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115540400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8505cf255310b4f659882c40eaec332ff1c19ee9754274a784fc0f5335f2a668`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 11:15:27 GMT
ADD file:e3651409d9338da981cd9fbd8d9b8511edbde0700ac9e0df8937b859e004990d in / 
# Fri, 26 Mar 2021 11:15:29 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:16:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:16:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 13:17:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dd9021b04def024e25507cdd1b0967a20a384ad5cc255120cfb8c5f43495fa74`  
		Last Modified: Fri, 26 Mar 2021 11:26:11 GMT  
		Size: 50.1 MB (50073977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c6023b28762fcb2cca84dd988c0545da69e2cb9cea40e5fb1a14dce3d7d186`  
		Last Modified: Fri, 26 Mar 2021 13:48:58 GMT  
		Size: 4.9 MB (4920097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94408c405dc2689a60515a2dee289cb3495f53f4b4f9758de6995e07aa073eb2`  
		Last Modified: Fri, 26 Mar 2021 13:48:59 GMT  
		Size: 10.2 MB (10218160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd339501262a81addad6326243dbcf62ca43943542cc42a3b06aeda9a9cdec3a`  
		Last Modified: Fri, 26 Mar 2021 13:49:44 GMT  
		Size: 50.3 MB (50328166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f005c9a7ffa9e399ebbea3826b41f63fe6064cdde552f76f5cac0143fec67c77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124228903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b577cd38a297a28ed0be7193c1cda142d0a0135d44f826b96b988b6e322b8433`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:40:38 GMT
ADD file:7a01671cc1e0be7531bee33435db95fa465b434bb5f683b3418f6e0768eb5367 in / 
# Fri, 26 Mar 2021 15:40:42 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 04:10:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 04:11:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 04:11:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aadeaa81c69d313bcee9d050d099f2efd49d3c36d4dc100444f09cd71321f257`  
		Last Modified: Fri, 26 Mar 2021 15:47:37 GMT  
		Size: 53.6 MB (53555170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658bc452bf9be006159874b02c94f08d809e2583b8dd7391adce7cb8cdb8e482`  
		Last Modified: Sat, 27 Mar 2021 04:26:37 GMT  
		Size: 5.1 MB (5139822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1e794367c2db608ea61b995e4171ef23dc7cc1b2308b5251db2abc290a6568`  
		Last Modified: Sat, 27 Mar 2021 04:26:38 GMT  
		Size: 10.9 MB (10867643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e8786a82c0b910129fc3ece32df1ad66d5096a7d6059fc5e65579facafa53`  
		Last Modified: Sat, 27 Mar 2021 04:27:05 GMT  
		Size: 54.7 MB (54666268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:bb2c76a88da737750fa9435b712d5415ccf01422afa5f8e67b0656af86b33ba7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128318140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0b147919fd794579b106c522201e2605406ebb82c0499d3dc704085641687c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 13:52:22 GMT
ADD file:a351d1298a5051f829e330b747943dba9a67cc050d1f23f62be062f669830e9a in / 
# Fri, 26 Mar 2021 13:52:23 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 22:41:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 22:41:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 22:41:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fb6fc5804fde9f18c538230f43ec9b5dc9c2466d8fc49f7510911c12de70d991`  
		Last Modified: Fri, 26 Mar 2021 14:00:05 GMT  
		Size: 55.9 MB (55881460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47770a32ee01d7a5a9ea596d431299fafb3e5ec55cda781b4b8ba77139d3b742`  
		Last Modified: Fri, 26 Mar 2021 22:54:02 GMT  
		Size: 5.3 MB (5278994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b619575768f273ceeaf065659966267b58a5378b4b7d52fdcd0648e68b378227`  
		Last Modified: Fri, 26 Mar 2021 22:54:03 GMT  
		Size: 11.2 MB (11248822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce028724865c02e9ace59fe70b5f2ea0c85782a125e91d44e337fc658f84434`  
		Last Modified: Fri, 26 Mar 2021 22:54:36 GMT  
		Size: 55.9 MB (55908864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:47335ed37ad5ad0bb64b948ce0199b99c49e39aad14216ac3a93a4ae1e7833bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122410906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23601ef8a9b6fa5044ea0336b0a3203ebf67c9467b5102a4462aa0dcca851619`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 08:08:46 GMT
ADD file:7e11d2e31071a03f4f43a78cd6af64c7034e2267c839bee84afd1e3bb9916f3e in / 
# Fri, 26 Mar 2021 08:08:47 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 18:13:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 18:13:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 18:15:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e3b00636426049a0189d8511a90dd5801df2b5793acbaa564ad20c57c4ff115`  
		Last Modified: Fri, 26 Mar 2021 08:14:22 GMT  
		Size: 53.1 MB (53128793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c11a8343730b68d55c2c17295713c1932bfdeed6cd26ba010cb68214e4f5638`  
		Last Modified: Fri, 26 Mar 2021 18:27:18 GMT  
		Size: 5.1 MB (5112340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503e0f155ade594fd8b18a219ba3f1174ed82e7465c9b852325d8a8a11c870d2`  
		Last Modified: Fri, 26 Mar 2021 18:27:20 GMT  
		Size: 10.9 MB (10870299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5514c276e4dbcbce3dce646bff262cc3c13a68791d15a0585f7a759615c558f`  
		Last Modified: Fri, 26 Mar 2021 18:28:10 GMT  
		Size: 53.3 MB (53299474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3acbefea54b6c3865dbb6a60514a49df919d0a76d0d7e6ccd01f31a1b5f14fa4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134622038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9954ed350f1f32e08d008065ac376d26457d9fdd95be10fce4215ea7cc9340`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:12:40 GMT
ADD file:28f7d129aaacc2de6bb78dec104b788d0aa25aaac87e07873668354a5b755268 in / 
# Fri, 26 Mar 2021 15:12:49 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 17:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 17:13:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 17:15:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:18ddfb418fe2dc2d92f9b851d0345827010c7b001ef98bb5a8b1730d80e2eace`  
		Last Modified: Fri, 26 Mar 2021 15:20:35 GMT  
		Size: 58.8 MB (58756702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e58f4581a73db06180cd5d10d619dc8b47cdbf57bed71dbf9eb53d28bc4749`  
		Last Modified: Fri, 26 Mar 2021 19:34:46 GMT  
		Size: 5.4 MB (5399177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e302f47f5e7c563d0f23745e32bd160587a44a206808295a2ca9d29a6b9d67`  
		Last Modified: Fri, 26 Mar 2021 19:34:51 GMT  
		Size: 11.6 MB (11619666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9f221c0a34707baac4ad94f19a4bd62b803303c74a200e7d8ced228745c108`  
		Last Modified: Fri, 26 Mar 2021 19:36:24 GMT  
		Size: 58.8 MB (58846493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:033377fc76ad18a8c8eda2ed3d7f527a21f542882f779fca5bc76cfb9352d85f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123079434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f2c005e666e9ae589b4fda2ab2a6bc4db7c967be34f58bf63c919e90103662`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 10:52:51 GMT
ADD file:6dd7d4b323fd63c8ee8a655a79017b62cdad999e420310b15e9568404d02e856 in / 
# Fri, 26 Mar 2021 10:52:58 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:39:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:39:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 15:40:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7fcb7355b5dda69e2044a1c24be0597b43954f9d3183dde70ac38aac25df7adb`  
		Last Modified: Fri, 26 Mar 2021 10:56:55 GMT  
		Size: 53.1 MB (53147819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4483fa86d703794bc974862181191f13737481044629eefcee195f179e335064`  
		Last Modified: Fri, 26 Mar 2021 15:53:59 GMT  
		Size: 5.1 MB (5134107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e227b0ad592b8d4f1e74bc91d5c854ab0a75abf65452545c61ce392a04f489f5`  
		Last Modified: Fri, 26 Mar 2021 15:54:00 GMT  
		Size: 10.8 MB (10758559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e907d7501cb26d3573f807160ae0b0b98d3c254793f034d9f3356af99600645d`  
		Last Modified: Fri, 26 Mar 2021 15:54:24 GMT  
		Size: 54.0 MB (54038949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
