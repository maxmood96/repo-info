## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:29dfbc17d669dc9318888e2b5089685fe4576414742c81d451e459e587b976d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:f8d0b91052dd33bfa5805168e703da5363b7d2387246a9f82534c66b72064463
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50500350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df6534542e81c4036cd9fd6305617363852ae9327d7de982987f6b535f68b29`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:15 GMT
ADD file:4e52d5e3f0dba851dd387bcc5e3412801f94a31c666401171c2677eb381d2712 in / 
# Tue, 13 Feb 2024 00:38:15 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:38:20 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:75f3ee849d53ae19939bf3c4d3d39637622bb7488d64924f9eb8e2e930301445`  
		Last Modified: Tue, 13 Feb 2024 00:43:48 GMT  
		Size: 50.5 MB (50500122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26632594a6118159943479904613fdc18f379fa9fbf78570594ca15a21732fd`  
		Last Modified: Tue, 13 Feb 2024 00:43:57 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:3ade968aa6ba4864f9e4652c026ec0928830e9d5548b4a0610e610f55c132a57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45967855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed580351c65ded33aee626a59356c4bcb6af920836c9975b93708b1e672d908`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:21:27 GMT
ADD file:5d6631534290520eb333410774389155939aeb8389fc4b6cc381d9686d5bf5ce in / 
# Tue, 13 Feb 2024 01:21:28 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:21:34 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d3597855d4ad297e82785ddeae3d52029f6af4a687da8f3ba890c9039681c047`  
		Last Modified: Tue, 13 Feb 2024 01:28:45 GMT  
		Size: 46.0 MB (45967627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6596df8d960fa1cfc10df823df23bc0da44b878f4dcfceb699c743faa556c5`  
		Last Modified: Tue, 13 Feb 2024 01:28:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:61f1c836c6722ea6dad2ec458740dd80c08dd979776c6d1e05fa098441c6ca47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49288989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf84aad44487d899f64f04480eeb9159521be9476466a47ae67553ba220cc92`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:56 GMT
ADD file:b5e851b4e0139c24b0530f3b60e8f6c776cc14a0b3bb6c7bfcefef971bd07eb2 in / 
# Tue, 13 Feb 2024 00:41:56 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:41:59 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:41caffcb920af8646ce68d6c31e1c6d52438442ef13d200e2bae8603fa1c906b`  
		Last Modified: Tue, 13 Feb 2024 00:46:34 GMT  
		Size: 49.3 MB (49288763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c83fa249007dcaf9176eaafa22552dc1457e8b9e5f3e334cf1c1613e1e48fd`  
		Last Modified: Tue, 13 Feb 2024 00:46:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:133b69f384a975ca777b6eead210b5525ea56463fe45d1cc2d4daaf5de2a9e6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51255589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d55fc7e34a0f5b53af82e054d5c4eb12f42c6e82862131b0c5ce71ac9623f97`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:52 GMT
ADD file:a8836bd6a74ee761db6e3f72aeca349a2a582f5cc81ae7bbf675ea240ba9cddc in / 
# Tue, 13 Feb 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:39:56 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:575f55e08df46270f1d846f6b24a92c870053473c5457716aeed7ec6ccac9943`  
		Last Modified: Tue, 13 Feb 2024 00:45:47 GMT  
		Size: 51.3 MB (51255363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c545a9c993a9fc71637d86fc4b2a76976bd97859d27a7ff1e7f9540e2cb2f6df`  
		Last Modified: Tue, 13 Feb 2024 00:45:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
