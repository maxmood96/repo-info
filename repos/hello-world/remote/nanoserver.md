## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:3fcc9313a21cbd67f88e4cb5a193b5cbe3320d0e481308a10a0ac2351d4f1b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `hello-world:nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull hello-world@sha256:d6e6504d7ec61ce1e15cd54d57838a2c036e25b2fb480026431cb67394a24b7f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190144889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7f5a332b02a3318f00c486150820a88ff07b04aab6eb00cc51d426f6b5aeb7`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 03:09:58 GMT
RUN cmd /S /C #(nop) COPY file:1ae3735b36d6b3fc6ef1fd1d2d12badf8f42ad5660d983c9a406cb560633ed37 in C: 
# Fri, 18 Apr 2025 03:10:00 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6908451bbaa87930c8e434a11632a47a055c5183c2267824d9e06dbf8cbad4f0`  
		Last Modified: Fri, 18 Apr 2025 03:10:03 GMT  
		Size: 1.8 KB (1777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa3f6c7c371cc05ffeb51ab4a14006e4b907c90d370e4779ea8e0085f6d6b90`  
		Last Modified: Fri, 18 Apr 2025 03:10:03 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull hello-world@sha256:7a74da18f0e142334209634df1d0e8b7c423884cc16da82a8fde7426c44b92e8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122541860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e455f68eb8b42e993433af79229d279932e9e5a856d0f71d328fc1db05f1e01b`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 03:09:12 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Fri, 18 Apr 2025 03:09:13 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41dc116d63f2ec540b4e898c60abcadae4da7009ee12bd270b5cae20f0087787`  
		Last Modified: Fri, 18 Apr 2025 03:09:15 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3000f9622770d846efa587e7788c5a86f9de8ec512f0e8737d2619914d44a7b9`  
		Last Modified: Fri, 18 Apr 2025 03:09:15 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.7249; amd64

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
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3d767572703fe3d7a0178b5acbb98b3acfecb0dcee8684d02611e1e5648568`  
		Last Modified: Fri, 18 Apr 2025 03:08:39 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a55de0aaad7fdfcd503b60de6e9057fe131e3b2540e0313c54df2790647ba7`  
		Last Modified: Fri, 18 Apr 2025 03:08:39 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
