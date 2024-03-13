## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:38b381e6f2834d3c5120087f02c9d13f238a2142f54568a208fa74d554bb62d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:1bb4572909b97a5aea3e76230e9d09a1078a21d41ba7000bd5afbe5225fc1568
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110290182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a1f3d16c6f5aea885d55ec76e40c984ca8763448ae4b9b424ec4d5bec24fc8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cd82df1e1baf71960c98c3ca3996de090e25ce522c16d07628ea7705a1c7b`  
		Last Modified: Wed, 13 Mar 2024 02:26:26 GMT  
		Size: 5.7 MB (5663658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce47417df81557c57ff79790516751ae140155b5d06e2f8538fcf4d7e94a1004`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c07d5748899da1f68ed98e7331fa02c4175552921ad31f2ec6ba40f208c69d`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89220da9dce87f2d7ea149e170563fa7bac7ae732a1b8c89f51d60e5da18020e`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78635ce16de8337563a88c3a78835fed97c207dc9254d2dc0d06594b9926b0e0`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
