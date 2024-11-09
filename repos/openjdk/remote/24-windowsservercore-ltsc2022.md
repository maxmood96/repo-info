## `openjdk:24-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:1a5246aafde152846158c39debfefd5425f192da9ca806eea32644f7f32eac1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `openjdk:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull openjdk@sha256:058498ed0a4b223a45802935140b701ba29b02440e3e2d203b41fe7116978e19
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2009844213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07712de216130c461922e720580bd5749c5d8bedb4f36dbaaca16dc832a008e6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Sat, 09 Nov 2024 02:03:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 09 Nov 2024 02:04:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 09 Nov 2024 02:04:24 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 09 Nov 2024 02:04:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 09 Nov 2024 02:04:31 GMT
ENV JAVA_VERSION=24-ea+23
# Sat, 09 Nov 2024 02:04:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_windows-x64_bin.zip
# Sat, 09 Nov 2024 02:04:32 GMT
ENV JAVA_SHA256=9fb6091495ba5cf912000206d77fcacbcb294c4cb27a11538fa5b1eb69ffc1d6
# Sat, 09 Nov 2024 02:05:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 09 Nov 2024 02:05:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd5bed3ade7fff0edc5a7892cc49918710c780c9009fef47c98fad854ccaa44`  
		Last Modified: Sat, 09 Nov 2024 02:05:10 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77be1ef8fe770ed749b7730f8bbf82f2f34e906d87e9f3310db7d5e73608b941`  
		Last Modified: Sat, 09 Nov 2024 02:05:10 GMT  
		Size: 494.4 KB (494418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab1df8e0cd45ce6bc916ce0d1cd86ced99c90de9b01f4d3021f38ec31d035da`  
		Last Modified: Sat, 09 Nov 2024 02:05:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499eff960881ac01b5dee295b93d4c89cb683f47bbf31677d85fff073d242623`  
		Last Modified: Sat, 09 Nov 2024 02:05:10 GMT  
		Size: 312.5 KB (312455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca36a6c7ac4f8c6941a39213a727a117861875c92f85c248c8f9fc98feddc73`  
		Last Modified: Sat, 09 Nov 2024 02:05:09 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747e3c3c8253945e7056accb866d34c0d2d9cb1ce48ab12584d19053f9330289`  
		Last Modified: Sat, 09 Nov 2024 02:05:09 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d03b329872ef228cf770d27f2405e9db131d4026c853c6306fe419cddf09ada`  
		Last Modified: Sat, 09 Nov 2024 02:05:09 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7ca5d54ff506dbcda9c5ac572d07ba2bac5b76f54c8eb22054cfd0172e696c`  
		Last Modified: Sat, 09 Nov 2024 02:05:20 GMT  
		Size: 209.7 MB (209687869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6a0460e9a46e82a01281fe6889503e853b0acf1322dca2730a4d75afd49e99`  
		Last Modified: Sat, 09 Nov 2024 02:05:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
