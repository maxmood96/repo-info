## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:3c256e2ee885661142bcaa18286f62d5bc0cceb00244b881e044c0e2c6836ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:dd30ab77277b0920d382b44be742ddeb050190940b4c6ee85db0313d26fa1756
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160942866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad0d23d9c98fea62ed0ca323a5e5f13a7cfb0062b0f7cbfd03d79dac249bc04`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:41:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Sep 2024 01:41:02 GMT
RUN cmd /S /C #(nop) COPY file:c54cab0bcb90d215c31a13829d36e0dab6494e8460be22ca70c4e415081fe7b0 in C:\nats-server.exe 
# Wed, 11 Sep 2024 01:41:03 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 11 Sep 2024 01:41:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Sep 2024 01:41:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Sep 2024 01:41:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56238ef630ea819f3bf5690628ac46f909bf2db26027a52788070368a5bc5c9e`  
		Last Modified: Wed, 11 Sep 2024 01:43:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b90d1e6a7ceec79c827a01c14a37d6df290b1de68d6a034f3d889de3ff115b4`  
		Last Modified: Wed, 11 Sep 2024 01:43:28 GMT  
		Size: 5.9 MB (5856096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca900b4e1c65031efc114fc747953e96ccf0cce1694295712278b467a77835fb`  
		Last Modified: Wed, 11 Sep 2024 01:43:27 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b8d8553e0501c714d2376a06dea2a3af180c9ac140a972447e854097317fb7`  
		Last Modified: Wed, 11 Sep 2024 01:43:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38add6ec9ca2315037f7840a93a8d5be3db3f2d00e6155d5780a36924e59f80`  
		Last Modified: Wed, 11 Sep 2024 01:43:27 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf771d3ff063b3aa1a5b343b26ff7ae969969fc9cefcde202e1ec09f8c423ea5`  
		Last Modified: Wed, 11 Sep 2024 01:43:27 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
