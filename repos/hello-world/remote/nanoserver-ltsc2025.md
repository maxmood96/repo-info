## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:7c996a81316aace8693b4202669d1dc032d9ddb90c1d4907990984e7cc827be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull hello-world@sha256:ae7ea054bc645dcb17b77711793c72befb15cccbafc4af8f755fdcd70a0bec58
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205893106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a563a14dfbf577f13d1a74c4badce20c2c7e2fcbea9d07362c282b5d2d936fb4`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 18:15:34 GMT
RUN cmd /S /C #(nop) COPY file:1ae3735b36d6b3fc6ef1fd1d2d12badf8f42ad5660d983c9a406cb560633ed37 in C: 
# Thu, 27 Feb 2025 18:15:35 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5736904805ab9d01ebb6fd24d5a0c8501eb4417bb31180d5758210425464b8d`  
		Last Modified: Thu, 27 Feb 2025 18:15:40 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ee15bcb9c08902687843991154d64b467a271fac41fcfe3c8b94e490a30982`  
		Last Modified: Thu, 27 Feb 2025 18:15:40 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
