## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:d35b6c4a3418f8ef1ba66c3bcc1a8b938fa440fd3718b2a63b4f66d4d9e2ad1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.3568; amd64

```console
$ docker pull nats@sha256:93e77d94d5181b2e8ca9efbacd8c6ef9401b54c6c318b9dd23b7e5751e1653d1
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5743587455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28335910c356ede194b2dcd9233b435a9cf6f610dd9c49e62c6bab814e302781`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 18 Mar 2020 12:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 18 Mar 2020 13:38:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:26 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:16:27 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:17:26 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:19:04 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:19:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:19:07 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:19:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:19:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a5d20b7a2294a0d2631f74f49fc34574484a692913559546ef0bceae789fd7a8`  
		Size: 1.7 GB (1658775203 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8cd5aa189dca96a2d4bcc0e2516d85f8a69d277957f44aca08575ecf42e5bc2f`  
		Last Modified: Wed, 18 Mar 2020 13:22:17 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddde0325982310255792cba68184203cd656b044bf4f46ab5c1ebf779122527`  
		Last Modified: Wed, 18 Mar 2020 13:42:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d2e783014460190d162f128fa5710a117cd9136ff0582c542e645c5f0b10f`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0a23ecd71b35608af4c4e06f1857aab4211c34048dde0a2072401bc8421176`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9948d714ad0c8a48c12fe7b9becc3fabe09f61d4d66bd75cf77d91316713000e`  
		Last Modified: Tue, 31 Mar 2020 21:20:24 GMT  
		Size: 5.4 MB (5384998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f47e480e660c2de16210e4a70aaf550bd0dd240bf43f1766a7049cfe020cf25`  
		Last Modified: Tue, 31 Mar 2020 21:20:30 GMT  
		Size: 9.4 MB (9431821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d276126def9ffa1ac85e80e3ce86f78dc9f815bf1241f060c953972b16fe8459`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6342f41571faf0fe60bbb2d11b642f0a8499c91ee7b7b48806b4851a5ebd95b8`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662962efab83cc3a58e4d9c59b9e23abc78f4f8634c5ea2d5b87034063037ec9`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a4c33960d69a58662fa5a7dac06bd5ceaa709df8079062bf9f684318c0c1b0`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
