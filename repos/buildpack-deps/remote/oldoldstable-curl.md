## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:2bb04b0f4a39bf3f26a11c142fc55968c7a5bd203c477b8da5842e8e158a1151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b2de84a8c765d95c036c71d80f60a7433d79bf24da35356555332a505627dc96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68077565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f94d7322c96d0f9ff82883fe9d2dd53d5b16128ea4ad6229c6251297d63d71`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:19 GMT
ADD file:30ed10904e3533aa50c332544532891f0dcf06cce020988e07af9afa6b2f5df4 in / 
# Wed, 16 Aug 2023 01:00:20 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 07:00:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6b7393fb4f375905c31c483d81ce2a2905f88aba8cb198874da2b54035bc41d`  
		Last Modified: Wed, 16 Aug 2023 01:05:31 GMT  
		Size: 50.5 MB (50498099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df43ba252b5f813936a37cbf85494d91f16f450798f48e64a3cf44f647b128aa`  
		Last Modified: Wed, 16 Aug 2023 07:14:44 GMT  
		Size: 17.6 MB (17579466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1f82d9d6d25056fe6fc40e32cccd2fb79b2b19a55a3b30d694740a37e1204751
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62178146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc04b2bd46b3344ee4a82315b3fb423ee077d0af9ac5592445f96d517929eb2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:17:42 GMT
ADD file:9ad3ed36bade2e2cd71bd8f66dc47946e90d205f1846692ae9c240560758b4f4 in / 
# Wed, 16 Aug 2023 00:17:43 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 05:31:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ed63aeb0ff951576d398ae0e8de7a2dc582157c60523055321f47ef26ce88e00`  
		Last Modified: Wed, 16 Aug 2023 00:22:28 GMT  
		Size: 46.0 MB (45966229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee91fed073f248f84b680e14ae33a93203a05d62cf51fef886cd7ce0b3ac7d45`  
		Last Modified: Wed, 16 Aug 2023 05:49:50 GMT  
		Size: 16.2 MB (16211917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:693fba8369c38b01ea7646361a202296d268f8452d59f1622d04534bf8363085
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66741963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da913c23eb14e30f7e30aaada367ad899839db75c2d632e31b6c1d7ce8752659`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:18 GMT
ADD file:366546a703fa234d38591d2a54f10fbced83cc0e407775ad31751f0111c348c8 in / 
# Tue, 15 Aug 2023 23:40:18 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:24:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:745797452665e0b4d6f5d0f9b05ae67a86bccfea4ec3a2cf7c6dd89cbfafdd37`  
		Last Modified: Tue, 15 Aug 2023 23:44:16 GMT  
		Size: 49.3 MB (49290964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d4e21e88dbd3e72136906f1d37cb7c9b29c4a4c107fbe1c8b0385f5e663d2e`  
		Last Modified: Wed, 16 Aug 2023 01:40:15 GMT  
		Size: 17.5 MB (17450999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a2f6bc9bc0541882d918d0b6b577d0fc0176c4f25f15e3c1991d4650171fb292
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69351416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e1f222da00d74c27c7fc35eef2dacdd3f2a6c346602e90d5b74493308eb88e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:33 GMT
ADD file:f985eed393788dbeb3e4d9ab7f77d632d72f60bc5da30c59bb7de8fa3de0681c in / 
# Tue, 15 Aug 2023 23:39:33 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:29:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ce293edb9c35c6521b0a7d87a0d8e0252e4b0cab665a3103cb6d06e3e37cf414`  
		Last Modified: Tue, 15 Aug 2023 23:44:33 GMT  
		Size: 51.3 MB (51255460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d7c3776eae51e29722c4381d59391e00b49339c7298dcbef6adffe94829182`  
		Last Modified: Wed, 16 Aug 2023 00:37:17 GMT  
		Size: 18.1 MB (18095956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
