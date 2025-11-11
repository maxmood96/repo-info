## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:0e011d254704fd79c5c4f4e3e674e85ee72f105013a4b7e133cc508920a39062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `hello-world:nanoserver` - windows version 10.0.26100.7171; amd64

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

### `hello-world:nanoserver` - windows version 10.0.20348.4405; amd64

```console
$ docker pull hello-world@sha256:0cfafc8b96f7eca7ce4ed61745802a8b05b400ed584f606699cadc08363e9a10
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126351958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64127f307634241b048680ad68eeee1c1204f808e6ea4ee3ce8a111d7addce82`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 19:09:32 GMT
RUN cmd /S /C #(nop) COPY file:9fca1d3c77d0758894ceeb7952e49e3b465b238dc4943832e9436b0ce84d8ae0 in C: 
# Tue, 11 Nov 2025 19:09:33 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63e8123e3ed5d7b0d7fec6620b0ee5262202f94bdb6620a185e8e4bfd52e6dc`  
		Last Modified: Tue, 11 Nov 2025 19:13:26 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e51f30fca8999183a3c20cdefdf7084b9a8eed63edfb8af46c27f87a7ff031f`  
		Last Modified: Tue, 11 Nov 2025 19:13:26 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
