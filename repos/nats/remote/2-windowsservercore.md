## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:709794fd754e2c5baad0d8b6a200da48fa8139654f73038b74a3c115ebd9a169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64
	-	windows version 10.0.14393.3630; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.1158; amd64

```console
$ docker pull nats@sha256:da6bdbb3e4b18381c6c8bd65e77e65362cb7093aaee4e8e75847d8a99d0408b9
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2284059992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f78b59d77e6829d438329fa647c002d8909b0c67092c0301d26dfb40b7baea`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 16:22:01 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 Apr 2020 16:22:02 GMT
ENV NATS_SERVER=2.1.6
# Wed, 15 Apr 2020 16:22:02 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Wed, 15 Apr 2020 16:22:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 Apr 2020 16:23:36 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 15 Apr 2020 16:23:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 15 Apr 2020 16:23:38 GMT
EXPOSE 4222 6222 8222
# Wed, 15 Apr 2020 16:23:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Apr 2020 16:23:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eabc35632c4e9dfdc3df34c8c1768de1a8aabc637c634f666a062e04e7a01ee`  
		Last Modified: Wed, 15 Apr 2020 16:27:28 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5288564da248aa7179bae08b69418aad39d084799753bb07bfdd1661ad2333`  
		Last Modified: Wed, 15 Apr 2020 16:27:27 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27973c84fc7465c3ceeb48281ce8135848a6dcb336f1273b0137b360f9a131d`  
		Last Modified: Wed, 15 Apr 2020 16:27:28 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950a95d662fcdfc3a25fa648ab13266ba927dfeffbc98d3a1e66834762115c5a`  
		Last Modified: Wed, 15 Apr 2020 16:27:28 GMT  
		Size: 4.7 MB (4669475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4555dfda5583c4fd9be24b85380650589476c60b894b59d99ec6a382713b58`  
		Last Modified: Wed, 15 Apr 2020 16:27:27 GMT  
		Size: 8.7 MB (8673637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3b82a014997f818a346ad784acea3202845bff46f62107b2e463570cecbd50`  
		Last Modified: Wed, 15 Apr 2020 16:27:25 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe13eafcd76e84ce1b4f08336aaf2c43f14f11b4b8f8a49990f09f577d368d7f`  
		Last Modified: Wed, 15 Apr 2020 16:27:25 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bc2054912b5068f6e12959261449f157019effdffae5a62f112770ad472350`  
		Last Modified: Wed, 15 Apr 2020 16:27:25 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983c805853aba21f8626b5cf6797e20a38a6905e59d4302c96116689b260adae`  
		Last Modified: Wed, 15 Apr 2020 16:27:25 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.3630; amd64

```console
$ docker pull nats@sha256:66d7ae5a3047d921cdd982db951c43132b2b9f955f9c94f969a526f379644046
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5742882659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362ac08032a58455577b6f347ac3cd8a762b2d2bb2f56014d6b0b017d15d62f6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 16:24:09 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 Apr 2020 16:24:10 GMT
ENV NATS_SERVER=2.1.6
# Wed, 15 Apr 2020 16:24:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Wed, 15 Apr 2020 16:25:07 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 Apr 2020 16:26:48 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 15 Apr 2020 16:26:49 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 15 Apr 2020 16:26:50 GMT
EXPOSE 4222 6222 8222
# Wed, 15 Apr 2020 16:26:51 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Apr 2020 16:26:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc6613d0d14b27f603772f6d2e32bc83e9cae7a2c5405bb55e04dd2afcc7965`  
		Last Modified: Wed, 15 Apr 2020 16:28:02 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9b2a9b009b5d32772c3e5a1b4266c0345d79830d28510e291416655fb32705`  
		Last Modified: Wed, 15 Apr 2020 16:28:03 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98891503dff691a3d836c03239d6c6855b25d57938484a3a5a25ead310bebaf7`  
		Last Modified: Wed, 15 Apr 2020 16:28:03 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a31b768b5812d2bb57739d75ffd7bc8dad60ce71628ea3af3e9a31f905dacea`  
		Last Modified: Wed, 15 Apr 2020 16:28:08 GMT  
		Size: 5.4 MB (5381044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc99fc11ca890a479faed2238fb44758549834a92a6d69bd4f73fa248fb82f96`  
		Last Modified: Wed, 15 Apr 2020 16:28:02 GMT  
		Size: 9.4 MB (9424463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d664d8f00459b6469eaf80e2b19d667e689b496b0fbd878c5e6b8d61cde564e`  
		Last Modified: Wed, 15 Apr 2020 16:28:00 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c4814c2ae0130e15bab2fa7897d662cc2b737e3171a6e9cdead5280315e51b`  
		Last Modified: Wed, 15 Apr 2020 16:28:00 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312de9f796b94fcf03a3bb931cbc289d5232b2fa3182ce5a4a3ced2d6833ddb1`  
		Last Modified: Wed, 15 Apr 2020 16:28:00 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827eed70b785fb9807bdc599571dc408e1638b24badf64bb049a0f6a6a963151`  
		Last Modified: Wed, 15 Apr 2020 16:28:00 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
