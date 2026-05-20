## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
