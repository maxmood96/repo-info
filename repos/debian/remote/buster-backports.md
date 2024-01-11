## `debian:buster-backports`

```console
$ docker pull debian@sha256:45f82371ba51d63be3e86bc057e7ee6aff7098f4ee1d96d421c6218d411b8828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:f6b200054fac22a8cde86a55795f904562441d9281a8d199c32ae6f4491cd9b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50500476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460dc00f4a971df8638c71c2ebf18c77816f5ba72410219145d57b8eb2b6c8ac`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:27 GMT
ADD file:ac13007eb56f6e064fe27101dfa666f02b04f4ce9a2bcf3ade6cf6055562b7e8 in / 
# Thu, 11 Jan 2024 02:38:27 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:38:31 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7418de5ce68f67dad705c01c70a7bb811f9b886f8d7aac2b66110d376046fdcb`  
		Last Modified: Thu, 11 Jan 2024 02:43:26 GMT  
		Size: 50.5 MB (50500254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5295b073360f437747757a36a505201a3cdbb75cf5676089c6e9e22c2defed42`  
		Last Modified: Thu, 11 Jan 2024 02:43:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:66c8e965c3e038bf71d8f263052e628bc95ff7004b331a47071fbafc3bc71a22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45967829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8530df0a23cb821c8469949ddcb61098883c6ff057e83cc4a2574b861cceeefb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:52 GMT
ADD file:7f9fc3dd3778509079c1f4010b0ef89a6910aa3a83b317c5134489675daccb47 in / 
# Thu, 11 Jan 2024 02:42:53 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:42:57 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c11d78fb5679ceced7c7aa83357081cad2ce04776bc24c72152ce12e6b5b8411`  
		Last Modified: Thu, 11 Jan 2024 02:49:46 GMT  
		Size: 46.0 MB (45967605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076981b64a816af7a4da48242083fa4c598af85e6d1f10bc241154aa6826efb`  
		Last Modified: Thu, 11 Jan 2024 02:50:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1f252353313a595bb59a29898098ad302e1d3e861050701397280f86402fae94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49289092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0409ef88431bc265b9e960aa01fbd2bb9a5917956fc700ce0ea8336ee8716bb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:05 GMT
ADD file:e9cd54dd40d18756610852bf97172fae748b0dc8eb39d2fb1c97181382daed3b in / 
# Thu, 11 Jan 2024 02:41:06 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:41:09 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ff2e543b6a43ccfdb1731587b58c288c29eb3947f78a5877f4fd9bb8dfa918b5`  
		Last Modified: Thu, 11 Jan 2024 02:45:04 GMT  
		Size: 49.3 MB (49288871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec110c3a9da884f9f57a9df79e1ca3a6c8f998fe96ac7715dd5a317c3ce588bf`  
		Last Modified: Thu, 11 Jan 2024 02:45:16 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:0d071b874037751d7a6e675b6f3de32440fc9dd54385894d37ae8f0daa848f27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51255428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d512e199ea47f6998b38416454a0fc3b81def67036eaac4d87252b5be77c9ab1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:39:12 GMT
ADD file:1e68cfe2a77ca5be656fe9cf5a3e89e23630239ebc044ace148ba49124dbaf7a in / 
# Thu, 11 Jan 2024 02:39:12 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:39:16 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:94764bf084b89ee796b567eb9a1b71857d957204137c0ec8781723a4b7ae71ae`  
		Last Modified: Thu, 11 Jan 2024 02:44:28 GMT  
		Size: 51.3 MB (51255203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ec760fda5230461a5033c7405d8553e161dce0765d5fe3464176ecb836ea83`  
		Last Modified: Thu, 11 Jan 2024 02:44:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
