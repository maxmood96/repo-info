## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:7e0428dba71a73c21cf18a83990daccd695802963a5066161b005c0fa2aee2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:8d78380851c70c44eea273d3aaff4c424ad191c679708c42bc171878d9500fac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711490510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a201f7790c138296ade85180ca7a6fb58d90b5c11b47fcf00561b8c1f8912412`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 14:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:00:40 GMT
ENV NATS_DOCKERIZED=1
# Fri, 19 Nov 2021 23:14:14 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:14:16 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:15:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:16:41 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:16:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:43 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:44 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:16:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db1ba835bccbdc73ef254c175ca6ae0dc3f0bd759c1910c3b123cfb9613223be`  
		Last Modified: Wed, 10 Nov 2021 16:21:11 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3df59793c391e0eb7e6a2ddb65801dfa94397b370daa52d04e242ba0274e3d`  
		Last Modified: Wed, 10 Nov 2021 17:06:13 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ee32c5b0f8d0e25d55f2155058787d912af133c85d6e693f1b829b4247b631`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8dc647b82c6c8b1c1e07221e4f9d39e1a2ab5d5ba52da0c81f7787c5ae5999`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fa0ab98575757356ace0336d5e3c425b48de9137d943b065c182545960785`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3745b3fbaa0d3f89421d0a9f02890206569705c76260367007a8ec3958a6f8ce`  
		Last Modified: Fri, 19 Nov 2021 23:20:33 GMT  
		Size: 368.7 KB (368732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2736dce76765262fdaa9b8f1cb72e12a54be251a592faebc20887d9ffdf021`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 5.0 MB (4987456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d319abe61026f65f2bd4bfc0ced76d5d6e68d5636948772c2ecbae70bf85da2`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786db0a3988ce428787cfe588a08d3b9c1c897c7ebfc24a579e54bb19f546fcb`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab8b864113ad6fef653342907be67b1f880316a291dde505550e5eddac3e870`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d6b4b4f014b764cb75cc10988c8c9fcc2c6943f0c7ba3f24115f2bedf602c5`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:6ab359fa36226d90c1aafd6638846ec1a0bd53484f30e04842e1efc41cf6eda1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278475967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f606e5e79c17f6ad740d2394f5ab64d8d281e6ccd57599ec6138371bc5578`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 14:32:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:03:18 GMT
ENV NATS_DOCKERIZED=1
# Fri, 19 Nov 2021 23:17:07 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:17:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:17:09 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:18:18 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:19:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:19:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:19:50 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:19:51 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:19:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6f303e73635c7923a8c64f8938e7ba4c10210fd15a6ce63aa8a62d5a8ea8c0a`  
		Last Modified: Wed, 10 Nov 2021 16:21:33 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5db4062c12269959ca71caf00b70e9baebf61b90c49c74db0e2cdb04cf83e8`  
		Last Modified: Wed, 10 Nov 2021 17:06:51 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e3554a67b57f2a9aa17f80c9675be949b9372a709bb0f7fdf1dc7a3954a8a7`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eeda6412c8ef4a5587519bccde86a7d03ede9e3d88c0c2ee7b4edaa24a9d25c`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ca635911cf274a387f2d940588371058db1949e9b10f093b7fd1da6d1a30fc`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672969c6f430af654d3a77eecadafcc5149020360859599bfac5eadbdf52388`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 360.6 KB (360571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf6b57aeb7766a77d7c0ba1400216f6aa339f8607b7fd2302e8b30f4ff8f140`  
		Last Modified: Fri, 19 Nov 2021 23:21:03 GMT  
		Size: 5.0 MB (5011302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b11540a8a97137b66a8f28531a07e5ec3db99e327ab93821000188e02bc98bf`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca98906943111b8c8be9af092d51081d9ff4e7ff0613c220636cb567764349`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d92f48165676375740936c62ff6e30aca04671b4204790a0b8c7a481a64e77`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5b6e62a393187d7daea5065dc7e4285f6ff881d7575c53739d47f068b86803`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
