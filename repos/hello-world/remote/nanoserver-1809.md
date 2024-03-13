## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:389ef291cdbca6c4e14984cb2fdf558668c7ffcfaafd20a867c9004f952ae031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.5576; amd64

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
