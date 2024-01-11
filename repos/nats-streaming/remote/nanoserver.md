## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:d9baff41672286456cb25553f6b3752ff4195b72941e2d751078740011015a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats-streaming@sha256:9040f45949185aa31e9ba6f2ebbee0dc53dbf39d1c2bc1dc9126c5989886a411
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112535314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61246a9f36f2538b44b2683657710097a065db5b770955abbfcec5842cbaa756`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 11 Jan 2024 00:22:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 11 Jan 2024 00:22:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
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
	-	`sha256:a2d99a3500b296e1a4c18f430fc41a7c97484378839749328221a462d6686d73`  
		Last Modified: Thu, 11 Jan 2024 00:23:02 GMT  
		Size: 7.9 MB (7939720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6942b3af1e5d39cd92daf589553d832e60cc4a61e3b822daffba9ca553a8b479`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f48ed9fda722cf6aae8ec7922efb1a64a1082ec4e59f3102d52e7e23fdb052e`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8282b138066213461dc4281e25ce96528b046ca517df50c831315e1c9c44965`  
		Last Modified: Thu, 11 Jan 2024 00:23:01 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
