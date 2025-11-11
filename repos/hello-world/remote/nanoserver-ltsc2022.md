## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:6c609c4ae3ac68e4defee92f041cf339202aab359bcc47d9c1622497556e93b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

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
