## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:8e39ccb7d3005e688d59526f7ec9419451780528d4b13440348cf2bff65a1d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull hello-world@sha256:e5186c0a754b32be8905baa4935d2371f43e59000d334f1d3b8a017bb7a3c75d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155270326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74dd06ce00d942bd38f2f5c5ee520b093416d4b3e1f717d93fa687cc6eb25923`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Tue, 14 Jan 2025 23:27:06 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Tue, 14 Jan 2025 23:27:07 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Wed, 15 Jan 2025 07:23:16 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992e0af2da997ef6a20c8c003eecd705504394b373c256dc6b162bdb2e450556`  
		Last Modified: Thu, 16 Jan 2025 00:01:29 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d68d49ea2f85f180af358314d9417884f460f54dcc746a380493a08f1d9716`  
		Last Modified: Thu, 16 Jan 2025 00:01:29 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
