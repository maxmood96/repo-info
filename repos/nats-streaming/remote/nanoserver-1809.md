## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:342af7a76a4817b4daba3e8a86897a80277c73b3710d9803c83b9476383ab389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats-streaming@sha256:be621af34ec3e46ea4c5f9f5749b8310430fda30eb643036ae77e9a1023b2e54
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106619719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669b7ec70426c846ba6709d8549865a56fcaba1b652b0ef77ddb74861632ee6c`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:31:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 22:51:08 GMT
RUN cmd /S /C #(nop) WORKDIR C:\nats-streaming-server
# Wed, 11 Dec 2019 22:51:10 GMT
RUN cmd /S /C #(nop) COPY file:d333dfb9aa0fca02ce2e2300447082af645803b49703ee1671951f7dba266042 in nats-streaming-server.exe 
# Wed, 11 Dec 2019 22:51:13 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Dec 2019 22:51:14 GMT
RUN cmd /S /C #(nop)  CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0591285374eb5389845162a5833b3c4604d58ef1e79438fd4b95fa89f87e13e6`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e482770a9db5a664ea26ee2d70e8dcce77222c397c4a7e014f17d98a06609b53`  
		Last Modified: Wed, 11 Dec 2019 22:52:28 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e890d3a0ddea00dc56a882bda5ab113766a3e658cc61e3873a7da6d140d783`  
		Last Modified: Wed, 11 Dec 2019 22:52:28 GMT  
		Size: 5.5 MB (5509670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942c2a594c04ad12c8654be2573b2451ce4ffe95d263c24e690128f683d1e9d5`  
		Last Modified: Wed, 11 Dec 2019 22:52:26 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0cb119a2df1996d9a2c9ca4538f4cb058ea904dc99b32157a332c8449dcbf6`  
		Last Modified: Wed, 11 Dec 2019 22:52:26 GMT  
		Size: 928.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
