## `nats:nanoserver`

```console
$ docker pull nats@sha256:bc0de37758065df1fdee1d3eb9b083525094efda302ac2b97beedd8b0e4277d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:09b474519b02def21c913f3a3d593e0abe2ab316a543289a069840061c7f8d41
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112952027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edf9e0600c446bc3c0a2a074319fb9a6e73ade269fdbef0cf1a7752c64a3895`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:14:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 01:14:16 GMT
RUN cmd /S /C #(nop) COPY file:acc152dfee9c5ddc38d24e3c08e54d57b0488af147b7d3bca35c3b0e9cd44184 in C:\nats-server.exe 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b4be985892cbff5859ec15f83fe1e9f9ed395059ed0e19fac5d71580b8ea28`  
		Last Modified: Thu, 13 Feb 2025 01:14:25 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a66cafcad785d7bacc02b7f1a5b4bd5680265969297b75f9c944d55c5bf132f`  
		Last Modified: Thu, 13 Feb 2025 01:14:24 GMT  
		Size: 6.0 MB (6030535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec61010dcd23b9212494167cc57412d179fb3808ad619346ff806e8b1122c4b`  
		Last Modified: Thu, 13 Feb 2025 01:14:23 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e6a84b10a4fe9377faf5481f4a4e454e66ee769b9cd93f52d8d41216ccb931`  
		Last Modified: Thu, 13 Feb 2025 01:14:23 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a33e1efb27f4723e99b6ddba1c07b8f673336f30f347cd7055bcb20e6bb8f8`  
		Last Modified: Thu, 13 Feb 2025 01:14:23 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f94af37d86ac27dd25a6e4901ef0e0960adcbc3bf6bc840fd5a8bc84a6dad6`  
		Last Modified: Thu, 13 Feb 2025 01:14:23 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
