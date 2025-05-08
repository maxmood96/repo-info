## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:604fff99badb91eef609759050249d7005edb127ceb84ecff7d99dcfbdcf8036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull hello-world@sha256:6238568916516255ec37cf51ff73cce4d80c782fec2d569491bd4797a75f84b1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108755060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c82cff8bdd866000b4cfd5a3c0c3b15a050e35671257bf6a685b9b8f54a436`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 03:08:35 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Fri, 18 Apr 2025 03:08:36 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Thu, 08 May 2025 17:05:23 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3d767572703fe3d7a0178b5acbb98b3acfecb0dcee8684d02611e1e5648568`  
		Last Modified: Thu, 08 May 2025 17:09:49 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a55de0aaad7fdfcd503b60de6e9057fe131e3b2540e0313c54df2790647ba7`  
		Last Modified: Thu, 08 May 2025 17:09:49 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
