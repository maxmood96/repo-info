## `mongo:8-nanoserver`

```console
$ docker pull mongo@sha256:6468007507feea785f8d941966144e1b273177b36552dd742aee241d04b96f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `mongo:8-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull mongo@sha256:b1836c60a0e8f57a96a6f073bbb1b94555c28d308964ac41fdd209b254b67e5d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **903.3 MB (903306680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f58841f03fa56a7ef23c02e96ee9d61a1b478d828cd74191714985b4b7a488a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Thu, 21 Aug 2025 19:09:42 GMT
SHELL [cmd /S /C]
# Thu, 21 Aug 2025 19:09:43 GMT
USER ContainerAdministrator
# Thu, 21 Aug 2025 19:09:49 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 21 Aug 2025 19:09:50 GMT
USER ContainerUser
# Thu, 21 Aug 2025 19:09:52 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 21 Aug 2025 19:09:53 GMT
ENV MONGO_VERSION=8.0.13
# Thu, 21 Aug 2025 19:10:17 GMT
COPY dir:e7bf28cd040ae0a17f9db7e90dd1f2393a4c8043b5ce1df4294c0e1cd576ef89 in C:\mongodb 
# Thu, 21 Aug 2025 19:10:38 GMT
RUN mongod --version
# Thu, 21 Aug 2025 19:10:39 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 21 Aug 2025 19:10:40 GMT
EXPOSE 27017
# Thu, 21 Aug 2025 19:10:41 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d967ccaba8eff193d786869b14a592dbb4c644fc801851d91cce83a2cd3f8ba1`  
		Last Modified: Thu, 21 Aug 2025 19:11:54 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7e5859268b02785dcb1174ab234f007bf7d358d7e1912a0ad22efe212fd55f`  
		Last Modified: Thu, 21 Aug 2025 19:11:54 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbd8c581cf5ba0fc632c62df6a5c0ac5268e37e3a9b27c761c60cb4ed1cad74`  
		Last Modified: Thu, 21 Aug 2025 19:11:54 GMT  
		Size: 77.0 KB (77007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9197d104cc21b562a89b3ddd3e98071193e412aca6b83f69ffa5db3efc92d6`  
		Last Modified: Thu, 21 Aug 2025 19:11:54 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460c0e819403ed4dee9905c2b03b06d5c2b62b469fecbef7c8abab64ee96cd7e`  
		Last Modified: Thu, 21 Aug 2025 19:11:54 GMT  
		Size: 275.2 KB (275168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff3e16ba4027c86086f80536bd66ffcc53e9f07bddbcb6932d88f5aed9271c6`  
		Last Modified: Thu, 21 Aug 2025 19:11:54 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17da7cba588e0308c1c430cc83808233bfe7afd3ef1b0239c97d664486c0ed8`  
		Last Modified: Thu, 21 Aug 2025 22:08:31 GMT  
		Size: 780.2 MB (780184625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee6849bc8c6d7da8b767ec68a897645d6d7b05d024bea902a1120ce26012652`  
		Last Modified: Thu, 21 Aug 2025 19:11:54 GMT  
		Size: 102.3 KB (102335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a88d7992b4e60966c28cf298e1cc74e1b6815212f2352d3c53e6520f53a94c`  
		Last Modified: Thu, 21 Aug 2025 19:11:54 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971a50f4d666361dc8b6da1c45f82720639609d9c8842cf88b58a4c578c0ab79`  
		Last Modified: Thu, 21 Aug 2025 19:11:54 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cfddbd08d7976ac42ae617c1e5e759e829e561aa99b5412c1c426a475e5c06`  
		Last Modified: Thu, 21 Aug 2025 19:59:17 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
