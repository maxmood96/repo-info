## `nats:nanoserver`

```console
$ docker pull nats@sha256:decd1f161f484155c8ca7a0c7e99247a35f4cb1b9d297b9f821b6e07246b56a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:ee000864a3122839be74300a01091298092421330414b26a5bd46dd177c45413
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3efb56477e7b9c48586d8290198510d573b31cedd83e0a3ffce9e7e6657e36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 04:01:12 GMT
RUN cmd /S /C #(nop) COPY file:f6f49d606f9f811d8d95cfcbfc0c7db19c139753cf9d4aec8e19ceb60cae5eb7 in C:\nats-server.exe 
# Thu, 11 Jan 2024 04:01:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:01:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf42f1aafdb6016daeae38b38330cdd9dc19c174db9d4af6b68dd916e6eb084`  
		Last Modified: Thu, 11 Jan 2024 04:02:15 GMT  
		Size: 5.6 MB (5616337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c327a7a2c7b1f345092bbe2268b1cae828a27ee468658e4fd8894e7e6e66cc`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba577085c3d41035606a7eea09d46f81aa7b7d70cea80113a9f07d14e31ede2b`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c8f4ceb3d31803fab29316067ffc5129a0d9b9c208f0b52fc86161329769a`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d929e177552db84f77ab4e31fc7399f97d242ff17d7b23874f7ef22d1c912e`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
