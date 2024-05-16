## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:0a22b6221a53ec9308912e67fb7e16100e178e25ef35ab5cd8cdbdd8ae7b7342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull hello-world@sha256:e468fda6898b696f3a862a7a4766c70b7e9ffd2a847f2dafe828ee81cbfeb512
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154944157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f739d540d88ea1abeed62277c8ddb8042d5d1d57514290d79e11c6c743cad0f9`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:51:46 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Wed, 15 May 2024 21:51:47 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ea5e2605fe51b84b6dde74548be251ecf2bc039a618a100e567f020dba6327`  
		Last Modified: Wed, 15 May 2024 21:51:49 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db92d999c812e468e468fff22825d7ed883f16042f9a8751896efc5bd4614fe`  
		Last Modified: Wed, 15 May 2024 21:51:49 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
