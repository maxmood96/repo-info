## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:c0e6bf87601d280984400f3caa801b41dc2c51333bb373df938097d9644ae437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.2966; amd64

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
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2b32f9c54b4d18282180e56773e9860f10d00068b7d91fc9f5ec8fc9a12d1e`  
		Last Modified: Wed, 11 Dec 2024 20:29:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f054f1cc911326f34ca2a843109ee889160d14ef0e9a0546bd0a35f4950a355`  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull hello-world@sha256:111895d48d0701685b1eebafbd9d5cf7ceab55bd0c9c05f2533dcd08514111e8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155234389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6067c50cef15519498633170e3a1ee1f187a674cb7231170fe2365683f712190`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Wed, 11 Dec 2024 20:29:25 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Wed, 11 Dec 2024 20:29:27 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8192e4d745e64f41a98c231ce0e229bbb361f1808e4c5a02540564e54a18697d`  
		Last Modified: Wed, 11 Dec 2024 20:29:30 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700fc8f787ae0a42b45d86e9decf6c3f8ead129cdc5ddbeb7c551a8537392c47`  
		Last Modified: Wed, 11 Dec 2024 20:29:30 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
