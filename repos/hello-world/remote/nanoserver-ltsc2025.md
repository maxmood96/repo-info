## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:8b333b51bca6f2e54c6192246355573d16122404ad12bf34b50306bb6b11195d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull hello-world@sha256:e9a883dea35fe460353694fe0671f746b1f6d936c50da66738b6fc818b5c7f0f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194029562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823fdfcd60d7fdba665ee3bdc84d7a549c7f29878d2014ae5cbf81bac504d6c8`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 11 Oct 2025 15:58:41 GMT
RUN Apply image 10.0.26100.6899
# Tue, 14 Oct 2025 20:39:55 GMT
RUN cmd /S /C #(nop) COPY file:22c7ae19fd4cf03d26e9cf1357869206bf69101c4233df05ad5f8fa29b73cde4 in C: 
# Tue, 14 Oct 2025 20:39:56 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:463edd10ad50b00cf92c69fc3eaa85e1fa40aad1b7938fa232899405bd80f001`  
		Last Modified: Tue, 14 Oct 2025 22:41:48 GMT  
		Size: 194.0 MB (194026741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728b8365920fd07550e8adaa1dbe876ebf56d65c375dd13c000d5df504742cd2`  
		Last Modified: Tue, 14 Oct 2025 20:41:10 GMT  
		Size: 1.8 KB (1778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c52bf723d68f12fcede49f7a1e1476525b50d5c55af6e3c9d2c38bb158a9979`  
		Last Modified: Tue, 14 Oct 2025 20:41:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
