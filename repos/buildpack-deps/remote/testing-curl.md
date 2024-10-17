## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:c10fa60b440190903e6ae63a49b6319ab6d9f82a0f4f7b26f7b8605b681a0b43
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:329fc0881ca3ce9edb25230bbfe199cc68c98c5ed74cc0e4ab082559a3a7540e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73884877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6169a54b9e4c1e1771ca845cd6d60b8c02eadaa57f758aa051ebaf02a06c94a2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:22:22 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Thu, 17 Oct 2024 00:22:23 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3af942d5f32a53d271e49824c635bd83b9f44545e34efa1a534acbcd19cf8c`  
		Last Modified: Thu, 17 Oct 2024 01:12:47 GMT  
		Size: 20.6 MB (20646136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:511848f89ac6a9a59f3a996fa2313c2388ad6d9586959bfe53c4efb8360c0b0d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69412995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ebd13eb50f8d1965d055ddc0a5075c31cd7dd24537c24838d2f298c9407d8f0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:20:21 GMT
ADD file:3b9d682e7d68f9176882ad1aa7f4dcae0a81c3f93bb197b8d0a3982c411d2ae0 in / 
# Fri, 27 Sep 2024 03:20:22 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:01:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:655ea019a1ac93e4a06df6c69d688fcb77e3e8581a9c73eaec0ab2559d7233f0`  
		Last Modified: Fri, 27 Sep 2024 03:23:36 GMT  
		Size: 50.1 MB (50140675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5a645996979bd86734316a948faaa2699705e7844398497f9933957b686774`  
		Last Modified: Fri, 27 Sep 2024 04:05:36 GMT  
		Size: 19.3 MB (19272320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:98d0d2d989c716ceacab3193640a9356b37fa827f72314d00a0270c8006197f6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66262823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7602a452f4245dfc17d03f43f1bc3130eebba36523027d5e4c9116d704a13c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:15:43 GMT
ADD file:13242b1f67d07c997aa23e4b688f29c3a6c6dd2678f15f8738e88d4e66cd5ad8 in / 
# Fri, 27 Sep 2024 05:15:45 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:35:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2e00dc0285e0f577d99c5fb34081dcf709cc26a9e85129b9e7bf7486f41e9f93`  
		Last Modified: Fri, 27 Sep 2024 05:20:03 GMT  
		Size: 47.6 MB (47633953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39e04951abf97af56dedf87c98cd7cc72052708138c6c90da2eaa7628520ed6`  
		Last Modified: Fri, 27 Sep 2024 07:42:12 GMT  
		Size: 18.6 MB (18628870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9aef11957c014ee01c467128ef31a08b32c6953f31ab48378266d1d08cfb0599
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73655342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830955de46667fa98d512e386318f49ac6b2fe117dbdd5900d9bcc4c8945eefd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:36 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 27 Sep 2024 04:39:37 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56925e2753eebe331e1e7850cdb33fa7fabb783a0365763734fb7f7fa68594e0`  
		Last Modified: Fri, 27 Sep 2024 05:27:28 GMT  
		Size: 20.0 MB (20038741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9a0b61de3c77cbd4f3951d1b86e89f18cebda6691e831e4aa5fbdccfebade913
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75834438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344e608e55235f5addc0ddae1867daa1d6cd1b8fb3ce562a6c212b6ba100a304`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:40:55 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Thu, 17 Oct 2024 00:40:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8bca6b1029fb346ac8c3fd8fd0242c8617b39ff467401ae5be38d72823e794`  
		Last Modified: Thu, 17 Oct 2024 01:13:34 GMT  
		Size: 21.8 MB (21756980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b0efa492445a57ae8f018beda4851659a8e6053a22551603bc71c032105227f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72707610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a371a0285e3282b682d0fbe1dd7641d3091c0f79793691f7a9a26b96272421dd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:07:36 GMT
ADD file:36ad397edf2d75e04dad5f0c65abe533f9f2e989bf5ea18e70a4df00cc6e490b in / 
# Fri, 27 Sep 2024 09:07:41 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:53:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b62fd707f1ed2218f3c1012d35ec60cef1c2b262cc2ca3f48b17a6725ccdf4b3`  
		Last Modified: Fri, 27 Sep 2024 09:15:53 GMT  
		Size: 52.1 MB (52096393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033fb77739bc0534e9ca7a6324d61a359557ff7525765c989f7fe43292a70678`  
		Last Modified: Fri, 27 Sep 2024 11:08:13 GMT  
		Size: 20.6 MB (20611217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:67b5d9ed541257d6e7b0df6d704b584840267e267ce4aca7916a91445998a679
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80041558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9902d8e9389a2a68eb6148b4670a752f6b44e04ea16d3fda06e7857e2a42494`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:34:36 GMT
ADD file:330305dfad891b7801b7bc1444b22086f483c0101ecad9aa8a8e0d005896f0fd in / 
# Fri, 27 Sep 2024 05:34:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 06:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1c9d9c0ae5911d02f7f099685f31c9a3bdecfb20000d904113c26e622dbe3be3`  
		Last Modified: Fri, 27 Sep 2024 05:38:22 GMT  
		Size: 57.1 MB (57100357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02cae32b1fb8881345e1371c36b7be22b1f7ed12f1c0b8c022946020ef2ea67`  
		Last Modified: Fri, 27 Sep 2024 06:06:52 GMT  
		Size: 22.9 MB (22941201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4e5a879b654c7c746335d5c86a83cb9cf26be40ec7ff2bc53b6e28d0ad3f6463
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71302497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7431eff14b4cf260214e2c7494998e25d9583b82cbc1558c76e490b08c437b30`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 12:27:18 GMT
ADD file:da1da406a30d8c871e2184104ce67d821e790fe334361223691352f3f2de2066 in / 
# Fri, 27 Sep 2024 12:27:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 13:58:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0a4dce9b327b8993d0aa8d580f47160e8320c3015f48472eedbf0d06fbb649df`  
		Last Modified: Fri, 27 Sep 2024 12:33:20 GMT  
		Size: 51.5 MB (51492798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5dbfe1ea856752f068e2a64375dcf7a47fa54aacb79b8eb7df476c2bc442322`  
		Last Modified: Fri, 27 Sep 2024 14:07:27 GMT  
		Size: 19.8 MB (19809699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7a815adf7f34038e8af8937945bc9715fd6dd87d23264894e5b58ec62369aef2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74165458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab392593f47f6c95908f64b1886eabaf06a961df79034a9462742eeb8dfbaca8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:45:24 GMT
ADD file:62bc4f2057452df8dde276d456f3954e7e27a723040dd9314069695b18b4c75a in / 
# Fri, 27 Sep 2024 02:45:26 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d4e554dd357d755b1103e6fac1ca2fe641d4ec4ce0581cc222f4bffe8b54c0c`  
		Last Modified: Fri, 27 Sep 2024 02:48:50 GMT  
		Size: 52.8 MB (52771035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f683d43e465332ea4b3a44a602cd96364371abbd8a8e9766b4a056ad242572`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 21.4 MB (21394423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
