## `openjdk:22-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:682edd491bee608b571a7581a4424fbf8fd692fe557c7f0edb6483eb489d4210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:22-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:08ff8680f0c8f3b1223e0e34e87231d4c982498ca5abfdd42a07fbf8c8ae8bc2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268328593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4233dcfc4e899e5b60495a929399815dd5b18b55271a6604a2b96c7b5cbfc585`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 24 Jan 2024 20:49:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Jan 2024 20:52:33 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 24 Jan 2024 20:52:34 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 24 Jan 2024 20:52:58 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 24 Jan 2024 20:52:58 GMT
ENV JAVA_VERSION=22-ea+32
# Wed, 24 Jan 2024 20:52:59 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/32/GPL/openjdk-22-ea+32_windows-x64_bin.zip
# Wed, 24 Jan 2024 20:53:00 GMT
ENV JAVA_SHA256=849804cc5a37d7768413d7e7a0e8088f31eb6ccc91b7f0fb7f517cefec0c5931
# Wed, 24 Jan 2024 20:53:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 24 Jan 2024 20:53:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d1075a5b18138b30999ecddb855e1498321e49619e141f0a6a7830c2a84afe`  
		Last Modified: Wed, 24 Jan 2024 20:53:54 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47cd12f92580fd02469b916f4937ec592d65a28f2809eef165a6d0e3cce5e4f`  
		Last Modified: Wed, 24 Jan 2024 20:53:54 GMT  
		Size: 502.3 KB (502311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12441b1f8e571ebbf5318d2bbc6198b2d3ed7858f178e939b3cf19f2cad94a4`  
		Last Modified: Wed, 24 Jan 2024 20:53:54 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80907d85aa541acbae5b2c76f3b0075bb2aa3d9058f92e5cf041ba5ab92601b`  
		Last Modified: Wed, 24 Jan 2024 20:53:54 GMT  
		Size: 349.1 KB (349053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa5872420ed222af9955bd5d0b7070a5f5bcde0ad6ac93473aa61552920b517`  
		Last Modified: Wed, 24 Jan 2024 20:53:52 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c6a2642490c8094d6c04dd030316763f31f1a58b740e902ec1d097fc68adba`  
		Last Modified: Wed, 24 Jan 2024 20:53:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84c860ceefc20d6d52f6693b91ab533a1c1510f725a5105acaba6f8e8693cbe`  
		Last Modified: Wed, 24 Jan 2024 20:53:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62de7e2f3c261628d0e8db1cb8826bb20f667fee422bd7c72e69229240f250a9`  
		Last Modified: Wed, 24 Jan 2024 20:54:03 GMT  
		Size: 197.7 MB (197746881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e752e8bcb132949b7d6e31eeae2fcbee8c3e62a0eb5fccfb0fc206b7005c38c1`  
		Last Modified: Wed, 24 Jan 2024 20:53:52 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
