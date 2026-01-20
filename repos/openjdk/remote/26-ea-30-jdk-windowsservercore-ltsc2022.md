## `openjdk:26-ea-30-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:699cb5d509de4f98e56ddbab7951846bcbd6bff1be4f77611c6997d9b34c19a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `openjdk:26-ea-30-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:d8dd373304d857e9907f49a50ad59b6d5d5eca66fe848bd22ad1f8dbf37339fc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2060708795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef3c0143d5b8f270a7e20db71bef97f74d2a2caa9b3783178c0e6a958271e5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:54:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:10:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:10:45 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 13 Jan 2026 23:10:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:10:50 GMT
ENV JAVA_VERSION=26-ea+30
# Tue, 13 Jan 2026 23:10:51 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_windows-x64_bin.zip
# Tue, 13 Jan 2026 23:10:52 GMT
ENV JAVA_SHA256=43834141dc2e692e91f2f08c4cdfcbe91d8e33dea1abaace5b34ca7b14913f44
# Tue, 13 Jan 2026 23:11:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:11:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f08760e06519dd29e9a52391dac11e5952f68046c79c4bdea23cb54196c9897`  
		Last Modified: Tue, 13 Jan 2026 23:04:06 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4808f5095eed5048da9d8c0297b6117383db4a47baf032f33f6144af28df6a01`  
		Last Modified: Tue, 13 Jan 2026 23:11:43 GMT  
		Size: 483.6 KB (483585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da961f082c8915158eb3dd9db2ca6dff8cb2e4778f7b39570ce3f9c1336fff60`  
		Last Modified: Tue, 13 Jan 2026 23:11:22 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46840288a57e1c13393653027c3697419c9d380cdddec99f9c9da07ca41d857e`  
		Last Modified: Tue, 13 Jan 2026 23:11:43 GMT  
		Size: 334.1 KB (334145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588998e1f6701f51445f12d78df1794cd9a50ef26520ac7f95c3961cf0c7ad68`  
		Last Modified: Tue, 13 Jan 2026 23:11:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e598e22c53f3d96d467870ba47a825c366b9f241e97bf0d493534d5c6ef201`  
		Last Modified: Tue, 13 Jan 2026 23:11:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5040b122641d59e1883ae53152cdff153d8de6acdc108f1a68a268654f026c1`  
		Last Modified: Tue, 13 Jan 2026 23:11:44 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e189b5645be5c659967d8db1a6af08614d911433ad61c14debafc63225b475`  
		Last Modified: Tue, 13 Jan 2026 23:13:44 GMT  
		Size: 224.2 MB (224224077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4ea3423cba7bfe0e45216bd72344c90aee8080a01df3ac10734c26c2e4958d`  
		Last Modified: Tue, 13 Jan 2026 23:11:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
