## `openjdk:24-ea-35-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:a5bdd0a5573d1a6357ecbe4beece4db8364596f2b2038267c0730a90a2e94561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:24-ea-35-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:09e030b949cc2e69c1757d1b1bcdab4e75261266bfda0534f6318397fc9fc041
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471952089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8961db783aabdf78f66c36057fa9e8dbaf5f18d86a723464bcf34a003c9012`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 04 Feb 2025 23:31:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Feb 2025 23:32:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:32:59 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 04 Feb 2025 23:33:12 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:33:12 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 23:33:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_windows-x64_bin.zip
# Tue, 04 Feb 2025 23:33:17 GMT
ENV JAVA_SHA256=1d56c9650251685d5d3007781088385fe316738b84a354ef2d3a42b83a38bd46
# Tue, 04 Feb 2025 23:33:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:33:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05882df6f8da50016aa567c66b23091c8af56572c4b9ab1b6af994f38ae90596`  
		Last Modified: Tue, 04 Feb 2025 23:33:57 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a41ef58d03434f8e5bf7d6149e8336123f6d2db1fea34c600e7651e1d11397`  
		Last Modified: Tue, 04 Feb 2025 23:33:57 GMT  
		Size: 365.0 KB (365019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05d41d6606ba5eb6b4e7d32820b927fc90800a78d0386c0e89d77ff634430c8`  
		Last Modified: Tue, 04 Feb 2025 23:33:56 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290f2b5e0f9a9d843a00121ff3b8c5f6bfd5af045b1cd83bd2496c9c09de0b8f`  
		Last Modified: Tue, 04 Feb 2025 23:33:56 GMT  
		Size: 312.5 KB (312484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bc437ffe8eda74c89eb06ccf88cd1f7a2f1a4f5b0f61160cc0a89b0de98141`  
		Last Modified: Tue, 04 Feb 2025 23:33:55 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5380f7ff3459bdcc2794ac0a8256d908a5e718f58d12f900dfb3bf255436dd75`  
		Last Modified: Tue, 04 Feb 2025 23:33:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef3016435f40a5dcd18ef8ecdd28596abb6179d7fb54b5953e2587778886ae`  
		Last Modified: Tue, 04 Feb 2025 23:33:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d2abd11df77799b007570098ea8414ff660bbc2eabf96d2d0b1157463536b`  
		Last Modified: Tue, 04 Feb 2025 23:34:06 GMT  
		Size: 208.9 MB (208881621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c005b5ad1ab12374ef0804af65fa587c9c8a6a5e63ca707c9051addc2247fb`  
		Last Modified: Tue, 04 Feb 2025 23:33:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
