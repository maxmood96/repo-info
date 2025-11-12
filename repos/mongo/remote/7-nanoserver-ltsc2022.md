## `mongo:7-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:7eb08909fd9a057375bf2c21efb93d8f2ad96f99e6d26fb91d63ca4876a68e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `mongo:7-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull mongo@sha256:4fecb024d068b864060ec43f338bea6981e3bd23512caad0970e84a4a756c4b5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.0 MB (743973373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2796abcaa7e1d654f91bc20c7bbe8c0c57f8026ea1ffaf092f7f76851bbcc649`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:13:33 GMT
SHELL [cmd /S /C]
# Tue, 11 Nov 2025 20:13:33 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:13:37 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 11 Nov 2025 20:13:38 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:13:39 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Tue, 11 Nov 2025 20:17:19 GMT
ENV MONGO_VERSION=7.0.25
# Tue, 11 Nov 2025 20:17:57 GMT
COPY dir:997cfb622d71d1844c777e5a30f23a94e0ff185e3d9fa77e1de86a6c03fa4ec1 in C:\mongodb 
# Tue, 11 Nov 2025 20:18:12 GMT
RUN mongod --version
# Tue, 11 Nov 2025 20:18:12 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 11 Nov 2025 20:18:13 GMT
EXPOSE 27017
# Tue, 11 Nov 2025 20:18:13 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d58e2cb9f074a2a60cf406b0cbecc018f6c742732c8573358ebfcf891f45df`  
		Last Modified: Tue, 11 Nov 2025 20:16:14 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db671f9f87ca9c03032e8ed49b2f8f3d9d41268619b1f9ce93dcb039a8f8a66d`  
		Last Modified: Tue, 11 Nov 2025 20:16:14 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604f16dbd57d3f49845af1b286cf35ab42d8bd5f8aa279851164df1a1fe1e573`  
		Last Modified: Tue, 11 Nov 2025 20:16:15 GMT  
		Size: 85.6 KB (85611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c212f93a676e4f493815e843758f29bd8c5c73f8572203e3318be1b3301b583b`  
		Last Modified: Tue, 11 Nov 2025 20:16:14 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76c58c3d09be383404a20155b65bbd58e60b6f3d40973899da91b17ff6024b8`  
		Last Modified: Tue, 11 Nov 2025 20:16:15 GMT  
		Size: 275.2 KB (275214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd13bc5e72b5e59513fdb52f1bde63bd9fddd7614808f7f0338ac9ab1a2ce06`  
		Last Modified: Tue, 11 Nov 2025 20:19:31 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4ab714b40e51ced4f47b133cbecb4a9858567ea9868916fb008b6b2cf5c56f`  
		Last Modified: Tue, 11 Nov 2025 23:10:19 GMT  
		Size: 617.2 MB (617165104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08244d71187b23fb5611477f76dcb414c0a8af8c69c034fc959cf4272becbe21`  
		Last Modified: Tue, 11 Nov 2025 20:19:31 GMT  
		Size: 90.9 KB (90892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6080672311e6dea0a622ca531b2dd6cd61f7178aa494fee8ed796803008fb9b1`  
		Last Modified: Tue, 11 Nov 2025 20:19:31 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da5c280670f64e294e3734ad69a562b13e72af1dcba3a08276d9854239f402b`  
		Last Modified: Tue, 11 Nov 2025 20:19:31 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e741fb909fbca08d26912c885dc28d8f366e3a0ea64347b59cdd0d4e5bfacb07`  
		Last Modified: Tue, 11 Nov 2025 20:19:31 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
