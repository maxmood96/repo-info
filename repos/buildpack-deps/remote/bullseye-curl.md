## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:49f701fe266ce2a7425fa78cd88adaf1a32e472b72411ae8c2368c82ae207243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2df346f6bf0a09c1b581bfa52800a87da97dc79a4c075abe911cfa512ddaafc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70666703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8aa56ed68dba89d198819c24d6f7406f16d7068d0490cc5648d04cb04f7722`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4ea105f4c54a69fdf29a66bcead17f11b33895523ec9eb4786da771c122e0936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f358d4fcc3f6327c0916ed130bd1c75b5731f999b5556491b61eab4f9885f33c`

```dockerfile
```

-	Layers:
	-	`sha256:41bc55e2a522382fd133dfd3161739a2e1becdf81df08d432ceece6009104b53`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 4.5 MB (4492180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:563ae519ad78eb8647e2644e539048e36d372cf39041bf4f75247792a023461b`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 6.8 KB (6801 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ce982925f7cb662229a416b8ad803c7a5ed65c69917a6fe3e519ac657ba2ee15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65119280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcde28c3186dce242f6150e5ebe0bb3c3a8f9fe6a7287a3cf88c06f85631668`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9811aa580423a2e552be714c14e210eacb5d77955466d3ca3381faccb47f5832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4500434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75437541a1b4d8578a4168a6c973fc1938cef6004aed71846971abe640ce1adb`

```dockerfile
```

-	Layers:
	-	`sha256:ee4e340b3a5aa96d9edd30cd59e56c6a84097292c754303d197005b000003d1e`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 4.5 MB (4493778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc400e038d817658fe4f5c569d165dfce2496c578f62facd784e7288a97c447b`  
		Last Modified: Sat, 19 Oct 2024 00:56:45 GMT  
		Size: 6.7 KB (6656 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b3ca5e481e6e265be7ff4f1f665bc4702a4e7fd5c3592baa01884a67936d99b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69300660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e48eea012caf1b9fdcee3a320590d0f965b183ccbd3e2ac9027d6a49ab8425e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9e545ff305fe56558a94b064a901c16b373a3501daf5519f82ec19db6a3655`  
		Last Modified: Tue, 12 Nov 2024 11:16:34 GMT  
		Size: 15.5 MB (15543588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e95d2cbb57128b37e3aeb93434885a8fd4f24488e58be893a7fc19edced4c584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5dd407061bac2bbf6554ae718d25b67268b9b4f1229edd0431ca2b3e092472`

```dockerfile
```

-	Layers:
	-	`sha256:3d5cdaf50f3868d2492b29e300367b85b38f1460b7b8f6e9c9a20540301e0778`  
		Last Modified: Tue, 12 Nov 2024 11:16:33 GMT  
		Size: 4.5 MB (4491792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:914df286e10eadb4badd71b8c9c813a4d97e87d5866664eec95ab4e0f7030517`  
		Last Modified: Tue, 12 Nov 2024 11:16:33 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:28db40634d8196c741694964927ffbcce7a32e46ce629d076ac4180059acc1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72155351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4af437b3c1ada7e3c006fa019ec1cb83212d5e1723583a7a203963cd7812b6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7489e598cae5c0812e1ddaf1d0b649b6033369bedffceac2506c8d523d0a1c5d`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 16.1 MB (16061669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:adaffba9878783500c58c160462f440fa73a4d51cc25f766be5463aa7ac39bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779e7f15590d0bf3c8710f0aac9cc10c85719c2601c08b05b9695f106959c996`

```dockerfile
```

-	Layers:
	-	`sha256:0654c325eacf20f2fa53094181831e09fd652d1356c43ddcab4d5bd8bcd3fefa`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 4.5 MB (4488619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4019c97fc7b3b49f34fc5ee695b048f164cef6227b6864fdb3a3d5d99adaf8c`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 6.8 KB (6779 bytes)  
		MIME: application/vnd.in-toto+json
