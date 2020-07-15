## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:e8de428286e28a02542f45bfdafd29e3d962ccc531a948bce6f1bf3f20b3e6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull hello-world@sha256:6cafacb78bc50470f3f33d96298d4bf67969642c0d09c7ee599601568c18d59a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100898116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98257792ecf661e57ec22684f7f010cfd98fa812266f750187ba5eb50c62e82`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Tue, 07 Jul 2020 13:50:07 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jul 2020 12:13:21 GMT
RUN cmd /S /C #(nop) COPY file:0afaffc2fa64462107b7178b2ae7d20404ff12f637eabe3a8046192b9d9a0338 in C: 
# Wed, 15 Jul 2020 12:13:22 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:dc95608099543221ef539391bfece5c1ce37b97af9da457f5990349cab028a12`  
		Size: 100.9 MB (100895619 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1fde5d28e17a58003eada2f71e7ae3dac06d146475922101d0b06e5a490ab429`  
		Last Modified: Wed, 15 Jul 2020 12:13:34 GMT  
		Size: 1.6 KB (1606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566994b78a4c26ddaeb79d91bb74a8d2966594d6418b8084a6ffcac7ce410a32`  
		Last Modified: Wed, 15 Jul 2020 12:13:34 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
