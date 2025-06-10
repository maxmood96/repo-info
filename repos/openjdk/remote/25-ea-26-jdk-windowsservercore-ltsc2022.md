## `openjdk:25-ea-26-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:c38d884fb653262a8e148dc2d4652640e660152d7cf27bfced028b828b3a3397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `openjdk:25-ea-26-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:815bdd54d54a708b45e4fc93296f82e1fe5dbea124f310720bd8a609cde787ab
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2493098474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fa12805567ebd6cf6e5155e67e88f65e879f0341a92330860b64d2188edce9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Mon, 09 Jun 2025 22:06:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Jun 2025 22:07:54 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:07:55 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 09 Jun 2025 22:08:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:08:04 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 22:08:04 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_windows-x64_bin.zip
# Mon, 09 Jun 2025 22:08:05 GMT
ENV JAVA_SHA256=6600725ff08e343ea49db5bdac0cc8ef756053c899efb6a504b5f9e4a2fcc69d
# Mon, 09 Jun 2025 22:08:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:08:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40a73470b9f9ad63fd495f460ee0fcb26ee7390bbc1915596a44b3629e4d069`  
		Last Modified: Mon, 09 Jun 2025 22:14:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0e63d9b861c13c668164f2903bdaed1eb5b96068e4b9efb7000b8422aa7a51`  
		Last Modified: Mon, 09 Jun 2025 22:14:52 GMT  
		Size: 360.4 KB (360357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee332543e2070ce2f7ac697bbf44ea9f5db89ef86e291da9e83f68b165d83f13`  
		Last Modified: Mon, 09 Jun 2025 22:14:56 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c835abdf02f16813962564296521b2f8630250e9df74355f07d6297ee67d24a3`  
		Last Modified: Mon, 09 Jun 2025 22:15:02 GMT  
		Size: 312.2 KB (312179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcff9d733c04076556260e0bb709d8ec0d59fa9cca70ece2ff0c3c3cabe8fb0`  
		Last Modified: Mon, 09 Jun 2025 22:15:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0666c4a5e81df20ec8eb367c7a0c1ff7f1c685f9a201dd692952a009a9233e77`  
		Last Modified: Mon, 09 Jun 2025 22:15:12 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ebf4dc0f40d28af7a2d90fdce9ab674888c9208a52b26e79e55a055c2b38a3`  
		Last Modified: Mon, 09 Jun 2025 22:15:15 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c3bc91e56f6a192b9a98f47a45a280f979b7e0cf61e24bdf3c2466f1daf5ef`  
		Last Modified: Mon, 09 Jun 2025 23:06:54 GMT  
		Size: 218.8 MB (218790098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8097dfe449e600ae045372db9bc94fc7a962337b4b35e8e59bc1d5ed337d7de`  
		Last Modified: Mon, 09 Jun 2025 22:15:18 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
