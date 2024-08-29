## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:cb6328be8b110a77e133cf6563ecf60a3fb05f2935bc0e96f8a5dd2f7e8b48e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:9fad6c4863943446d592590e79cb11ff553e6fc191778720110f756df33657e2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251857590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be6364da5c3d0e9e048ada69b72a0838e7b1008175e1ca31fda37c7638df8aa`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:45:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:45:39 GMT
ENV NATS_DOCKERIZED=1
# Thu, 29 Aug 2024 22:14:58 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.20/nats-server-v2.10.20-windows-amd64.zip
# Thu, 29 Aug 2024 22:15:00 GMT
ENV NATS_SERVER_SHASUM=8c95a904e0c2c7413d3671fca3d41cbce6d71af797362c394a24bbb15f95dc7f
# Thu, 29 Aug 2024 22:16:15 GMT
RUN Set-PSDebug -Trace 2
# Thu, 29 Aug 2024 22:18:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 29 Aug 2024 22:18:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:14 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a01ddac643cbd49eec6aff688d037d7a551e855201124b4b91f640dc4af4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a022697aef59a6692fd1a03334c036f85c795eb0dc574e189565788b877520`  
		Last Modified: Tue, 13 Aug 2024 20:51:12 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941f3a5cc11d8a7fbfbd4e829b3c7a9ae76dee2abaae9d6e868e1748486f3368`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ca51263da3a2de900934ec683721597afdd2d2425a83a5c9ab3d3c92718c7c`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011007d5fc07497ebd202455eda52967d15dc7cd82ddaaaea4a3e065ac0dc87`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9073b2d25f44c8c42efcd2187bd5b55ab5b79fa77d5fafddb85410f2814fd691`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 471.9 KB (471885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af0492ad69b1e8bdd0d23994a4a3a34c734c05dee99e4b5ceee2c7469095dc2`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 6.2 MB (6169168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970f9ed7f958aecdcd2ceefe686404de25c77f9c9ac0e2bf106b9e5e45ec23b3`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a10dad646d9e6377922ecc8e09974aa0a75d43fe346d96b58b8fa8e743c2513`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee14dda7874c31357043651dbb5a77d45efef0ad13d61954d861527697a56367`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b340e1c0e1043e7c180bbea7fb252f25d08b982896a61938d5484aeba71de9`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
