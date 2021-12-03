## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:b78771ff3e48ef90ba8b2f574b397da1d6d109e52976b268bbdb9feca65b219b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:fdcf94ff9f56185e96e2d34c14a819b244e403758d7013151609dbfcb360c5e2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278478824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af4423e4e1bb0fc02b0a493270852db3199a402c345f19d3d87a57cbfe0845d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 14:32:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:03:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 02 Dec 2021 23:17:38 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:18:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:20:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:20:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:20:20 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:20:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:20:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6f303e73635c7923a8c64f8938e7ba4c10210fd15a6ce63aa8a62d5a8ea8c0a`  
		Last Modified: Wed, 10 Nov 2021 16:21:33 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5db4062c12269959ca71caf00b70e9baebf61b90c49c74db0e2cdb04cf83e8`  
		Last Modified: Wed, 10 Nov 2021 17:06:51 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f30fc57b535f4a7dc20a4d1e1b43e91c4163d15d8d67ce035aa644e312a15e`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74da680686aa5c2ba65208b2c6cdcd1bbd18c45f58aaef8256cfdf8cbc32a03`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10729ec66b57b11f89be7b5130e80d980cf37a601f683c399e671662cac1a110`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0763c02a9f5763cfe1dd77eea65dfc154b93bf42b877a34e753f1c2449c3e70d`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 359.0 KB (359036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c875dd2ccaee8f5e6d8ccf71f31d170077b75efb53b7e75b3fab222c6e823ef9`  
		Last Modified: Thu, 02 Dec 2021 23:21:40 GMT  
		Size: 5.0 MB (5015739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa98d451592563d3d6480b9a59e70f5f5fee7ea754916118efdca39bd399a86`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.9 KB (1938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b28f7a1a71fd2916d9a8178df2cc31b372a0c5b39b207c9b5ba959495536b33`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24851a6f0e21f835dc6befed813f920721c0485952726b8ef9ffef97d32fe88c`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa050e14310da7375267a60873fd4a6aef2356ad89388b9737efc083526bdf`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
