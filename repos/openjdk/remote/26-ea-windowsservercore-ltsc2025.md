## `openjdk:26-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:a051a3143282d73016cef90e6032e304128a9d8eabf292350fef2415689249bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `openjdk:26-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:1922cb46cf8becd498f0acef25e82b4825a62eee37b2d0bf61c722c0c4e39420
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3695805475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e3fafdd4ad784e959aaafe678a32288787b015996897dc3ca0cf17f11fcc27`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Mon, 30 Jun 2025 17:34:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 30 Jun 2025 17:34:41 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:34:44 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 30 Jun 2025 17:34:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:34:59 GMT
ENV JAVA_VERSION=26-ea+4
# Mon, 30 Jun 2025 17:35:04 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/4/GPL/openjdk-26-ea+4_windows-x64_bin.zip
# Mon, 30 Jun 2025 17:35:06 GMT
ENV JAVA_SHA256=bb9270496ac199b05ed1ccbf5c3caa75f278f93900fac9444931bbbc76524588
# Mon, 30 Jun 2025 17:36:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:36:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341c918446e3dde2759dba1159661b8abc690af2c7c07ee9fb229f09767d319f`  
		Last Modified: Mon, 30 Jun 2025 17:39:33 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc85c3ceee5134ae13594ea065c2fda143b4d8501b5cd8f073b78f604eb1f480`  
		Last Modified: Mon, 30 Jun 2025 17:39:34 GMT  
		Size: 397.1 KB (397059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eb76743d37c0a1d2f199f7c1134c271794ea7dfc3859f3b5f166a8facc5176`  
		Last Modified: Mon, 30 Jun 2025 17:39:34 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f26a26fb4260a8d8ea2bfb28bc5ed9e6ccd46a8d3584be12d663d8e56edb34`  
		Last Modified: Mon, 30 Jun 2025 17:39:34 GMT  
		Size: 382.3 KB (382328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41620ba50e80908c7bfff6eb9e9cc29488d030b2fe7cef70cf5aa80cbaa6b8f`  
		Last Modified: Mon, 30 Jun 2025 17:39:34 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb04c66236e735dbbc39be0869fda42ad1d3fa09bc29ed96fe683ef747ea3d9`  
		Last Modified: Mon, 30 Jun 2025 17:39:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27140cd831239c112827350ed62853f801107ff043208c2203c276d46eefeb7`  
		Last Modified: Mon, 30 Jun 2025 17:39:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1920e3769b35b3ec37fe13aa2d3fbcc95048e18157a67dc9792e383adda1e9e8`  
		Last Modified: Mon, 30 Jun 2025 18:09:53 GMT  
		Size: 218.8 MB (218844233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2047eba5c9198d0f9973e54324993efc51adc2e6eac33d77b0840dea7ac904c0`  
		Last Modified: Mon, 30 Jun 2025 17:39:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
