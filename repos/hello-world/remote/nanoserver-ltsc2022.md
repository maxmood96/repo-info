## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:3a03002040bea041e761b3210dc7c36d69074b85adfe7fcef963ccd9207d9615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.473; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.473; amd64

```console
$ docker pull hello-world@sha256:7e9c5b2a36bdd391c713b800eb7ac7047207f04faf92ec4aff8667c85540b41b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117336183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618fd25c1455708b34f08ed8354f2131f471ca8ad310b8a22b6a5ebfd2b64e23`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 16 Jan 2022 04:54:46 GMT
RUN Apply image ltsc2022-amd64
# Wed, 26 Jan 2022 15:03:07 GMT
RUN cmd /S /C #(nop) COPY file:55c009fa8b983e38026b41064e5367bc779dae76c0d404a11886c3cb19ec4509 in C: 
# Wed, 26 Jan 2022 15:03:07 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:7691725ee3658d154f940d82fd8c3ff07c0dc589a0c9a93df47ed0ede92a76ab`  
		Size: 117.3 MB (117333150 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bfef10deb78a77121ec999eeec2bb3c2f65e023e0ea7b6e64deb72ebc25791c3`  
		Last Modified: Wed, 26 Jan 2022 15:03:33 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdae4e65c07ded85b7bbfab7eccfc2043f5892407e48ded900879c6c9ebd24db`  
		Last Modified: Wed, 26 Jan 2022 15:03:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
