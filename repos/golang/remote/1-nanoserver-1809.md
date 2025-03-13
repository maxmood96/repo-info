## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:84e5c43e5874a421dcf25d3a0c7109d43e10bd2b9de6142b8942cf188176ef22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull golang@sha256:330f38cfadda793a73a1051d2fc35271d6cf22c7312c6c8606236d1d91dc362a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188881410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6928366205874ecaccbb9c125584575ff089cb28dcae90dfab246e74f8341d40`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Thu, 13 Mar 2025 18:23:39 GMT
SHELL [cmd /S /C]
# Thu, 13 Mar 2025 18:23:41 GMT
ENV GOPATH=C:\go
# Thu, 13 Mar 2025 18:23:42 GMT
USER ContainerAdministrator
# Thu, 13 Mar 2025 18:23:45 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 13 Mar 2025 18:23:46 GMT
USER ContainerUser
# Thu, 13 Mar 2025 18:23:47 GMT
ENV GOLANG_VERSION=1.24.1
# Thu, 13 Mar 2025 18:24:49 GMT
COPY dir:1c8a5df65fcdbd0ad306edfb20884d0712989c03ff01d990889cdc983af886a3 in C:\Program Files\Go 
# Thu, 13 Mar 2025 18:24:53 GMT
RUN go version
# Thu, 13 Mar 2025 18:24:54 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fb0c8f7fb742c9ff89271a76b4c3d7c3c9cba0753b93e695a990de6431575d`  
		Last Modified: Thu, 13 Mar 2025 18:24:58 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6340de275842ae7e2c18bfa41cc7ff5c85564e7605dd3b95544235a3e6ccd53c`  
		Last Modified: Thu, 13 Mar 2025 18:24:57 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4e328bc42e43f7cafc201523ed6315dfaaffab6dc1a7b94c826880c2daf7e0`  
		Last Modified: Thu, 13 Mar 2025 18:24:58 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc49e74da145484d9b29d2e4ace7abd24acdd4f7d9a4d4cad8df52e482d1212`  
		Last Modified: Thu, 13 Mar 2025 18:24:58 GMT  
		Size: 70.7 KB (70728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e032a109b3d2850ce81bdb6c52ce5ba461e688c832472adc26ab59f9b86443e`  
		Last Modified: Thu, 13 Mar 2025 18:24:56 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a458c7b63ab6851bacabd261ba897e72139e63329927695b9ad14ab57854658a`  
		Last Modified: Thu, 13 Mar 2025 18:24:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b5723c4b964f567f87ea0ae764af75bfbdccf3254e390169d7b217db3edfcc`  
		Last Modified: Thu, 13 Mar 2025 18:25:09 GMT  
		Size: 81.8 MB (81817846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f1753135fc2aa5ce46250ec22dd33f591e50c4bb42d7010e7414e7371732c4`  
		Last Modified: Thu, 13 Mar 2025 18:24:57 GMT  
		Size: 78.7 KB (78696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c1451060a2e26904c62e9a99cef6331c7c9297c98c770ae5f23858f303a65d`  
		Last Modified: Thu, 13 Mar 2025 18:24:56 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
