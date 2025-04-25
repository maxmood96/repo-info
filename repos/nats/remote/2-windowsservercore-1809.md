## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:4ae66a1afca1485f7e5ef943f427685142d5ce607c4caecb5a0456e3a2625cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:864cd49a9319a3d243c7945cc4b1d847eeb62fc7ed3bff149dc06d3c11d80e98
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172714568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ee4030f14e129a49644c86c19599562d252f3c124fb474a5bb9ba9116a2acb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 25 Apr 2025 17:53:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 25 Apr 2025 17:53:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 17:53:18 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 17:53:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.2/nats-server-v2.11.2-windows-amd64.zip
# Fri, 25 Apr 2025 17:53:20 GMT
ENV NATS_SERVER_SHASUM=27bc84446495ed13983a86044d77cc24e4d5661a3ea3caaff3003c2d19dc3db8
# Fri, 25 Apr 2025 17:54:01 GMT
RUN Set-PSDebug -Trace 2
# Fri, 25 Apr 2025 17:54:20 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 25 Apr 2025 17:54:21 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 17:54:22 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 17:54:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 17:54:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5220f32a15f4b9e4e60e00b789f7e5aed30ed16d768671ab81f2f7c847ce188`  
		Last Modified: Fri, 25 Apr 2025 17:54:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0adc223c6b3350c772df065f39904be980c1d151c04e822e6a524cae9a559b`  
		Last Modified: Fri, 25 Apr 2025 17:54:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e092e70456ee50a2b46c19beee1220448b3262ea35a4dc2762cf6dc92372d2`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe1399f73f5fcf68f18961cca3a08258165d8d8540bdeaabb55205a570b3ba0`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3a098a1765813b5d39dd0a8b00f285c110efca73a5308620bad065b8fe9782`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a9eb31776168317086fe75476b44574d1431a1e21f3d07a85279eafdd7341c`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 344.4 KB (344375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475c0b5a54a450e6b02e46614be9dfa7e5c0f7df6b4f4a34cf03889a90c6002`  
		Last Modified: Fri, 25 Apr 2025 17:54:27 GMT  
		Size: 6.8 MB (6832182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e6c6bd274e68a31e4fb7c629bd35c2bb6ef85a104202ba5864944cc76411b4`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae5da4614649984507429fe2b6390a40f34095fd8fff099faee59172c99e03e`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc162497b3b567edf013a6577d06c352d56ab30ed7750e30f3161f5a2b5fa4`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4b4ddd55fce7bccd5d5d53bfcb816dc5f0d980b8c904a6ef424c27bb6fc10a`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
