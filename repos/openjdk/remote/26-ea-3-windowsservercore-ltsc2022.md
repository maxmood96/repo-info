## `openjdk:26-ea-3-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:24111eadb6f6f03c9c7a3264b4da00b7b6435ccdbe9bd11895826349b8b803af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `openjdk:26-ea-3-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:c93e3a7284d9ec3999b68ddfbd75be6cabbd61bc5a2e4ceb5236a0465f02df2a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499755152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c0008a30faf21d95c07dcddd868cec4f22c655e8cd7f40b3db280ecf528ac`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Sat, 21 Jun 2025 00:28:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 21 Jun 2025 00:28:37 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 21 Jun 2025 00:28:37 GMT
ENV JAVA_HOME=C:\openjdk-26
# Sat, 21 Jun 2025 00:28:48 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 21 Jun 2025 00:28:48 GMT
ENV JAVA_VERSION=26-ea+3
# Sat, 21 Jun 2025 00:28:49 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/3/GPL/openjdk-26-ea+3_windows-x64_bin.zip
# Sat, 21 Jun 2025 00:28:50 GMT
ENV JAVA_SHA256=b5728414606c8b9c7d53d32794dcd985c83d5aad7e57dec16cd8286ccdcb1aab
# Sat, 21 Jun 2025 00:29:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 21 Jun 2025 00:29:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d7bceb951443b726cbf5ee2e116e22ffb4dcfa097cdc536e67b397c9f7a327`  
		Last Modified: Sat, 21 Jun 2025 01:07:27 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214b1e31bb4e7e50e03d59be01289a42b654e0629388de74c7abf9184f545cbf`  
		Last Modified: Sat, 21 Jun 2025 01:07:29 GMT  
		Size: 358.3 KB (358325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61966dd8c89586f2fb8be047b39eb3139741481be03da67d00598f1e27399682`  
		Last Modified: Sat, 21 Jun 2025 01:07:29 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69dfed4bb8869af16f5848b98a80bb07deeac9fa76329e6c9be26539e3cbd0d`  
		Last Modified: Sat, 21 Jun 2025 01:07:30 GMT  
		Size: 346.8 KB (346802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f81039140c85746f251bbd508b9f89adf5a982ead0545b1346e64520568d46`  
		Last Modified: Sat, 21 Jun 2025 01:07:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefeb79d2ec0e8330d5b1c3e34b4a0ba9eedcc35848eeb8a666cb2a0d8cd3f16`  
		Last Modified: Sat, 21 Jun 2025 01:07:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa39b304ecf78f98a16eee7ab7f9148b359fec6c16034ec31e08dbf0c969482`  
		Last Modified: Sat, 21 Jun 2025 01:07:34 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3e9b837053b4a7118a137a9199fb795fc3b540e1422b3a3f796b8e5694855d`  
		Last Modified: Sat, 21 Jun 2025 01:07:45 GMT  
		Size: 218.8 MB (218790720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2de33c11a2b6a41994692c1d29316213e58c75a29797381a7b67b7f6bec609`  
		Last Modified: Sat, 21 Jun 2025 01:07:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
