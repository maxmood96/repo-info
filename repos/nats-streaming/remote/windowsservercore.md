## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:13afbbc7fb819cb2ef32a9925a884f999e75c196066146f5686390c8a9801a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats-streaming@sha256:7085b9f85756a82377e6cef8cbf748446e50faa28e08fe53dffb096baf8f80f9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1659033159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3b38bfa5f25baff80d98e8f97d4219cd8ce0d63cd600fabcd8f3618698b10b`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 19:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jun 2023 20:17:19 GMT
ENV NATS_DOCKERIZED=1
# Wed, 21 Jun 2023 01:50:48 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Wed, 21 Jun 2023 01:50:48 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.5/nats-streaming-server-v0.25.5-windows-amd64.zip
# Wed, 21 Jun 2023 01:50:49 GMT
ENV NATS_STREAMING_SERVER_SHASUM=709b481bfa3537dc7941490365e065554f19c7029830d765ef49e8cd16657b75
# Wed, 21 Jun 2023 01:51:11 GMT
RUN Set-PSDebug -Trace 2
# Wed, 21 Jun 2023 01:52:19 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 21 Jun 2023 01:52:20 GMT
EXPOSE 4222 8222
# Wed, 21 Jun 2023 01:52:21 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 21 Jun 2023 01:52:22 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3929a070e5d6b9cb95587cf41492d8ef77aaa7e9f90fa3cd1b32619fae5debc2`  
		Last Modified: Wed, 14 Jun 2023 19:51:36 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc032b2e13168aa149afc2fa80f0046e2522b46496b0b11ae5e6e6cde6afec87`  
		Last Modified: Wed, 14 Jun 2023 20:19:35 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32142ab146bb620b0a96a3146636a5c61d0f09307ffbbd8320e1c2f540456ac`  
		Last Modified: Wed, 21 Jun 2023 01:52:59 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f314de8e17d2bacfbacc35b263435a140f1d3e2541b4d310e58df7919844538`  
		Last Modified: Wed, 21 Jun 2023 01:53:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc60267aa9f7b9dc1fd6234e32b9dd78d74b882e3afb0f3ae81e0d90c6352aa`  
		Last Modified: Wed, 21 Jun 2023 01:52:59 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a91cb9c2658cb44eadb238562f9f857d77dd797858ceea0144e5e42f3c0790d`  
		Last Modified: Wed, 21 Jun 2023 01:52:58 GMT  
		Size: 320.6 KB (320632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067e9290166af32eae44d675831538c6a8ba358e4422025f56d449afd422a9ad`  
		Last Modified: Wed, 21 Jun 2023 01:52:59 GMT  
		Size: 8.1 MB (8081626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b2135b2017461fa13ed6c922905c91269f915461cb0d61bff57c011166e0b9`  
		Last Modified: Wed, 21 Jun 2023 01:52:57 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc9e6b6414e068c7dda38dee7aae029a4ebef3d9e37eff0a80b7c9b9cfa4a29`  
		Last Modified: Wed, 21 Jun 2023 01:52:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add238b48ced45161881e70ca2699d3ccd8b9a6a78816290d2a8ad73c30650d4`  
		Last Modified: Wed, 21 Jun 2023 01:52:57 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
