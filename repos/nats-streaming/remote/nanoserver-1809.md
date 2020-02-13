## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:8bb0ce4bdf89e0db48f596fa738cc8531fc2591ff60cf18a47e9febc2dec81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1039; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.1039; amd64

```console
$ docker pull nats-streaming@sha256:eb3299435dcd62d8e2e717171a12abbac2203ff981cad74ef7e9de2d1287fc0e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107149598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8766ac946638e7986437e0d4317bf3df7991ac6cae53647a3d2ce98d7ee48aa0`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 08 Feb 2020 11:49:13 GMT
RUN Apply image 1809-amd64
# Thu, 13 Feb 2020 02:15:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2020 02:15:10 GMT
RUN cmd /S /C #(nop) WORKDIR C:\nats-streaming-server
# Thu, 13 Feb 2020 02:15:12 GMT
RUN cmd /S /C #(nop) COPY file:d30725f7225d14fba35e88513adf63da18fc9fef9c4f6c817dff8f784f19a7c1 in nats-streaming-server.exe 
# Thu, 13 Feb 2020 02:15:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 13 Feb 2020 02:15:15 GMT
RUN cmd /S /C #(nop)  CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:388cd8053ec3a1b11d469bf9cb5b05147c5e39d171fb5f47a976030ae021fb61`  
		Size: 101.1 MB (101093465 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f3b33fe25639aa784f59496fbb914492e379d6052401c336ef47bedef504dc6e`  
		Last Modified: Thu, 13 Feb 2020 02:15:58 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9cb2af6217311e6578d46bccc22ea288f4b4f17d68a635ff995d5271bb831b7`  
		Last Modified: Thu, 13 Feb 2020 02:15:58 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dabdbcc14d9063c8a305eba1f0b3d5755e6b84d2e47abba9914f9bfdd83482`  
		Last Modified: Thu, 13 Feb 2020 02:16:01 GMT  
		Size: 6.1 MB (6052172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a938839f93958630fc9ba8ebab6c2e12d5ffe10ee943b44ec38508f53b0e3826`  
		Last Modified: Thu, 13 Feb 2020 02:15:58 GMT  
		Size: 950.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d193ad23c98e6ca05cf17885a08d129d92a794f90ad7dc211558dda6e8429`  
		Last Modified: Thu, 13 Feb 2020 02:15:58 GMT  
		Size: 937.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
