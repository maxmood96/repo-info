## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:bf19d4980ecf00f544f3dbf73f06c7bd88adf27b537b1bc2d9d48ba37a850395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3866; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.3866; amd64

```console
$ docker pull nats@sha256:0bface4bb75895f9199eb5d6c903d4dfd6b33de95397efa57b8a68ec24d27c24
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5757484291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96755e6aa9687beb1cbc44dbd19b93506cee5eee3735391e15cf738d0cbde5c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 Aug 2020 12:23:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:13:46 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:47 GMT
ENV NATS_SERVER=2.1.7
# Wed, 12 Aug 2020 15:13:47 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Wed, 12 Aug 2020 15:13:48 GMT
ENV GIT_DOWNLOAD_SHA256=1e1ad5c00929cc145341fd65f8b0a41a38e942b9b9fd9fdb0216c47654afdc8f
# Wed, 12 Aug 2020 15:14:51 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 15:16:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 15:16:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:16:27 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:16:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:16:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:44c31749d2d4be3aede3e54780d9e54b5a7eeaa617e1adf027e92fce2ebf0f2a`  
		Last Modified: Wed, 12 Aug 2020 14:52:35 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966377bd81e347a691363116c353d48b02f40befd2b38ce2a9f31459dfe79978`  
		Last Modified: Wed, 12 Aug 2020 15:17:51 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ff217b5d5bc8c8fb41e01c3eba376734cd65c568cbbdbad4f1b8ccb343094e`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6904aa06a0a62b5c80e74f511a5c8873ab6cb3f831cb07b8cb7d11c1dce548`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a4e430ecc8ccbf747007a59ada2a242e3bd877de9f9f8340b68fe64dc16006`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f21f629b2ebf35877201ffedc54c17cc42ed1ff6d5a1b103cbc509fad733de8`  
		Last Modified: Wed, 12 Aug 2020 15:17:49 GMT  
		Size: 5.4 MB (5391292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc789bee248747dae7caa25fcef8fe71174cbda62c0fb0ce6cb3ad9614312de3`  
		Last Modified: Wed, 12 Aug 2020 15:17:49 GMT  
		Size: 13.9 MB (13935154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55d61fc54488846a758ce45ea5d71a778d33da5666007bdd5ed760d5387bf20`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.6 KB (1622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043116cc2890a72214497abfc0adc7a287ea917ad5c29d71c63318e068e9d4e`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f6d4aab762740fae48f892182795785925e79465defac676880314cdeec2f`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994575a0eb610ea577e32ef234217e7cc59a26bd3cfe05726ddbfb9b7df25e93`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
