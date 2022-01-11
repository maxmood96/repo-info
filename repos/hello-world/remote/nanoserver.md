## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:699e82dfae4c5ac1bb3fb8011ee4e6d8d2ac5754c03ecc5cd57afe6def8977a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.469; amd64
	-	windows version 10.0.17763.2451; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.469; amd64

```console
$ docker pull hello-world@sha256:8ad7c869546021c7af55ebb2c376dca59c3829ea4588e7fd22a4a1c8f5bcb472
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117337353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9ca78832b1805382ef71ddc1b108b5a65f0e49e9e24b6f285cc537c5072c46`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 06 Jan 2022 03:34:42 GMT
RUN Apply image ltsc2022-amd64
# Tue, 11 Jan 2022 20:48:49 GMT
RUN cmd /S /C #(nop) COPY file:55c009fa8b983e38026b41064e5367bc779dae76c0d404a11886c3cb19ec4509 in C: 
# Tue, 11 Jan 2022 20:48:50 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:b2bb136f79c12b0a42720d7bb83469bce3f7bf2ca5c8bc68a36228796311fc6b`  
		Size: 117.3 MB (117334348 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1693f2bb3e1cc4eda5d0bd640e0efedc1778ecd9610aa18ab06fdf3dd46d6c35`  
		Last Modified: Tue, 11 Jan 2022 20:49:17 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698f7fae438e6cd3f9363993be625d0f68f81f160c816177da50be9acff80218`  
		Last Modified: Tue, 11 Jan 2022 20:49:17 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.2451; amd64

```console
$ docker pull hello-world@sha256:0c2ccdb11489ee191e87a8b56efb724915b76e91b1907dd1279c30e6d1878e5a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (103017632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b29f50d39bbc02e868d9fbd1d664435b7d831ecb54b2e92bfd1bd3f2bc66b88`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 20:48:57 GMT
RUN cmd /S /C #(nop) COPY file:dbb4e437ca342a79d5980fcb71c065abfe00353f696b1b54084e7c09d32ec085 in C: 
# Tue, 11 Jan 2022 20:48:59 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6a7a45351f0d35d3015a23e2b621cacc416d30540c7006ec26f9b48d1acaaf5a`  
		Last Modified: Tue, 11 Jan 2022 20:49:23 GMT  
		Size: 1.9 KB (1851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536f5f58b451eb0054a1082a298cbc56130dcf021d91c38c7c42f05c5c38a5bc`  
		Last Modified: Tue, 11 Jan 2022 20:49:24 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
