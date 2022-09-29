## `mongo:5-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:90457e5a2720bc7da13f6a6a6c50f1145147d3fd0a5ec08809bc186b06e4c137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `mongo:5-nanoserver-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull mongo@sha256:911e13242b7140814baf932e8e18f28479d0e9aa285d43e78e8182f5a13d67a4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428544316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cd18c0b0613b935536ca6d254effea5d7bf8365d890219ddaba009b7f0e87e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Sep 2022 20:11:22 GMT
RUN Apply image 10.0.20348.1006
# Wed, 14 Sep 2022 12:59:22 GMT
SHELL [cmd /S /C]
# Wed, 14 Sep 2022 18:16:41 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 18:16:54 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 14 Sep 2022 18:16:54 GMT
USER ContainerUser
# Wed, 14 Sep 2022 18:23:48 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Thu, 29 Sep 2022 20:29:04 GMT
ENV MONGO_VERSION=5.0.13
# Thu, 29 Sep 2022 20:29:37 GMT
COPY dir:644971c5551a7576841d7084c8a9e1086a2329d8484b2783b73ea3b245ca1a2f in C:\mongodb 
# Thu, 29 Sep 2022 20:29:54 GMT
RUN mongo --version && mongod --version
# Thu, 29 Sep 2022 20:29:55 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 29 Sep 2022 20:29:56 GMT
EXPOSE 27017
# Thu, 29 Sep 2022 20:29:56 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:09629875cd6ee57fa551626fa2963d8b54718ba9acbf28e7cb5d684a9cb754d7`  
		Size: 118.1 MB (118131331 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:66db2526be0f06c7bd6ba20bdc126ca2d5645acfeb41b5784e4664de37e72b49`  
		Last Modified: Wed, 14 Sep 2022 13:25:26 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f7ad598d1a94ba1f1296571a4da5bf04dde81c7c49e4007c0d7536a959195b`  
		Last Modified: Wed, 14 Sep 2022 19:02:01 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a642c0d7ab9ac57ad706b35c64d641cfc15ba1205447d6102442e8658f3711`  
		Last Modified: Wed, 14 Sep 2022 19:01:59 GMT  
		Size: 99.3 KB (99284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a88827dbafc40e378d95f1d1d7f0924c103f97c9f4ceff294cc2d0eea393aba`  
		Last Modified: Wed, 14 Sep 2022 19:01:59 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bccb161631572ecd27c567a9f0ef6e1146fbc6093ddb42af4f6b8b55eb929a`  
		Last Modified: Wed, 14 Sep 2022 19:07:35 GMT  
		Size: 263.5 KB (263532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9972a2d9f726b5aa7ae8213b9dfb09ba89c7e68fb68159b1100b63fed6c5b7`  
		Last Modified: Thu, 29 Sep 2022 20:49:23 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9b39121b880da150677e215b879968c4bbd8647b02a34d7d090974eadbd059`  
		Last Modified: Thu, 29 Sep 2022 20:50:18 GMT  
		Size: 310.0 MB (309969713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d06763108046cca41b9294525fba5ca9e20c588f9bd097f0fed3f965558289`  
		Last Modified: Thu, 29 Sep 2022 20:49:20 GMT  
		Size: 72.4 KB (72364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68901e9173fa6a21bcc57474ffccd52fec5040d19f56654eb45cfc6825c94dbc`  
		Last Modified: Thu, 29 Sep 2022 20:49:20 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ea91fb9b9053b1712303a1393150fa292631fdab272f61422e16bce552abde`  
		Last Modified: Thu, 29 Sep 2022 20:49:20 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac37905b14609bda2af277199642f5583bd99f6a8bdb7c9a29b1856471ad1e08`  
		Last Modified: Thu, 29 Sep 2022 20:49:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
