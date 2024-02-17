## `openjdk:22-rc-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:10dcef05764121407a33a9eca8241e4e8f0b5c76a4ce2b2cb1c5e930d36cc626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `openjdk:22-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull openjdk@sha256:99304f54beb2911f46ef15c814dc758ffc0cc197d157f8779c78a5a343638177
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2109266661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a9e92c8951cdff88155128659ab9484b8ee8a13153ea9bd58d479afed3ded5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Sat, 17 Feb 2024 01:04:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 17 Feb 2024 01:05:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:05:06 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 17 Feb 2024 01:05:11 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:05:11 GMT
ENV JAVA_VERSION=22
# Sat, 17 Feb 2024 01:05:12 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_windows-x64_bin.zip
# Sat, 17 Feb 2024 01:05:13 GMT
ENV JAVA_SHA256=8f5138fecb53c08c20abd4fa6812f9400051f3852582a2142ffda0dff73a5824
# Sat, 17 Feb 2024 01:05:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:05:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ff04928a44b4919be4000a2c0fddd267b6ec4c3b8f56a08c9e5b468a75f207`  
		Last Modified: Sat, 17 Feb 2024 01:05:36 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578ecf76f9c90ad06ea52113b39032941f017a67069a0367002e29047389fb54`  
		Last Modified: Sat, 17 Feb 2024 01:05:37 GMT  
		Size: 504.6 KB (504612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25c56159f6955f2a2c8dcbf16359de1243db653c855d17e3dd81be55d646a1d`  
		Last Modified: Sat, 17 Feb 2024 01:05:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb523523ba6a899a4c8fe89b594f9d180a62dea8eeed7854b14adef43fdda40`  
		Last Modified: Sat, 17 Feb 2024 01:05:37 GMT  
		Size: 355.6 KB (355644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c5166e4a5a51629f53f8b390a4981e5ed4ca8f39173bc0c7d7d0a94dc71ac2`  
		Last Modified: Sat, 17 Feb 2024 01:05:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce28c3b7bb76b78a97aef7055963682e0fbdba66b253a0dcb5abd5d6f5d1b75f`  
		Last Modified: Sat, 17 Feb 2024 01:05:35 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c94c6542f6f18d6a3db285032b9d882e36dae77d9f3df575f43916dbaea28a`  
		Last Modified: Sat, 17 Feb 2024 01:05:35 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe97c65938d9fc1f520075ee05d8d134716b159c58eda187c375b216c1c5fc69`  
		Last Modified: Sat, 17 Feb 2024 01:05:47 GMT  
		Size: 197.7 MB (197744487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178f6d09c31332b3ce9109d02ba79809e4bc54bb9c5a0bcf49c42c5a2cb52637`  
		Last Modified: Sat, 17 Feb 2024 01:05:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
