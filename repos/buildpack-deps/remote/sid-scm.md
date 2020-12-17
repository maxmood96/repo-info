## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:6945b39c8657e109ee65a4f248dc7a046d83c156e474aadf2cbcc4840af24690
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

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0fbe6079a41a1a669ca1b9c081932ae2f9bd5e77f9069f682a24de8867d326ae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128116881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fce4d1158c2ea89a5cd6aec41fcfd440895acb0dce75f4a9e193f4460dbe96f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:07:48 GMT
ADD file:51a85ad79ebd7e288cd0ea14cd2ae41990aab2d77352f801f09c3a4682cb83a9 in / 
# Fri, 11 Dec 2020 02:07:48 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 16:59:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 16:59:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 17:00:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ff8cddfd21234a3c42ee0af471b251a807aa29af4ca00392976a17d3257ed269`  
		Last Modified: Fri, 11 Dec 2020 02:14:23 GMT  
		Size: 53.4 MB (53352668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58120f59d80232cb93b7fff568312888d13cf4167158305ffe8adc4483af30e5`  
		Last Modified: Thu, 17 Dec 2020 17:27:16 GMT  
		Size: 7.9 MB (7909957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37776afef7b17d4680060a625bb43a68146d6e6d5ab006be07856897c2aed6dd`  
		Last Modified: Thu, 17 Dec 2020 17:27:16 GMT  
		Size: 10.6 MB (10648135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43542ad23e1682377f889e0fd8dd5dd662b4d9f1b8e85bf63145a64dcaed34a1`  
		Last Modified: Thu, 17 Dec 2020 17:27:37 GMT  
		Size: 56.2 MB (56206121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f3a372c67ce22d463e33931c9e56a7ae023b090c220ee82cc47f48860ae5c79d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122941544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:113aeff9d74d55177bd21cab8a2574298ffd5ed47a89f95bc47d0a63c77e6ca6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:07:43 GMT
ADD file:a57353f597051225232a9e7abed847b86e4c6dddd2072732b4625acbac7128fd in / 
# Fri, 11 Dec 2020 02:07:47 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 01:58:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 01:58:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 02:00:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:af6b8b544b162386c7b3c6d5c131158e341ff3b454198faf077cc6c1427321df`  
		Last Modified: Fri, 11 Dec 2020 02:17:13 GMT  
		Size: 51.3 MB (51288429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af32247566aa2494e1bf6e9f3c3f6665570e5b6ca9c0efc4201c1ffe6fb588f9`  
		Last Modified: Thu, 17 Dec 2020 02:16:24 GMT  
		Size: 7.5 MB (7464549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79eb6eeea7eb9883a84eadf7c898a88cc2a4964df470eae23c4ff5d9d3a43b01`  
		Last Modified: Thu, 17 Dec 2020 02:16:24 GMT  
		Size: 10.3 MB (10335113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f6c898d79741c0a4f968f3105ec2550e291341c33ffaaeda29f2e0c23a1793`  
		Last Modified: Thu, 17 Dec 2020 02:17:04 GMT  
		Size: 53.9 MB (53853453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7188e7c4f53a1b439fe8ce0dd29d7b5050ed8ef72f824423df543fa044db4ec2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117914025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057d7503c319165927594c790ce0c0898c4e0d87e289eac4998ad5f86b27892e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:26:33 GMT
ADD file:fa1941c40adf31f1de7cad83033e24d208bc560e0818d6c0977fe2e74ef87e0d in / 
# Fri, 11 Dec 2020 02:26:39 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:20:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:20:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 08:21:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:54bf394474a2aad8c49632d0f0974854752ca4ff40354a996cb0806ea65d7253`  
		Last Modified: Fri, 11 Dec 2020 02:35:33 GMT  
		Size: 49.0 MB (48987318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138f735b8d86c59a8efe8701930d51f00aab24ac3ec03c9701b22176d372ffc5`  
		Last Modified: Thu, 17 Dec 2020 08:53:55 GMT  
		Size: 7.2 MB (7203215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da4363bd6c95216be34a5d4d34419bc9306f517103d0013669f9fa1bcfd225a`  
		Last Modified: Thu, 17 Dec 2020 08:53:55 GMT  
		Size: 10.0 MB (9974250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca4553babd367bf8d6b7757a8b6a2c6dd3e97a75a65c48ef81cd51dcf85e9c9`  
		Last Modified: Thu, 17 Dec 2020 08:54:19 GMT  
		Size: 51.7 MB (51749242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8cae49c5b8cfa8a3ff28f66cc015b406ab642db3b68180166accfeee3c8f7066
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126912796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cade1d12702dd89fe71710820395ca358e4bcdca2ab9816fd908e8d393e5d783`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:46:54 GMT
ADD file:f2ae922bdd400314a7bdccb54b19fed4d2441eabfa76c14f4656754f4639c9f2 in / 
# Fri, 11 Dec 2020 02:46:58 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 10:09:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:09:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 10:10:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56da081f64fe82857d727ffa4501fbe0725d416c8b8062202081a62f97fd37f6`  
		Last Modified: Fri, 11 Dec 2020 02:54:16 GMT  
		Size: 52.2 MB (52214368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c005981f7ee140e28c3d2e8afd11ba4168bd84130ed5887eb9c2bf7799c9d7`  
		Last Modified: Thu, 17 Dec 2020 10:39:38 GMT  
		Size: 7.8 MB (7771435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0395265f0c70c22b0a204b62d47d48c5edb8cce1630c9a39e29b983acf94fad0`  
		Last Modified: Thu, 17 Dec 2020 10:39:38 GMT  
		Size: 10.7 MB (10653926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e05607ee0271eec72950d14a651abb4a701aa2136eb0ec0fad349a547e3f6a`  
		Last Modified: Thu, 17 Dec 2020 10:40:01 GMT  
		Size: 56.3 MB (56273067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4196455136664ad3ee180d8cb2166b2407d5514ffc67067eca8234c95c15b9ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131156653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f595e8161b5c912d2c9e4fb1b8e65cef2f077514057c4e656c2297d4fb2762ef`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:43 GMT
ADD file:ac372b15438c9387718286ebd1a5b9512e674cdc90319668b3612fcb0cd99441 in / 
# Fri, 11 Dec 2020 02:04:43 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:10:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:10:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 08:11:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbad886384348be399f916b804d2efe113827e77f3c2b05f9b19a4dd67bff32e`  
		Last Modified: Fri, 11 Dec 2020 02:11:56 GMT  
		Size: 54.4 MB (54407631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107edbf54231bab6e619380b341236d89d7c373021e0ca4ced89d4b094f74537`  
		Last Modified: Thu, 17 Dec 2020 08:27:04 GMT  
		Size: 8.1 MB (8083852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770453472dffc640059e49933b5042237ef0d2a63e4ecbc572da6109134c440b`  
		Last Modified: Thu, 17 Dec 2020 08:27:04 GMT  
		Size: 11.0 MB (11031266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6aff5ce2d179cce5128375be4a9798643c0eece646c52f9f561fc0a83103843`  
		Last Modified: Thu, 17 Dec 2020 08:27:29 GMT  
		Size: 57.6 MB (57633904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:55a14432e47a6c3edeb7aa8074e823515d3f82fd446d6efcc8f5ce22528b86a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125064977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c955ebc3dc50237edbe6ec23577eabb2ffd048536cbf6540ec67d7f74c995b0d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:03:55 GMT
ADD file:144f263fbf8197586830814ff675d3c7d3ac8e3df7debe6633a1e91f84ff845b in / 
# Fri, 11 Dec 2020 02:03:56 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 02:16:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 02:17:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 02:18:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b60fb1f705939e8d3e124cd99cb825ac48613619a7a75de5656f0bde8bb1f05`  
		Last Modified: Fri, 11 Dec 2020 02:11:04 GMT  
		Size: 52.1 MB (52069726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b68d01e1e193d2323fdb149c22c9d1eabf16cc4c4941778e09e00b76b2f652`  
		Last Modified: Thu, 17 Dec 2020 02:27:52 GMT  
		Size: 7.4 MB (7430962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0d13fc3849ec4bd1574242ac59b139c9b0b7dbd2d0afa316911acb27045559`  
		Last Modified: Thu, 17 Dec 2020 02:27:52 GMT  
		Size: 10.7 MB (10656643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc9f97b68d53e1079a6372e2db34d03bbde1f3d3ecf4df179d09936896b9658`  
		Last Modified: Thu, 17 Dec 2020 02:28:48 GMT  
		Size: 54.9 MB (54907646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7865936d39d79df9f75f21a98fbfc049f54f052224b1d7baa0a9b1dd720f0af2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137732177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a95c83cb950911e87fa624f554c3e677b7038d880f833cff69ddd1e0b74a40`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:34 GMT
ADD file:d6769e024c4c1bf3ac50de798e3b70ddbae5e8dc6c4edc64cbf31ef39fba2896 in / 
# Fri, 11 Dec 2020 03:34:40 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 11:52:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 11:53:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 11:57:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:897184b44dea4f1c1b646278a369b1024dac0562097178b81b92da84665fd760`  
		Last Modified: Fri, 11 Dec 2020 03:42:05 GMT  
		Size: 57.3 MB (57314487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bf9998295a2348e5ea5ebbb24a1bb17e57e20b1c41f8d55a26942cbf9ecd66`  
		Last Modified: Thu, 17 Dec 2020 13:42:13 GMT  
		Size: 8.4 MB (8363493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f68f738f0b4ea98f73eedce2726aaa0b017e60b3ee74625615e9fe42eb3d6b`  
		Last Modified: Thu, 17 Dec 2020 13:42:18 GMT  
		Size: 11.4 MB (11421158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a257d57292a484299d176728b9425b924212f272740dac171d871150b47e6abc`  
		Last Modified: Thu, 17 Dec 2020 13:43:37 GMT  
		Size: 60.6 MB (60633039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ffe8e69f81a5b578a3661639201236bd3f512342e7c5633eb9ffdd10b4842566
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125695897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5baf16f0890c303960ee06a49cda09f1397be731f7286b12c75e6038b5c1ae29`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:12:29 GMT
ADD file:81f25bd988cd2db6809416e7139b279a1a04ce8e2b864c71e35768d7211232db in / 
# Fri, 11 Dec 2020 02:12:36 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 11:18:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 11:18:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 11:19:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d882124dbf8a54501109f018ee08c93cb805beed092d3bf2e6979740fad5f861`  
		Last Modified: Fri, 11 Dec 2020 02:17:27 GMT  
		Size: 51.9 MB (51894888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d19883059c6574b24a1136327bfb2a42e1709d68c54db24a7b443ea27ba6fb`  
		Last Modified: Thu, 17 Dec 2020 11:47:32 GMT  
		Size: 7.6 MB (7585305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3620af9fd07136686b0a9a787703282d968f4e2b3e04654c62094c925d7eefd`  
		Last Modified: Thu, 17 Dec 2020 11:47:31 GMT  
		Size: 10.5 MB (10525413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5636f80b0edab0a99700edbedaee1ac005f359c022f913368483c3495326e1fe`  
		Last Modified: Thu, 17 Dec 2020 11:47:49 GMT  
		Size: 55.7 MB (55690291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
