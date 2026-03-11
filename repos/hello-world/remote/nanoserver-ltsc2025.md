## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:189be39d73abb39b03c1838044ee2221a10dafb91be7f72ff61628d88d6f493b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull hello-world@sha256:757c27fa04a236632f4b8e0d57da73375f27fe29b9c9b18d01abfb24b7897ff4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.4 MB (199412152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524c2db457cf00447b01eacb8a770b54b9c54ade05de0952e5971c810d4d04d5`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Tue, 10 Mar 2026 21:54:11 GMT
RUN cmd /S /C #(nop) COPY file:22c7ae19fd4cf03d26e9cf1357869206bf69101c4233df05ad5f8fa29b73cde4 in C: 
# Tue, 10 Mar 2026 21:54:12 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759f570961a03ea97f0cb9c6465b2d9affbb25329507b859212a297569d519e1`  
		Last Modified: Tue, 10 Mar 2026 21:54:16 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea65d4b2d066eae65b98aaed5a4010a668c2b021fd9249b9d92a22dd0d5d477`  
		Last Modified: Tue, 10 Mar 2026 21:54:16 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
