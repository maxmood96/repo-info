## `mongo:5-nanoserver-1809`

```console
$ docker pull mongo@sha256:ed3980fb23fc9ebaf4d9db65b9658f72e96acb2ff41779fd39e7f96a2ea7aab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `mongo:5-nanoserver-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull mongo@sha256:59dc7fcea79e10e6487028e7dbe820396f96068e02b9b969e6826c9d0c365474
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.4 MB (417369391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8a99370e7ebca3b8b8b1a6642c6bce5ae72ce5f6b64e111a490a3df4accc49`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Jun 2023 12:28:32 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 18:53:10 GMT
SHELL [cmd /S /C]
# Wed, 14 Jun 2023 19:23:38 GMT
USER ContainerAdministrator
# Wed, 14 Jun 2023 19:23:52 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 14 Jun 2023 19:23:52 GMT
USER ContainerUser
# Wed, 14 Jun 2023 19:37:26 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 14 Jun 2023 19:37:27 GMT
ENV MONGO_VERSION=5.0.18
# Wed, 14 Jun 2023 19:37:56 GMT
COPY dir:ab74dbf9ad27d2154a3f270894c5c95f10fe56a2d5ec4c1875a57c2afdba8cff in C:\mongodb 
# Wed, 14 Jun 2023 19:38:08 GMT
RUN mongo --version && mongod --version
# Wed, 14 Jun 2023 19:38:09 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Jun 2023 19:38:10 GMT
EXPOSE 27017
# Wed, 14 Jun 2023 19:38:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:234d39d9b188e7f36d5a77b0d54990ea826551314b6703c83aef3ef20b1a7050`  
		Last Modified: Tue, 13 Jun 2023 19:06:23 GMT  
		Size: 104.4 MB (104397895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84163792b788702ed02647fa84aaa1ebd7ba0473cb5b5ad12bcaa9a2c6cb5de1`  
		Last Modified: Wed, 14 Jun 2023 19:10:26 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd799c88299e1ebd604eaa844089e95b8f35888e44322cd7da278cf0f9f6de5e`  
		Last Modified: Wed, 14 Jun 2023 19:55:04 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4502866eaaaba58a010f68a9deb71bef8bcc8181d4e895d1822b78614358f4`  
		Last Modified: Wed, 14 Jun 2023 19:55:03 GMT  
		Size: 73.9 KB (73909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f7d3e438ee6e0b29ca19f74c7af5de2b036744543135f66aaca8c7644e300f`  
		Last Modified: Wed, 14 Jun 2023 19:55:02 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39d010ffcf015dbfee63dd31d3c6f77ddbc5ca13cc31754cbb7d113e2b899c7`  
		Last Modified: Wed, 14 Jun 2023 20:06:27 GMT  
		Size: 263.4 KB (263366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092ab42a946e2735bade0f32e8d84d24856d8010e198b2131d23f69cfb0915ed`  
		Last Modified: Wed, 14 Jun 2023 20:06:27 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afd1cc306518d949e854d518229bd4807feb581c7ea060fdfe52381f9707d24`  
		Last Modified: Wed, 14 Jun 2023 20:07:20 GMT  
		Size: 312.5 MB (312540008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c182432cb0812083fff7da535d059a48b4094a1fcd050c19efb4525854774d`  
		Last Modified: Wed, 14 Jun 2023 20:06:24 GMT  
		Size: 86.6 KB (86612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c38bd1154bc6f0318240df6e4da68549f1bd4c7c75f68b9ebb3a477d5185eb`  
		Last Modified: Wed, 14 Jun 2023 20:06:24 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ba107409978d782ae0c9d4ef87eccb77accfc31a8207ae3694018e5335f271`  
		Last Modified: Wed, 14 Jun 2023 20:06:24 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e63546af5179f2ad7fd5c2bc1bb7db25a35337a578753eb1bc7b79dfda4bc6`  
		Last Modified: Wed, 14 Jun 2023 20:06:24 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
