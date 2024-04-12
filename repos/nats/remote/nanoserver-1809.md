## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:c4e93178913a7dc9281ab1eb2774ebb54399e2457abf80cc1603c25ce3a3ac46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:6462b474ccb2befee7bff17ad1d24d5b03466a468d3c42b1bbf56c6e89187aae
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110565865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71480a424d6c525980b2f098eab78e6a62d184e05386b520da1ecbd08383dc1`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:43:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 12 Apr 2024 00:19:28 GMT
RUN cmd /S /C #(nop) COPY file:d87795d159e46999757150e2d8f7e66e8f209e1e618883dfa828c7749f3fafe0 in C:\nats-server.exe 
# Fri, 12 Apr 2024 00:19:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 12 Apr 2024 00:19:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:19:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 12 Apr 2024 00:19:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d34fcda621b296890090998100732b227a2fded8eee4d47e58e23e4a707e0`  
		Last Modified: Wed, 10 Apr 2024 01:48:21 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90de70e7302ec7786910381f2b5b3d2e8585b6156128c0446c93a0465c753d63`  
		Last Modified: Fri, 12 Apr 2024 00:20:38 GMT  
		Size: 5.7 MB (5670339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e304a6f89bdb5574fef3c36fc94f61b613c113aebe7abdc8e20dbe4145acb6`  
		Last Modified: Fri, 12 Apr 2024 00:20:37 GMT  
		Size: 1.8 KB (1779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92a705d8ceb8ba665b82a6ce09fb8fe2c7aaf2ae6eb30101c7162ccec66cceb`  
		Last Modified: Fri, 12 Apr 2024 00:20:37 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0341083f34c34b30ad0e4d33279fb0cb7113da7cde62d4040539d3509ab5f8a`  
		Last Modified: Fri, 12 Apr 2024 00:20:37 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2469b6b6bf1104a6ceb2b1e457a3f0f4c3ebd3774fa3aee88c3d5a0a4fd456d5`  
		Last Modified: Fri, 12 Apr 2024 00:20:37 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
