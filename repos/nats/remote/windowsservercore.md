## `nats:windowsservercore`

```console
$ docker pull nats@sha256:9d847fd779f302f9d241623f856ab3521eb8d5375d35312ca8a0293987c409ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:50d24781f65efa4753d3f69caa810d9876b7b78f38e89f24316aaf00260288c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718570973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5dd0772263590a54e8fd596675ca09934aba47b6f0562a6df8fcec11d7da36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Mon, 24 Jan 2022 23:18:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 26 Jan 2022 01:15:08 GMT
ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:15:51 GMT
ENV NATS_SERVER=2.7.2
# Fri, 04 Feb 2022 23:15:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Fri, 04 Feb 2022 23:15:53 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Fri, 04 Feb 2022 23:16:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 04 Feb 2022 23:18:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 04 Feb 2022 23:18:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:23 GMT
EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:24 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1e63a09e013659f9cb51a44694cf1487fd0ea2ae5528ca387357386508f2b93c`  
		Last Modified: Tue, 25 Jan 2022 00:07:22 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d2d5bbe3c541fe8decf0e3c04bd30aaa74313119e1269d9b03d461638babbd`  
		Last Modified: Wed, 26 Jan 2022 01:19:16 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3ee08d029d143858e524a3f871d67ab08883f876c9dfb98e00ba4d07896130`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8215fd70836c74bf673367169f6c48b8683e1bf07655ccb33834d5bd9817e010`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c38ade2d53ceeced34948ca25473c5112d3a98d579b3fc97616cf3ab1d1a44`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89942494ebde2b32297c9120eb73fb52237c786054b320ef2253f93595e72e57`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 368.3 KB (368299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886bb1ccd4c447ad4705d7ee2026bca172826fcdf3ac6172f4e3a954b55826b0`  
		Last Modified: Fri, 04 Feb 2022 23:19:09 GMT  
		Size: 4.9 MB (4867790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dc3006c1eb769eefbc435fb9fd9df5c5693d6d6dcb54963d04281196928a97`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 2.0 KB (2008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af99d7e3732a21b5c82dcb9cbf6e9fd0f8321231aa773ed3180fedf3b8df6d76`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f7d7190f43b971dc09434fbc244ad13f02e0cd6fd3baa7e19a601afc3c3727`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba1ff369fef52867e63aa5f9b1afec5c370b95d40580395dcaebbe90fbe3cd7`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
