## `mongo:nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:7a982b75a990a1d56e4e432608cb6b40a82619d544f260936e03a5d663de8504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `mongo:nanoserver-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull mongo@sha256:29fedb6a717fe2f9131590745b5f239805d718b63c943e7878e1af8d46c030d1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **890.5 MB (890527826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665ea7fc076742955ad459a57130d838ea0bb37b77eda531cb8fc489b87d2758`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 03:15:54 GMT
SHELL [cmd /S /C]
# Wed, 09 Apr 2025 03:15:55 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 03:15:58 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 09 Apr 2025 03:15:59 GMT
USER ContainerUser
# Wed, 09 Apr 2025 03:16:00 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 09 Apr 2025 03:16:01 GMT
ENV MONGO_VERSION=8.0.6
# Wed, 09 Apr 2025 03:16:26 GMT
COPY dir:47addd2041f238d9b83e7dd713c01f98ea55ed04233b1ceccecea9b019529183 in C:\mongodb 
# Wed, 09 Apr 2025 03:16:51 GMT
RUN mongod --version
# Wed, 09 Apr 2025 03:16:51 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Apr 2025 03:16:52 GMT
EXPOSE 27017
# Wed, 09 Apr 2025 03:16:53 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7412dc27956b6a348c71c329845a9bf72b477248c9cf4f67232bea7f5313811`  
		Last Modified: Wed, 09 Apr 2025 03:17:01 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777cdee54da9ead50a4b40e0a370e86508e520663a951ce760532f28f99f807c`  
		Last Modified: Wed, 09 Apr 2025 03:17:01 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4f896424d34085c629a020b7475c93e0a7382a3869e6ae14a85af625f977af`  
		Last Modified: Wed, 09 Apr 2025 03:16:59 GMT  
		Size: 76.4 KB (76363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d1c74171cd9253cd21729e20e152b9a9ad3f2e66e912dca98fa436c82d3243`  
		Last Modified: Wed, 09 Apr 2025 03:16:59 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9497fa7e1713dbcd622063c437228a31a88c8f0e45f0bd49bdf28fbcbd3a111a`  
		Last Modified: Wed, 09 Apr 2025 03:16:59 GMT  
		Size: 275.2 KB (275154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b75867a011dcd908f9f44e4ba3a074baf2b91da06c4c4a3ab606bd87b1ad1f`  
		Last Modified: Wed, 09 Apr 2025 03:16:59 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9e4451b3203234c749e760190a493dc3aedc78144ff9ab6f0454216fb66965`  
		Last Modified: Wed, 09 Apr 2025 03:17:56 GMT  
		Size: 769.3 MB (769341707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc1cc0d2384e1ea410c5908291cb2e2a171da62bc768e46c8eab8ffcc0f67e7`  
		Last Modified: Wed, 09 Apr 2025 03:16:57 GMT  
		Size: 91.1 KB (91095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b6a7af2e9e3a54dec4a1001c7f8e57e243a4dc323639cb8d615f6685ad5894`  
		Last Modified: Wed, 09 Apr 2025 03:16:57 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38929dfc0c67333e519a07dd23b93b842f68789bd471efef2014618151840b35`  
		Last Modified: Wed, 09 Apr 2025 03:16:57 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909c08f121383f183b16088afe4cd294abaf622e3cab8b440eede7d72c81432b`  
		Last Modified: Wed, 09 Apr 2025 03:16:57 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
