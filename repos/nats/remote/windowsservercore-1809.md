## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:aaea1dd766da7fc6a58b336bfefb58022101f3e3d93f120920b4b5c34448302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:ae559827a74bf00c693d5e392de9db1d605d650b1233ec14c668795487b1db38
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2158347713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919feee07cf792e7a2e6c3c6b3fec09153ae6d902f20265fe1d35234619562d9`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:52:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Mar 2025 18:52:18 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Mar 2025 18:52:19 GMT
ENV NATS_SERVER=2.10.26
# Wed, 12 Mar 2025 18:52:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.26/nats-server-v2.10.26-windows-amd64.zip
# Wed, 12 Mar 2025 18:52:21 GMT
ENV NATS_SERVER_SHASUM=e1f9c4eee642bd521878dc493de8514b25c1468e3f2420312aa52f96f7bcbabf
# Wed, 12 Mar 2025 18:53:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Mar 2025 18:53:23 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Mar 2025 18:53:24 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 12 Mar 2025 18:53:24 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Mar 2025 18:53:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Mar 2025 18:53:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea43e9930f0637f931e566900db3d69f5a73be287d4fac09d45ff221ecbd949`  
		Last Modified: Wed, 12 Mar 2025 18:53:33 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2b42117bdf90f3597cb03ece3d9883532012501754ae9398d2a69b1f2c536d`  
		Last Modified: Wed, 12 Mar 2025 18:53:32 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ae1f2b373b6ce9ce5b0836aaebcc55e579c622c10bf9ead6ffd68c92689949`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465fcd15286859b84b50d15a612d3911ac1734305befe65630cacc1b86a11e58`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f024cd749afb64fa0383ac5fe6dced08be9d6afed933df6b790de8b34cfd09`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd59fd63579ec0df922b00adb8812d7a97d8f784a2016749acac40f35b4e90f`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 323.5 KB (323516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5b64997bb4e5891f3d1cae95a727e5a0fbc35fb7630e9ec97ea0cf237ed47d`  
		Last Modified: Wed, 12 Mar 2025 18:53:30 GMT  
		Size: 6.4 MB (6377283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2917d392ce3cea8e291e8df56a91d98b7fc81c8e99f6245989b0a347ee67e2`  
		Last Modified: Wed, 12 Mar 2025 18:53:29 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51373b6fa562be410dbd8ba4b02d6afd9919910429b03c46061a3484cf7d8678`  
		Last Modified: Wed, 12 Mar 2025 18:53:29 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3283b86f1fc3e22f2e4bf1e6b6b20fafa89fb4a79998482809c9ccd9fee0797c`  
		Last Modified: Wed, 12 Mar 2025 18:53:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615d058681ba1353e13556b5b00004a928846392193716ecc3fe69acdedaa414`  
		Last Modified: Wed, 12 Mar 2025 18:53:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
