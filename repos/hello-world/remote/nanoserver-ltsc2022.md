## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:85bbcc1b27b33f8689c9b01402a2260e27194c8c4931a937aae631d4e91631e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.469; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.469; amd64

```console
$ docker pull hello-world@sha256:8ad7c869546021c7af55ebb2c376dca59c3829ea4588e7fd22a4a1c8f5bcb472
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117337353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9ca78832b1805382ef71ddc1b108b5a65f0e49e9e24b6f285cc537c5072c46`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 06 Jan 2022 03:34:42 GMT
RUN Apply image ltsc2022-amd64
# Tue, 11 Jan 2022 20:48:49 GMT
RUN cmd /S /C #(nop) COPY file:55c009fa8b983e38026b41064e5367bc779dae76c0d404a11886c3cb19ec4509 in C: 
# Tue, 11 Jan 2022 20:48:50 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:b2bb136f79c12b0a42720d7bb83469bce3f7bf2ca5c8bc68a36228796311fc6b`  
		Size: 117.3 MB (117334348 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1693f2bb3e1cc4eda5d0bd640e0efedc1778ecd9610aa18ab06fdf3dd46d6c35`  
		Last Modified: Tue, 11 Jan 2022 20:49:17 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698f7fae438e6cd3f9363993be625d0f68f81f160c816177da50be9acff80218`  
		Last Modified: Tue, 11 Jan 2022 20:49:17 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
