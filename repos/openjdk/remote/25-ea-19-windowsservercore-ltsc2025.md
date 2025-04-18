## `openjdk:25-ea-19-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:9ee09627e4f3b5f368d8b0457d2a7ef1e38b5af29da1b9cb86ff2d98a0533f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `openjdk:25-ea-19-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:c453471d04d3a81c4761a69bfa99c74e00becd3b776e010e599a71b7bc1d66ac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3603926190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f800c8dbbece89c50554cc0abea0841c7ae25f4b113c9d7b30439525c660826`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 18:43:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 18:43:30 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 18:43:33 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 18 Apr 2025 18:43:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 18:43:46 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 18:43:48 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_windows-x64_bin.zip
# Fri, 18 Apr 2025 18:43:49 GMT
ENV JAVA_SHA256=29058ee51e7562ec5fb02d09a78c3540286db223bf48aacf93c4a95ed664fc7a
# Fri, 18 Apr 2025 18:44:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 18:44:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e977ce3042fcbf3048a6d6be511f9eedfab5d90562f5fe924d3bc2f9e7264f62`  
		Last Modified: Fri, 18 Apr 2025 18:44:24 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45ecb0bc33fbea75165dc931e49fe1845c2b7b9e473416d4144633686492dca`  
		Last Modified: Fri, 18 Apr 2025 18:44:24 GMT  
		Size: 364.5 KB (364518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a579206e7890579b5fb3d1cb61fd57ee92bc9a2c2db208ec7b7f2abd8fb7ddd0`  
		Last Modified: Fri, 18 Apr 2025 18:44:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528c7a13cfe1636d89fcdd05f168afa009a3925b7263767a0e67f352b069f6cb`  
		Last Modified: Fri, 18 Apr 2025 18:44:24 GMT  
		Size: 348.1 KB (348138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1df98110716b64faa647c1d7b14892af15a9361dfdc23180bf6cc08786c36e`  
		Last Modified: Fri, 18 Apr 2025 18:44:23 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2a17945bddc4d570df63181269d3292ff82981bfb0f0481180072309e34404`  
		Last Modified: Fri, 18 Apr 2025 18:44:23 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2092e9c977f882583f739784a2af05a11a3c260b022a05c77175fa265fd408a3`  
		Last Modified: Fri, 18 Apr 2025 18:44:23 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d198f480bfb14f8ed8b2df93229da3c09c0ddf9cf9929e906bc7bafdc7d0fc2`  
		Last Modified: Fri, 18 Apr 2025 18:44:38 GMT  
		Size: 208.0 MB (208044289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b7c202c5437acd501e738334562f1f53b2d22a9c6a0eb3a3f8c2c5d39a2d6`  
		Last Modified: Fri, 18 Apr 2025 18:44:23 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
