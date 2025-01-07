## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:f2127738662b7d5328e214dde4d7e716bff4c930a27019485885fbf5bc090c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull hello-world@sha256:79e2520a76c5b50ad2fa2f101d8d9293124f2ceb3239e97beb82a9df6e7ee3ef
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120604080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fda71fe26c799960c0b0fbaf0999d48bb0a2c364bd32b7b7b6f2374707eff18`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Wed, 11 Dec 2024 20:29:31 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Wed, 11 Dec 2024 20:29:32 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Tue, 10 Dec 2024 18:34:17 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2b32f9c54b4d18282180e56773e9860f10d00068b7d91fc9f5ec8fc9a12d1e`  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f054f1cc911326f34ca2a843109ee889160d14ef0e9a0546bd0a35f4950a355`  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
