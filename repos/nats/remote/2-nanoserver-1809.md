## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:57c95a4019f74c260f06f9db81db80a8ee6251cc783f779429765a73bd7b4324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:5f5322bba05b71576e20f209c4b340bd995bdcc31a29a5e40f898e03cd2d591a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161299217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ed26b7d3e8ce4cc01b1be218c7301f56f4ed9c1cef651493d28a2a6204f2dd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:50:12 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Jan 2025 17:50:17 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78be4d7c7554d3cc03be58653079e805ee14881716e7be4da21ed08dc92aecf`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a53c7b6ebfde3e19109bda127b7e6dd65afe79e4f181aff08978e4eeb4f5f35`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 6.0 MB (6025790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43d64cb96be0aa298d48a5812e2c3932f539ffb951d2c5b686e9d942b3ad671`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fff7bbd5ae2661700128fd04b604cfb063ecfefd7316d5f3f135990a00f5f52`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaab287c955c223fb7639ef1c45f7ee8e6cb71fc27b5392944fb1ee749e7aad`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6ccb426c9a0f0d72f25a723f8c4cfa93a19577d1cb7d21fd99203d4720936`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
