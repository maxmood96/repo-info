## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:0878c4e78a75484f54769596e37358dbc8a00b55f02488e12641473f6ba614a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull mongo@sha256:708481a0a339ef8f40dbd37d5d547402c5ce79648f40505f2165424ccad79335
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.6 MB (732592709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddb6152c08563d35670c161bf58a5948369378c06892990eb6cbe49b831ea85`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Mon, 24 Mar 2025 21:39:04 GMT
SHELL [cmd /S /C]
# Mon, 24 Mar 2025 21:39:05 GMT
USER ContainerAdministrator
# Mon, 24 Mar 2025 21:39:07 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Mon, 24 Mar 2025 21:39:07 GMT
USER ContainerUser
# Mon, 24 Mar 2025 21:39:09 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Mon, 24 Mar 2025 21:39:10 GMT
ENV MONGO_VERSION=7.0.18
# Mon, 24 Mar 2025 21:39:28 GMT
COPY dir:6fcdcbf736bed5967b918eb56898f440804e5aea220d223d7002f3a8d481815b in C:\mongodb 
# Mon, 24 Mar 2025 21:39:44 GMT
RUN mongod --version
# Mon, 24 Mar 2025 21:39:45 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Mar 2025 21:39:47 GMT
EXPOSE 27017
# Mon, 24 Mar 2025 21:39:47 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c15356725c88b5b4db0a715cfc9fa3853a38cd973a00f16d78849ea6bd0e813`  
		Last Modified: Mon, 24 Mar 2025 21:39:52 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b328362a64c8a8d5fd2d28180e0514f1bf8c66aa6f80f7b309c84bcc4f4fcd`  
		Last Modified: Mon, 24 Mar 2025 21:39:52 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba8ba5d2c7887bcc2fa300f6e679f8b0d3556466f3501a6f11fd7c5ccde936`  
		Last Modified: Mon, 24 Mar 2025 21:39:51 GMT  
		Size: 75.8 KB (75834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8282b2d9347af9361602b598376d414e50167ad10e0cc3d6d1d7d790889f61`  
		Last Modified: Mon, 24 Mar 2025 21:39:51 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb454b39550a390fb1a536c568f5aecc476900c29ad06c13f77d4565feb83399`  
		Last Modified: Mon, 24 Mar 2025 21:39:51 GMT  
		Size: 275.2 KB (275159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c42d6df36d182e2742fe3c98cb19c70282c26f5ef8a93d29806cd298d589b3`  
		Last Modified: Mon, 24 Mar 2025 21:39:51 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7126bfeb0a47c5acd4ece575035a6e15c55bb4603326c74ee142fb33c004e6`  
		Last Modified: Mon, 24 Mar 2025 21:40:37 GMT  
		Size: 611.4 MB (611438739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e0ab9cadad626dad45a721b46e5e847a191ddc563f316f4c0e996e32c52b0c`  
		Last Modified: Mon, 24 Mar 2025 21:39:50 GMT  
		Size: 100.1 KB (100119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588199d8565f156331f6ac323040fcf98e0b4f7bf455ab594a6022796cd81b43`  
		Last Modified: Mon, 24 Mar 2025 21:39:50 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605a18760c997ffcc1215d048c1d9ba55351b3cdb40714833b3deef9423eef24`  
		Last Modified: Mon, 24 Mar 2025 21:39:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa0dbdd03b088344f975a5462eeb32722d13534fdedd784ab7c908ea139a96f`  
		Last Modified: Mon, 24 Mar 2025 21:39:50 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-nanoserver` - windows version 10.0.17763.7009; amd64

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
