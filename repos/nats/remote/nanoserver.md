## `nats:nanoserver`

```console
$ docker pull nats@sha256:5762142a7f15bd3e97dda219ec3985997c351ce00b39dbfc9a771e735ecdce49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:aa92b18c4aaa8b4a86b817c76c7879136117bb5f6e506cd57b2b407612ce8ee5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da025743137b99ca37782c7c65b87197d643ecdd42e7210da78e20f218769df7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:40:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:17:52 GMT
RUN cmd /S /C #(nop) COPY file:8e415274f0a16ec3fa03a87478f007a6a8ede142612bbcd4aa265fef9c8611e4 in C:\nats-server.exe 
# Thu, 17 Oct 2024 22:17:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f6a46f1af9b261dfa3ca4c23edabd47ada1a0c2242f883f8fc4e82d0e08abf`  
		Last Modified: Thu, 10 Oct 2024 00:41:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ede2810b9c7050684298f17d5ea9f7733eac55d920c1a344403c3a47adec223`  
		Last Modified: Thu, 17 Oct 2024 22:18:39 GMT  
		Size: 5.9 MB (5870144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6fdf5dc8052b24e56cd315505d0c008ec1aedadf4826d83b7c970cea8c887a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038bfb23519c0926ece84c8e7e5d34e03f7a0722a552518de0ddb674adb4806`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514425d814a52dd1a55dd2a61bceb51b7700a3e740c02b0abffd877c7dfef55d`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f9d7551799d2a32fab62c45954fd3d568fa4f52ad0dabe4670e12c857e87a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
