## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:f4ce9335607b7d0a7576de660ddede10582400f97b5ebe39a2d35a2e3866050d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull hello-world@sha256:29fbaecbfe3e2c6e11f0f6b881dd26065773eecce704318bf91a6eb04653e682
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.3 MB (199254520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961d2b5de9477213c0499f7a98dc30514a31b6a6e0d58d29bbed5c071b1f114a`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Tue, 10 Feb 2026 22:49:30 GMT
RUN cmd /S /C #(nop) COPY file:22c7ae19fd4cf03d26e9cf1357869206bf69101c4233df05ad5f8fa29b73cde4 in C: 
# Tue, 10 Feb 2026 22:49:31 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282ab27bbb7d8fbf08bd97d26f3736bf3ede5a2baf63ee06a955a14dd27d18f`  
		Last Modified: Tue, 10 Feb 2026 22:49:35 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce32bbed4f4baba3b59217dcacdc2552ae8373a860a8dbeeed59b8570edbeaa`  
		Last Modified: Tue, 10 Feb 2026 22:49:35 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
