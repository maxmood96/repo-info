## `openjdk:23-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:9b96f5454697997ab99f6fefc76df65eb05ba20951cf4055a8904827d93c2c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `openjdk:23-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull openjdk@sha256:b8e396abc1b364aa7b7067c82011e1e1a52675f4751a6f10c2fbe7d4fbcf71f6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2318151043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0589174154ed5dc6482db25f0ea4e057f47a7ebad87c241dc21131a336d23c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 22:00:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:00:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 15 May 2024 22:00:27 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 15 May 2024 22:00:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 15 May 2024 22:00:33 GMT
ENV JAVA_VERSION=23-ea+22
# Wed, 15 May 2024 22:00:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_windows-x64_bin.zip
# Wed, 15 May 2024 22:00:35 GMT
ENV JAVA_SHA256=a849b0c4f58cb28b02e6c43660886859ce8678d18224b4038ad69c1e3ead6249
# Wed, 15 May 2024 22:00:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 15 May 2024 22:00:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b25e2aa5b0f0eed7caa2bccb0bf82f1fe9cdfb7143a210314b5de0b3afc6b2`  
		Last Modified: Wed, 15 May 2024 22:01:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd625612b5cf9281af127ce591158439b4f678aa2d91784c126443b5081d514`  
		Last Modified: Wed, 15 May 2024 22:01:03 GMT  
		Size: 359.2 KB (359208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaee157c9d897ff5dc3dc66edc620bbaca6cb104f622c026fb290e44b7201cd`  
		Last Modified: Wed, 15 May 2024 22:01:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749adcef71c1519cfd2925fdabddff609e3e930ffe50d505ac13c3c37e94fcab`  
		Last Modified: Wed, 15 May 2024 22:01:03 GMT  
		Size: 342.7 KB (342659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3edc6a76496fd042367259aebc95676ecf0fa7d2e4dda2f0d50ff254597a807`  
		Last Modified: Wed, 15 May 2024 22:01:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc576ca03f454200c1da3874811c6e25feb42cb8c3cf555fe03949980034fbdf`  
		Last Modified: Wed, 15 May 2024 22:01:00 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea8479107a79477f93a5aadf13b6132a124a724dc9bcab9134145458aad4f0b`  
		Last Modified: Wed, 15 May 2024 22:01:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715208dab702d7172c6c56c193659f2a36915f9834d918549536d85bfa5035dd`  
		Last Modified: Wed, 15 May 2024 22:01:12 GMT  
		Size: 204.8 MB (204770067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5a21fda36dce738b3dcb4d3ebb9a29b085a3f169d10c42bbe025163ae3d58d`  
		Last Modified: Wed, 15 May 2024 22:01:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
