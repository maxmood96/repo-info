## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:a65b71e50a922c23f3a2a941dad06f2a199b52bf8b81d534af1c493991add684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull hello-world@sha256:563c31a6b24347d3f367df5dc33890ab1aec20e9470e5d998f3b6a8fc6eb5763
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102664370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7acc395cb5190d3f6eca8330eadfa3d2666becbb9960a2dfa7bbbef1f72d21a`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 07 Oct 2021 08:01:14 GMT
RUN Apply image 1809-amd64
# Wed, 13 Oct 2021 12:20:43 GMT
RUN cmd /S /C #(nop) COPY file:dbb4e437ca342a79d5980fcb71c065abfe00353f696b1b54084e7c09d32ec085 in C: 
# Wed, 13 Oct 2021 12:20:44 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:934e212983f208dc2bebc5de38259a6a62f1761868aacfee2cb3585a13b1e24b`  
		Size: 102.7 MB (102661372 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:105a5ce4ce14779701660c1c93917420b43117535c32a71b22690f4c27a53204`  
		Last Modified: Wed, 13 Oct 2021 12:21:08 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6512b9624c09c870e109a0bac0e917a666ce1ce895f30b5c0c21c8d7e8e11d6e`  
		Last Modified: Wed, 13 Oct 2021 12:21:08 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
