## `openjdk:25-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:5c11aa5c6e005ead2cb25d1fb9b01a50f4465b18614a7f83e7116fefe7469806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:25-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:6b3a41a27c22d049a46022606d7fe9d04843a935866530726877fc2f792f6431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2708840642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b9087da181daa419a5b344df9d07bf88331b07ce95aba85c729985befe61b3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Tue, 28 Jan 2025 23:34:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Jan 2025 23:34:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 28 Jan 2025 23:34:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 28 Jan 2025 23:34:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 28 Jan 2025 23:34:32 GMT
ENV JAVA_VERSION=25-ea+7
# Tue, 28 Jan 2025 23:34:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_windows-x64_bin.zip
# Tue, 28 Jan 2025 23:34:33 GMT
ENV JAVA_SHA256=98590eb26fdd8ac407ec4fd6fb11819d381f179d87174fea5a2ac7d5b051c11a
# Tue, 28 Jan 2025 23:34:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 28 Jan 2025 23:34:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e7940fec99849e6c960be9e26e87a2f03cc6d8e8de8234666f263fac7ddfcc`  
		Last Modified: Tue, 28 Jan 2025 23:34:57 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bc4c27420d585013e0fde9d0b84098d044fa9ed9ed00e5881758f8b97a8687`  
		Last Modified: Tue, 28 Jan 2025 23:34:57 GMT  
		Size: 393.3 KB (393344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5870ad41af3cc4bd58210ae9b4c4d5375a4bf41f49d65642dbde8479214e95`  
		Last Modified: Tue, 28 Jan 2025 23:34:57 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6566e9d47962f37f06257e7b1d4a8e6efd54023299e0cb265fbf0d560f1948`  
		Last Modified: Tue, 28 Jan 2025 23:34:57 GMT  
		Size: 377.9 KB (377885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b354356dbf6764fab54c7f42fadd46dcab82fbdd95f1b105dffc3933032cccab`  
		Last Modified: Tue, 28 Jan 2025 23:34:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa635a681a20ca1df1ba7a072c3cc29f81fd54a5e577490870145e3c3b46c71f`  
		Last Modified: Tue, 28 Jan 2025 23:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1550e743196406c182237c06dde309e4cd69cf556e4f19a41edb67ced7156e17`  
		Last Modified: Tue, 28 Jan 2025 23:34:55 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb69abab699d88bc50a5b0699ccd8ef312a55e77444184ec287e0ee05740596c`  
		Last Modified: Tue, 28 Jan 2025 23:35:09 GMT  
		Size: 207.8 MB (207784025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce1f388e9621b93a739b81e37c7ab7ea549f03a98621e11c63405506d293283`  
		Last Modified: Tue, 28 Jan 2025 23:34:55 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
