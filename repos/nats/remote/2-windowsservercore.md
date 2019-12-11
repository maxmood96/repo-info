## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:bb8453d8412bb5c67ac9cd66f7bc527e02e5de89c6a569c562155fedd1031f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.17134.1184; amd64
	-	windows version 10.0.14393.3384; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:8695bfbe190624bb49dbacf2767ff9fe07ab06422dd496729462e65a0eb56163
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229422573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708cd504c572d596223e163f3f123a37a7063958791895a990d4c0527374f81f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Wed, 11 Dec 2019 14:56:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:23:50 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:23:52 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:23:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:24:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:25:38 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:25:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:25:40 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:25:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:25:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6095b83882ccf9b8fa968e24adeb7b300cf94138c6c34f21c5d0425dc8a63803`  
		Last Modified: Wed, 11 Dec 2019 17:59:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37bfc31cc1d6689ebcc794ca795d6863008d588fb58098bf49718e1c95311fa`  
		Last Modified: Wed, 11 Dec 2019 18:32:47 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a17f634b9f04fb2b01c0eea2f5ab18d0b62a7a4834efc8ffe5db1e6aee5310`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d27ee737d70e216b7a16a3d38df258d540e106de9617f5a4b81a3ca06faa48`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72eca62560c65a1777d29f1135f137eb4cd135f949945cb1fbbb73a7ee5a868`  
		Last Modified: Wed, 11 Dec 2019 18:32:50 GMT  
		Size: 4.6 MB (4579739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5a8a3b69f4dd6d3719dd4e52bedebb7859cc8c9ba8b8f6f42e50f66ce3993b`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 8.5 MB (8529444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f4ff6fea0aa9033ba6fb25adaada94ddbe1e7fb3b82b3ebb9231fa2c1a47eb`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b55c626ec98a1131a7587023e14cef2a1337996e25f85c82331dc0644e5a22`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531969eaaaf4369ad4c576d4862c71e0cc520537edd7744a70f7bc65372feb3b`  
		Last Modified: Wed, 11 Dec 2019 18:32:44 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9a9d61fc03794eb6005d554c25cbcb1286b9699fef11fe0be5e851ad72fe75`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:8d1394d4f2586a41dcbde8b9fd4614db9d4d98d4a6068c90cca278762422a33c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2370299684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598c8951572c322c90229487e8d0bb71106ce065df0d05ea2717164d6b8dc936`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:25:55 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:25:56 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:25:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:26:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:28:03 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:28:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:05 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0fcc6f597904ec5ed4a706026a53ae4f49b0c4403a2ad32bcffffef74a098d`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb32f52d2be0386946a41c3545a20c11d0fa83307e8a990c5321170376fea24f`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484e976dc1a2f1dfc0b302ff83b6f00bae4626b1330c7cc63d7c0f7a9f1a1c56`  
		Last Modified: Wed, 11 Dec 2019 18:33:32 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d9622e2321945cae6465f3dd630fddd302120e3d818a330993729b8917ce4`  
		Last Modified: Wed, 11 Dec 2019 18:33:33 GMT  
		Size: 4.9 MB (4887442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec317fadd39572048352ae32467514419317b35bd72d1e0ce7635bb5edb2e1c`  
		Last Modified: Wed, 11 Dec 2019 18:33:34 GMT  
		Size: 8.8 MB (8840350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f202fe95f354af858faa79537de9ced45bcdf9a87b2ab20f6d003810bf033096`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305db9f7c12c732c7907ecbcd75a03a78e975c9187666d854bd0cdf0edd913b0`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ef83dbdfe3dd965d8344e40e07fa7c2deaa3e4b52f01f2a24916460c2d9aa1`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c871b6d043d414ed7fbf5efecca238d8cca52defd284399e884d21b6374d2a`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull nats@sha256:9504d07894b580a2fb99be201c641164e28693fa7c2867df37fcf9af9a47786f
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5737430879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6658cfedaecfeab92b158f20ca7aa71545cc3a1d80a764e1f7b8490675dcf4df`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:28:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:49 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:28:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:29:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:31:26 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:31:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:29 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:30 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:31:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa11fca135b9d60cf92ac2ccd0a9c4cacd6c45bb607b33b786e27aad02d0a74`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b842ca9abad8f34dd3d712250bdbe2c87fd93732a92681202f4e100bd4e8e3`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227678cc0ef2c8f3f87e09fd25fd1946578a73d85ecf8db095a6b5e9b0d69e00`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44efe6d263710e7df5e1a9d3ec9484256c5142a574e0f3bbbd4b4c22103c5f6`  
		Last Modified: Wed, 11 Dec 2019 18:34:55 GMT  
		Size: 5.4 MB (5362286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6073385b46342a6e9b9307a07a82e3bc1e9608c1abd37e4759b999e18282672a`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 9.4 MB (9354624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb99a78ed2ca0c9a9bbf4782f2d505d9cf39e456031b8d324d7752f39fd1136`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93ff97d636e1e97e91be8221a986b6b37e94cf2725ce56417d19fa542ecaee8`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f570bd7d7278eb21a1c121861c889f17fe6f3f6994ad09706303d5e6cea88f`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafcc2a2ef8ed11d0cf04f9a6d5f865c624525b958123598ef36ad82255ea5d3`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
