## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:087252d2ea30ea3ab0d89da967572ac8756131b5fc9e33a9fd7617f79a8fb805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:cb7ba5453830fa4b1610a981c9ea36d92c9bbd561bb774e3f71d3a0946fb069f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113368849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e64b4fcd6d57238b7d33408c337f54eba590256714f9cc678625d54943e1ef`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 19 Mar 2025 22:07:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 19 Mar 2025 22:07:40 GMT
RUN cmd /S /C #(nop) COPY file:15d682fe943bd0a85193b4305627addb8f063cba56411dc1ccaeb8a61d0564b9 in C:\nats-server.exe 
# Wed, 19 Mar 2025 22:07:40 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 19 Mar 2025 22:07:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 19 Mar 2025 22:07:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 19 Mar 2025 22:07:42 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a47df565d44873f952ab7728a5895a6c632119200503a6bae0c17b185dd266f`  
		Last Modified: Wed, 19 Mar 2025 22:07:45 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3e8e98c8fd1b0213d5a733ada9ea5c6b40d408aeb3b91ce797a4e34897e94d`  
		Last Modified: Wed, 19 Mar 2025 22:07:45 GMT  
		Size: 6.5 MB (6455270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8589fea82a112e37ef5362b1ba630677a51f968addc6686b3d41b37e33f10d`  
		Last Modified: Wed, 19 Mar 2025 22:07:44 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a369fb2a070a0597d8a5a11a9654c8621968985d64ea6d65ee9e7bb240e1f2`  
		Last Modified: Wed, 19 Mar 2025 22:07:44 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d125157dbd1f36bf2a074381323b4bc9913e6b14204991a68880ef4deafda1f`  
		Last Modified: Wed, 19 Mar 2025 22:07:44 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dd54f60c51551596518b3c12d1860f0748316e9bb73882e9e527530e5171ef`  
		Last Modified: Wed, 19 Mar 2025 22:07:44 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
