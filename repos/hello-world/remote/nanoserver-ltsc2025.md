## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:3aaa840a587d5ff74bfb35964ffe290393ef6ff5a2f4cfb62427066e253af158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull hello-world@sha256:efa3d57dd0d961b70f9a72900c216271a5dd7d65acfb4c75bb4c9a17879c15e3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197939345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c41ac8c58d369ca92ab0813ea0cf47894d441bfb84367fe3d1c1a7979b0d57`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Tue, 11 Nov 2025 19:10:18 GMT
RUN cmd /S /C #(nop) COPY file:22c7ae19fd4cf03d26e9cf1357869206bf69101c4233df05ad5f8fa29b73cde4 in C: 
# Tue, 11 Nov 2025 19:10:19 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc18235d9630a922f298b6dfdfc5bdbadcd1e72410b733d15095e6593f97b3a9`  
		Last Modified: Tue, 11 Nov 2025 19:13:26 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17801e8935462bbf17bca0b4bdd66f38fe4551678ad0e7688b92386824214870`  
		Last Modified: Tue, 11 Nov 2025 19:13:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
