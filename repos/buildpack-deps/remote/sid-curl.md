## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:f231ff61c0b06167acd3423880f8b73d160d54983cb11ec7996a51efe443c4a2
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bb63de05706aa903c44a187423410064757ed4dd7b0fefe8ba2effc0d45f9434
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73319093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3647ed5810949bbe8d894a4b2290f0a8af05479d3712f47399cac937258acdf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:13 GMT
ADD file:ec9b256ad5af9d6c88b912d94fd4e58256e2b29a1c5ff616fe47488c72c1256c in / 
# Tue, 13 Aug 2024 00:21:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0ee0708ec9247cb19ad61d1bba3a89642d7eb4cfcd5031f23018c732b0ce201c`  
		Last Modified: Tue, 13 Aug 2024 00:25:12 GMT  
		Size: 52.8 MB (52836188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba418b28cb46180ce179bf48a7dfa7135087eefa79b479acfa16fedb4e4a1c2`  
		Last Modified: Tue, 13 Aug 2024 00:51:48 GMT  
		Size: 20.5 MB (20482905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f7b8be926f1bd951849a9c75815f36d1c7e532df7497cde939244a305ea7f090
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69311252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34583e63b9066ab656cf7f884c618cf83e0903e526aec63de39a9e145253044`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:10 GMT
ADD file:cf690ebeafabc8d93fcaa85c06bf4be7451eca6abfcd3d67e6a0b14ecae9eed6 in / 
# Tue, 13 Aug 2024 00:56:11 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bf57c73982c97d1f73ecf70b56ea68e85c073b81e6abeed2594a6b283cfa2910`  
		Last Modified: Tue, 13 Aug 2024 01:00:06 GMT  
		Size: 49.8 MB (49825762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff530185f1ceb17692b30c50fb36e4c0f4d38b0de29fcfddff312093b1ae816`  
		Last Modified: Tue, 13 Aug 2024 01:31:57 GMT  
		Size: 19.5 MB (19485490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c7dc4e6049764f081160698153ecfad9136256620b12394278be8aee0b660a8e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66155909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abb71d3adc483f422aad6581c1267129f92f7105d00902c11f14515fa4e4834`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:58:22 GMT
ADD file:e72a0297e96519fce159ae96a576801ad216aaabe4ba4c18342172c3277d4f63 in / 
# Tue, 13 Aug 2024 00:58:23 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:27:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5985c1abf8d738f84db0f982b117de5f003cae7137cf3fbeccf69d06419b0eb0`  
		Last Modified: Tue, 13 Aug 2024 01:02:30 GMT  
		Size: 47.3 MB (47328276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e5fa1410d891dd62139493e077da1c08e4361f989c17ff8f13e730fab01e12`  
		Last Modified: Tue, 13 Aug 2024 01:34:27 GMT  
		Size: 18.8 MB (18827633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e75ffb7a2e7f4ad78b5eaaf80f80ceee80cbd1c4b9a765b3eddd34c903a3b5f1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73845558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea665e856755fa51885b312d1ce870241400d83b9292e1f1436b26cd6b56621`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:29 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
# Wed, 04 Sep 2024 21:40:30 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b16294a36c4e8dd71bc29360d35bd73856218dada114029995773ff9ab59e9`  
		Last Modified: Wed, 04 Sep 2024 22:09:48 GMT  
		Size: 20.2 MB (20248325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cb5e40a7be972b1172bafa92ab71f6a08c143e06b0981336a4bc4d8af23400cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75244435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d80a37e21c9e25d3737094c1c4b40886ed52181492e44fdc9dfbddf970ee8f0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
# Tue, 13 Aug 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce604b6ec46af20835c8de06fb56b6d31f8dce22f35194ea4cab29c2aac8c355`  
		Last Modified: Tue, 13 Aug 2024 01:16:14 GMT  
		Size: 21.5 MB (21505961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:84b61ff5dbbeb62166e032082928afcd108dec8f874958c9c8dcf6799ca93767
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72530526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c4826139623ef2ef60d33d9f29bae5ba7e34385f1be56999cb44c59b995631`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:14:27 GMT
ADD file:c2b8305463bd9ec2de5e34b309a574fda4d3201acf2be1eeaf77b17be497d769 in / 
# Tue, 13 Aug 2024 00:14:35 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:96d1cb60a321cb9bcad04942005c2d893de36bfa358a946f876b980ee7696e7a`  
		Last Modified: Tue, 13 Aug 2024 00:25:52 GMT  
		Size: 51.7 MB (51720781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b7d979c2998ea5e70acbec3a94f9d7fa9dc5f798c6ed50c16c126082a82356`  
		Last Modified: Tue, 13 Aug 2024 01:37:39 GMT  
		Size: 20.8 MB (20809745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c4be7903db01dfd7116ff52391f931caac99a1be00c70abf81dd84b7d4272b4c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79873713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d224a800248ee906a9bc5cb5a7b1509c10a69fb16353a6773e668aba67d0956`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:23:11 GMT
ADD file:e6eea681cf56e20007639454c01cfebeefac45036637c0c5aa781f32e61086f3 in / 
# Tue, 13 Aug 2024 00:23:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f94a26791ad674a64a864ec5ea20fbd30c5f7f3fa34d6b6d03306d943685df53`  
		Last Modified: Tue, 13 Aug 2024 00:28:16 GMT  
		Size: 56.7 MB (56729826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca71ec9e44bb7c30c2064fe97015df0afbf2b63ff8f9d8c898855ea953932aa1`  
		Last Modified: Tue, 13 Aug 2024 01:37:08 GMT  
		Size: 23.1 MB (23143887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:98648aba4f123076952d703ecae9417a6a3a3a75fc01c6176ea66bd96224e729
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71119009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c0b075f1bb889473052aba7b3c18d5e0a28ae1a38b5b378d338f90fd329682`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:01 GMT
ADD file:97cc40f71485a0c47367bf7de8cb1715072dce719d216195de9b049516a29e45 in / 
# Tue, 13 Aug 2024 00:11:03 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:37:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e7e6753663bf71667278434bd9ec3bfbf244788b1855805c384ac83204bc13ef`  
		Last Modified: Tue, 13 Aug 2024 00:16:18 GMT  
		Size: 51.1 MB (51106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b04e5a15fbe73c8e7dfa541c5d04c781d3c5c4ac6a9ce7895b41cfeb8e40e71`  
		Last Modified: Tue, 13 Aug 2024 00:47:07 GMT  
		Size: 20.0 MB (20012849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f5d604130680eacd1da47d3bc2917df80e404d80e5f62bf34ea52ddaf846a16b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74043533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f39594b5c80df5065e24356bf1588fda37b42791ffcde078d45147ead22f0ed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:43:57 GMT
ADD file:b1f8fb7433720897f885f62e5bb1f6d60cfbf4392c753cd6772799dbe4712db3 in / 
# Tue, 13 Aug 2024 00:44:00 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99d54a6f148f09f9af6f5923c0f9be21666ce72118617d82a7147f9b44fb20bd`  
		Last Modified: Tue, 13 Aug 2024 00:48:34 GMT  
		Size: 52.5 MB (52451278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af2c8424c4be16350c34c6e764d7f747d730b61b1e8a159beefb887a4aec6f4`  
		Last Modified: Tue, 13 Aug 2024 01:26:16 GMT  
		Size: 21.6 MB (21592255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
