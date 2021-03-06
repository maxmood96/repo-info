## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:b12e8b3dfa1b9d88660effe50501fa509603693f4fa5655587cdc080e8cd35c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:933cd8e0c95d2b799cd2d7f79f6ca02ed810d003ad461d98d37c1fa7437b74ad
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2459529438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9439320b463e26060941107b4a470296967394ba75dd8f3a936bfc440f893`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 06 Feb 2021 05:03:14 GMT
RUN Install update 1809-amd64
# Tue, 09 Feb 2021 20:26:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Feb 2021 16:00:30 GMT
ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:15:16 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:15:17 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Sat, 06 Mar 2021 01:15:18 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Sat, 06 Mar 2021 01:15:49 GMT
RUN Set-PSDebug -Trace 2
# Sat, 06 Mar 2021 01:17:09 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 06 Mar 2021 01:17:10 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:17:11 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:17:13 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db4edcf0861ff3fdc41851a5a218965ecb2ab6cf4ec9448fb80cc4b6792fd46c`  
		Size: 720.9 MB (720933935 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:751b8860e89a7e6999d74a11dc393620b118057ad881cb87f1d6e3653cb2db43`  
		Last Modified: Tue, 09 Feb 2021 20:48:09 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f01e717591f83c73890556e7a4c77e53caed8daf6c9b0150f497e094a4a698`  
		Last Modified: Wed, 10 Feb 2021 16:06:05 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ffc35aa8c784e2ae1c53bdf12ef4dca08443101be895d09b0fe3dd743f3966`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf80997c587a8af113076c94add4be4d39d952431447634ba07a94332e575649`  
		Last Modified: Sat, 06 Mar 2021 01:21:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bf4e6129fe21a7ad575932f2a76dc0dc6d1beb2f353c58f75c65e41c74c35e`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9644b7f129edd50be8299c9021153e7a54036686fb5987014479a65d0896403f`  
		Last Modified: Sat, 06 Mar 2021 01:21:43 GMT  
		Size: 5.1 MB (5051560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044214cbb3458d290a88f677c47be5f08804c225dde815bcd4ed960101a1a53b`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 15.2 MB (15199849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0b5cd3070da7067e3c89e605aae52c1ebe57b69b6f0436f2efaa3e6d3b589b`  
		Last Modified: Sat, 06 Mar 2021 01:21:41 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69bb3643d207d59a56cdf191a574ea0db42fb3e12ee906a4b31d9512ac81bdc`  
		Last Modified: Sat, 06 Mar 2021 01:21:42 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3499ca15c55e19bd3b457821bc3d8ac8c541acc3699caa9fddc86fe46516f742`  
		Last Modified: Sat, 06 Mar 2021 01:21:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
