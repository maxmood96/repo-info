## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:181df5142aea41aa0901309ffd02c00ae7926e3af39dbda47800de6129b6945b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

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
