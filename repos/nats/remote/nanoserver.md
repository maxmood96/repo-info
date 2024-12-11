## `nats:nanoserver`

```console
$ docker pull nats@sha256:f0e492514748529a5d7d0ce2efc7f2dda4c0f353614f55fe6a866e1c09a2a9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a3bb6c91e3449cbd30540fb2490a5c003eab807abff5723c05c3c9fc255140d7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161246960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5750440207dbaa7aa1a2d07ababb79c735ac51e214e16c91d227f19f1aef88fb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Wed, 11 Dec 2024 00:27:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:30d04105f2ee103eeaefb4dfeda74eb010a83b5e5fa9197d530ae8b0c97bf56f in C:\nats-server.exe 
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 00:27:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342c7f2f005a3ad1d681ab2ca14dc1ea4c2733d5227836c6af61c7767a24e3e3`  
		Last Modified: Wed, 11 Dec 2024 00:28:03 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f803c64951e363e8bb6e13fc56e77d3bd1d9097615ffe352b24d544ddcd14e`  
		Last Modified: Wed, 11 Dec 2024 00:28:02 GMT  
		Size: 6.0 MB (6026775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19e8e4b929fa87b385d81646b8abc8268e33896c609eef70f7c1e00a1f6a72e`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e44ab9a12591fa447b36a9be3edbdff717f54bfd33730388a91cba21e9b7b`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74b942460a0488783b56ec5d5e6e791000eec5f5474d6f61223331815d524f5`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5034f809175db916849c3fb45d58ee4bac77cc8ec00e5fbc2886451da153972`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
