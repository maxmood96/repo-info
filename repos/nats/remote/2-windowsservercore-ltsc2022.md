## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:ba84c77cfa19323fd377034bb18a360dc69318846089272b1ea586b7d8101aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:b33dad99cd236d1e37cc4eb8ed9206b6316eda4c64187adc7f1e65ffce3cdb72
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2287473702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5d3e602d1e1e318a7bbb885b4a46c7d27f44a285183c5babf5d78687759b53`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 26 Jun 2025 20:17:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 26 Jun 2025 20:17:13 GMT
ENV NATS_DOCKERIZED=1
# Thu, 26 Jun 2025 20:17:13 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 20:17:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.5/nats-server-v2.11.5-windows-amd64.zip
# Thu, 26 Jun 2025 20:17:15 GMT
ENV NATS_SERVER_SHASUM=32b71f33c65cbee21894a2a7b82e5e8f0d7b15071ed591a115637ae9bbf67fc5
# Thu, 26 Jun 2025 20:17:32 GMT
RUN Set-PSDebug -Trace 2
# Thu, 26 Jun 2025 20:17:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 26 Jun 2025 20:17:53 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 26 Jun 2025 20:17:54 GMT
EXPOSE 4222 6222 8222
# Thu, 26 Jun 2025 20:17:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Jun 2025 20:17:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a1c92883cf6e9b17042332de88a3dc30e79476a8df292435d274ff25663a63`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363721f0db417ab1ab377e6bf9123acf262a0b35c2c361e1026c89439c93c089`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5558cc62efdd7b0998e08a4ecfa776ef70871516275984b80a192f2c15ac5b5a`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfa5c078273d6cf527c751ed1c752110b3a862d0f746ef91c23feea7ca14353`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b2cfcd8172bc275be5a4eef1b7fb8b868b5c35c2ae018f62cd580e0a9ec74c`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e632d9a39cdd638851c72936a39eebbcf700962d71ce0fce0ab1a6463fcd76`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 352.0 KB (352026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedcaa6c58043c1e708d7ebe440178de6af7dd752846fe9dadaf8e69dc67357c`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 6.9 MB (6857935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eba4e672ef32c33580896edc49992582d020ca5ee032917311bf0eb466dfde1`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74212ea9e5dfddac2be0bf465d397594828dd1c10415d6c523b647fa3738834`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb92634ba25710d95df0eec641298bc77fbb7eab9879e0681faf82f0e6aa2d8`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecdd379742fa5e86e868683db8922cc7e21ff8a9d87e7e55eec7c3277575a77`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
