## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:9afaf6e7bb12f6b1e076cef3be990a3458bc9c996751ddf7f7aeeee1c8389f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `hello-world:nanoserver` - windows version 10.0.26100.32690; amd64

```console
$ docker pull hello-world@sha256:3a04009b28c80cf83eb68c5fd28d3ff8b2d98f10ef8bfbb96061bc792e5c71f0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199719978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c655f9ff744460b2d94f2f6f465b3f8759524293dbc5777cdd6857c6aec9f2cf`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 14 Apr 2026 20:59:06 GMT
RUN cmd /S /C #(nop) COPY file:22c7ae19fd4cf03d26e9cf1357869206bf69101c4233df05ad5f8fa29b73cde4 in C: 
# Tue, 14 Apr 2026 20:59:08 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2296fe3d1530e8b77392b9da74f8600cf2d50349a6579fcd33e087a4e9134927`  
		Last Modified: Tue, 14 Apr 2026 20:59:12 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c3c5aef8bbf8e0b3394e98c0ae092160fd82fb55c98fdb20b969a334d47633`  
		Last Modified: Tue, 14 Apr 2026 20:59:12 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.20348.5020; amd64

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
