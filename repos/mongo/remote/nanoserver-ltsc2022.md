## `mongo:nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:84538896bfd36d2c8cdef418c8483dd2f0e0fe52ab7fedc02babbbbe289a2824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `mongo:nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull mongo@sha256:5f3145850a6325ebfd75acade73ae35c63e14474c6d2f1221b6abcf572396da5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **892.2 MB (892206235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187daec040e89b20fb84116ffab9c809af3763bcadde3dfd33c59edcd07a084f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:21:56 GMT
SHELL [cmd /S /C]
# Fri, 18 Apr 2025 04:21:57 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:21:59 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 18 Apr 2025 04:22:00 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:22:01 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Fri, 18 Apr 2025 04:22:02 GMT
ENV MONGO_VERSION=8.0.8
# Fri, 18 Apr 2025 04:22:25 GMT
COPY dir:72b416844fc933841484cbf4a72c928cbc4d580829e8d356764afc081e298d11 in C:\mongodb 
# Fri, 18 Apr 2025 04:22:50 GMT
RUN mongod --version
# Fri, 18 Apr 2025 04:22:51 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 04:22:51 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 04:22:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80dbe026a5526d1c19610ff84b52e38b6781a697898d2520f55b062ed7de6197`  
		Last Modified: Fri, 18 Apr 2025 04:22:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bc672e7467d380339194a4ad669b00762b7b6628dde60f03dfd60b70f2de13`  
		Last Modified: Fri, 18 Apr 2025 04:22:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91c08a89f7e439ce4b57fd04efd2b5cd1be9c310203ca07e92fd42501aee7ae`  
		Last Modified: Fri, 18 Apr 2025 04:22:55 GMT  
		Size: 76.1 KB (76103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a5bf59f450fff235d7e752d9d3aa4ab880c237ce9bebf713471f55420ba4f0`  
		Last Modified: Fri, 18 Apr 2025 04:22:55 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24ae9a92c6dec1679ce0d3f8dd93acc36c770f94fd58e52f6b462db1ee1f643`  
		Last Modified: Fri, 18 Apr 2025 04:22:55 GMT  
		Size: 275.2 KB (275173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4639fcbd9e5db85aeff54d4af3fba859f524c509499cba273f915c9b6da0a2fb`  
		Last Modified: Fri, 18 Apr 2025 04:22:55 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a58780edf58c846fbd769ad459a300669b7f3fd00e6444fa002e6d4ce53e8a`  
		Last Modified: Fri, 18 Apr 2025 04:23:55 GMT  
		Size: 769.2 MB (769212265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895fb902461d9641d66965a79488f0cfbc1109cc6f4b5039bda201c05fbdd237`  
		Last Modified: Fri, 18 Apr 2025 04:22:54 GMT  
		Size: 96.3 KB (96335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e766513a194907ffabd58c427db81c6f81bb60efc5f4c2054daddb3ae4f259c9`  
		Last Modified: Fri, 18 Apr 2025 04:22:54 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50992f4f6d74771a0396a62ee15f8afe2dd75350f64ffc6e366b9c5360f3565`  
		Last Modified: Fri, 18 Apr 2025 04:22:54 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633820d1f62ddb3249dd7367c3332041c9f174467e3ba63fc2507b265b76a78a`  
		Last Modified: Fri, 18 Apr 2025 04:22:54 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
