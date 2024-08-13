## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:15d9704c30682833528a5815c262cf95f046b7da412183425e7a87517cf40595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:9deb3d85ee4a7313a1a7defc1dde3752112125c3f462c9960c7a5d9607648ba8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251766997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dce49344ab08729315489c1817eadb7bbdbc60535969f780fa3846c8544657a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:45:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:45:39 GMT
ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:45:40 GMT
ENV NATS_SERVER=2.10.18
# Tue, 13 Aug 2024 20:45:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.18/nats-server-v2.10.18-windows-amd64.zip
# Tue, 13 Aug 2024 20:45:41 GMT
ENV NATS_SERVER_SHASUM=191a6cb6f7391005b5f886ae4fb700907dd977149f650febda9ae433701bf547
# Tue, 13 Aug 2024 20:46:34 GMT
RUN Set-PSDebug -Trace 2
# Tue, 13 Aug 2024 20:47:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 13 Aug 2024 20:47:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:47:56 GMT
EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:47:57 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:47:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a01ddac643cbd49eec6aff688d037d7a551e855201124b4b91f640dc4af4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a022697aef59a6692fd1a03334c036f85c795eb0dc574e189565788b877520`  
		Last Modified: Tue, 13 Aug 2024 20:51:12 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c910c8d678572d8e48160d9face57f1ce0b7adf4cde7d11f5f7741af8feed8a`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eabbb4d0b71be6e451b4985f34eb1822d7caf828feb1de07dcf4ca27a2ccfce`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b04856d100d25b0685b009b6c272646f0ceb1f8af538124e0797af7e763295e`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8699203a8af558d97aab77c2e798b5b822b003cbe17c3b5a8a981cc5d2c5ccec`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 448.3 KB (448326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcd0c2303d56a322f8734315be86ce538db6358d06084a0935622915c75c748`  
		Last Modified: Tue, 13 Aug 2024 20:51:10 GMT  
		Size: 6.1 MB (6102263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed1f2d2efd078f52ce4ba389e8e512e2d7326377ec1ccdb677258db0ccc6135`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993179548ba778ab1bd08307bba50a05d8fdfa0f7134a2cf90f58bf22793b0c7`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b663cad9877357139f8c191c15e724f9c4a52ef7ec2674e0e658531671d78b`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4de46aaa98aea62afe476e42c0d9eb20f074df65dab03b022a73090d5be37b`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
