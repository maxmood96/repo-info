## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:46849a5bd89a3e2a774a457b0f4bffd93c10e117f30690f78155c8931e51bfdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull hello-world@sha256:9b5bc67a906559930648466409151b8a78ffbf63fd2f267eda038b51fbf639c5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122579422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b663e04880427bb9742aeeabb169dc2fc6119b5065a1a406ff4d2c6b3acce43c`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 20:49:34 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Wed, 14 May 2025 20:49:34 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Tue, 13 May 2025 19:42:18 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81016aab28446563c3d1c40c0389cdfbd567057c241a1967de5f0b2a2d2476e8`  
		Last Modified: Wed, 14 May 2025 20:49:36 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ca0a8c734908c93ec7779d301e164794354ab8c0dcd9b3e67699b1288ebbee`  
		Last Modified: Wed, 14 May 2025 20:49:36 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
