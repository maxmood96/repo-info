## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:ba4b48de17ea4bf3dd45a183af928cb7cbea4686b5c20b8a2bb2142b1915ddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats-streaming@sha256:c9d3520c171dd02c0d97416eb27c7c643ca56cef5f496c171ec59ae0c548f4d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2080443117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c708bba3694fbfcc1923767269f4308324f4f942b5a0a39dddd01d843d37c15f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 02:40:26 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:44:29 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 10 May 2023 02:44:30 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Wed, 10 May 2023 02:44:31 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Wed, 10 May 2023 02:45:56 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 May 2023 02:48:28 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 10 May 2023 02:48:32 GMT
EXPOSE 4222 8222
# Wed, 10 May 2023 02:48:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 May 2023 02:48:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cee93ab2781cfc08e135a3a7ab166e5342ee6817c34fb47e0662c085bbc29`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5856405e72972496afbf612f06bd9c56483b3ffdcc1f1f765a39b96373db164`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f34a19213ebbfd3e71144d5a8ca3ed8d42f0b17b50d998fc496d16828c830b`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ea34cc555f2d95a16c0b18af06b76a789b93880c77e9f95b3a7472f4dbec62`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a347fb78d623251d604dd61bc05b7dcbe9d8f08593aae32ecc84762a7a9a1`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 424.7 KB (424664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de400e4f555d84e45ee3fc33ae8599c0d8b5d48accb86db6ca1abad19479546`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 8.0 MB (7971913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c10a5c8c435e5a841c49d51114c544a1c657deb0b6aa76fae32211bece286`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7079014b7aa61da27a4c38e1027fd7939ff72e0b76977b2a30bd941a3cff01f4`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e78054f97dafd0ca0b369edd7447dd3ab27d54e1d5455754a3a33d48516fc7`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
