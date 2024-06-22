## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:aab77587aa6bf960da1509aa7486e49622e519c74f8f38098436be610178ee7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull hello-world@sha256:d9958c926e37a9700d85698bc9872cae110bbbb26f551a9684da9a8332dbb778
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120502323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78ae902b550731ac17bfc560f7ebc0dc09007d0104648cc8718a74cc455efe8`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Fri, 21 Jun 2024 23:54:39 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Fri, 21 Jun 2024 23:54:40 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c9816903701133197e67f7ef017b59b526a34244afaf782fe5696f159f3ade`  
		Last Modified: Fri, 21 Jun 2024 23:54:44 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907ea000aac247469eb42ac65876290a3b357a2174a0db6fc2286cfd8cf6b1ec`  
		Last Modified: Fri, 21 Jun 2024 23:54:44 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
