## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:38c96a09a41b3e7a3ac3e4c738306ce08657bf27d1a70278f9f1b92b98d43df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull mongo@sha256:8a8b331032056e6d7a6f92e6cd038fb307025d226f127f61fb84e37c6d14f1f9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.9 MB (648864059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697f562744c4076fda6ac0a9dad80f23423bade2dc9bb7a0c728c7f4f2848a91`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:19:49 GMT
SHELL [cmd /S /C]
# Fri, 18 Apr 2025 04:19:50 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:19:52 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 18 Apr 2025 04:19:53 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:19:54 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Fri, 18 Apr 2025 04:19:55 GMT
ENV MONGO_VERSION=6.0.22
# Fri, 18 Apr 2025 04:20:12 GMT
COPY dir:4b15d5e4d896c710da0908054bfc1acda67a6afe024035e1b165242aea0e7d87 in C:\mongodb 
# Fri, 18 Apr 2025 04:20:24 GMT
RUN mongod --version
# Fri, 18 Apr 2025 04:20:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 04:20:26 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 04:20:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7a9911b10768e85ce7baac34fd650529642a8e92df23f00178ea7be65bdeda`  
		Last Modified: Fri, 18 Apr 2025 04:20:33 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d26f26432eec6f54915af8a7ae2aaacbb39295269bbf9f0b54f08436a68021`  
		Last Modified: Fri, 18 Apr 2025 04:20:33 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fceba58bc696e2e8b5ee33ec417c4ab77a8632347356dd91001d781baf21af5`  
		Last Modified: Fri, 18 Apr 2025 04:20:31 GMT  
		Size: 75.9 KB (75931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7870bc8cabf468cfeec8fa58567f36306e352855d9391c6d2c235e3a7c43548`  
		Last Modified: Fri, 18 Apr 2025 04:20:31 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c145ab2cd4edd6749d40c4b1976079ca37334aa31c8e74c8013086ffa40a7f`  
		Last Modified: Fri, 18 Apr 2025 04:20:31 GMT  
		Size: 275.2 KB (275167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583249df4ff7dd267ad4d9030d566000e0382c8ff5f0e51764cebccba14427d3`  
		Last Modified: Fri, 18 Apr 2025 04:20:31 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92752e526c3227220fa5e811d2a2e671762aade6db9992079d066796cdad0ab4`  
		Last Modified: Fri, 18 Apr 2025 04:21:15 GMT  
		Size: 525.9 MB (525872257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ee5a5b3f66512a3488dc1878edf68a554a71b554f7a5e2e9bcb0a7f96ccd15`  
		Last Modified: Fri, 18 Apr 2025 04:20:30 GMT  
		Size: 94.4 KB (94424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21be0bd93c93a5d39a0a994e11f500c17389b1e4a4bec4372eb5e1ce09bdf0bb`  
		Last Modified: Fri, 18 Apr 2025 04:20:30 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778c274b56e7ec874279a6e929aa1af4a27923000fd0a5fa1bfc92933b21fe60`  
		Last Modified: Fri, 18 Apr 2025 04:20:30 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f88c7b035529b7ab156aa0a2d103c25b8eff372975610b4a2b1759da85b255`  
		Last Modified: Fri, 18 Apr 2025 04:20:30 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
