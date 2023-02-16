## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:9820bb90c2166b7b3e91b1b790f775a84fb8e983bde750d363f97ca1a2a368f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats-streaming@sha256:1aab8afec65a4c816b5c434ed62ec46e193dc725cb5d8038f614b91decb4bcd8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1971619439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472fb0593adab3b9d72b160e41b61f35a9fbd55e08520929c06c0bac60d71d52`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Thu, 16 Feb 2023 00:42:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Feb 2023 02:04:44 GMT
ENV NATS_DOCKERIZED=1
# Thu, 16 Feb 2023 02:09:24 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Thu, 16 Feb 2023 02:09:25 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.3/nats-streaming-server-v0.25.3-windows-amd64.zip
# Thu, 16 Feb 2023 02:09:26 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b25aab68b84cba76e3edec5d524d2a792f460127d159ecb4d2e6168c7635c10c
# Thu, 16 Feb 2023 02:10:30 GMT
RUN Set-PSDebug -Trace 2
# Thu, 16 Feb 2023 02:12:06 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 16 Feb 2023 02:12:07 GMT
EXPOSE 4222 8222
# Thu, 16 Feb 2023 02:12:08 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Feb 2023 02:12:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531f6c3ad9784fc2870ea5ca08c4adccd9318602ed534d822e12b8b658a7b0b6`  
		Last Modified: Thu, 16 Feb 2023 01:37:30 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724509671085dbea52985b930945ecf6cb7694ecee9924bc0226a51a4e01d8a5`  
		Last Modified: Thu, 16 Feb 2023 02:08:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee234575c48fac9b1995bc758b521560c9756ed1bbdaff966629a2944187b4b`  
		Last Modified: Thu, 16 Feb 2023 02:12:56 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307129fdf42d0415cb74930e36bb0c754a7096403648bf56cd124f0ab1f28d11`  
		Last Modified: Thu, 16 Feb 2023 02:12:56 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4857c6bfecbb25152eb09de8857f11922bbfc8a9a18cc146ce4d36cd55864ac0`  
		Last Modified: Thu, 16 Feb 2023 02:12:56 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d13f2a033988cd2ca5b154b5994afe1d13ddf06586a5dcf69e197bf8b14531`  
		Last Modified: Thu, 16 Feb 2023 02:12:55 GMT  
		Size: 508.0 KB (507994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7d6c54356fd3c9dd35aebb1965fe828d6352510d5555e75286108f03f520bd`  
		Last Modified: Thu, 16 Feb 2023 02:12:56 GMT  
		Size: 8.1 MB (8142357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25008fe73ce204b46f7b6a0f89c7e5009a880ace2fa4c89c12c749d7f50e37c0`  
		Last Modified: Thu, 16 Feb 2023 02:12:54 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000fc36a3148fb357f3b1e548db26e11d332f8745e2a952a74da7bc2e3e38d0a`  
		Last Modified: Thu, 16 Feb 2023 02:12:54 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e27861647c501645b9b5ffbcac548624b264d4302c3e431da7201ac07d8d3e8`  
		Last Modified: Thu, 16 Feb 2023 02:12:54 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
