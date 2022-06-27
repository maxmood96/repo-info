## `archlinux:base-devel-20220626.0.64095`

```console
$ docker pull archlinux@sha256:84206d3ff36e7907508a4eef56196132404aa7b30ad8b4ac1675dab938d7d174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20220626.0.64095` - linux; amd64

```console
$ docker pull archlinux@sha256:e1be09cb704212345af41fbd6f9039dba109d8313c634a6584b0eeb34fca00f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224898835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d400e037c040a0060c913820dedc67b7b6e229a44cf256d89a0d219aaebb15`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 27 Jun 2022 17:20:57 GMT
COPY dir:390990430178124e352b418547c89afbba4c88a5aedaf52d2b448e3fadc3ad03 in / 
# Mon, 27 Jun 2022 17:21:00 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 27 Jun 2022 17:21:00 GMT
ENV LANG=C.UTF-8
# Mon, 27 Jun 2022 17:21:00 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:76c8667aacef579140d2d668bee5ce000211b11bf0bb90fe260c5f034319a21a`  
		Last Modified: Mon, 27 Jun 2022 17:22:17 GMT  
		Size: 224.9 MB (224890667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b7a4f1a8e5c58d97f7795af18375c81b6c4953b1ebd1c209c0d94c6125093c`  
		Last Modified: Mon, 27 Jun 2022 17:21:44 GMT  
		Size: 8.2 KB (8168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
