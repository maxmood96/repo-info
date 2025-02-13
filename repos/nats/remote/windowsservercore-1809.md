## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:90f6a9c218e54fca8ddb8f5ef49c6f6ebebb7d89b03b8c5a782e1b66ef645041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:39cb1968945038e1a49d2050366ab438dc18b480e87b5e44619232a9a091d74a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143618063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e340f3813e5c62bb1e880a8b92500255ed31b661ff6b11d0b1af0896b9a598ca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:30:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Feb 2025 00:30:43 GMT
ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 00:30:44 GMT
ENV NATS_SERVER=2.10.25
# Thu, 13 Feb 2025 00:30:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 13 Feb 2025 00:30:46 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 13 Feb 2025 00:31:05 GMT
RUN Set-PSDebug -Trace 2
# Thu, 13 Feb 2025 00:31:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 13 Feb 2025 00:31:22 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 00:31:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 00:31:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 00:31:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a6bf8fa2712d05ebc326aab9183f1d96892ad97f7899cac56ffc2167dd7dd6`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94310c02275f95397d489002b6985a9c5f753a130c8cf91f17c92aab6c63eb8`  
		Last Modified: Thu, 13 Feb 2025 01:08:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cbe9da0a2b25582259cac86013896d1e60d2fdd77b464761a1b13c9b8dee41`  
		Last Modified: Thu, 13 Feb 2025 01:08:31 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d84ab9a7cce9d71959a0b1ec3046af767c37fa3a03d4cf12c29069ecd1bd93`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6de08f536a814f14692a28bcb492e5c871eb2b54808cd729f95d81f106c6ee`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1affead666dad44febd2844d6a314c236311ade14424d414ea854abfd093cfd`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 330.0 KB (329975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde71a66804b443be4d558b5a4f9b6293313bb94ada1231016939e3aa798f9b2`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 6.4 MB (6367013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c58e512d44c301353256688edcebda6a361be0c1f85d839c93e158f7c461ae7`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cedfacb86bd6297cf6883668655328e219bb4f07447398deaedcc979a70c01`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd56707341ec29eea3c040fd3725f0c12f05232521926f774f7c3d4984b746e`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a6f2dd1d597249ee9e821ff329437a94cd5fdf27f241db76281d489d0ff46c`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
