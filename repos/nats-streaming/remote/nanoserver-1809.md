## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:42ad5faa287997d7c3bc1db6f877c808fe82bc27026b5b17fe437c2f50a41902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats-streaming@sha256:8d785c77527708a37ad3a3c38ec23a19021cdea96572c58dfe069c16aa124f70
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107075754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5e535687839c51413e680943603c070456f08a0db0c8194ae1291ceded674b`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 14:50:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 May 2020 18:55:31 GMT
RUN cmd /S /C #(nop) WORKDIR C:\nats-streaming-server
# Wed, 13 May 2020 18:55:32 GMT
RUN cmd /S /C #(nop) COPY file:d30725f7225d14fba35e88513adf63da18fc9fef9c4f6c817dff8f784f19a7c1 in nats-streaming-server.exe 
# Wed, 13 May 2020 18:55:34 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 May 2020 18:55:35 GMT
RUN cmd /S /C #(nop)  CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eafb3f3d63d93b402dfcc428e091787a4242326bc71283a6e3ad40046a60cba0`  
		Last Modified: Wed, 13 May 2020 14:55:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a74b9fd11c319df04c6246ce8c5bddd935b1beba8c38310daae79df9cdc371`  
		Last Modified: Wed, 13 May 2020 18:55:59 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6850f8b285fce6d37decea5c8b278319e3688739a4a812303f96b5a3555d57ca`  
		Last Modified: Wed, 13 May 2020 18:56:01 GMT  
		Size: 6.1 MB (6052119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f91c2f8b5a2fce9e882ec86eee6e420a44c99a8cbb1860d3307db0a7b3fb252`  
		Last Modified: Wed, 13 May 2020 18:56:00 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0f6987c347315d6587f87ab1b88f058914661055debc062e1daafb8dbd180c`  
		Last Modified: Wed, 13 May 2020 18:55:59 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
