## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:658cf180ab30324e599219a118884b114a0e22ca27c0a9ffbf9b596eaf84f8fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:17a261a61287529e5ed1936477a24c98c41119d5b65ca5c10a0689175da99677
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115274891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69d61fe47c32123a4844169e449808441f139cf10af1e504267931c4a7d60c6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:45 GMT
ADD file:545fa4a7e3efbc02fd93b103a922af1496dafa1358953302d1e9112772a46c6d in / 
# Thu, 23 Apr 2020 00:20:45 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:53:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:53:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:55:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f4cbd35197708a9e2a08a980f6184996202108f81f5a0a2639bba1f4e070c56b`  
		Last Modified: Thu, 23 Apr 2020 00:25:23 GMT  
		Size: 54.4 MB (54390774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cc73abfb4303b455fc8d3efa21117aeacb8235e3eb27426aca3f86f2d09e6a`  
		Last Modified: Thu, 23 Apr 2020 01:03:49 GMT  
		Size: 17.5 MB (17545895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e28fdf8450ab7cca43fd94de3108f4c22436aca0ae9c3097446d26e5a88cd2`  
		Last Modified: Thu, 23 Apr 2020 01:04:01 GMT  
		Size: 43.3 MB (43338222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:631fa67727fa18f80b5a67f3150bb837b28f0ff7ecee2885073023494833ee47
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110778828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05e942f772a4e1bf5cee9ff5f83fc3d16277ea4b71a7c013268cb55bc3102c6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:50:35 GMT
ADD file:3089394d65cfc4adc7aeb2f3e7b24f63a90aef0c8f2b95a327c448e34d5ceb28 in / 
# Thu, 16 Apr 2020 00:50:38 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 07:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 07:46:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 07:48:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f4cc8a14da483bbaa3a6110327b3809d7bc68157e01be1dcb9380511b8352c52`  
		Last Modified: Thu, 16 Apr 2020 00:58:49 GMT  
		Size: 52.6 MB (52581355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7427d5beb5e7d08f1850b5004caeb34f468469efaaaedefb9fd9be1a413b3c`  
		Last Modified: Thu, 16 Apr 2020 08:07:12 GMT  
		Size: 17.0 MB (17037220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17309d642170d28b544bfb6ed4174d1daf23a05d5de0f5614b4e9f38120ad42`  
		Last Modified: Thu, 16 Apr 2020 08:07:33 GMT  
		Size: 41.2 MB (41160253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:17718cb62a06b3a8f013c386540dea1a4d55e356ec4149367435890bba15476e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106805072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f62c28dae6bca9ce485c37d627d56ba163f19718af5d8cd9ef14fc3e9d7d375`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:00:13 GMT
ADD file:0b08b600835a16058b725946cb7ae338fea6a14cf6998584f9728d2c62324f1e in / 
# Thu, 16 Apr 2020 01:00:16 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 01:44:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:44:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 01:45:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc084eacfbe394e053f99559ca63f9d660d60dad0b70a31347e5088af534b2e9`  
		Last Modified: Thu, 16 Apr 2020 01:09:20 GMT  
		Size: 50.3 MB (50304312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2753eba5d276059ffd460d19c6e651040079c4a18c7d6a93682bef3e285c0b9`  
		Last Modified: Thu, 16 Apr 2020 01:58:21 GMT  
		Size: 16.7 MB (16723352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff41b20f0ffb69690b5b8efa517a6db82e30df6bbb8a1ba31dda7369f437c9a`  
		Last Modified: Thu, 16 Apr 2020 01:58:41 GMT  
		Size: 39.8 MB (39777408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:870d895727f5175803af7bfe4bf76c278a76e7bf088c79c55d7bd4927b0ca9a0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118443886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4736dd2b1f9e0bffdaaf52b6f62621dd7e188eae62256e735c1f2669ead15654`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:40:13 GMT
ADD file:fc5ade2a561dca01c2a4d4035601db636d098801b5655a1bf239e8b706395f87 in / 
# Thu, 16 Apr 2020 01:40:14 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:23:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:23:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 02:26:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:582c227f31bedb5a1092c02e624ef551c8659052150d9e9368da891fffd1528c`  
		Last Modified: Thu, 16 Apr 2020 01:46:40 GMT  
		Size: 54.6 MB (54607914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1866a4665d6ee342c90adf77b23d7002ec3ef1fc701d3c2df2ca95ab860994`  
		Last Modified: Thu, 16 Apr 2020 02:38:43 GMT  
		Size: 19.9 MB (19855771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e614c5ad0e7f598900eb10a2560d248d97421d118be8b34cc663827e5e9b0f2b`  
		Last Modified: Thu, 16 Apr 2020 02:39:00 GMT  
		Size: 44.0 MB (43980201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
