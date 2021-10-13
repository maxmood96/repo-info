## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:acf8c637080ef930e4a4f0351e31e07cfe05e88518229ee8a7ec9205a18d87c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.288; amd64
	-	windows version 10.0.17763.2237; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.288; amd64

```console
$ docker pull hello-world@sha256:31801872aacfc6245ba5277e07dc2c9a482a473c87d625f25c3e6d5de930b35d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116942543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e564d7360cfa5451bc1d616d8871f6a17f1b2f977a68462a7259bce110f8a754`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 07 Oct 2021 11:15:04 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Oct 2021 12:20:37 GMT
RUN cmd /S /C #(nop) COPY file:55c009fa8b983e38026b41064e5367bc779dae76c0d404a11886c3cb19ec4509 in C: 
# Wed, 13 Oct 2021 12:20:37 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:91284e7e8fd4bd7ebcfa98544a3e4f59639f38281225c81c34b6fe22e0dba4e5`  
		Size: 116.9 MB (116939483 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:84f480fc2b679166f7d1340f9ee5ffc1ce7f860cea8e850365fef57631f1908f`  
		Last Modified: Wed, 13 Oct 2021 12:21:01 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f41bfcf238a5a974261c1f9ce6c039568585a03e2d8966083e273d7448d275`  
		Last Modified: Wed, 13 Oct 2021 12:21:02 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.2237; amd64

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
