## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:bc0400ced7d29b7b508292a00e8a30e281648d3fbb214c070959cfd707e7c1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2300cfa42872270c1cfdebe01b3801ef884a8bdee78fdfa6b699ef92b528f01a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71936669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f24b7e1b7e6a5232315d05c509f9251f5e4e5838dad44ab08814d9ba689e08`
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

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:63cb3585e2cdeb3c22b12b48670c0b2111daaa0cbd01e63b8f0639abbfc032d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69618575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35efb70a4391ddea84a36cb5e8ea91059ba2ef1f287a39ecdd0de4af7b83665`
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

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f31c39b5fd7515bf0db51301f4f19eb199fe1bec9afe07fe7d75ad0e0fb38079
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67027664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da1b237044f964087658b9d80398029330908ef6d82ebddc93f9777eaf2bd4c`
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

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:052787992f53a811092c7976a0e74790a1b84837bb2e94bedd894e8b0a14e2d8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74463685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de3400688e4ef0e7e8f85aa5f58ff988641270e5408546e05a717664aaf6f0e`
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
