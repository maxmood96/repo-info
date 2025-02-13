## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:20c329687f0b71d18b54f9af7aa40830553d33381d3753430b4439ea4e15717d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull hello-world@sha256:01d0af4ccf62079415ccc6f718b01c09def42b8392cd4402984bea12978e102d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120669384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ab5e9e4b884f9f1f5b1c2ec34ca7e818d76b69f0f9d28bef07f8de461669f4`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 00:28:00 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Thu, 13 Feb 2025 00:28:00 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:49:39 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deafd885d2fb0adc49a6ae6ba5babf9642332bed5fcc91396f93e2c3a09f38de`  
		Last Modified: Thu, 13 Feb 2025 02:41:40 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c01454f8e89eae3973609c8d8655838cffc120290c8fb1bdbc21e0b996c692b`  
		Last Modified: Thu, 13 Feb 2025 02:41:40 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
