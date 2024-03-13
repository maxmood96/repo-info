## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:9009d88409b3bcef47088bfe0fd1b70188603008d1090b63d0df7e14447f9b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.2340; amd64

```console
$ docker pull hello-world@sha256:2f19ce27632e6baf4ebb1b582960d68948e52902c8cfac10133da0058f1dab23
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120705489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4df9232a51a135a5445363e5812f099cb9aebac338cc04e857c09b50475d92`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Tue, 12 Mar 2024 23:58:00 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Tue, 12 Mar 2024 23:58:01 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96349c1d782fecae40700091dafe28fa8d14f366569fdd910fa187a63d65b580`  
		Last Modified: Tue, 12 Mar 2024 23:58:03 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0057fc59369cf17cd5e000c5cdcde520da9276c8478befe99d5d700a621dd21e`  
		Last Modified: Tue, 12 Mar 2024 23:58:03 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull hello-world@sha256:3a0bd0fb5ad6dd6528dc78726b3df78e980b39b379e99c5a508904ec17cfafe5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104622881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c1a1831e9db8870b186245c0749d84300097c5a1084933288aec4c588a3b5d`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Tue, 12 Mar 2024 23:58:06 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Tue, 12 Mar 2024 23:58:08 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c002186dc45b4c33cf56c8bf687876d87e61926e34668206965a87174511c959`  
		Last Modified: Tue, 12 Mar 2024 23:58:12 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262e273c7d6e33518b03421f162f097b2721cbc94b52d8dee33eba7bfec993ab`  
		Last Modified: Tue, 12 Mar 2024 23:58:12 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
