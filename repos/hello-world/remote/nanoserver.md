## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:8b55adf49906654ffa7016d1d6b36ba13738a3c58af0c1ce0f5e92415a5fb9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `hello-world:nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull hello-world@sha256:468a2702c410d84e275ed28dd0f46353d57d5a17f177aa7c27c2921e9ef9cd0e
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101052856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b209aa2b650ec933db6f0c41a2879569b5bb7c26556b04067e72d8fde7526ddb`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 12:13:34 GMT
RUN cmd /S /C #(nop) COPY file:0afaffc2fa64462107b7178b2ae7d20404ff12f637eabe3a8046192b9d9a0338 in C: 
# Wed, 11 Mar 2020 12:13:35 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:543ff0f9573f8cd59e942d73f2f25f85f5ce5ba99aeda8e6b6bd5ba32b0e7f23`  
		Last Modified: Wed, 11 Mar 2020 12:13:52 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01167dd6121e6f035b620eef2c90e4137f63bdfc18bffda70f1467b58d61946`  
		Last Modified: Wed, 11 Mar 2020 12:13:52 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
