## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:e48f218ef9d456ce97d6339ebd4f029fc9740c768263cbb7f2c0ee52ecb24e3f
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

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a0dfbb6189f79fd0e2bb7eb008c62b2ff1de8588563a52aa79140c5f8e4da203
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120023461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ba591687c5bc3fdf1512d03321e0570b9f8310aa1832af9750d30d54589fb6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:20:19 GMT
ADD file:a50affde4f5ccdfd6450a642199121ffc180bb8cace944a55fab7a78ea851199 in / 
# Wed, 13 May 2020 21:20:19 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:27:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:27:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:28:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:be2ea06d55bb33c31098151d199a24029c4e0dd6bc5b3da9f617bb04e37d79d9`  
		Last Modified: Wed, 13 May 2020 21:26:07 GMT  
		Size: 50.4 MB (50387525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b353a80f0a7f8fad0ab9c83c30a335d821e084c20b62cf5ea881c00f5ee6aff6`  
		Last Modified: Wed, 13 May 2020 22:45:09 GMT  
		Size: 7.8 MB (7812385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f42905b195f8e4cad9788956a131dedb26c1be58f7e369ae2501e029fa863cb`  
		Last Modified: Wed, 13 May 2020 22:45:09 GMT  
		Size: 10.0 MB (9996250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c983e7b0e4d15e55eca9b2619b632703323413da9e3a2f4115776ddd2a5eb18a`  
		Last Modified: Wed, 13 May 2020 22:45:30 GMT  
		Size: 51.8 MB (51827301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6968067c4d20080524c2fc12ef00b54df5d44b8a7057d5e246b554cf5d1897ce
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114724920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49877f2b16a3b9b7f2e44df80e0f3a28d39fb1ab8e318e90046e3b5de70ad9e7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:49:42 GMT
ADD file:0d750ede80457d700cc7920bf7758097730f05dd745594645d18f752b03ee4ac in / 
# Wed, 13 May 2020 21:49:44 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:31:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:32:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:32:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:daa20d7c2fc68b19ac519617f67e18594a86dae573165b8260331168fd68440d`  
		Last Modified: Wed, 13 May 2020 21:59:00 GMT  
		Size: 48.1 MB (48105223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1ed27e51f518bb7f9d3d8f217e841fa0e04cec84e4be751525518dcc9a05bf`  
		Last Modified: Wed, 13 May 2020 22:55:11 GMT  
		Size: 7.4 MB (7359297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6799de4bbd5a170a48ae198dc7bf17edd128910c4afe2e792507f17519938`  
		Last Modified: Wed, 13 May 2020 22:55:12 GMT  
		Size: 9.7 MB (9687057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a20c21d3f5a3259a90a0f246387bf2d405adcdbc3d6d94b2d18c8a7cbaa1a21`  
		Last Modified: Wed, 13 May 2020 22:55:40 GMT  
		Size: 49.6 MB (49573343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:636730fb56b815c8401e9e2e241d2757b2ef63479435668789f771eee0cada1e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.7 MB (109661329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4564f11b3b69ad45e52ba0046f3842a74950997e72d406d944da0b5f09700c56`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:03:01 GMT
ADD file:67087d9a080132a9a5865637874fa3dab5059ac619630d071c563e75a7a5d977 in / 
# Thu, 23 Apr 2020 01:03:02 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:07:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:08:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cb6703531d2fa1d357cdd21991ae844400ecd207dba47fdd9afad54cdd9ce65a`  
		Last Modified: Thu, 23 Apr 2020 01:10:47 GMT  
		Size: 45.9 MB (45864280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdc86c4352df3ac4c13ca4ce79924328408ad32ad3ca32fc8b264e8f6988e7b`  
		Last Modified: Thu, 23 Apr 2020 04:29:47 GMT  
		Size: 7.1 MB (7096585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4dd8c9abb1148c2fa5d4b85b1125efedc4ade033de3fab02d2591844f8edf0`  
		Last Modified: Thu, 23 Apr 2020 04:29:48 GMT  
		Size: 9.3 MB (9343325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc2b159da9e1c38efe967b03bb5f74e84377be266117339a6b8f0494590a1f5`  
		Last Modified: Thu, 23 Apr 2020 04:30:14 GMT  
		Size: 47.4 MB (47357139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:eca24fdb8fc5b4815d1c91216ba0bd28d699a0dda71beed2bc36c7037e45a160
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118989634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79b5327f341d4604d263b57bc0e9823cd364614181adb3767fa66b9a4819a1d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:43:08 GMT
ADD file:685903e2621502d2f743969aaf293a5feab58680a95cd93a5ebf2b07f3b5d358 in / 
# Wed, 13 May 2020 21:43:10 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:24:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:24:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:24:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0be831822ade5f87765ba6ff26243b12a3ecd4c379df96483549a7992c1fd35b`  
		Last Modified: Wed, 13 May 2020 21:52:50 GMT  
		Size: 49.2 MB (49168115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2879905fcfbdfe9945e6eb39396c6b52b929faf145449ab656f7b35bb6387a`  
		Last Modified: Wed, 13 May 2020 22:39:40 GMT  
		Size: 7.7 MB (7681618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2769f7d2af01c05219ba1529b243249dcedccd56fabeee3d41d792b819f494`  
		Last Modified: Wed, 13 May 2020 22:39:39 GMT  
		Size: 10.0 MB (9983943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e8c22f4290c6000d75544c42d271474d93302f7cd74ef79832ba3c93c962a`  
		Last Modified: Wed, 13 May 2020 22:40:02 GMT  
		Size: 52.2 MB (52155958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ea7d97ae6ec77c31101b8a6aab2bdee7aef68f9f37fc5f664403dd20b1152fc6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122893279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d1b2e92dc6408b2f431063e1aecbd580cf94d3a2989412a1a9e5371b8458d4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:39:21 GMT
ADD file:10751e25934ebcf54b529ebd800a690886012d472846a404b452a1b27dc97eed in / 
# Thu, 23 Apr 2020 00:39:22 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:41:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:41:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:42:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5ca4f2c0deeb8dae824229454aa24e8d27bb031c4d3229fbc5465ac18d0fc46b`  
		Last Modified: Thu, 23 Apr 2020 00:44:20 GMT  
		Size: 51.1 MB (51147043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f881ee9d4d2861d84758ae7c12cdd5838df3cdc7b780bd444f77e6a14197c8`  
		Last Modified: Thu, 23 Apr 2020 02:00:10 GMT  
		Size: 8.0 MB (7981683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686b1690d58468427345d34e51ebc5ab5c2e615e596813bb02ac9bd8b6dba668`  
		Last Modified: Thu, 23 Apr 2020 02:00:11 GMT  
		Size: 10.3 MB (10338457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816415adf565f653dcab208b65d7f8c976b680c63f88265b394c5845bad3cad4`  
		Last Modified: Thu, 23 Apr 2020 02:00:32 GMT  
		Size: 53.4 MB (53426096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9f796674d151ce2d9fc1864170c1903db315bd9b213aa6c2f1dced01ab0f477e
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117103381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8417b67ab188035e5685ff597485d9c22bd7f45ea69ed7c391c91c5083609c99`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:09:25 GMT
ADD file:ef71e7285bfdea3942f5b4db577b5b14ba7dbc37538dfeda1886a6afcef86692 in / 
# Thu, 23 Apr 2020 00:09:26 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:51:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:51:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:52:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7754e26af5c07372dee067377cd032efd21a4266d2a432d0bfd78f25f8cb5e64`  
		Last Modified: Thu, 23 Apr 2020 00:17:03 GMT  
		Size: 49.0 MB (49019159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f28a98e4f99b5de98625c7c22aac4386fa49e62ae575a28c1eb055b99d09a5`  
		Last Modified: Thu, 23 Apr 2020 01:09:50 GMT  
		Size: 7.2 MB (7229680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87ca975a0efff511dda1467506a9c016219ebcb1621628925ad53008318f87d`  
		Last Modified: Thu, 23 Apr 2020 01:09:51 GMT  
		Size: 10.0 MB (10015780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a4bae253397bc57fad0e495b9bf420f3acda3cff409553300952578e291229`  
		Last Modified: Thu, 23 Apr 2020 01:10:46 GMT  
		Size: 50.8 MB (50838762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8682757e04b0617659cace85f5ea651651f2cceb7fcfecc9adfef72e1b0964d8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130579096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb936ff652869f9d1a56934ff1c48544b4c57098b671e2e9b2ec5b4dafd6e50`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:34:50 GMT
ADD file:31369dd617691a0d7181117a065290be8cd8c32814e443ef0a7c7adf7e9d800a in / 
# Thu, 23 Apr 2020 00:34:54 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:50:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:51:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6bf15800932473d1ca0a2cca9bfac073da118f1172b9027f7e78394850b02d05`  
		Last Modified: Thu, 23 Apr 2020 00:49:32 GMT  
		Size: 54.1 MB (54139621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b057e3462b9249cef48bcf195d058fc780ba16864e4a60f748aef5438a7570`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 8.3 MB (8252627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576b11ea0a4ca8856dec1ec3ce909c13942c2616bd753bc99ee754fa9837da2`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 10.7 MB (10727087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ce7710ab098018d07af906f197b0de4ecc8a4f1f6f411c31a2f1c00d83b191`  
		Last Modified: Thu, 23 Apr 2020 02:24:33 GMT  
		Size: 57.5 MB (57459761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5bd9a429cb8e2881a94e2290c9d11757b0944f517683ba452a21d5557f82a121
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117598928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c2d3bd8f83fe1d80a0113310d2ec51d741ba62f60cd399ef3ed4e304090756`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:42:20 GMT
ADD file:8f8ce7623c9f93bb85bf3b2bb1f2515de7b053e11c2efc56feb959322aefc0a0 in / 
# Wed, 13 May 2020 21:42:22 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:39:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:40:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6542b1e7bcc740fe79dab47cd5bcdb30fe618acd5d0d0e2583571b2ed256809c`  
		Last Modified: Wed, 13 May 2020 21:46:45 GMT  
		Size: 49.0 MB (48965117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfdd777c0ca04e5c74f52bdae1cc0e2a1ba232e895f109269bf84d8bb598a7a`  
		Last Modified: Wed, 13 May 2020 22:48:24 GMT  
		Size: 7.4 MB (7382349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be4faee9a8c310dbd16b8d77a0a4eee7f207a8cd04340c0852eb46655b9e7e`  
		Last Modified: Wed, 13 May 2020 22:48:29 GMT  
		Size: 9.9 MB (9882141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e46e850fe7f7138b3f6c7d0aa73ac1e5c4d1c8ee2d6272e32c6727088efcd9`  
		Last Modified: Wed, 13 May 2020 22:48:43 GMT  
		Size: 51.4 MB (51369321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
