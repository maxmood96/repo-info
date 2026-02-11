## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:dd2fd3bc598f2bd8b625fb0c8cffdedef29485bb0e07872c761676fd3d824257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull hello-world@sha256:c93abf3adc49a6dd060d5336bcf38fbed10d96512163af7e87a0958364807b67
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126648664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fba75fd4e3e87261fa81ad7d242bd9df6a7be565a122226011bd9370664b6d`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Tue, 10 Feb 2026 22:50:31 GMT
RUN cmd /S /C #(nop) COPY file:9fca1d3c77d0758894ceeb7952e49e3b465b238dc4943832e9436b0ce84d8ae0 in C: 
# Tue, 10 Feb 2026 22:50:32 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5544a86cf93c78da63cd772ec94d6ac51a7cf44fd3ec56ba3360f1d8f6d562`  
		Last Modified: Tue, 10 Feb 2026 22:50:36 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74da384cf41aafaccbae6980ae438a0765af841f85ec02f07727ce1e56409a4`  
		Last Modified: Tue, 10 Feb 2026 22:50:36 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
