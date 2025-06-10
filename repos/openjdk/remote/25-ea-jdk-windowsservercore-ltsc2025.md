## `openjdk:25-ea-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:f85ab61591b6f5dc2a9a52fcfbdfd0def3f3a778784add34a86c54d070b8aeb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `openjdk:25-ea-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:26e2dceedd7fde64c9c6b6d8ee16bd9a3a201ca9cf14fca63157f0a4015f7953
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3650396329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37741a49b057171051478776fb1fbb3dc95cb21551b7451bd3e6c862ecd174d4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Mon, 09 Jun 2025 22:11:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Jun 2025 22:11:27 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:11:28 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 09 Jun 2025 22:11:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:11:34 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 22:11:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_windows-x64_bin.zip
# Mon, 09 Jun 2025 22:11:35 GMT
ENV JAVA_SHA256=6600725ff08e343ea49db5bdac0cc8ef756053c899efb6a504b5f9e4a2fcc69d
# Mon, 09 Jun 2025 22:11:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:11:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d20626c5356d286dc015bfc02a35c7439fa6a1fdd0f0e1c3154150718ff7a4`  
		Last Modified: Mon, 09 Jun 2025 22:15:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cd14ae314c9c9b272c7f402fd6496b43000a857368a520a42adc83233191b4`  
		Last Modified: Mon, 09 Jun 2025 22:15:18 GMT  
		Size: 392.6 KB (392600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf47c0531eb0639c8eccc653ad181edae4490fe18edf26320730c4d0c2e5b455`  
		Last Modified: Mon, 09 Jun 2025 22:15:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516cfd8c532eb4e0995446c98ff9eaf65b106b2c247cfdfa8bd22edfa9d9397b`  
		Last Modified: Mon, 09 Jun 2025 22:15:19 GMT  
		Size: 376.7 KB (376681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45f464e18614be4653f31ea5378c4f1bb5d7d2133ddc6fd9081451d2250913`  
		Last Modified: Mon, 09 Jun 2025 22:15:19 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d512a3814ce42a725be31ba0409e56c4b1dc6f9cc45a33c1e7bd61d5357ccb01`  
		Last Modified: Mon, 09 Jun 2025 22:15:20 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a0d78a720374bd1625e54ddc2371212a47abd1717d57723789efa3c4b14c5`  
		Last Modified: Mon, 09 Jun 2025 22:15:20 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7a562c357564c25f10e19a0bcb09dfd845bf42f02efc1b144c648a54605923`  
		Last Modified: Mon, 09 Jun 2025 23:07:05 GMT  
		Size: 218.9 MB (218853417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d339aa7fb9e8388ef037a23b3ea9a4a0272b81464a3e0b9fdfdb58500a5436b2`  
		Last Modified: Mon, 09 Jun 2025 22:15:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
