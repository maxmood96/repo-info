## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:86757f7875e8f0062c77495438d7757b5412e5c67887adcf9564cc12467c0b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.587; amd64
	-	windows version 10.0.17763.2686; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.587; amd64

```console
$ docker pull hello-world@sha256:83ada69f673f74b81a3e2ed03edd56fcf190be8b1721f9afc4d25309908d7213
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117488530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1a3607c83c3e2cd46ec2fcbe5bc3107369653e6f2bc77976f4e83173c8055a`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 03 Mar 2022 04:50:34 GMT
RUN Apply image ltsc2022-amd64
# Fri, 18 Mar 2022 01:15:29 GMT
RUN cmd /S /C #(nop) COPY file:ac9f104fd739943f22886335a779468d86b20ac43fd3168171f6b23fc28882b9 in C: 
# Fri, 18 Mar 2022 01:15:29 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:dad81795ce109a7e20ebf80ad31925797ed97f9ba2a559f13f96ce3be5ea712b`  
		Size: 117.5 MB (117485491 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c76b7a831b8d3710d24874d5dfd820de311bf33def1c3e5a6c8e2fc2e0cfe133`  
		Last Modified: Fri, 18 Mar 2022 01:15:57 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd53ea1b7b2b52d2a8ffb3919744ae36ba26857a3d6102763efa2912b7cc725`  
		Last Modified: Fri, 18 Mar 2022 01:15:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull hello-world@sha256:acd65ed93903ec23468247a22d7ea0390f2e5e09b0ea3a93965a24b25b905c1b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103057541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756271127782036359622cdb5d32edc2671c44b15bfcf41d8e6d4792c3b4f4cf`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Fri, 18 Mar 2022 01:15:35 GMT
RUN cmd /S /C #(nop) COPY file:994f63bc3cea8285310afa5f4677df29bf99dd4cd1881c7e381100a9e794ba71 in C: 
# Fri, 18 Mar 2022 01:15:36 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:026225b3819b614d196f5b6b5b714cfa54e8501e187e15b4546af5bd30c6a767`  
		Last Modified: Fri, 18 Mar 2022 01:16:04 GMT  
		Size: 1.9 KB (1853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc6b8742d7233d05a39a305e944b3d1d118b53dff17f5117477a666ab5081db`  
		Last Modified: Fri, 18 Mar 2022 01:16:04 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
