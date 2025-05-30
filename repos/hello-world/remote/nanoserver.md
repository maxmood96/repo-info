## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:de7c95d81f2b68b86f2c1674ebc54ad79438db42b71ce17d9810f02494264c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `hello-world:nanoserver` - windows version 10.0.26100.4061; amd64

```console
$ docker pull hello-world@sha256:45767087cbe67a8edbfcfc013026d1730c662cc14e4160f449d534b2d439603b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191414894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178248e4c7d3c52d4576c3b8a860ccc1f39cecd43dd7ed62bdf007ea5f390c5b`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 20:50:27 GMT
RUN cmd /S /C #(nop) COPY file:1ae3735b36d6b3fc6ef1fd1d2d12badf8f42ad5660d983c9a406cb560633ed37 in C: 
# Wed, 14 May 2025 20:50:29 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Tue, 13 May 2025 23:02:56 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787a49ff64bad1bb68d7207522bc0701f0d3aad782397a83ef86c1992def81a3`  
		Last Modified: Wed, 14 May 2025 20:50:32 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd2b583015cbb38f3fa8ce3286b6d7e8733898535cbe6daf972acd760f33ffb`  
		Last Modified: Wed, 14 May 2025 20:50:32 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.20348.3692; amd64

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
