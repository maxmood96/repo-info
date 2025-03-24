## `mongo:8-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:b3fb4e35dc8b6b089a0b7587af7767d826e8f7c04745991d5c33b2b963fec3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `mongo:8-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull mongo@sha256:19625012350f608eb08635e946e00e040a99a1ef82fbab4cab28baddb12ca4ea
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **890.5 MB (890497955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552a201140d0434916ad1f372407f4f94b76ec2b5df0823b9c092dd770581bd7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Mon, 24 Mar 2025 21:49:38 GMT
SHELL [cmd /S /C]
# Mon, 24 Mar 2025 21:49:39 GMT
USER ContainerAdministrator
# Mon, 24 Mar 2025 21:49:42 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Mon, 24 Mar 2025 21:49:42 GMT
USER ContainerUser
# Mon, 24 Mar 2025 21:49:44 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Mon, 24 Mar 2025 21:49:45 GMT
ENV MONGO_VERSION=8.0.6
# Mon, 24 Mar 2025 21:50:10 GMT
COPY dir:47addd2041f238d9b83e7dd713c01f98ea55ed04233b1ceccecea9b019529183 in C:\mongodb 
# Mon, 24 Mar 2025 21:50:31 GMT
RUN mongod --version
# Mon, 24 Mar 2025 21:50:32 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Mar 2025 21:50:33 GMT
EXPOSE 27017
# Mon, 24 Mar 2025 21:50:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2304c76a960242ca20104ef8da8fdd1704e9420fa4399a8c43cfeaca63d95f52`  
		Last Modified: Mon, 24 Mar 2025 21:50:38 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacb13a7d920394d688e7a428e7c6fc78ff4de692696faccf1e2934fb0eb6bb6`  
		Last Modified: Mon, 24 Mar 2025 21:50:38 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a89116caf6e503023bcffe4ec2046aa8049bc32be9ed336b3da2ec4138835c`  
		Last Modified: Mon, 24 Mar 2025 21:50:37 GMT  
		Size: 78.1 KB (78084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65802e98c743bd19592d30f6e4e6c11e9279e5dd4abc4d86fb1eeadb06353398`  
		Last Modified: Mon, 24 Mar 2025 21:50:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8138af8c5a4ae9f8249179d73c951585b6b2b98ee9c75efdedb48081a68ea`  
		Last Modified: Mon, 24 Mar 2025 21:50:37 GMT  
		Size: 275.1 KB (275147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefed8b57c98a5786f05c4bb4715680ae445d225c2f796ac83240b0f3e226d83`  
		Last Modified: Mon, 24 Mar 2025 21:50:37 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7190a26fde567f1e7d686196d94b5b910869a6c0aaeb39ad783e4ed1445c0fdf`  
		Last Modified: Mon, 24 Mar 2025 21:51:35 GMT  
		Size: 769.3 MB (769341626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2561dff88d70fce471acc1fb764b07832d859d0c6afa091aacfd3df72fdb5cad`  
		Last Modified: Mon, 24 Mar 2025 21:50:36 GMT  
		Size: 100.3 KB (100305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0fb933cdb5418a9141b8e9e6f142f6a897dfd5c55367edd4d665a32241c865`  
		Last Modified: Mon, 24 Mar 2025 21:50:36 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5edbb70227fe61383b589e454fdaa6555d1ca427cf791ed6e1aa10ba41f58a`  
		Last Modified: Mon, 24 Mar 2025 21:50:36 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f12e954e9cac9ad7ad5a9d1fdd247bd6b2d9cabb8726b9e7f0d93eca50d17e`  
		Last Modified: Mon, 24 Mar 2025 21:50:36 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
