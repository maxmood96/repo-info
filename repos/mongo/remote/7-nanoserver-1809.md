## `mongo:7-nanoserver-1809`

```console
$ docker pull mongo@sha256:01b1cabe826a209abfb15df53f9cc8a31d928caf41cb832d0c1957ecb3793870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `mongo:7-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull mongo@sha256:2ac2b72a4997374d330bed4743e9e893828d00dbda02108032cb8f3af2ae1ec1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.8 MB (720769569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d194d1968622eac7f424fa3098bd28d64fac8ff59a1faaf3985ff983d655a011`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:17:00 GMT
SHELL [cmd /S /C]
# Fri, 18 Apr 2025 04:17:02 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:17:04 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 18 Apr 2025 04:17:05 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:17:07 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Fri, 18 Apr 2025 04:17:07 GMT
ENV MONGO_VERSION=7.0.19
# Fri, 18 Apr 2025 04:17:44 GMT
COPY dir:9c112edd2ccbf73f54eccbe10e51c93e720a60d4adf79e8d4bde4396b3fc6121 in C:\mongodb 
# Fri, 18 Apr 2025 04:17:52 GMT
RUN mongod --version
# Fri, 18 Apr 2025 04:17:53 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 04:17:53 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 04:17:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff37c9096f8e7f68234c0eef85b95cd7c09c16c7d2a74148a27ef02203bbd7a`  
		Last Modified: Fri, 18 Apr 2025 04:17:58 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a68d7bc6da0cbee87ef177c1825cd029358c1dc7cc49c48c0a28891615cf3e`  
		Last Modified: Fri, 18 Apr 2025 04:17:58 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78891da01fbd1d9dd755f2ae0ff2c765e07f467e6885acb95907c0ac8ec89f78`  
		Last Modified: Fri, 18 Apr 2025 04:17:57 GMT  
		Size: 69.5 KB (69511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8eb9c65dce76ca53091b17a3784e9e7353ec118648719d27480858380c20c8`  
		Last Modified: Fri, 18 Apr 2025 04:17:57 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa80cfbe02b93227b9307a335b5ddd58271f260f3b1ce83ab0826960c0b37f6e`  
		Last Modified: Fri, 18 Apr 2025 04:17:57 GMT  
		Size: 275.2 KB (275159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038726ff27b5302f5e58a489fcd85bed24660e8ec2c667f87c462fc932fde5ff`  
		Last Modified: Fri, 18 Apr 2025 04:17:57 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50ba0981e77647b97d100fdb2b0e4d44f721846b8895634ba89540e2ffa1057`  
		Last Modified: Fri, 18 Apr 2025 04:18:44 GMT  
		Size: 611.6 MB (611592134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e933b613384628865ad191da28a9ef336615d3d5b9e775c6d8141d1bd6c2f55`  
		Last Modified: Fri, 18 Apr 2025 04:17:56 GMT  
		Size: 73.2 KB (73240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a80da2c86947e53b450caaca03ff68c4ad08e9c51d18b610ff01ca01ebb768`  
		Last Modified: Fri, 18 Apr 2025 04:17:56 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af6c1098c68daea4b61fc7c45f8dea8bcfe15fcdda7a03b33a632262e26891d`  
		Last Modified: Fri, 18 Apr 2025 04:17:56 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a9d6d73de5cf76e38a2aaf7a3257597aeb7c5cc03da0cf8d423603a75b7a10`  
		Last Modified: Fri, 18 Apr 2025 04:17:56 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
