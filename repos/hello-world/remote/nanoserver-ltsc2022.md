## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:8e4337e162d78a8772bcc490b74f42c4aca6757377e6791c4751dd4331070b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull hello-world@sha256:1478a9feb091ce38c879124c8de618ad97edd7993bd825e104f52941c18f0cbf
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (126958773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c2cbc4500c3926cab0e66ab19a0434c9d21e737dc982628f16c97dc66bdb55`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:00:07 GMT
RUN cmd /S /C #(nop) COPY file:9fca1d3c77d0758894ceeb7952e49e3b465b238dc4943832e9436b0ce84d8ae0 in C: 
# Tue, 14 Apr 2026 21:00:08 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26035ad45bc86ddff7246e442d508f7f093b2440140a92cc4a0576d4b6e63e5a`  
		Last Modified: Tue, 14 Apr 2026 21:00:12 GMT  
		Size: 1.8 KB (1779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52837df14b5b693eba6397a88caffce433c00515cee94920bf349888111dc45`  
		Last Modified: Tue, 14 Apr 2026 21:00:14 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
