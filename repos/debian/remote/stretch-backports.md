## `debian:stretch-backports`

```console
$ docker pull debian@sha256:0ec5caa95010c116ec140a724a97e28c51b925cbd8424810bd2aabc7cc8327f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:24013bac930a097dd445cbf025c582bce454a6f3051d24e377bff9c027e4f42e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45366929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032c916d0a8ddb4614c29288e37a4a936ce2de4ef6d504d5aa606502146b495f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:32 GMT
ADD file:a28d8a949b7577768d87fcbac346797fc5f7bad0539625339edcd09a32d6bf77 in / 
# Tue, 04 Aug 2020 15:45:33 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 15:45:37 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:419e7ae5bb1e4875c367f3249b7bb7f8f39dd27dfceb4ee9d6a92191ed1c452f`  
		Last Modified: Tue, 04 Aug 2020 15:52:05 GMT  
		Size: 45.4 MB (45366706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3395d080f57af265f40899e7c6f37f605ab630646ec40363687b5e1beaefca`  
		Last Modified: Tue, 04 Aug 2020 15:52:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:e3decd61012b7c7e4f9158ef96cff7a029f09b2472c392794ceed93d6a91c0b0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44081446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfa578e927bc15ed6fadd3e88711103ae438cb9cef42b1e27de4f13ea0efaf7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:23:56 GMT
ADD file:c82979276574ae052b356c92955110dfb283d33659ea097871176d1a62ed98ff in / 
# Tue, 04 Aug 2020 03:24:04 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 03:24:45 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8653f8cd9e4c7c5ecd1cd925507522d43ec49dea7127050e56d71d3447f39292`  
		Last Modified: Tue, 04 Aug 2020 03:38:23 GMT  
		Size: 44.1 MB (44081220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2689e285e5451089092bd3fa4d0e551872d5e73e944ee6bd67d3517727611fff`  
		Last Modified: Tue, 04 Aug 2020 03:38:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:862bd09b3d2ab23b347463a174e5be437a7614b6f77d8d40e7591998196b6de0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42111607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92cf524d667492d23aa8823a53b921dd1fb1a215e87fa8e2ffaf4830959517f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 05:01:16 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6f1c8ddbe824bb2a9ce7f0ad328d89038d5b288e289e94de3137f65e458387`  
		Last Modified: Tue, 04 Aug 2020 05:08:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a8243c5b194f805d9b118fe0d4367f9b095d86cd02b7b35151fbbeac26c2c241
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43171867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabbb2080398709e33a8ac1a09ab3f4a8401aa7e15695e69c48fabd9a40497a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 06:59:49 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325326ad0ce765e99f4cf8b42f769fb765113c1c54ed5c154be154c205af8f9b`  
		Last Modified: Tue, 04 Aug 2020 07:06:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:cdc642b99bbc33cb48875fedc3f468d9aca417356721bcc8c508911e72e4af8e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46087001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b446a1d9ca14dd448941b68bc2ebff0a75dafc2bea9a647e8d59c0d33747c50b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:39:59 GMT
ADD file:af30f23f89d9bbdd6ad60199f3d978a5e426835c6138e0c76a3453680945a121 in / 
# Tue, 04 Aug 2020 03:39:59 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 03:40:04 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:36eaaca1a8d1677d2d2aa93f595d838e71ccbe4254f548ff566f97e8d555df1c`  
		Last Modified: Tue, 04 Aug 2020 03:45:28 GMT  
		Size: 46.1 MB (46086777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4d2c2badd53cd2fe3de49bcd7e2c043577b8b1da44ed66eab8b6439e70ae29`  
		Last Modified: Tue, 04 Aug 2020 03:45:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
