## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:244aa0dbb6f9023459a0009be93d3a23d57f28f1e48573f091d04cbfb7b261ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; s390x

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cce513c1ad2a19b051d052e0860f76f867aac45cf84ef4a7608788481c279d9d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68823963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69cbc5575a3e9e3069d1498b95a52a83f47567a82bc563d325893b9c62126c4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:49:00 GMT
ADD file:565dc0a92c6ce86500c032d7c7e8112f62771ff3bac3aa84192e8309ae7acbba in / 
# Thu, 02 Dec 2021 02:49:03 GMT
CMD ["bash"]
# Fri, 10 Dec 2021 21:49:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Dec 2021 21:49:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:92dd04f71649984a91d8241840b2fa0a06cee72bebcd6503ece93ae1b5f47d07`  
		Last Modified: Thu, 02 Dec 2021 03:07:38 GMT  
		Size: 53.0 MB (53031153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034d98e044e9e53481f8d4d8abf3a1c951af6e2e0302f2d5c7b0bafe2d4ef536`  
		Last Modified: Fri, 10 Dec 2021 21:58:02 GMT  
		Size: 5.2 MB (5181891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07dfbba8655504d3ed9b02abdf2cb4d87d6795189ed0afd4f34e9f46363bebf`  
		Last Modified: Fri, 10 Dec 2021 21:58:04 GMT  
		Size: 10.6 MB (10610919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6153de1ec63e62cf418b13862bbc92515e271c492821f012023992e60f574924
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65962827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c750604612e6dc6eb5268a0ffb44f2cd5d2a3e01bd1b3704b6eb89a3ecdf4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:03:39 GMT
ADD file:bd5233b326b625660d820fa962832e6c5413ff9a56f64a6f072b9a9adfc545b2 in / 
# Thu, 02 Dec 2021 09:03:40 GMT
CMD ["bash"]
# Fri, 10 Dec 2021 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Dec 2021 21:58:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4dcb906f06af542b010e092a9a4d4ad8ccb110debf57beb0d4ded9baa51b82a1`  
		Last Modified: Thu, 02 Dec 2021 09:18:59 GMT  
		Size: 50.7 MB (50667986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6290470e339a2322159fc965896cd31eecd849410e2d52a8d8ecfd35f27f39`  
		Last Modified: Fri, 10 Dec 2021 22:10:56 GMT  
		Size: 5.0 MB (5041382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffd92cf9cc4dbaae187824ff4063b4fb6ee16274347a41c15b4c1609885dcfd`  
		Last Modified: Fri, 10 Dec 2021 22:10:58 GMT  
		Size: 10.3 MB (10253459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1ee765de5788629bb1e3bb68f52e749868bbde7b03252a60888ee26f90273167
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70528069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f492c7ab861855de5f24a68b7601afe53c16a1e37d56f34402093b605728db`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:07:31 GMT
ADD file:78d948a7fd7213b583a0b4e09434d4542df75c0620617b011ad06accb9b6f26f in / 
# Thu, 02 Dec 2021 08:07:32 GMT
CMD ["bash"]
# Fri, 10 Dec 2021 21:39:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Dec 2021 21:39:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f8d7e615d51e5d3f12aa3d99598a9f720f067abdee11ee16a770e8dcedce3069`  
		Last Modified: Thu, 02 Dec 2021 08:13:28 GMT  
		Size: 54.6 MB (54576381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4187246b128c7640be85fa42378deac3729f1c44f80d7e4650bc193d1ac0659`  
		Last Modified: Fri, 10 Dec 2021 21:45:38 GMT  
		Size: 5.3 MB (5271370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a5bf4c27b174518d1d82dc378754db6583bebd3213079698195a9aa09d93ef`  
		Last Modified: Fri, 10 Dec 2021 21:45:39 GMT  
		Size: 10.7 MB (10680318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:89fa661a5e08cfa13c06c5e51d11343e420410fb350bf2b776d52295cf1964db
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73310492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623ea579e88e2e7a633fdc4eaa14770db8d740a49081e350e7dc17acdc579eff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:07 GMT
ADD file:233579a3cce5db7166a5e91e9473aa28283fe69ec6809ce49c166994ffe2d461 in / 
# Thu, 02 Dec 2021 02:39:08 GMT
CMD ["bash"]
# Fri, 10 Dec 2021 21:38:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Dec 2021 21:38:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:66c36ad92a7d15b3332cd4cd2fd424021c2ce01463b45621fcab89004c4c763f`  
		Last Modified: Thu, 02 Dec 2021 02:46:31 GMT  
		Size: 56.6 MB (56610224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000b28bf4d3708c758d942cef89573516be5bfdb5fd88cec572bd0d4db3adda5`  
		Last Modified: Fri, 10 Dec 2021 21:43:12 GMT  
		Size: 5.4 MB (5414458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f3f2081584246e66256c4a57ec88dee6a4f9a1dcb016f94120cc8ad84b497a`  
		Last Modified: Fri, 10 Dec 2021 21:43:12 GMT  
		Size: 11.3 MB (11285810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2627cd9cb56bf2d909eb64d9ce8c5868c0e72f8116138d4621973e72879d142c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70416331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64327a029e3fdd09da3b6d3af5a084a7a12adfe32af016e90b31fd939214a194`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 03:07:51 GMT
ADD file:2b78b392bcc6daef3d9c93dcae4adf8b84cac89c57ed08bd43854d23774078d6 in / 
# Thu, 02 Dec 2021 03:07:52 GMT
CMD ["bash"]
# Fri, 10 Dec 2021 22:07:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Dec 2021 22:08:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8c4a35c3e932252ccb2418c1bc14531f11d21f13ba131d0a52cd9cb690dc9623`  
		Last Modified: Thu, 02 Dec 2021 03:15:53 GMT  
		Size: 54.3 MB (54269592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5382fc82d142248068645a004ecdcba9b86008e8e6d072fb2a8b85524a38c87c`  
		Last Modified: Fri, 10 Dec 2021 22:12:49 GMT  
		Size: 5.2 MB (5239618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715d5f987669cd4335e12d30a8b21fb2532368af6d0867a4749dc32ef5e0350f`  
		Last Modified: Fri, 10 Dec 2021 22:12:51 GMT  
		Size: 10.9 MB (10907121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:34c3e8ff0cea83ea8a9b6c6466eab196714b83a60433ee0ca326c838c523a3d8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69926718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f24ebdc7e63ee0b55868d64d1017400f3b1693ebeb3f64b0decbf74278cb03`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 07:18:15 GMT
ADD file:4a1285cad893d349a6acf3dd79546f01288abd1351b9b86f32011a9d1dfa80a7 in / 
# Thu, 02 Dec 2021 07:18:19 GMT
CMD ["bash"]
# Fri, 10 Dec 2021 21:41:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Dec 2021 21:41:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2ce0b9fc523de2185f9dbec93dc5492c43667e801a28c8f6f3d92d45e3017e7b`  
		Last Modified: Thu, 02 Dec 2021 07:24:22 GMT  
		Size: 53.9 MB (53866800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11b9482d6d3f7b986c9ccff3f956193f86e00de74eddb78445c1afc38a53a8b`  
		Last Modified: Fri, 10 Dec 2021 21:47:34 GMT  
		Size: 5.3 MB (5263148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55dda9a67d0ae9a3e70227b3cadbcfb35c5b3fc40c8c9bb1d7f02da972eceaa`  
		Last Modified: Fri, 10 Dec 2021 21:47:35 GMT  
		Size: 10.8 MB (10796770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
