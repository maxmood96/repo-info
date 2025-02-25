## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:233003250b692176800f60561bc1e7435c816813ef5ce5111639c543e0922302
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9a79cb42e7462f840f2300444574993b3197f28a216fdaf11ba67b2ad49f70cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73660440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2a93c914f451d2865488e76c186f6f40220932d10725436a5dcbe3e1181db7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:950923b83892d84e409583fe8acab5a43a4ded92172eb9eeccc75b10012df546`  
		Last Modified: Tue, 25 Feb 2025 01:29:43 GMT  
		Size: 47.5 MB (47450585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8896ab25253a01ccf34a69a21881e74b41a25ff808e9b6217bda2404edb01961`  
		Last Modified: Tue, 25 Feb 2025 02:12:39 GMT  
		Size: 26.2 MB (26209855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:678f411f74ca2c7331df0f3edf5c70ce868b836557e303e874ba9f7dc69f7d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439c8139e1f055fdaa29a0d7ee14d150fe780106a0c1ece8f2c0ba9a4fbc1894`

```dockerfile
```

-	Layers:
	-	`sha256:e601932c9c54f53022d9a059a8ab3ce1df31ec9e61a781431b53c8e76fb09c6d`  
		Last Modified: Tue, 25 Feb 2025 02:12:39 GMT  
		Size: 4.0 MB (3962529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7d42870cdb0e17b452d32fb5960ad6cf775c58dc1da1b29c32c88554b91fd77`  
		Last Modified: Tue, 25 Feb 2025 02:12:39 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f45875ec73ce9b7c8aeb688b988e4dd79e4b6c842cd21b893b5f398a492c94ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71452663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b92a325e484088d0c8688eb6aea68ba80bc45eb8aafc520d1518ed29e7fe90`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:969faa28a060b3165779eb5369b5e31931290ad408fa4e8e60d177e2f80c2611`  
		Last Modified: Tue, 04 Feb 2025 01:38:51 GMT  
		Size: 46.7 MB (46706175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd2fe3d3c4202f31101bc1bc73cd3af8a62f52a1188e729c8a3228780cf83d0`  
		Last Modified: Tue, 04 Feb 2025 08:03:51 GMT  
		Size: 24.7 MB (24746488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8134fda17aa6d80f9759a5952f0ffeae4602704b27b326298b638578d10d443c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fbe16f31e28338f95f054b58a4401aa744e22829c9917e4841dedd2e5ab5a2`

```dockerfile
```

-	Layers:
	-	`sha256:c4e2ff509be119eb73702d3d519a72531f576a70f9908862c43a7786492a6d96`  
		Last Modified: Tue, 04 Feb 2025 08:03:50 GMT  
		Size: 4.0 MB (4044425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe41ba8a61745b055d7c1ff4fcead3d482410c8dc06a548e6382e5c4c140e1aa`  
		Last Modified: Tue, 04 Feb 2025 08:03:50 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:feb9c2d61fb4c4c7b0252883717ff509c78811124a512a8ce3ecb9807979175d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68731225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba6aec6b23b2b51d61ff1c09d4b883bd1ccf368730e25c946e90282a46f6033`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:eaba0613b673e68ada7f5f2b5e4971d3556823043148e63c2a6887ee2d5edef0`  
		Last Modified: Tue, 04 Feb 2025 01:39:12 GMT  
		Size: 44.8 MB (44838928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6395c61799d55a9640c01c9ef3b8549d20d61a975f9340e0353ec8e6422685f`  
		Last Modified: Tue, 04 Feb 2025 10:43:02 GMT  
		Size: 23.9 MB (23892297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd556847f4ae2a75b56788585a6dbed042bd64bebdf265e9ad9a60375b4529d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb443e4c1924cb01c661174585062ed0e2396c690d9a227622c118244322b84`

```dockerfile
```

-	Layers:
	-	`sha256:7a16946bcda3770000ccad1fec8abad756c10a59958b8efbc69b478d0a12a6a3`  
		Last Modified: Tue, 04 Feb 2025 10:43:01 GMT  
		Size: 4.0 MB (4037021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbd45c6d9e9057c1679f44da49613d30cf0a4b169f2b71b52dbe6b2392d94da8`  
		Last Modified: Tue, 04 Feb 2025 10:43:01 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3cf31dfb3b9a512d37f417618dc8d2c709472b36c3d7493768dcaa9a394e0b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74377354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13d99c12b3cd6acb985c585b0342c53dd123416f363f2d506091c48cb376ab`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f518c8f510cd10fda797c5ee77280d7c81b61ff1077c267de12ce9c337ddbe7b`  
		Last Modified: Tue, 04 Feb 2025 01:39:15 GMT  
		Size: 48.9 MB (48874714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b09bd24e474d679cb3c70ae42560294c37e17235d92a739791f20279494fa5e`  
		Last Modified: Tue, 04 Feb 2025 09:01:04 GMT  
		Size: 25.5 MB (25502640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b762f13089947f528337b22e97a2034d96f4970fb44b8514f374c981f492adb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4044577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2924e69ba8c13f46c71be66ca59a7404e757deedae5b1d977d6d35cfdfe739d0`

```dockerfile
```

-	Layers:
	-	`sha256:e50add4bfa70921343045e27ae494c4ba6b21657d3117a96e9e96c8f3143af4d`  
		Last Modified: Tue, 04 Feb 2025 09:01:04 GMT  
		Size: 4.0 MB (4037693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accd7297c44bb051bb6828c0c99e27d5fcba3fe49d95e31fdc9ff6b84e6b2fdf`  
		Last Modified: Tue, 04 Feb 2025 09:01:03 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5e2af4dda850796aa953d94bc9e79aecec70b9cd0c203b4ca10ad9400fdec7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2bdb615c37d5832d571b8ed1bc5ba785b83bb84baf4e7c4d43a4ccd073c4d0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aae1e98269b26509d10518853922a459fafd0d625e12a0e3bd33654e86d19bf9`  
		Last Modified: Tue, 25 Feb 2025 01:29:54 GMT  
		Size: 48.8 MB (48759296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75db5fe14e7f8d4a4352afc6fbce8a608d64e144a93abb709938695801d5f5c`  
		Last Modified: Tue, 25 Feb 2025 02:12:27 GMT  
		Size: 27.3 MB (27342554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cde158eaa281ba007667f5842729915148b1c7bea5282e51f07f6696d70bb6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8567f943c0f3211a5f29c890f45c15a3b1ab40dd22c37e42a71b2f3e29c1552`

```dockerfile
```

-	Layers:
	-	`sha256:5b89c87737da5ddff01fa9d940d1a2d43568db61ef2f2449a900abbbcbd7948d`  
		Last Modified: Tue, 25 Feb 2025 02:12:26 GMT  
		Size: 4.0 MB (3958296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a70ae078d0809f733c2f001529ed23fc056eed00709095ba774e3076981e0789`  
		Last Modified: Tue, 25 Feb 2025 02:12:26 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:aa05dc86622d5acdae657a6e8d533c854b47c91390e4a8fd9461b0f2395b4425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74749601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640bca2ee778df3ab3b2cb62893467ff967aea76ed7bebd6d55f83859c7988dd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ba41641f188bb1d74522008f197d258fe218bbf039fa1f236165286ebcda75a`  
		Last Modified: Tue, 04 Feb 2025 01:39:07 GMT  
		Size: 48.7 MB (48680970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1214950258d5885930b9bdcaedc26eedd6794e5ab349aac8800d95c05105fa89`  
		Last Modified: Tue, 04 Feb 2025 19:27:31 GMT  
		Size: 26.1 MB (26068631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f52175c9c93d64bc7cbee5a46e631add140778fdb42a7b920f358b8e12bb6cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:accf8d55da0e331b61a0d7a392e7eefbb99473ccb2a8fe278877de6a783e5614`

```dockerfile
```

-	Layers:
	-	`sha256:99420b32f3fd16ebd660e100b21537b3aead41e288962036279524044dd08e70`  
		Last Modified: Tue, 04 Feb 2025 19:27:28 GMT  
		Size: 6.6 KB (6637 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2494d35de6f345102df0d3b32b40579656ec8543bec87cba7626a46e3a8ba4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78856026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d85dfc3a4c305284c5eb80373f65cf6f9d6e2bca6b1613430d8c18bb005492d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9370c4ccc640520942cbaafa9d1bba72d3a14bc22c93d4c585e6cf8f83d65274`  
		Last Modified: Tue, 25 Feb 2025 01:31:22 GMT  
		Size: 51.1 MB (51109956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064a14d42f5e429844e608bdea207bfc8db8bb3a74d08ade67bcacfe19c5fbf8`  
		Last Modified: Tue, 25 Feb 2025 04:33:25 GMT  
		Size: 27.7 MB (27746070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9eefe030cf723f850da2d17aae2ba79568d509e2cbcb18316734270e41bcaafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3978006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c910b1dfb58d4078b1480c0add701fdc108396817fc8f8b1bdc89680c1cf0fb`

```dockerfile
```

-	Layers:
	-	`sha256:3b6ad4a085d9d2ae36f15020c9a65ecb3bf812f1c044a87db26b31f845dfbef5`  
		Last Modified: Tue, 25 Feb 2025 04:33:24 GMT  
		Size: 4.0 MB (3971170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73d7deed42ea49d91b713057b65727e3b1128135c70c4ce7c12804d4112f4c82`  
		Last Modified: Tue, 25 Feb 2025 04:33:23 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a378d1e1ed31ee4ea19d1a2804fb679f75438da10445d9561312ecc88e8ed682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71551308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de53561f8d97f44d27a70fa72691cb3d666541fd10a9f9c9498d6677dd73378e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5f390d4530b68a73e13f0b8647d2db7253fa60266e1fb90ae3f587c71a006f52`  
		Last Modified: Tue, 25 Feb 2025 01:32:10 GMT  
		Size: 46.0 MB (46003542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6542aac923569c10399fd56cc5e2363a56a89b5180e2dddd54f84754ded5a213`  
		Last Modified: Tue, 25 Feb 2025 02:36:30 GMT  
		Size: 25.5 MB (25547766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0ba113ffb4cc3b393fe8005b6ede56ccd9b7750c2594041fd82f2d8e4ecc8fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce97e70ab2b645fa35532ec6311472437b6a94af274efff4023ba2c25223c8b0`

```dockerfile
```

-	Layers:
	-	`sha256:46b4e489e1c9565c9b71198d22b237835f379c963170aca2442345dc4737aa81`  
		Last Modified: Tue, 25 Feb 2025 02:36:27 GMT  
		Size: 4.0 MB (3953903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c768f45f936f0675c3c094a04bccdebb92810e44c8ceef3372c12a79a9bf42`  
		Last Modified: Tue, 25 Feb 2025 02:36:26 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9bfc1f75b6c330678bfeecb972d23b039582cdcd8872fd0f8c2bfc48680361f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74867096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176e40243a2bf6075206546040ec9d22dcd849d956de2c08d25a50a2ce47a315`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bb029d344ac2942bf1f98be4221b2466495c100c4662a25e8e6338cf9c0f606e`  
		Last Modified: Tue, 25 Feb 2025 01:30:43 GMT  
		Size: 47.5 MB (47498543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a284e667f853bfd37a5b5f735f1448b941efd88d6ca35d51858f3d1bc02320`  
		Last Modified: Tue, 25 Feb 2025 04:05:10 GMT  
		Size: 27.4 MB (27368553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7448dcd052651cfa9c0809ed9e744bb96df3cec2c9bfe28ac18f44e5ba0f9a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3975668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b72911c36c80ad1e40b01df1d9e481d685ec6bbb7e1728ddcc85ea533122b3`

```dockerfile
```

-	Layers:
	-	`sha256:82509b881a94aa8026e1387b51f5c0fbc08a5b5105a2ca69c776d773af3f88c4`  
		Last Modified: Tue, 25 Feb 2025 04:05:10 GMT  
		Size: 4.0 MB (3968864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3c5837435ad28f62ba69eac3b7418557085610c87bc41e31ce86d9e22a638a9`  
		Last Modified: Tue, 25 Feb 2025 04:05:10 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json
