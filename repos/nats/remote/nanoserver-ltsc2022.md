## `nats:nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:4b5bc1dda10956fffbd5637c74ca36f1f8e8999841816091381b80f7f4368b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ad9de8f09f3634777b25adb56728db4ae6804eb3e93cf167d338af2569150272
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129178975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e567374bac2065f94b8560a0f1747b427e881b5faa654919d1f7abccc554d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Thu, 14 Aug 2025 18:14:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 18:14:05 GMT
RUN cmd /S /C #(nop) COPY file:3fa3039439cf4074860757aeaaa6c458fcb2a8fd53320637e2edb93570462bde in C:\nats-server.exe 
# Thu, 14 Aug 2025 18:14:06 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 18:14:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 18:14:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 18:14:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dd762bbc2519848d92e4250ffd2e8ad506e67e2ccc6edb8b28deb7bd6a4cc3`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8303cc1b67f588378cd15d48f0f9092ea5f9e1d8e2832d99a509bdd9c8ff70a`  
		Last Modified: Thu, 14 Aug 2025 18:14:54 GMT  
		Size: 6.5 MB (6512850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204fc3573607851e777581d8f3393c06877a1b385138e9ddb562e41c44ae04f`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e67cadd8e8c18aa9f537c4147610482318cb56ca5e6a1ff3cff5d96e4cfc`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b880e68edcdaf39200bd33cc61fd60fab56c1eae85a872652a20730da3d12a`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbef80910535149a3762e6bfc014c51084a8c11fa366889b246185411c39fb9`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
