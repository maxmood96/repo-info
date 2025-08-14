## `openjdk:25-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:1f6726b8e0bb4bd194399d09e7b8955dd0173da2f7a20f0c19d9c9f990eedd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `openjdk:25-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:5c1e21d400397e8585578aef7ecb8518c78b0e81509bbe0820cc704269a246d7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2501296525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e3dc026535949468cfda6dd80ac2c47ad6ad3966118d90c21ac32d8796c67d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:34:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:34:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:33 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 12 Aug 2025 20:34:41 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:43 GMT
ENV JAVA_VERSION=25
# Tue, 12 Aug 2025 20:34:44 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_windows-x64_bin.zip
# Tue, 12 Aug 2025 20:34:45 GMT
ENV JAVA_SHA256=1bf872a4dc38579963ad34a757b3077296c2d2ccfeeff041d1741a87e6bde898
# Tue, 12 Aug 2025 20:35:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:35:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbec5ba5fbaf8526882e529bf6308a967876f12f49c4b2191c42409e5337636`  
		Last Modified: Tue, 12 Aug 2025 20:36:56 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea518cfccdcf12e8110d052c4ae08de06ac5c2f4305e5d63625c708f13e68a5c`  
		Last Modified: Tue, 12 Aug 2025 20:36:57 GMT  
		Size: 349.0 KB (349012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f55a317cf2d0b87b7f395b81d10531c6c98b96eb2b66b9cc024e01948dcced`  
		Last Modified: Tue, 12 Aug 2025 20:36:56 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbece82af0bb546b65f441f474fcae8ae7f0454db67a43bd1990a392e602c96`  
		Last Modified: Tue, 12 Aug 2025 20:36:57 GMT  
		Size: 334.7 KB (334717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d32ca0c40f91aa184dbb0a64b8b4e1b4ec2003cb1d107f0346c342ef6206b4b`  
		Last Modified: Tue, 12 Aug 2025 20:36:57 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba9f5c3e70478c94ec6d33ae6372eae9ad909dec35bc3194b14773b69fe2916`  
		Last Modified: Tue, 12 Aug 2025 20:36:56 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25afbc5eba7bba913b728859e49753f842026cb2eedaa11202dee8e28199c6ea`  
		Last Modified: Tue, 12 Aug 2025 20:36:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b139bd5a848d7e28616bdba81db7f152d4911d2f6133e3e99b7a66b79a3585f4`  
		Last Modified: Tue, 12 Aug 2025 20:46:09 GMT  
		Size: 218.9 MB (218913119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9773bd0082384ce4c3c48065ea3d012cabb450d4bf4cfb9124fa5855b5f60440`  
		Last Modified: Tue, 12 Aug 2025 20:36:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
