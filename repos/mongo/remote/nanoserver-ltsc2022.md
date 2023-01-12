## `mongo:nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:6ac37120d4478d6f5ab0f13eabae7949bf1d1333cef8e571b82fdf2ff6cb1ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `mongo:nanoserver-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull mongo@sha256:c957df9330c46a144a6bbe08701f39d9efb42e22e2e19a1596dba070785691e6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 MB (634498028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4bcca82af0ae116b3f4dc0fa0e247d6f06567a50c5b9ba08910e8176d7f663`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 06 Jan 2023 23:36:49 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 03:07:34 GMT
SHELL [cmd /S /C]
# Thu, 12 Jan 2023 04:07:43 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 04:08:26 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 12 Jan 2023 04:08:27 GMT
USER ContainerUser
# Thu, 12 Jan 2023 04:08:28 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Thu, 12 Jan 2023 04:08:29 GMT
ENV MONGO_VERSION=6.0.3
# Thu, 12 Jan 2023 04:09:27 GMT
COPY dir:504ba3c422010154364f85a9b7f5ebcd0252fe3e628d277d138a4248175996a9 in C:\mongodb 
# Thu, 12 Jan 2023 04:10:09 GMT
RUN mongod --version
# Thu, 12 Jan 2023 04:10:09 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 12 Jan 2023 04:10:10 GMT
EXPOSE 27017
# Thu, 12 Jan 2023 04:10:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:83e9437e818022c1c28f0e07002dd46995c8614e62b9366138fa23b94f43d9ad`  
		Last Modified: Thu, 12 Jan 2023 02:51:06 GMT  
		Size: 122.1 MB (122099566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e0e139d1c09b743fda52fd8a19bdc3c829ac2aed829d2e16beec0fbbd5dd5d`  
		Last Modified: Thu, 12 Jan 2023 03:48:59 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f52222b54787457572d99db7ae10e4c9512dafbe7ba244b0969616e6ac8be1`  
		Last Modified: Thu, 12 Jan 2023 04:40:59 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22763c78aa844e4b52e36432c545ee28797056da12caa5444e6d4a90bef22859`  
		Last Modified: Thu, 12 Jan 2023 04:40:58 GMT  
		Size: 96.5 KB (96468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e4a405601da327afce0142718dcaeaa3dbb5563a90b9abaaeff0770d008467`  
		Last Modified: Thu, 12 Jan 2023 04:40:58 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f9d04bb2d3ad2dae68778ea67f3f38c0df1ce7f74005997a797635eee7435b`  
		Last Modified: Thu, 12 Jan 2023 04:40:58 GMT  
		Size: 267.2 KB (267183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8594303c597f6c215548406a8bfb6d82ef609a2c7cd5170d5458527bab56b79`  
		Last Modified: Thu, 12 Jan 2023 04:40:57 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38554bdb34f922268557822fab20bc35891bc405b7ca81f769d7b6454a85486f`  
		Last Modified: Thu, 12 Jan 2023 04:42:36 GMT  
		Size: 512.0 MB (511967939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35414b753e53b5ce70e5af4a964f9e21dc7341d1276aadb61c0efe11409b72ec`  
		Last Modified: Thu, 12 Jan 2023 04:40:55 GMT  
		Size: 58.9 KB (58911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af2fce620b5fe2434e8a60743b9f1c4d65335a71dd7bb6b4e1a0044b6c2f8f3`  
		Last Modified: Thu, 12 Jan 2023 04:40:56 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e2d6f82f5ed54c16327eb163bdc8a61ddb191de9696a71c406f764cf16dfd0`  
		Last Modified: Thu, 12 Jan 2023 04:40:55 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d783125e9afbdc3ea226dc35619e36e8d4994468357bf8fa39f44ed0898c36`  
		Last Modified: Thu, 12 Jan 2023 04:40:55 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
