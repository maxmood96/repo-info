## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:070f9e269bf92f0bedac63b5a0f269f7520ad54e071f7953b5c35621160ad025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:af099d0ad09f68427f6716cbe03227c5409000f9021c92a4981a6099e9901dc7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161090154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23925b656567c9ef8ee2bc478e0ada3269421cc962f905108b7ac70bfc5d2f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:26:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 21:26:11 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 21:26:13 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 21:26:14 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c935cc00e1acf8d3769c81d23f3134507c1149593f2af1de160f98fd769e3`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb87536f0d2cb71d86892dcf0a7036c92d682cdf7e3a8dadda31d9569a62118`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 5.9 MB (5870083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929a1f4fa9be7e6e28a451ae8e437938d70bb70ab75539f175ac46be518d2292`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d64f781d33814e56a5a3e633b6778e34fb06d03ee0cf92a7b1931ffea43af5`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f881ff7235bc92d60a608d0336719df84a7f2a45c17ef58277f678e69e3acb1b`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d5e5b49ab6c4788712962e67498e176b4fdb803f692b97a96580ca87f612c`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
