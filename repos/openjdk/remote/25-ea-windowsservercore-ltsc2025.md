## `openjdk:25-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:a8d30969c2d1df027e6822588d19c4268239ba2948120a61cbc757fa94d3bab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `openjdk:25-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:6506d6bb85c1de8ac30a4a243e3ee3fc3b7c64d619af20a6a2df8b6f9d7be79e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3117371676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f701ca969bdb34ca86d47f8dabc54524299423ac209edb7f85e3f410fd93a876`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Fri, 21 Mar 2025 17:18:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Mar 2025 17:18:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:18:19 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 21 Mar 2025 17:18:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:18:33 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 17:18:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_windows-x64_bin.zip
# Fri, 21 Mar 2025 17:18:37 GMT
ENV JAVA_SHA256=a095e71a2552995360224643760900b2c44fc91dad10cab9d289bed71fa936dc
# Fri, 21 Mar 2025 17:18:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:19:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f29c6dad3e1d96433b03ed05cc6309f224ea92a969bfab4887167529bd13d33`  
		Last Modified: Fri, 21 Mar 2025 17:19:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dabe5df79724f97b77b6a2ae2dfd576801a9c0ba0aa5afec9f7deb8af4fe268`  
		Last Modified: Fri, 21 Mar 2025 17:19:11 GMT  
		Size: 401.9 KB (401919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410d739f391e8433c3eb33d92cdfdf11e0a3000f2e6ef5b6adf7485cd9665f49`  
		Last Modified: Fri, 21 Mar 2025 17:19:11 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10b4e9db977732cf18dcba6e85eb5dd1ec9ee95a27e73611500da08336efcf7`  
		Last Modified: Fri, 21 Mar 2025 17:19:11 GMT  
		Size: 385.3 KB (385286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf378787f91bad6a2467b655ef19bb5532578365e268a653571dcfc63a630acb`  
		Last Modified: Fri, 21 Mar 2025 17:19:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43df5ce49f6a47b2f2b3d80a330fcf41850c6cc86a181135a2309bdbd52907ae`  
		Last Modified: Fri, 21 Mar 2025 17:19:10 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9007cf78149c45d331fd747cffdd24e5ae7398bee87e0c1366eb04eafeaae`  
		Last Modified: Fri, 21 Mar 2025 17:19:10 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0417b4393bcc741f4057e53138efad28110760c4a03f3596695415be79aa1a`  
		Last Modified: Fri, 21 Mar 2025 17:19:23 GMT  
		Size: 207.9 MB (207928976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cff24e7b8e0cac7a58d4cdeb32a6b4373346f9b5f2441f187fdf0843d52309a`  
		Last Modified: Fri, 21 Mar 2025 17:19:10 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
