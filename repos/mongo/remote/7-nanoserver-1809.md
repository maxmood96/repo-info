## `mongo:7-nanoserver-1809`

```console
$ docker pull mongo@sha256:c49ff5f62c089d752d64845e26cc378a3d107a70b78a16a684592fadb2cfe54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `mongo:7-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull mongo@sha256:affec03052e2aa095e412984f8713dbb59d6df0f73f7a0b999853568af3646f4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.8 MB (718802147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb71dc2c739d0732437cf9952d3a70a25e3d7b22476e5288e6aba01d69b5d4b6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 25 Feb 2025 02:22:15 GMT
SHELL [cmd /S /C]
# Tue, 25 Feb 2025 02:22:17 GMT
USER ContainerAdministrator
# Tue, 25 Feb 2025 02:22:20 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 25 Feb 2025 02:22:20 GMT
USER ContainerUser
# Tue, 25 Feb 2025 02:22:22 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Tue, 25 Feb 2025 02:22:22 GMT
ENV MONGO_VERSION=7.0.17
# Tue, 25 Feb 2025 02:22:52 GMT
COPY dir:c1f7dac9e27c15774292d02d4d27685640b385b96631f12dcad5ed2ca42440dd in C:\mongodb 
# Tue, 25 Feb 2025 02:23:05 GMT
RUN mongod --version
# Tue, 25 Feb 2025 02:23:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 25 Feb 2025 02:23:06 GMT
EXPOSE 27017
# Tue, 25 Feb 2025 02:23:07 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2f0ab0e3018b70d7072fd63302da30b0d6f16fd384b639d04cb4e146dd7d1`  
		Last Modified: Tue, 25 Feb 2025 02:23:12 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5406fa8b55c841f298a7e84f78f2531f7589643b8745ec3665b2f0cb026aff1`  
		Last Modified: Tue, 25 Feb 2025 02:23:12 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3573a5aef33aa39cd06502c2cc36090148440de2245e4817eb9386897c0f4329`  
		Last Modified: Tue, 25 Feb 2025 02:23:11 GMT  
		Size: 69.0 KB (69050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486c0bcce946d222bbe4b10fe02132b7edb8cad02fa7918bb93c69d998e4352f`  
		Last Modified: Tue, 25 Feb 2025 02:23:11 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9794703f8fbe5300addc78478839e0f2e85b985b7520447fef3f0c70a4cb44a9`  
		Last Modified: Tue, 25 Feb 2025 02:23:11 GMT  
		Size: 275.2 KB (275152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a236b67636dd58d689bd294cc0b53e9fa0ba782883116048ece084b0f98bda02`  
		Last Modified: Tue, 25 Feb 2025 02:23:11 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9f782f53655396774a12d59012034d897b10bf51d58db9d286e88243f887cb`  
		Last Modified: Tue, 25 Feb 2025 02:24:02 GMT  
		Size: 611.5 MB (611461922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8abcc3dd391428a3bff56548d3bd236d2b09d9394cccd978cbd73836982bfcf`  
		Last Modified: Tue, 25 Feb 2025 02:23:10 GMT  
		Size: 73.3 KB (73314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487d7a8977aed6a2e3a31c5b2f740587d95d4f816a9047e063a4b1626a29e381`  
		Last Modified: Tue, 25 Feb 2025 02:23:10 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d94bcdd211bffee973c36a494cc84f07a688b999e4588788ed5e6526204052`  
		Last Modified: Tue, 25 Feb 2025 02:23:10 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc418036f460e2834c0579822e896ad2d9badb2df48f1dde1a988d712ccead0`  
		Last Modified: Tue, 25 Feb 2025 02:23:10 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
