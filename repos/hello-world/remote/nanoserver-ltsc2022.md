## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:17a9ff4d03372fe0afd3b0e6430005844e37e680b6618ac0d394aa107585febc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull hello-world@sha256:9d42acdd6e213819488f0020f230817c6ead7eb91c35f7f516c798e5c44a314b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122691736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ff686134dbf7394507b356ab10d06b0cb167398080f0575aea416bfa415436`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 09 Oct 2025 07:34:08 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:40:21 GMT
RUN cmd /S /C #(nop) COPY file:9fca1d3c77d0758894ceeb7952e49e3b465b238dc4943832e9436b0ce84d8ae0 in C: 
# Tue, 14 Oct 2025 20:40:23 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:f68a3bbf3ee20b515c5b8b801e5627a9dac3782ef264e37060c34ed80e5d8874`  
		Last Modified: Tue, 14 Oct 2025 20:41:53 GMT  
		Size: 122.7 MB (122688886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7531f51cb324f21ee5e810a214cf800ecf3787d580c918696dda2b45dbdb9900`  
		Last Modified: Tue, 14 Oct 2025 20:41:42 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc6ca0d1efa624f14922c0ec422f89449a3b28c36f6f805a87fe458f41f8c08`  
		Last Modified: Tue, 14 Oct 2025 20:41:43 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
