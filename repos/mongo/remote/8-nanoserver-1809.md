## `mongo:8-nanoserver-1809`

```console
$ docker pull mongo@sha256:8cc93e744a18e2466e1d0f23c786918ff450a3ee030478661bd4ceb3df68f3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `mongo:8-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull mongo@sha256:2709635b91136e536c0f28256112b2bdc566634bcd47cc4e2fdf70b78bd5b4ef
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.3 MB (920329188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1c3de800c799cf1758504c0b875f602e1ac6680a52eb706ee363e94c92711a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:06:57 GMT
SHELL [cmd /S /C]
# Thu, 10 Oct 2024 00:06:59 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:07:02 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 10 Oct 2024 00:07:02 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:07:04 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 10 Oct 2024 00:07:05 GMT
ENV MONGO_VERSION=8.0.1
# Thu, 10 Oct 2024 00:07:42 GMT
COPY dir:51be3647b815c20429813a5d3bc4dda902965341b9140467cfcf228524b19b00 in C:\mongodb 
# Thu, 10 Oct 2024 00:07:56 GMT
RUN mongod --version
# Thu, 10 Oct 2024 00:07:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 10 Oct 2024 00:07:58 GMT
EXPOSE 27017
# Thu, 10 Oct 2024 00:07:58 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98646b4e7c80ade6aed9976800f9d46c55bb79331d862bcccbc015b1db0db4a`  
		Last Modified: Thu, 10 Oct 2024 00:08:03 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c782014db10cb6a970beb54efb001204714e8eeef81b0e7b9824214b6f5083e5`  
		Last Modified: Thu, 10 Oct 2024 00:08:03 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667e7cdb6848f820a478cb26e95acdfb3748df66a68350879672e043a4bc23f`  
		Last Modified: Thu, 10 Oct 2024 00:08:02 GMT  
		Size: 71.7 KB (71652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78dc0dce07eccc0eff183340aaa89194a13212258f9b1379fbd335b4f9a031d2`  
		Last Modified: Thu, 10 Oct 2024 00:08:02 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afc74c8eb4b52da1a1b0211b74b3f8539c4934f004a833aa63044ae26cb21b0`  
		Last Modified: Thu, 10 Oct 2024 00:08:02 GMT  
		Size: 275.1 KB (275138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f12a4288a153432fdcf79701239bcddcd47a6c96e0c71ca66307b0198d12503`  
		Last Modified: Thu, 10 Oct 2024 00:08:02 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421f0cae51214c7f7cc1d323ae0c66240e09aeabcf21a51212146787a3888a8f`  
		Last Modified: Thu, 10 Oct 2024 00:08:58 GMT  
		Size: 764.8 MB (764795192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fbdd0524a460a88429baea8de4f18a39df50dce75eccf94a88cbc258a339ed`  
		Last Modified: Thu, 10 Oct 2024 00:08:01 GMT  
		Size: 86.3 KB (86329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71f376a12f6d7ba4333f18afc2746437d17bb5b51e7cd1cb7451b41b827c513`  
		Last Modified: Thu, 10 Oct 2024 00:08:01 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4c93b4ef6492c50a91dc11db3ad71e1e6eb9a27b73e0dbfebcb9f64660476d`  
		Last Modified: Thu, 10 Oct 2024 00:08:01 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650e529c3a2b4c8cbfd8171b31c065db3cca50f8c3f2537693ce5881c5850228`  
		Last Modified: Thu, 10 Oct 2024 00:08:01 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
