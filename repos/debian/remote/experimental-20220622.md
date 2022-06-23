## `debian:experimental-20220622`

```console
$ docker pull debian@sha256:f8043b692a4a75567c21cb258e69651a598b514e2e5a74d303c2ae9b77d040d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `debian:experimental-20220622` - linux; amd64

```console
$ docker pull debian@sha256:8bbeef6e32768cbc1213989edd62860a511278b8426fa6b9cba354bb569ca9e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53219164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c131b48619fccd62fa3488b2d0723ef5c154f0c7f8cc1f31db062ce48f75a10`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:49 GMT
ADD file:45d826596769429bdd8e44a7e4190e8251862fb92b291469c25a7f3adda1e39c in / 
# Thu, 23 Jun 2022 00:22:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:23:01 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:79d3127460f36c355c974cecc0ffaa2ec77e9b0ce6167c147a569dc304caf3ef`  
		Last Modified: Thu, 23 Jun 2022 00:30:59 GMT  
		Size: 53.2 MB (53218943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3252eb9414033e608e9dd7d4ee6106197abb35696108c27c1e4ac29a903c7022`  
		Last Modified: Thu, 23 Jun 2022 00:31:22 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20220622` - linux; arm variant v5

```console
$ docker pull debian@sha256:ae3904279e4a7137d63cc4673280b9a8345a1a0325d00278e0da12845b571deb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50998620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2860fe94635e21ba4b2216c8bdc164849c9369f34637b472eacdd2abae35817`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:57:34 GMT
ADD file:4bf21aa467ceb4d839160af4de449dad29d044a520791e6c71c54dde704d8bc3 in / 
# Thu, 23 Jun 2022 00:57:36 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:58:09 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b3478ed536c9e1abe83e1e0f866445e3e0fe7c2007c7aa36ad9cb504bf924a0f`  
		Last Modified: Thu, 23 Jun 2022 01:15:39 GMT  
		Size: 51.0 MB (50998397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6830b78a40c2a50a2a77f63f25a19a48b4a0ca0217fe3ab00744d28aa8ddbd1c`  
		Last Modified: Thu, 23 Jun 2022 01:16:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20220622` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e4949f1c9977bb50247083eec20e6cf94083fbfe96d39c52b65e9267c6eb8609
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52287637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1683fc5d56f55d039fc0ea45b130834b71f229edfaed1fde1588fa513020b082`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:43:32 GMT
ADD file:83243e9276a2db4b32b9db70b82082b9916708ff78aa48e853bf66e25b94b55a in / 
# Thu, 23 Jun 2022 00:43:33 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:43:46 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0218b9399fe5f1e2e433bc15dbf6072585ecc85deee0767ceccbedb8147965f2`  
		Last Modified: Thu, 23 Jun 2022 00:52:52 GMT  
		Size: 52.3 MB (52287416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00ff63e1b97ec637fb6f7cac8c9e7ddba40cd3e80d9a82682c14e41e8c353e9`  
		Last Modified: Thu, 23 Jun 2022 00:53:18 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20220622` - linux; 386

```console
$ docker pull debian@sha256:6ade15546332e04863eefd6156caf1f4ccc937ff5ed975ad217abcbcfdde91f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54181242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61666d64e40360cf6ddded307f9aa6d956e235123fd1d0c10e6dec5d2a6ab69`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:33 GMT
ADD file:221a0bb9f7148b5afbde0413b44b6c045f3a16aa0815f6fc546a8cb3a332c492 in / 
# Thu, 23 Jun 2022 00:42:34 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:42:49 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:535ec83ce1df319a594b28beb916bb8e432bd69ff7ae87214ae8403e59bf3eee`  
		Last Modified: Thu, 23 Jun 2022 00:52:26 GMT  
		Size: 54.2 MB (54181020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc3482c7dcf8466972a526b7412833c9f848b31d483918262fcb7b884eabf50`  
		Last Modified: Thu, 23 Jun 2022 00:52:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20220622` - linux; s390x

```console
$ docker pull debian@sha256:e0be942a53e4a08734b663517895eac8b14e6edab651d7b018f17360aa6a8b51
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51752933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509078a9917626a11e35d8e11a09b4195f0bff4b803ac9db4c8d1ce7482ae93b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:47:50 GMT
ADD file:504b35536ad1298c4d98bea6c9ecb7cec0678c23c1ec4fa0866086c78a416ffc in / 
# Thu, 23 Jun 2022 00:47:58 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:48:28 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4363c17af4ae14e6a29a78f38293a36fd01b27bbb843a5f2740ba7cbdf0fd600`  
		Last Modified: Thu, 23 Jun 2022 00:54:41 GMT  
		Size: 51.8 MB (51752710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a70697d679f2b63c75be1a4e835353b77d274b9c33fd9cb35136ac136ba0558`  
		Last Modified: Thu, 23 Jun 2022 00:54:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
