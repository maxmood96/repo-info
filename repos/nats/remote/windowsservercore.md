## `nats:windowsservercore`

```console
$ docker pull nats@sha256:fdeb661f9c106521de9c0e4ee3957743c6a01bc53dad9a910000b17181c280cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2183; amd64
	-	windows version 10.0.14393.4651; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:6ddc52d3e875f9554d59a33b5d1104fb42532c547d4d8f5206d8c781bbb5a6d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2692032377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79640873e27f02ba95f3fe49da175373a8a9ad553ad317e65a82f3f013c619d3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 13:14:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:40:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:14:08 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:14:09 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.0/nats-server-v2.6.0-windows-amd64.zip
# Wed, 22 Sep 2021 18:14:10 GMT
ENV NATS_SERVER_SHASUM=deba2c9db4dbbd820bc351efdb6cbe36a52e88dae6fe504e71fb1003012b733d
# Wed, 22 Sep 2021 18:15:06 GMT
RUN Set-PSDebug -Trace 2
# Wed, 22 Sep 2021 18:16:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 22 Sep 2021 18:16:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:16:38 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:16:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:16:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6c4091e033b8590db7b89fded6d31ac2224162744daa4d7a7a66cbebd4b8c228`  
		Last Modified: Wed, 15 Sep 2021 15:04:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c75402e6fab70f623ca8becfa5bb563e5630bbb4dac8adb11e385d75e171aed`  
		Last Modified: Wed, 15 Sep 2021 15:45:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07141c7bd13ff557354ae70dc72a7227ab19912c70d3c3cc4bec996a7655fd56`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77418125b04da08a7f44f805ad699df7585eee0222040b996e32ec745a6fb697`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9e4e9c985c834ccbfff1ff7ad155154a05369a7f919fab1c5bbfddcc785707`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3620819d7f2e3d530e1ec4c86284a111b32e0762c5d2c6e4143432838d163d5d`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 365.8 KB (365754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d12675a3560b6328442167831b90f74ab44ede0be36abda31297d4e58d10cc5`  
		Last Modified: Wed, 22 Sep 2021 18:20:24 GMT  
		Size: 5.0 MB (4955548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55c4436ed073542d01e386f4bc5f03d020ecd52dad574b31970789141c1de78`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccb89b26f377943b12e1fee4cdb39bb72bd8df511dfae8a449036522f487945`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053b9e214271ecaa071b0a98ecf97a0b2f5855eb783d34be9bdd2531fd2129e`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ca19ac6ce761f376a3c541e1df6f545e7d529741b14181e8f220f419c88ec3`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.4651; amd64

```console
$ docker pull nats@sha256:314877eef7766a391b52ecf69b974a4748aa31d2fb95fbcb0e1a5d8e42c69377
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6281135566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed46a54daf861376ae8610d058e173573fb604a26caaf14af1c5499bbf441eaf`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 13:26:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:43:15 GMT
ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:16:59 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:17:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.0/nats-server-v2.6.0-windows-amd64.zip
# Wed, 22 Sep 2021 18:17:01 GMT
ENV NATS_SERVER_SHASUM=deba2c9db4dbbd820bc351efdb6cbe36a52e88dae6fe504e71fb1003012b733d
# Wed, 22 Sep 2021 18:17:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 22 Sep 2021 18:19:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 22 Sep 2021 18:19:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:19:45 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:19:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:19:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5796468f91731000e9a76e836156826a1cd4ed963bcd80e6558c538a12c2132d`  
		Last Modified: Wed, 15 Sep 2021 15:05:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611fe9c559abed986280087eef7d362a6ecb9ad281b1427395fdfc2d99d3d9c4`  
		Last Modified: Wed, 15 Sep 2021 15:46:29 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88fe5c5a961345978d08184ec37560319c1f229ebbb4d863376aefcbad7b4b7`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2304c6367aed5770ee0a8bd54e7dea8f2a203e192b70eeed63cd3408617f5b`  
		Last Modified: Wed, 22 Sep 2021 18:21:03 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d959edd2154d9d22f4a4c4012edcd1822a540ffb5b202b6558510034cd763b13`  
		Last Modified: Wed, 22 Sep 2021 18:21:03 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7fe2b4f2c28b84cfc71adcd6641ee59d1f42e7ed6931b962ec99f025abbee`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 342.7 KB (342699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a306cebcc4ab9ab2ac8339cd5d2b9f688dd69ec9868ff507dd8f90cb3fdccca`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 9.5 MB (9451560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b41fa3135fdcb6be75fbbd16394a5b9a17c1f92002f24c09376761f8147244`  
		Last Modified: Wed, 22 Sep 2021 18:21:02 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a91141728f944a1bd37f7c330b23c424cb2c8bde47c1448773a1e6bd5632ad6`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01e4512cffc332936bddbe616ef049e8f641e12912cb81575bacb8189e483c7`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a87f3457dcdf6c46117821892a75a957ac670a3efc04a713b772bc37c6d150`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
