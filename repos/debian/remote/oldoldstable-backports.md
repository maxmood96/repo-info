## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:7d82afd7c57b3b2fe61d474c0a9623698b188b7d6b2911961c2ee779c29f1324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:2b18bc51c1bbc8d20b5ea3115013ebc528a107de9fa1fb23b7e00703508a98ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50504215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7926d4d871b06861bd864b4540abb194b70ff6cedbdb10407f036c176028ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:45 GMT
ADD file:0a85b42ec334e9d09a9b936ef32ed24594b6d0d3ea7d0c95d7a988d9b867448f in / 
# Wed, 10 Apr 2024 01:51:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:51:50 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f8c5f46f1523ffce6f5c656232b130498b6678f135761f68e9a7b0e2464a74af`  
		Last Modified: Wed, 10 Apr 2024 01:57:12 GMT  
		Size: 50.5 MB (50503988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c139b4118ef44b71fc65b8496467ed5cf72c40bf2b89e32edd4c7d9a3878647`  
		Last Modified: Wed, 10 Apr 2024 01:57:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:35be321e7bd9c45d50c2ec453f87dd2c6585be9731e0ddbbe45c3c012a40318a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45962706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb60d15562407e74c9097a40608a830fa416bf87c6689cc6bdbff8b906c55fda`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:59:30 GMT
ADD file:af3a0030745f630af7131fc69ccc04f8dbe38f667a41e2a8f41a7d759e73e78f in / 
# Wed, 10 Apr 2024 00:59:31 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:59:35 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f5132684931229b8bc30578c195fe65dbac31349bb7d873ec829ad80f950e10e`  
		Last Modified: Wed, 10 Apr 2024 01:06:21 GMT  
		Size: 46.0 MB (45962477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ea6d56efdaeaadaf4cae2c0f9cf96ba16d9063bccb5eb472056ab56f0df2c4`  
		Last Modified: Wed, 10 Apr 2024 01:06:30 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:723008f17d0743ee189797906af22d38155e3a87bc5a51a8ded5e874da30b2c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49291055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4671f21f316f9894c9d72a05d083d25f0487163d4303b0ba8d60150a1e0934c2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:41:00 GMT
ADD file:ca2a3c2a7942307ae16165f590577dd52ea73bbaa9629dd7ad1668b924934031 in / 
# Wed, 10 Apr 2024 00:41:01 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:41:04 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8d4dda9f97051a7386322a2c064d4d75be8ad22fe38c06e0b5c5a41ea97b54d4`  
		Last Modified: Wed, 10 Apr 2024 00:45:46 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e7bd020e8db628028c5e36ff3a05bf7e8f82030658fa82f74e581380219a4a`  
		Last Modified: Wed, 10 Apr 2024 00:45:55 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:470efc55988ebd35ab171cae5b3345dfcbdda11d8973d5d19b743a7d24d6a237
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51256730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee1e11e1e2b4abc2ae367809f821ea118a82732013818228121085a34152b9c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:08 GMT
ADD file:c6b7d62606c7d1d21b3fc75ce8a8c25da6ef3db671e9938ab610d881eb77f512 in / 
# Wed, 10 Apr 2024 00:58:08 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:58:12 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:94697c259550bdadd226f6a3510b299aedfa79455587732aabafbe02a66b4d7a`  
		Last Modified: Wed, 10 Apr 2024 01:04:01 GMT  
		Size: 51.3 MB (51256503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acabb4a05d35b4b1c0f45db31f669f85bec7de9b5e89aab42658e99ce264931f`  
		Last Modified: Wed, 10 Apr 2024 01:04:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
