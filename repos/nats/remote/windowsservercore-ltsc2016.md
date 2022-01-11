## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:3d337d85e45c503e13f57109f85de0e1c916fc6781cf7bbd3f40ccffd0fb664b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4886; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.4886; amd64

```console
$ docker pull nats@sha256:e476d11dde611fc9b39eb6a45798c2e503fa1bfa4ece59509826bfaed6a4cbe1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6283541821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084594550a22f2aa624e5b2e740a29366a6846c2e1f194854e6e32270f5f0edb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 06 Jan 2022 14:33:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Jan 2022 19:57:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Jan 2022 19:57:40 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 21:15:53 GMT
ENV NATS_SERVER=2.6.6
# Tue, 11 Jan 2022 21:15:55 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Tue, 11 Jan 2022 21:15:56 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Tue, 11 Jan 2022 21:16:48 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Jan 2022 21:18:24 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 11 Jan 2022 21:18:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 11 Jan 2022 21:18:26 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Jan 2022 21:18:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Jan 2022 21:18:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8428508ffd63b4af1ba690ec41e82a116f10ec6c3fb70962348f5448d42e5835`  
		Size: 2.2 GB (2208216859 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25aec0a6b64c784bf7521344203ee5def4d38eedfdd68f4b452d3250b5b9ddcf`  
		Last Modified: Tue, 11 Jan 2022 21:19:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fffdd310a93f98578e45ffbf8e22c031b37efefcc042f21d2a63c2a77c4ee3`  
		Last Modified: Tue, 11 Jan 2022 21:19:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15052497c858a1a8b4a8159d05850fbf43551aad161e61ae0fd6880c46eb4556`  
		Last Modified: Tue, 11 Jan 2022 21:19:44 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080911a4b1ac40e1f062d68ed70319860e88ecb9abec2aef41d0bc3bae89098d`  
		Last Modified: Tue, 11 Jan 2022 21:19:44 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e79cea19a92f33c59acbcc8f501e9acdb5985bbad5b03ccd1190848ae1b4cf1`  
		Last Modified: Tue, 11 Jan 2022 21:19:44 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0544e04ecd7b6afc6366924310fd892736faf1983ea2ee9e40efd31a0ec502`  
		Last Modified: Tue, 11 Jan 2022 21:19:44 GMT  
		Size: 337.0 KB (337010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8906d4ca25b04680081cc6af81b8eec86a9756abb72e21ed2785f82372ba7c58`  
		Last Modified: Tue, 11 Jan 2022 21:19:43 GMT  
		Size: 5.0 MB (4988964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a01b43c4c8c06f528a3080b9f4d396d196ff851a603ac22c9ce560c3d5b082`  
		Last Modified: Tue, 11 Jan 2022 21:19:42 GMT  
		Size: 2.0 KB (1973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e156e4bebcfed633295afa0f9dacd6146736cb7de973581f01931fdf6d5f5ae`  
		Last Modified: Tue, 11 Jan 2022 21:19:41 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3ee9fcf4be90533587d2a54238465fc8f6bad0744784041f675b2e97a93bb9`  
		Last Modified: Tue, 11 Jan 2022 21:19:42 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e44c694323da6f62bebd7b52b659731c89b1e15c15e5c345ec43e24cba28f7`  
		Last Modified: Tue, 11 Jan 2022 21:19:41 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
