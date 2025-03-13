## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:9e452c3942e2545252a4e304f030bbbb5e7a9426882e87ffe2103726c0afe2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `golang:1-nanoserver` - windows version 10.0.26100.3476; amd64

```console
$ docker pull golang@sha256:011b3d838118d2d626b75515385d68b7885e10c3a87366c28f4615537f1918d5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.3 MB (288336475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed2762440dde093cbd7b9b11af1417d1e798e349b2314b011508d3bfd73f775`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Thu, 13 Mar 2025 18:19:41 GMT
SHELL [cmd /S /C]
# Thu, 13 Mar 2025 18:19:43 GMT
ENV GOPATH=C:\go
# Thu, 13 Mar 2025 18:19:45 GMT
USER ContainerAdministrator
# Thu, 13 Mar 2025 18:19:49 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 13 Mar 2025 18:19:51 GMT
USER ContainerUser
# Thu, 13 Mar 2025 18:19:52 GMT
ENV GOLANG_VERSION=1.24.1
# Thu, 13 Mar 2025 18:21:07 GMT
COPY dir:1c8a5df65fcdbd0ad306edfb20884d0712989c03ff01d990889cdc983af886a3 in C:\Program Files\Go 
# Thu, 13 Mar 2025 18:21:11 GMT
RUN go version
# Thu, 13 Mar 2025 18:21:12 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afaf66764c1c834c7e0595bb9e09227df8b5a9e46b32c15ca9b9cf6e052dc4cb`  
		Last Modified: Thu, 13 Mar 2025 18:21:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be48730b4b39a212f1cebb80f251d34a4510f65873f20c7428d7ecfcd14bd75`  
		Last Modified: Thu, 13 Mar 2025 18:21:15 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31dd4aa8567c5a7d61cc1f30f57a57d081142d78b1c321600507a4fdcc85b46`  
		Last Modified: Thu, 13 Mar 2025 18:21:15 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41b0d6f7e438b2ea47eca0eb665e4b21f581607563d32b3f96c50de4fa1a814`  
		Last Modified: Thu, 13 Mar 2025 18:21:15 GMT  
		Size: 76.5 KB (76477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f631b129fd04c7185ce60b81ff151315b4bca9d149868dacc947cc1dfe6c23c2`  
		Last Modified: Thu, 13 Mar 2025 18:21:14 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7124bb77d096ab4ded5bc95335037fcb207836e9a757fdc0d9de646844e102d6`  
		Last Modified: Thu, 13 Mar 2025 18:21:14 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1624ade04372c4b2448426a9f54cb9514e98d0bc37c3fe07f6fd304cc8c7cab9`  
		Last Modified: Thu, 13 Mar 2025 18:21:29 GMT  
		Size: 81.9 MB (81860748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c024e7a9bc84b669461771c0d6ea2a27629e2fd394a1d1deab099e7244802c6d`  
		Last Modified: Thu, 13 Mar 2025 18:21:14 GMT  
		Size: 90.5 KB (90515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ad0266de4b4803539590f85a981b2995a8fcdee254709595e47d1837d9b514`  
		Last Modified: Thu, 13 Mar 2025 18:21:14 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull golang@sha256:3370e2f27d1e5c6040b087315b4cbb00c081c551e592d70fda0863ea0a875309
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202689972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f86edd934a2045e85b02bd135c4fd655b3a75589bb4b13d61f0cb66694ccc94`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Thu, 13 Mar 2025 19:29:42 GMT
SHELL [cmd /S /C]
# Thu, 13 Mar 2025 19:29:43 GMT
ENV GOPATH=C:\go
# Thu, 13 Mar 2025 19:29:43 GMT
USER ContainerAdministrator
# Thu, 13 Mar 2025 19:29:46 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 13 Mar 2025 19:29:46 GMT
USER ContainerUser
# Thu, 13 Mar 2025 19:29:47 GMT
ENV GOLANG_VERSION=1.24.1
# Thu, 13 Mar 2025 19:32:20 GMT
COPY dir:1c8a5df65fcdbd0ad306edfb20884d0712989c03ff01d990889cdc983af886a3 in C:\Program Files\Go 
# Thu, 13 Mar 2025 19:32:23 GMT
RUN go version
# Thu, 13 Mar 2025 19:32:24 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac539fba92aabef6aa1334ed741c2cc76305fe7983c59d2e2813b7bce114424`  
		Last Modified: Thu, 13 Mar 2025 19:32:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d945086758e16255f96063e49f8f91f133a7222f341550b0bf9d13f5232654`  
		Last Modified: Thu, 13 Mar 2025 19:32:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca0d57e4a2c8eeaec6aabc75ecb3232cac1570fb6c9059dc00a046ad5e004d`  
		Last Modified: Thu, 13 Mar 2025 19:32:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0588951a65608595261db6b4578dabd6b4a07d69ebe23ceefbc58784e641fa`  
		Last Modified: Thu, 13 Mar 2025 19:32:28 GMT  
		Size: 75.9 KB (75869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa957882855fd355c7a985e33f8a8e7275880c00588697c1e77d952515418fe`  
		Last Modified: Thu, 13 Mar 2025 19:32:27 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be729eeb2eb0e195c51ca405401488d5038098498b1c09d01a6237b17e863839`  
		Last Modified: Thu, 13 Mar 2025 19:32:27 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820b61b699842a4c1d9e210737a8fabe061cc281d9db0a882774071df5510343`  
		Last Modified: Thu, 13 Mar 2025 19:32:39 GMT  
		Size: 81.8 MB (81819720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465c68cdaecc0f0e78f4286825c35dff934e8bec91f81034d4c06e3dee9a1f33`  
		Last Modified: Thu, 13 Mar 2025 19:32:27 GMT  
		Size: 92.5 KB (92455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778ed1d6cfb0059a4af9fe5aaef622b1e5ea3b97e5d2b34e456ac81861831779`  
		Last Modified: Thu, 13 Mar 2025 19:32:27 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.17763.7009; amd64

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
