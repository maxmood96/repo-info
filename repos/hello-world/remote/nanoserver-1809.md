## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:3385c88a17a232b8a7491387f8b6c1f00319a05b63908e67c4e2e6366959ea05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull hello-world@sha256:b17da88a43678dd8de2c335b977330a5f4e3f1175251a4204f54ef2ed1360709
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (103049615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbca594eee38d2bcbda18490d2667560b2452e74e73b8c26bddea59cb6920ad1`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 26 Jan 2022 15:03:14 GMT
RUN cmd /S /C #(nop) COPY file:dbb4e437ca342a79d5980fcb71c065abfe00353f696b1b54084e7c09d32ec085 in C: 
# Wed, 26 Jan 2022 15:03:15 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:149cdce3523df21ea29ed7f0fc0b1b9649bb7fc1e0ce8417bdaa204ce40cde33`  
		Last Modified: Wed, 26 Jan 2022 15:03:42 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec547840b7459a5ed163f9bfd7cc09526cec5d72875737d576c0a6e489c295d`  
		Last Modified: Wed, 26 Jan 2022 15:03:42 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
