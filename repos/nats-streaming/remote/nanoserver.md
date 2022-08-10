## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:2b6e1df0730790dab5769d15ddb8c565b72ae5933c365e5ead162256b496dee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats-streaming@sha256:1e75ed38b6e5d1f1226c472d87ee536bae0dfc56e51a21de753c6d28c4b4798b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110484578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aabd967e2925095a30014bcd38e3694a4d4e1716957146b9133ac9e0bcf561c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:30:21 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Aug 2022 18:15:32 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 10 Aug 2022 18:15:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 10 Aug 2022 18:15:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 Aug 2022 18:15:34 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a5df16ce106b092b5399678da04735c18584e4f99ea301691eb433072953e9a`  
		Last Modified: Wed, 10 Aug 2022 15:31:14 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a94c253a1d914893c796a96365b2c23395a7f15e97f35bce6013eb5fe86ee4`  
		Last Modified: Wed, 10 Aug 2022 18:16:17 GMT  
		Size: 7.3 MB (7275823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d807931f2cf3744980380ec807e58e997d09e581d7844efd5f5734d2046dbcfc`  
		Last Modified: Wed, 10 Aug 2022 18:16:14 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6ba290a45e01a5b5539d6350045bf882c6cc08edb8ed5cd6cf0e779a769eb3`  
		Last Modified: Wed, 10 Aug 2022 18:16:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8f6106ff00c4eb005f80d6f348130330b747f691057d8a43468d4398678fa8`  
		Last Modified: Wed, 10 Aug 2022 18:16:14 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
