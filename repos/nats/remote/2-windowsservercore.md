## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:be6518538136b27788b3b216ca05b65ddc6c47b2c64992d1381f3add500633a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull nats@sha256:0670c498f5fb25cdd8e9c1b21270ca3e44b76e274ece03d675733397eab90591
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289619951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e772e45f8862f0f8098074f862305c544beb440f90755782668ab6454d880c0c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Tue, 14 Oct 2025 17:14:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Oct 2025 17:14:51 GMT
ENV NATS_DOCKERIZED=1
# Tue, 14 Oct 2025 17:14:52 GMT
ENV NATS_SERVER=2.12.1
# Tue, 14 Oct 2025 17:14:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.1/nats-server-v2.12.1-windows-amd64.zip
# Tue, 14 Oct 2025 17:14:54 GMT
ENV NATS_SERVER_SHASUM=64d4702f31daa2560ba7a0291d2911b36fd6199277721f8ab2aae0d12eb2763e
# Tue, 14 Oct 2025 17:15:31 GMT
RUN Set-PSDebug -Trace 2
# Tue, 14 Oct 2025 17:15:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 14 Oct 2025 17:15:53 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Oct 2025 17:15:54 GMT
EXPOSE 4222 6222 8222
# Tue, 14 Oct 2025 17:15:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Oct 2025 17:15:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d6ba28adb159cc053464ed51bf3089fbb328fdaf9ce56e8dd5df9ac930c521`  
		Last Modified: Tue, 14 Oct 2025 17:24:36 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e2356ee8e318416e53a5dc29e5037688f72f4f7be9c2978762fa158123c678`  
		Last Modified: Tue, 14 Oct 2025 17:24:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0356b590c4a01215cf485c04f963b69dee104c657de8649e81df2a1df667cea0`  
		Last Modified: Tue, 14 Oct 2025 17:24:36 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe6f2128aaf2b7960f8d3944e12aa449a4ff91caab4012a387081aa5c881743`  
		Last Modified: Tue, 14 Oct 2025 17:24:36 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6511902730eb5aeece543398f96d5b0cf4ca8d5aa44b3158e0981e7a2a5c7422`  
		Last Modified: Tue, 14 Oct 2025 17:24:36 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe354adef4b9166337eeb9281b31945d743f54bf393ca217b53e057ab91a8be8`  
		Last Modified: Tue, 14 Oct 2025 17:24:37 GMT  
		Size: 364.2 KB (364241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee30320b51d5d68202a45cb614a83848f4ffa4a5e1b4446a784f4b067427b6b7`  
		Last Modified: Tue, 14 Oct 2025 17:24:37 GMT  
		Size: 7.1 MB (7098381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbd94afd84fb1454e0a69914e89438132ede8f0322dfb8dee05a24b4dac9743`  
		Last Modified: Tue, 14 Oct 2025 17:24:36 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de24d22b8f5acee96f1c0e1bee950bcc69e161b0f197017230ce41e1f85ae92`  
		Last Modified: Tue, 14 Oct 2025 17:24:36 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90143f6ff29eb91718a2fd4232c4f12424d0c311c7b5c90b39f31d3190785b1f`  
		Last Modified: Tue, 14 Oct 2025 17:24:36 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0aed132e240d1522007d3b8c9bd41f4eaf5d7f74a44cb4e57abab9c07957d2e`  
		Last Modified: Tue, 14 Oct 2025 17:24:35 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
