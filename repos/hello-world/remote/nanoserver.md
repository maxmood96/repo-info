## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:561b0f6a3d85130492dbadcb2b9b18bdefd4047422eb7c1a4cb932316adea12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `hello-world:nanoserver` - windows version 10.0.26100.6584; amd64

```console
$ docker pull hello-world@sha256:bf2f6cded1837e43cd52fc6476d8ada11a22c482382919f427d80e8ec60b255f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193553751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad056272374477ce63e81ea05f73394d280fd83db6836582570e71366b5e6c75`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Wed, 10 Sep 2025 21:45:19 GMT
RUN cmd /S /C #(nop) COPY file:22c7ae19fd4cf03d26e9cf1357869206bf69101c4233df05ad5f8fa29b73cde4 in C: 
# Wed, 10 Sep 2025 21:45:21 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad7dfb98a979f5d6802db21d133bc25e4ebd15831b7d6caa4171658072d6ce0`  
		Last Modified: Wed, 10 Sep 2025 21:46:29 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2475a3fec3bd13431541ba9def7fabd4a0a280e70ad1f5d7ac20bdd25e0141cd`  
		Last Modified: Wed, 10 Sep 2025 21:46:29 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.20348.4171; amd64

```console
$ docker pull hello-world@sha256:03cacc6befd335f7e92a4a0523ccf3422bdd514ecb60c3213ce72efaec8b0f41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122722751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16a0562ffc06f2b0c7c53688ed35d1296995eae28b72c210ee40a4fc2ef050e`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 21:43:31 GMT
RUN cmd /S /C #(nop) COPY file:9fca1d3c77d0758894ceeb7952e49e3b465b238dc4943832e9436b0ce84d8ae0 in C: 
# Wed, 10 Sep 2025 21:43:32 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bcc0a5ec2cd8feebb7923cd72a1032803f7836ba6e23e6fc7b7b66d17b9908`  
		Last Modified: Wed, 10 Sep 2025 21:44:37 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b105737bfd4047d5256dcd5e6bcaddf4ec22f3167114ca9865de6a7a7c9a75c`  
		Last Modified: Wed, 10 Sep 2025 21:44:37 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
