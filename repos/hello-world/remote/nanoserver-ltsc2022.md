## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:a279f5f7fc43246039a0fe0f9fced2afa62df36f41275b0d56d60f2726825cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull hello-world@sha256:647ab5a73cbda664339326104ca7d664268261ccbc4c5707febc0e3aea154333
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120512306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a08b952747fb8d6edd2e4f04c166d00ebf4f6c87f083b926c99e65da6381a1`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 05 Sep 2024 23:48:03 GMT
RUN Apply image 10.0.20348.2700
# Tue, 10 Sep 2024 23:58:48 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Tue, 10 Sep 2024 23:58:48 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:a447243899be39b01c34fc7e1bcecb47ce42b14668876fdd121f8b5e2d4d4a86`  
		Last Modified: Tue, 10 Sep 2024 22:28:02 GMT  
		Size: 120.5 MB (120509521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1fc28204f3aa55a0bfead48e7ba6ab05e9abadeee96bc16bcc9e4b84d607c9`  
		Last Modified: Tue, 10 Sep 2024 23:58:51 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8424b8ca3680437ec0ee6efd33655237b3254eda4659a53a25efb0a84399e776`  
		Last Modified: Tue, 10 Sep 2024 23:58:51 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
