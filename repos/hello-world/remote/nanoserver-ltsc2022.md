## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:1d7158012a1ab27d35b7d994d53665ce8766b83d779738e0602b0ce34c0ba446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull hello-world@sha256:5e98ef53f6ec1678c4fe3d4f8fe4a0e8308c1305bcad58944a2491f40ab8001b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120698349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1bd2628a13622d38f7ae22fc482430fe8ff538416b4bdc38e2d3de5c4a90c2`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 18:43:22 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Wed, 12 Mar 2025 18:43:22 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46da91e0662a661cee0e8653fb251ddf9ff8a7a79ea868baad10057ebb9e568`  
		Last Modified: Wed, 12 Mar 2025 18:43:26 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c489d3fbaf869b98e6866d6f9f703c955de90da0dec6fb073b058254166e3`  
		Last Modified: Wed, 12 Mar 2025 18:43:26 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
