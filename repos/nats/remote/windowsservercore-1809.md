## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:a549f64bd3a28ae3f48347dbdc1a0c2e81c9b3e042cc4dd94eabc376466621bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull nats@sha256:b8aefe1830f9831c2132acc0d476720df9b39fae66dc71a9577336d23e497733
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2243631626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e930c8f8b1e978baa56a5c0d02806211bae1c7926d69ed817351548acbd18fc0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 17 Feb 2020 06:57:13 GMT
RUN Install update 1809-amd64
# Thu, 20 Feb 2020 05:10:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:10:06 GMT
ENV NATS_DOCKERIZED=1
# Thu, 20 Feb 2020 05:10:07 GMT
ENV NATS_SERVER=2.1.4
# Thu, 20 Feb 2020 05:10:09 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 20 Feb 2020 05:10:46 GMT
RUN Set-PSDebug -Trace 2
# Thu, 20 Feb 2020 05:11:59 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 20 Feb 2020 05:12:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 20 Feb 2020 05:12:01 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Feb 2020 05:12:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 20 Feb 2020 05:12:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5405b7580792436b60c664b5fa766ea57f5a60c1d9a8c522cf53e99e4813355`  
		Size: 695.8 MB (695818606 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7f20f5493f581bb667af03f7639273e01559818f9d7dfe81dd7e9dfef3af2e11`  
		Last Modified: Thu, 20 Feb 2020 05:16:53 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4484ef29cc7280dad97223e8b986024c82253ebec1ab8ac720d68f7ccbfdd88`  
		Last Modified: Thu, 20 Feb 2020 05:16:50 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed1a0242d86d005ec01dd2a8fbfa46d326aae25aaba80e54cbf394acb81ba6a`  
		Last Modified: Thu, 20 Feb 2020 05:16:50 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad8d21a54b3715ab0f3fa90fb62b2e4350c1aa4673d12ac6fd3df54d99316f0`  
		Last Modified: Thu, 20 Feb 2020 05:16:50 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da8b13074c54e2e83d2e0a33ed0ea81af9e05aebc398103600ab63e704b457d`  
		Last Modified: Thu, 20 Feb 2020 05:16:51 GMT  
		Size: 4.6 MB (4567940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec47cd3229438fd1a2c95e790cc9da8cc895fc0e47f328cb93376ba22cfe392b`  
		Last Modified: Thu, 20 Feb 2020 05:16:51 GMT  
		Size: 8.5 MB (8549763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35502be6a1e19287f76da5a10271918bc5a1296c09790de2a8704db52da3a25`  
		Last Modified: Thu, 20 Feb 2020 05:16:47 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b85701ac6f1754ef38518709893a73c70b4795e10afdc4cc004473f13d35ee`  
		Last Modified: Thu, 20 Feb 2020 05:16:47 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3694c50b23301f2beb8f281f3144765835b70f99f7b2da2d6262cf372b546a99`  
		Last Modified: Thu, 20 Feb 2020 05:16:47 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f436000e88faf749dc2b3cf635720f8227a9f97545bd2c736f859375ec73147e`  
		Last Modified: Thu, 20 Feb 2020 05:16:47 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
