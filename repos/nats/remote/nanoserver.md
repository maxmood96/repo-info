## `nats:nanoserver`

```console
$ docker pull nats@sha256:aea7cc2831f9abd383f4174e38b17849df3606beea6648d63b824eb2a8b88dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:4ec9c8b5fc9c9f5ea875830d8355ac6e9f93d0e3fe5d374d24a5eb6bdf2608fa
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105092070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7678424b503caf1f5241062780f3e6969a8867e91fa257eff465274911c9568`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:16 GMT
RUN cmd /S /C #(nop) COPY file:5493aca6ccb800df74d7e7b98176527689b02c807794603a1f7dde376217279b in C:\nats-server.exe 
# Tue, 31 Mar 2020 21:16:18 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e455632008f14f11f8b72d69a1da128950a141735926961bcf2baf8c2ae12c2`  
		Last Modified: Tue, 31 Mar 2020 21:20:05 GMT  
		Size: 4.0 MB (4036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f44539e2ede61bafd54f622e8042099620ea0dafd8c87cf6043d295f17932f6`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030bd5a2e51cc12afa370bd2ec9b2ba2c6ad83cb09ce43555d0ba3b3eb497b49`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0425975dec676f07849687918818aa9a711883c2e2b6d39f40c1d922b71b`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ec1ea0b29e208f3799b3561fef99ab4b126884eeea9301d6c55f699847d80d`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 825.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
