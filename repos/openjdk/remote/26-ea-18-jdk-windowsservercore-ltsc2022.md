## `openjdk:26-ea-18-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:96f5eb1164cbaa19996a27a2b4416c0766266f6a06acf54167b9bdca254bab10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-ea-18-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:8181b29d8538d56ae8b4201be7c4f48b2babaee45cb41cbcade2fb0b4f685bc8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2504440436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b7b00c5b8fe7bc90b4358dc9c17ac9a4a7b7815eb2640707a8bd2a6f8d61fc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Mon, 06 Oct 2025 21:04:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Oct 2025 21:05:22 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 06 Oct 2025 21:05:23 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 06 Oct 2025 21:05:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 06 Oct 2025 21:05:31 GMT
ENV JAVA_VERSION=26-ea+18
# Mon, 06 Oct 2025 21:05:33 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_windows-x64_bin.zip
# Mon, 06 Oct 2025 21:05:34 GMT
ENV JAVA_SHA256=463cf324498dd66ed66418be8d8e730b4ee17b323f86d4df926264b071118dbd
# Mon, 06 Oct 2025 21:06:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 06 Oct 2025 21:07:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12bf9cb641edf8b33ed40a6dda5a202db5a83cbbdacabf7df86098ed18c2a0d`  
		Last Modified: Mon, 06 Oct 2025 21:18:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b48b5f7b459707ab739ab9a20515a8811b09add031ef9f9c98f6b7954b5bf0`  
		Last Modified: Mon, 06 Oct 2025 21:18:05 GMT  
		Size: 369.8 KB (369828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c6c54cd6d6d8a9d96f72a8644c7c2ade789adbe0cc799ae39cfa3ba8aa39e0`  
		Last Modified: Mon, 06 Oct 2025 21:18:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09673502a3897c2654843903e655dce169ca71bd0d53c3608d485a17a8c49e42`  
		Last Modified: Mon, 06 Oct 2025 21:18:05 GMT  
		Size: 351.7 KB (351653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834cb74720298b36d45aee6a78dc411fb330d5c10940d84d4aeb579678dca2d4`  
		Last Modified: Mon, 06 Oct 2025 21:18:05 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811ae4776db4caf5e17728bc6d676c900bbcbe5a1c4f25a6de0075faaa560b5d`  
		Last Modified: Mon, 06 Oct 2025 21:18:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3c85b1c89f5c6a862bdb5d5c3937874a010b63de96c18169dba906cfd5ea87`  
		Last Modified: Mon, 06 Oct 2025 21:18:04 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245bf45caac6dd69dffb8b214a0b686f9c67b980617ad24bb8dad571074ab94b`  
		Last Modified: Mon, 06 Oct 2025 22:14:10 GMT  
		Size: 221.6 MB (221566192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c81f036507cd8691c70f63d00d6a33ae4d85c2bf4d0385daa90e5e68c2f6132`  
		Last Modified: Mon, 06 Oct 2025 21:18:04 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
