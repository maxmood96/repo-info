## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:d096f3f3d31616a4d6fc218ceb95c3ce3edeb9f49aa9d94ff5733cdcd272af52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:95c23b528ae63d7a3ae7dd6faf7dc8187ba180b2aa14a066899ac7f4c1987a93
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110081754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd1a8131a097d2ee296a38a01f1c241b131694f7b6578bcfd45b02461c27f07`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Oct 2023 00:17:47 GMT
RUN cmd /S /C #(nop) COPY file:56de93ec6afaefd5f19b9effd4409842fdfa695280fb05da230b1d12a03db7bb in C:\nats-server.exe 
# Tue, 10 Oct 2023 00:17:48 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 10 Oct 2023 00:17:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Oct 2023 00:17:49 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Oct 2023 00:17:50 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b582b38db97cac5cc3e57c77b5d05f6ea002245efc38b39a8053018d8a1ce5f4`  
		Last Modified: Tue, 10 Oct 2023 00:18:51 GMT  
		Size: 5.6 MB (5582805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff0f4846850d65deffec92d21093ee6acf7b6b503a3ea4221f87a380d91a7a0`  
		Last Modified: Tue, 10 Oct 2023 00:18:50 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301c707e5250a85e17659b78c1db30c335bec94c0c0bd7a818fcb0a6583d55fc`  
		Last Modified: Tue, 10 Oct 2023 00:18:50 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627bea45f77ba997e19bb1949f5df191f9d509c1ea16719127c6e19bb098fd7b`  
		Last Modified: Tue, 10 Oct 2023 00:18:50 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b79e3d622b62528849dac885df8d34f46c255bee1103d7225bf02eccb74691e`  
		Last Modified: Tue, 10 Oct 2023 00:18:50 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
