## `nats:2-windowsservercore-1803`

```console
$ docker pull nats@sha256:01aecc0fbccaba0900bf9857189a1720a3055f6973ac7cea656b09a42ed2bdce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `nats:2-windowsservercore-1803` - windows version 10.0.17134.1184; amd64

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
