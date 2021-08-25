## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:6c691bb80388e286a736ac34253f62975b7da9bd039815b3fb7b82f3ebec4740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull nats-streaming@sha256:d6ba04cfbedbf1ce9e219918c40dd6989e1d50a8e2398bb1d69fb19597056636
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2694026981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54951a15532bfdfb9b767cb2b92cb384b91b1c66f44a6cfb259769a168458b7f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 25 Aug 2021 13:46:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 25 Aug 2021 16:05:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 25 Aug 2021 19:31:01 GMT
ENV NATS_STREAMING_SERVER=0.22.1
# Wed, 25 Aug 2021 19:31:02 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.22.1/nats-streaming-server-v0.22.1-windows-amd64.zip
# Wed, 25 Aug 2021 19:31:03 GMT
ENV NATS_STREAMING_SERVER_SHASUM=4516852b493111b73ec06477be4a27e66f5abc9ca1ff4dd2b970232271611264
# Wed, 25 Aug 2021 19:31:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 25 Aug 2021 19:33:24 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 25 Aug 2021 19:33:25 GMT
EXPOSE 4222 8222
# Wed, 25 Aug 2021 19:33:26 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 25 Aug 2021 19:33:27 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:985da5cbc0735e1c422e766af23125ba345f431cb337ea43ec32298d0bb8e4ea`  
		Last Modified: Wed, 25 Aug 2021 15:45:02 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3dbdd68a4b0c278695b3e1d401d7eddfb0f0e3aa1e28aed88eb700059648f8f`  
		Last Modified: Wed, 25 Aug 2021 16:11:02 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d02eff460789c6fa51a517221660dddad01c753689cf4d911deed4be925fdfa`  
		Last Modified: Wed, 25 Aug 2021 19:36:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67c923b3231b172039016dd78d64494840a068f83b7c2eb0610b3916e0f880d`  
		Last Modified: Wed, 25 Aug 2021 19:36:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c73a6e9ff96bac535744e077e3966558cf33b742d3b384e6b77e72d96b4a49`  
		Last Modified: Wed, 25 Aug 2021 19:36:40 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652b4bfafc795b6a09e751ef642f31936038547b6223596beda9dc1bbd74f2df`  
		Last Modified: Wed, 25 Aug 2021 19:36:37 GMT  
		Size: 372.7 KB (372655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d3118388d00fe0ce41388dbed69f505de317c0d9a6551664b34909e0308b85`  
		Last Modified: Wed, 25 Aug 2021 19:36:48 GMT  
		Size: 7.6 MB (7645717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35fd537c3fc591dceb1461535c52fc98243ac3b3fea45db58c6ebc492862440c`  
		Last Modified: Wed, 25 Aug 2021 19:36:37 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f9050479fb189fc4a85ae128bcc6a114f42e9139901390f4c6ef669c1ce49a`  
		Last Modified: Wed, 25 Aug 2021 19:36:37 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e587562615088e9b1f845a826539d4c81323caf3b84153496ac0f3c1c8afc45`  
		Last Modified: Wed, 25 Aug 2021 19:36:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
