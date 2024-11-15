## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:e0cb2c2b0df31a68c43caee59e89381ca62295d85a45bbc1435d26a2f1a5b12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull hello-world@sha256:e75b1b0b6308f6521fcfd008faef190952d7c4ad553b2b8ace047e4625f438dd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5f8a4511584b854075937d55f7c522c459da5585f599801908097215fc8546`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 02 Nov 2024 23:34:35 GMT
RUN Apply image 10.0.20348.2849
# Thu, 14 Nov 2024 20:04:27 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Thu, 14 Nov 2024 20:04:27 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:815d6b7f925aef8327c34c34073ae54cc1c82120f1058682eac4c8c14ca21c70`  
		Last Modified: Tue, 12 Nov 2024 22:44:32 GMT  
		Size: 120.6 MB (120604951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcefacebbffeb7efeb5de0c171d037ebb6ca0d973f55e0fa59f45ff3d71a830`  
		Last Modified: Thu, 14 Nov 2024 20:04:30 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c768068f173fda2055a68d55e1749afcf2a5e70bd6ca47ad0864a7cd03012c`  
		Last Modified: Thu, 14 Nov 2024 20:04:30 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
