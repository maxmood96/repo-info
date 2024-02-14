## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:b5d4fe3f6ce89e3bcf22da05af606fd96758e494479efb60164c96fa902f6c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats-streaming@sha256:302e53126d9b9b2338ce8da329cba1b502614202b841d472aad239ea6df81ffd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2089125234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc974b41ee9acf444c77c43307544e9974fdc65c67c07b138f2b1579da78178f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:12:33 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 14 Feb 2024 21:12:33 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 14 Feb 2024 21:12:34 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 14 Feb 2024 21:13:54 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Feb 2024 21:15:49 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Feb 2024 21:15:50 GMT
EXPOSE 4222 8222
# Wed, 14 Feb 2024 21:15:51 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Feb 2024 21:15:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b3259e00f84e65b0d749ecdb1c509cfaefbab41e8cb1f6543ed1330430502`  
		Last Modified: Wed, 14 Feb 2024 21:16:26 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61718a6e18dbd65ddf3f59fa04789e1f9acaec2f5cf25ce8cb26a3dd44c3282a`  
		Last Modified: Wed, 14 Feb 2024 21:16:26 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564a5ffeba7098ea453e541f16fce989d9bf9443e53b4a7da19cb16428f4d786`  
		Last Modified: Wed, 14 Feb 2024 21:16:25 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dab53e0e6ef70ca249e6e56bdd06de3a5697dd6cd838002e9be78c4e619e93d`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 444.5 KB (444454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d86bd8e6e200eb4bd3eff9524dd7128bfb365522a7df4a2171325010624067c`  
		Last Modified: Wed, 14 Feb 2024 21:16:25 GMT  
		Size: 8.2 MB (8221053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992357c2fc0a12399ad77caf56b874e927614befdc2b3f238971b92a4134141f`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd057cca0f909355ef1eaa7ea42b060645a1ebe3af92ea98a4fd2c16dffb9be9`  
		Last Modified: Wed, 14 Feb 2024 21:16:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7765553db67243ec6679030d92c818bc160158ea025ce173c15d19bcdb0f0baa`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
