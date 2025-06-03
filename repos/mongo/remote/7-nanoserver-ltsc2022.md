## `mongo:7-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:392a6927ca7465bb0a1c8e0ec063e866c0ab1f8a6b9b32831522c3c26042b31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `mongo:7-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull mongo@sha256:e33a596eb2422e94f72fb10dfcbfdf9d741b9fbb2cebf2f4546575f4278e56f3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **737.9 MB (737871547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45841269db406e4846df2ee5c57196dc97f560bee790fd8dab0e98051b2186f0`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 21:13:17 GMT
SHELL [cmd /S /C]
# Wed, 14 May 2025 21:13:18 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:13:22 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 14 May 2025 21:13:22 GMT
USER ContainerUser
# Wed, 14 May 2025 21:13:24 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 14 May 2025 21:13:25 GMT
ENV MONGO_VERSION=7.0.20
# Wed, 14 May 2025 21:13:45 GMT
COPY dir:3d7b19532c774165f3e18af6ab7d5314090422186feb24f01e23d159f15ea98d in C:\mongodb 
# Wed, 14 May 2025 21:14:04 GMT
RUN mongod --version
# Wed, 14 May 2025 21:14:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 May 2025 21:14:06 GMT
EXPOSE 27017
# Wed, 14 May 2025 21:14:07 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214c1ff0e3fda82a97513144b278e8e170fb5345431be3d8bd68f285eb588db8`  
		Last Modified: Sat, 17 May 2025 22:08:40 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde45e542ec23ffac793ed17863a7c759f22e8c81bdceefb7cc3b7419fda6541`  
		Last Modified: Sat, 17 May 2025 22:08:40 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54288dfeecc5e58d25dc7413dc9882dd125711579effcebac3757c4a56f86989`  
		Last Modified: Sat, 17 May 2025 22:08:41 GMT  
		Size: 77.5 KB (77482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2dbfb4e183df93a5358cabbb46e4939befe9efb6b19c2cc8ebff907f20fb2f5`  
		Last Modified: Sat, 17 May 2025 22:08:41 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c33dc4ae7baa5d053888cef968d0d59398b317d7ea60c123e37ca1f0c1143d`  
		Last Modified: Sat, 17 May 2025 22:08:41 GMT  
		Size: 275.2 KB (275152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f287a274a1649696af75e56b199937452ad0a7a5615d587daee3704d90885fcf`  
		Last Modified: Sat, 17 May 2025 22:08:41 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905af0d2c071fee5c7cadd3e906dd72f2c43c6260c90648205af96d98c05bd53`  
		Last Modified: Sat, 17 May 2025 22:09:18 GMT  
		Size: 614.8 MB (614837213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd54178cb73e5f8bf511ee98b4524bd75a4e0d4a68394db3656c77b8236e91c`  
		Last Modified: Sat, 17 May 2025 22:08:41 GMT  
		Size: 97.9 KB (97868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70146d38b512b869814a8fbd13f99f778b18004e05a063ed7e5a45901cbd9d5c`  
		Last Modified: Sat, 17 May 2025 22:08:41 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ade113e7383db2c3ea57cef3b336527d0e19d7d476bc2a7b6a6bbe33306aba`  
		Last Modified: Sat, 17 May 2025 22:08:41 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad03ef37be859270976a9b807edc6a5deee05c1d871d7bdc59db8430fd3d9938`  
		Last Modified: Sat, 17 May 2025 22:08:42 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
