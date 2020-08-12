## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:687e2e9d2a37d8697ee65d4a50e5afd58fa5db82f2750ab60ba88dd2ee6ca0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:fab4ee5c94bd9c5b51af3443a5e1256a21fbb5c5ee86a16019a9a829d595cc5e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105046160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df67809471568873f0b55fa2d9279ecd2de972502b1adce9bf5057aa042eeca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:37 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Wed, 12 Aug 2020 15:13:38 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:13:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf155fe2305c82a23507253332f17d7aeb14c022ac7a52f5155ae5aa5de1d45f`  
		Last Modified: Wed, 12 Aug 2020 15:17:29 GMT  
		Size: 4.1 MB (4056411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4d108e9f2e737a24742707fdf007fe8f7ca13bcedfd9129b96e0e5479628da`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74184b55b68844992dafa04e9428b3ee68812f3aeccaf54c77110f259dc95818`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053c0906cabdee780b68928e7fe89c9f700cd0b67b45da2e0dd16565fa396749`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 834.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc6a501b122f4b08c277b1526120f7c530e499393cefca21279714f60aeaf2d`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 830.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
