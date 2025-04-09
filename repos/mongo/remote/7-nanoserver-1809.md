## `mongo:7-nanoserver-1809`

```console
$ docker pull mongo@sha256:f372276699ca31d51a3479e5701615e510a94a55a8234657aa75001e8bbd2270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `mongo:7-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull mongo@sha256:f7593ec3b26c09b8a418539c924a8afac69e838d9aa77c951132f655183cb0a9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.8 MB (718768010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618572c7d5600ab6ed5e9dd462fc4c97dc84d17e201c9db298d7e0767bef5daf`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 24 Mar 2025 21:42:42 GMT
SHELL [cmd /S /C]
# Mon, 24 Mar 2025 21:42:48 GMT
USER ContainerAdministrator
# Mon, 24 Mar 2025 21:42:59 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Mon, 24 Mar 2025 21:43:00 GMT
USER ContainerUser
# Mon, 24 Mar 2025 21:43:02 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Mon, 24 Mar 2025 21:43:03 GMT
ENV MONGO_VERSION=7.0.18
# Mon, 24 Mar 2025 21:43:53 GMT
COPY dir:6fcdcbf736bed5967b918eb56898f440804e5aea220d223d7002f3a8d481815b in C:\mongodb 
# Mon, 24 Mar 2025 21:44:06 GMT
RUN mongod --version
# Mon, 24 Mar 2025 21:44:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Mar 2025 21:44:07 GMT
EXPOSE 27017
# Mon, 24 Mar 2025 21:44:07 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ba546d4e3506fce3c6ac088f25890acf65cad8f765c4ea8cbabed2cda7cbb9`  
		Last Modified: Mon, 24 Mar 2025 21:44:15 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad481615445000bdbc8bd92c3079e19278281f8a1d8765ed961c4541eda53ff`  
		Last Modified: Mon, 24 Mar 2025 21:44:15 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad2c4a14894520c9221ceb00d98b3369a0c942f5356df812bd1ce95693a0c2b`  
		Last Modified: Mon, 24 Mar 2025 21:44:13 GMT  
		Size: 68.2 KB (68153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668165f24c1968ddeaf2bfecf3f2e7df594d9ccaeec5ca86886ba81fd11ec563`  
		Last Modified: Mon, 24 Mar 2025 21:44:13 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1836dcc1005b9b0816f54abd4236d3b40bef94baeb42a076c1e73dfd7035b3`  
		Last Modified: Mon, 24 Mar 2025 21:44:13 GMT  
		Size: 275.2 KB (275203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e17e0a257ff73a0903706fc2c5d17bc6e16fa2b3a240aafeaac76ad6736765e`  
		Last Modified: Mon, 24 Mar 2025 21:44:13 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc546f80baf995bc1085330192db35a8a4362298ce2b677ca9922385b6fae498`  
		Last Modified: Mon, 24 Mar 2025 21:44:59 GMT  
		Size: 611.4 MB (611438750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bedbc261a68583101b11406c0bb11f3e816781739e1c02f87b2ef49f3d72f5`  
		Last Modified: Mon, 24 Mar 2025 21:44:11 GMT  
		Size: 70.5 KB (70500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc2d4eaaf74858db59465da0cb7c2260eb9132546690b24f41676365a18cc1d`  
		Last Modified: Mon, 24 Mar 2025 21:44:11 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a6f215d8d21cd9960fe0c9bfbe6c0ae7077518a5fe8765c769738e7d29dd81`  
		Last Modified: Mon, 24 Mar 2025 21:44:11 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d85f61581d6aabf3461c6210293489ef179e1495d84e936b19fefa740d5dea7`  
		Last Modified: Mon, 24 Mar 2025 21:44:11 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
