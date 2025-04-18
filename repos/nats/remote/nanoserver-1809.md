## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:714b0b324ae5c514cc8066861c1ea58b8e852b21686bd57938b4cad501106b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:70dfa0a823409d278307a2f602a989bb5088fc2ed408add1628e7026065e4f7f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115214035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10544dab15e09a82ee58dfe65c5cebe6e37634a0fc0e40720019d69e49ec056`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:11:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 04:11:40 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dab9cfa2f7ef2b19e95e68d27e3d0b208d9016da1b04298c500e78281a15e7`  
		Last Modified: Fri, 18 Apr 2025 04:11:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0b032347a8dcb65e359d04c00733934bf6cfe61db4b1142a1df5f3de23a9cc`  
		Last Modified: Fri, 18 Apr 2025 04:11:47 GMT  
		Size: 6.5 MB (6455931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b3350d5c31834bcca73478d5fc7c0d3c546c1676c042e1e9d1ec9afc85bdd`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658de08330e9b739dfbff680b38b2bb55dc4b4aec6d4064b19ecc24c7ba9a8aa`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0312f657691b722f56e7ed6bc33b2119988f7f21d9853fe0a8dcc79a3b5aec`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fc9ae19d64bc742bb97a1eec58e04de0d2eab1eb71186876fed513a4b21a3d`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
