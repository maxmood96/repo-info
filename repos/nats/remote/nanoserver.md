## `nats:nanoserver`

```console
$ docker pull nats@sha256:ccc2e7863f0515c0eccefb2e5ee10e747551774dcca0c93c009fbe20d1e688f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:58a031b71d94035b7ffcac75a55d4af99f3a7324305a08175145c444335d661b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160892303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0889744b15069353592cc77e8c6750a609e1b647625d4d383ee67429dec660e8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Jul 2024 17:47:31 GMT
RUN cmd /S /C #(nop) COPY file:597b8acb27656d6ed03f368919febfb8bdb37af32d76fdf02bde1220f352c5d1 in C:\nats-server.exe 
# Wed, 10 Jul 2024 17:47:32 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Jul 2024 17:47:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Jul 2024 17:47:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Jul 2024 17:47:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e4bc7f31f192963e8f3a3e89f1c1b64e284d889fda14143bf16c0917fe81ad`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 5.8 MB (5804537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888df09efeb767457fa5fd838b3c10398c77249b5bffb33a78b03f4065e9e3c6`  
		Last Modified: Wed, 10 Jul 2024 17:50:49 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163346c492a1f4532039ea7cbae77aecd4a82d52f642e642dff207419ff822b8`  
		Last Modified: Wed, 10 Jul 2024 17:50:49 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e15cbe5192fae81182ae87fcc0a1889f5144e9d77c78cb0cf1e3676490c6c7`  
		Last Modified: Wed, 10 Jul 2024 17:50:49 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3895e939f54fd4486f6bbe60bcc460eed1327c2511d305a2f8622efc702fd4c1`  
		Last Modified: Wed, 10 Jul 2024 17:50:49 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
