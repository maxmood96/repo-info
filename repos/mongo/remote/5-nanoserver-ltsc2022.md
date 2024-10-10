## `mongo:5-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:54584786516efb4bc135b900e1d803fabfe137a06cc7c2f39cdee161bcd1e645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `mongo:5-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull mongo@sha256:9f29d003ddc7c36083482a602ab0bb3843e00a3fbe111f2174f35824070759f2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.4 MB (432391814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a20549a287148c0e31fcbae8b7eaf179586c6edaac13aafad90bda1f313db2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 10 Oct 2024 00:00:47 GMT
SHELL [cmd /S /C]
# Thu, 10 Oct 2024 00:00:48 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:00:51 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 10 Oct 2024 00:00:52 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:00:53 GMT
COPY multi:241155f1c943760aaa62762c3091531649e347eeddd5ad65cf07160763241a3d in C:\Windows\System32\ 
# Thu, 10 Oct 2024 00:00:54 GMT
ENV MONGO_VERSION=5.0.29
# Thu, 10 Oct 2024 00:01:06 GMT
COPY dir:2a264fe791bba3a77954956eed4741f2ec3b2e15bd00a3c81924c3459cafe2f1 in C:\mongodb 
# Thu, 10 Oct 2024 00:01:13 GMT
RUN mongo --version && mongod --version
# Thu, 10 Oct 2024 00:01:15 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 10 Oct 2024 00:01:18 GMT
EXPOSE 27017
# Thu, 10 Oct 2024 00:01:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255c7bc8bbd2b1605269ebed721ea4b785a756140d547aff7ae070b4a59db345`  
		Last Modified: Thu, 10 Oct 2024 00:01:24 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18663f1da648859e943cc73db724d4c10336e3d0c98f063897b0b9df90e875a`  
		Last Modified: Thu, 10 Oct 2024 00:01:24 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88648bdc47532d7a9bcf6b5f62e8574888a79ed2f60cbdfaf481f2ec08e76ee0`  
		Last Modified: Thu, 10 Oct 2024 00:01:23 GMT  
		Size: 82.5 KB (82477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78f274dba9b98f2fa8af316187c5d7c4bff5bd1ce82a9d2515a2c2d41f04e82`  
		Last Modified: Thu, 10 Oct 2024 00:01:23 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad14fc9108efa2a6817355075cf5c4e1e2bcd465d5f65d0d67f08f33db3d32d`  
		Last Modified: Thu, 10 Oct 2024 00:01:23 GMT  
		Size: 275.3 KB (275322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7dc40050b48fe038286a26b8fe1e43d7b0d85016729b04b2518c016e46fde7`  
		Last Modified: Thu, 10 Oct 2024 00:01:22 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57c0001b37be8dea091b321732126672bdedfaeb39368b318087f11c0c90797`  
		Last Modified: Thu, 10 Oct 2024 00:01:51 GMT  
		Size: 311.4 MB (311423212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0e7cbfc99b337a9ffb3341366265172beed65d2b8ca6d3bd8416668ed5b181`  
		Last Modified: Thu, 10 Oct 2024 00:01:21 GMT  
		Size: 92.6 KB (92577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5705a0f992c0f4cc1647f168fc23c568d9b88b8a3e0f1053828ac691c86fd`  
		Last Modified: Thu, 10 Oct 2024 00:01:21 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbc2fff3a115ac1019728800d4585dbefb62e76072ce6bb6f07d16ba99ce320`  
		Last Modified: Thu, 10 Oct 2024 00:01:21 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b71521c11632e8ad08b1020e7bcbf17ba97c9dc08fec213e8dee2f4fb37534c`  
		Last Modified: Thu, 10 Oct 2024 00:01:21 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
