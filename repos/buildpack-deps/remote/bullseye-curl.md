## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:6f7e55c79f48e8c837557cccbf25e66f249d7cdff972b959544b383430d351a7
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
$ docker pull buildpack-deps@sha256:8ab97857735b9bb4ca0316c84af8cb47f468d79fbf7d69a7602a4a057be20d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69482684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b5ace0446f1a3d88fd6d7eb94cc84129b0dc299b80045b5e26f87a3ce7b20b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c985a2a0b84bb74f11845a54a2cf9b51f2f79c056c15b4bd2e136676c9383502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa0c728f5437aa596659b21909e26c3dc3ad3d1d64adb107edcf6d718397fc8`

```dockerfile
```

-	Layers:
	-	`sha256:6cfb03deb7abd3faa75a7f964fa9369e9644a2b85204515db2a447c862c83f36`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 4.5 MB (4491756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:488572740765c205abccf12b5ac1f0f9f380f18333e681fb042fc29b61ce5b9a`  
		Last Modified: Sat, 19 Oct 2024 01:11:08 GMT  
		Size: 6.7 KB (6676 bytes)  
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
