## `openjdk:26-ea-17-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:6aef55f19d0552a079b3a615b5d8f40f5141b40635f69ed6d0b867d8e8aae8fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-ea-17-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:32e62cbf59b691e1e2f1c948ac18df18f0273f211fe39a573fb7912fb117dc32
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2504379459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849b94694fa20c6da370c9ca2f2a791be3f0065f960e5e9433d03fc0f5a6dbda`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 22:03:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 22:03:56 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 26 Sep 2025 22:03:58 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 26 Sep 2025 22:04:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 Sep 2025 22:04:06 GMT
ENV JAVA_VERSION=26-ea+17
# Fri, 26 Sep 2025 22:04:06 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_windows-x64_bin.zip
# Fri, 26 Sep 2025 22:04:08 GMT
ENV JAVA_SHA256=5232e47e862086980b6e18c5b212648b57221ea3661f5e4a368a78a5a905f677
# Fri, 26 Sep 2025 22:05:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 Sep 2025 22:05:36 GMT
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
	-	`sha256:7380dd82e573dd1fb534faf790209813e4f1f136ded593b7e489f8e4727d7569`  
		Last Modified: Fri, 26 Sep 2025 22:17:02 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50323695b31e3d1d4cc7baf6c3e6d3f4de0bd1e149d261f19d53c8107cfbe4f7`  
		Last Modified: Fri, 26 Sep 2025 22:17:02 GMT  
		Size: 368.2 KB (368243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4172bb520e60e637f22921d9bc8c4bd6e446f15fbf70f93c40944ddebe41c07`  
		Last Modified: Fri, 26 Sep 2025 22:17:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824b6f7f9b98f8d81c55904104df1a0975fc02c2986f24803eea86731a49d5dc`  
		Last Modified: Fri, 26 Sep 2025 22:17:02 GMT  
		Size: 346.6 KB (346588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52204e8a94ec27f9196776e06d7c399ec17c76f9b545a0150ff42ac47fdea6e`  
		Last Modified: Fri, 26 Sep 2025 22:17:01 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4910947c4237df258772e8290558a4b2b113a2c6aa749180d1b81103f46387`  
		Last Modified: Fri, 26 Sep 2025 22:17:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f23730b4133f46419f0b0eba3ecff834c2a8fddd84b153e88935a9b985cc22`  
		Last Modified: Fri, 26 Sep 2025 22:17:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1081dd2e451c47cabc45b979ccdcb3b6b7e397f4abd30f8009c27a0082f89be`  
		Last Modified: Fri, 26 Sep 2025 22:49:07 GMT  
		Size: 221.5 MB (221511804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793f6cef32e8c0574ae4a4fba9611b9cf273c56d7f8dfa20e2ede6d9ea5bab00`  
		Last Modified: Fri, 26 Sep 2025 22:17:01 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
