## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:49ab1961c5a2a6b46189bbc058e1f108a656e585ab3d3fd4029cf33b2391fe4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:3a0a546e8a99a2706a6299068d8db887d6b7b2b21a4ad96ed6914c88351c78e1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110277530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542e10133cb9ba11753b6a63909dde6df6c0259ea64df1c8dee33f98663bfa12`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:06:47 GMT
RUN cmd /S /C #(nop) COPY file:4da0f8234ade3a140b7c5ab7aad542163d11d3bb3b44e16168afc22293437b5f in C:\nats-server.exe 
# Wed, 14 Feb 2024 21:06:48 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Feb 2024 21:06:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Feb 2024 21:06:49 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Feb 2024 21:06:50 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be50efdc684ee93a4c2c9ca2ea13d91020024293d5fd3d34e2cb5702d55bf2f`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 5.6 MB (5649835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3b6b1351e329bee1329ec3ba580885f65b310a1b7326a7fbbba5d5957ea69b`  
		Last Modified: Wed, 14 Feb 2024 21:11:14 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5bef0d7c9c5f45f145a4f398d28b0542e60aa4943147f6f2075fa9e974a573`  
		Last Modified: Wed, 14 Feb 2024 21:11:14 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea52894b9ecfe0ef1ad870f2c8a76569973bca0a4c345709a5c3d1006abf38d9`  
		Last Modified: Wed, 14 Feb 2024 21:11:14 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb03e404fd9173c4103a91d7337e9d049b54f9c0928b7b4f71e3d1063690799`  
		Last Modified: Wed, 14 Feb 2024 21:11:15 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
