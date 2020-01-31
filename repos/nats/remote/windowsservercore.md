## `nats:windowsservercore`

```console
$ docker pull nats@sha256:f635e84db146077c8ef8f2aed7a35a400e56b88d444d8043d9f021cd43d014d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64
	-	windows version 10.0.14393.3443; amd64

### `nats:windowsservercore` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:3cd1d4f67d1be8ddd5ce24eee17e14d4ee01ce9cdd54ee035ba49aee1ffb0106
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2230544935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c64e3e55e102dce9595319163c41fbc2a3817842d949f09ed00f6abf7e6b612`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Wed, 15 Jan 2020 14:40:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:41:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:20:19 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:20:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:20:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:21:50 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:21:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:21:53 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:21:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:21:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2397868e5c7aa285f662aaa9309fa4756277739e11d589a663a204df80595f2c`  
		Last Modified: Wed, 15 Jan 2020 17:10:53 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23c268ec0520ea9af1e83b69008728041b2a5f234937b9a6272d2a739fd92e`  
		Last Modified: Wed, 15 Jan 2020 17:51:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64db2fd4fc94c96bf74d4ceda66e789cc94f8564a3e7883c4ed1342bbafcf73`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95109215dcc59b85e8609afe1f1a937ae8b0e371b6e3fc87a312dca652bba88`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abe00c43ab7107f68a12e1168c1dcf4f270ae2838f9dbee912fffa64b29f8f`  
		Last Modified: Thu, 30 Jan 2020 23:25:45 GMT  
		Size: 4.6 MB (4572370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcebfa1af024a4a9c5c405f8e90e7516490239d94819cb2017d64f4e986ff97a`  
		Last Modified: Thu, 30 Jan 2020 23:25:41 GMT  
		Size: 8.6 MB (8551363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e85db3ba0a6f65fe27a002088f3e8e56d7e44e8505538fc3184b1004b67d0d`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032b6720c8426d9b09c64fb77d91a4c52cdd6fdade7b5861b7e3b6a7a71a5b01`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d3d6953ad42f738ea691168e451f77533bff19e02ca60651cc5ea8b0909c98`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be73e621a1b74a2c24116891bd94204ca37d37e42e009c8b5618f9fa4ef59ac`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.3443; amd64

```console
$ docker pull nats@sha256:b93a92c7137ce9e49e77908d56639a7979de1576fe2392dbad574eaf3b6af1b0
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5739398111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484d621c7c840a5096b8f22cb481c70fdfceb17ae28ac91d1d0e2f0c03c51b85`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jan 2020 15:20:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:47:08 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:31 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:22:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:23:20 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:24:55 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:24:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:24:58 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:25:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:25:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43da502775fb34b738d9f908cb549c2825c04f1451d1039ec99749be127e47ef`  
		Last Modified: Wed, 15 Jan 2020 17:12:02 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6771e606bb5340710c7ec7fa3294903a0a1f901e5c1e79211ee54fc1f074179a`  
		Last Modified: Wed, 15 Jan 2020 17:53:47 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a726042a1cbbb18db11b01cd4afb9a1827a05f1762d628efdfd36f44607d587f`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e838ce5d75be430b4249e23414b64cfaa1fe44c2ac38610b5309614d2085deb`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebe1a1b70129b898aa43665d07e08975be6969c32de34dd93c089d2d61ce532`  
		Last Modified: Thu, 30 Jan 2020 23:27:09 GMT  
		Size: 5.4 MB (5382508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c046f50b9363080341b7a2690e4a9be42c7774ffcafa964d579a0f8f710cbd`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 9.4 MB (9406281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320f4452a72cff84b1af502f71920172156ce34de4e7bea4f0bdc0ea3fbb9396`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca833ddc6c1c6e6affb374a6583b04a19307e144be67482ab44ceeb7c93a717`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0ec24ad2af324939951cadd30c9e492bc03eabc126e51ea070390dcd4ddb8d`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadd053a880ff838580bf99313b315b9d5fdb3ae9f14aa2e8057b2557d8390e`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
