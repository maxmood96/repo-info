## `nats:nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:950519f31ba604e5d89f5b7abb1aa2dfa10b04b00e7559e52cdaa0c5f077b564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cb08882db4f97531b99bb40e1ad43592e424ab9662ecea55270c3ffecf633dcb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129203884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61086a00f9a7a92dfa03e67a1cbbf4008ae7ccc07a75624420edbb3619dd750d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 22:08:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 22:08:09 GMT
RUN cmd /S /C #(nop) COPY file:1b1fcd7178cea6fb7bddd5819f166b3d91e649d03fb0e35c6dbd25342d3cce79 in C:\nats-server.exe 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 22:08:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 22:08:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7cd3ced6244771a57adebff75df542330263be15717b8587eba0706f05d7ae`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea961252df9f370c252dbfadee42af63576ed2d527908ff835809cc7d4ebcd9`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 6.5 MB (6537756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd26970cfc15effd40419fb02a46ab6251ac71d1f57a87ac50cb97785d8e005`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ad27018f963f0407bf1089ea2832e29f710b3b9678f87dab2d2d8fa5c6a05`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6a8b7a39d3531b55385b3be93ea1870b677b2f6ecc487a9aae86add343b599`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9fa7fe845651dc2aab94e869ad57b16a5ba27fd764eec87d90ab31376785eb`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
