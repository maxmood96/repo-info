## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:f5f9715cb491f3a80a1a6d0e17b9fcef131ee62d2752b9b4c783ed13f2e24961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.587; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.587; amd64

```console
$ docker pull hello-world@sha256:ab933db0b70dcc2e3f47240ecce8d9f8bb7f4799c2cff7ec860e374a8152d653
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117488441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b8102ed15a9e1835cd226861c7b0232007e0894452f35c9ed41d72ed0d7697`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 03 Mar 2022 04:50:34 GMT
RUN Apply image ltsc2022-amd64
# Wed, 09 Mar 2022 13:11:18 GMT
RUN cmd /S /C #(nop) COPY file:55c009fa8b983e38026b41064e5367bc779dae76c0d404a11886c3cb19ec4509 in C: 
# Wed, 09 Mar 2022 13:11:19 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:dad81795ce109a7e20ebf80ad31925797ed97f9ba2a559f13f96ce3be5ea712b`  
		Size: 117.5 MB (117485491 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:64c7463a83f4ff042a96ec6d00e5fe5f3428c3004c1dad74c93387f17d07a15c`  
		Last Modified: Wed, 09 Mar 2022 13:11:44 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0960811bb6d9747d7d57a26ae94238fe7d2a584bc07ebb777f04772b11eed77d`  
		Last Modified: Wed, 09 Mar 2022 13:11:44 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
