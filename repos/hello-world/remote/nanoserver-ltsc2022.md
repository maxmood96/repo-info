## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:a6b4ee7738bd419d191ee922e00f2b9deed4c7a198006c3f7ae98f25db9094f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull hello-world@sha256:1e00e4b67c3ddb20d60a424b278fc96b267e5587675321dcecb19dc55624fea2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120664387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab66d561eefe99f1e8c49e193e656626a012b7c0681ff368d505c05559ee8b0`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Tue, 14 Jan 2025 23:27:06 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Tue, 14 Jan 2025 23:27:07 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Wed, 15 Jan 2025 01:24:28 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdba3e6d94cbe8f9640224a4985a26e5abca2e7c8be0b25a16d67d606fb42a6`  
		Last Modified: Thu, 16 Jan 2025 00:01:30 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47131ca3f892f33705ecc9a13bd4dafca6dd980be0f39f766c4cc86c9e8a8856`  
		Last Modified: Thu, 16 Jan 2025 00:01:30 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
