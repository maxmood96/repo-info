## `openjdk:25-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:8f913c41d7457d425e906ef6921e1e85e793fc0ad81c4808b72575853e054861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `openjdk:25-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:228e21ac00c39a5e8d17af4ddb05d8659b7579bd0674244e6c715f9068dd85ad
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3640793339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325f6c9cc049c232c4507ac71b05afec535b6568ebea79bbb69728cb454fc1cf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Fri, 16 May 2025 20:58:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 May 2025 20:58:51 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 16 May 2025 20:58:52 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 16 May 2025 20:58:58 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 16 May 2025 20:58:59 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 20:59:00 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_windows-x64_bin.zip
# Fri, 16 May 2025 20:59:00 GMT
ENV JAVA_SHA256=903e77b6d79a2c808e32a4111a54802e149b11e39d15629d7a04ccfb97e4c79b
# Fri, 16 May 2025 20:59:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 16 May 2025 20:59:21 GMT
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
	-	`sha256:68cae493650bffa903e0895e1f2e266ee4f823b5825e8b836d0d3f0750399930`  
		Last Modified: Fri, 16 May 2025 21:02:48 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b4f788d335c5b01c14d439115092318bb6483081c3662a4bf1f79e7f58af57`  
		Last Modified: Fri, 16 May 2025 21:02:48 GMT  
		Size: 368.3 KB (368322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7569509716153e89ee383313a5bac62c47f605594c9592c9572004d74d04f524`  
		Last Modified: Fri, 16 May 2025 21:02:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46dfccfa9e8d36f9e96257ecfef309d620842a84280083b8bb77bcbf5de888a`  
		Last Modified: Fri, 16 May 2025 21:02:48 GMT  
		Size: 354.8 KB (354839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4146acb6e913e0fe08dcf090868d95d9eeac5ebae7b830683665084bd14d5562`  
		Last Modified: Fri, 16 May 2025 21:02:47 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0ae521cc9be633578ee31e64a2eb8973901cd9cab2e4195a1e6537c6241688`  
		Last Modified: Fri, 16 May 2025 21:02:48 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3a2a57af48d392d0664f2e04177490dfbf9629021ac31ed904168b31d2147e`  
		Last Modified: Fri, 16 May 2025 21:02:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa58bcddb8231f97aa861905859cb434a8e717b840488b6be26d89125fe0c0c`  
		Last Modified: Fri, 16 May 2025 20:59:37 GMT  
		Size: 209.3 MB (209296578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f880421a49694c5468de61ca3815140d1662983afbffdb3d679718d36977990b`  
		Last Modified: Fri, 16 May 2025 21:02:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
