## `openjdk:25-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:b569dfe41c5bf21dd44e9a4e4593a8df8a77e2d94ec0268ac6a5e4b8ff8cbe85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `openjdk:25-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:cab96658709c7178416a658468702b8fa2298c29a23680f202255294a93c184a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3718545717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46374309e7a88fa84da845af329dc846e82ca4dbb08063c9fa89f03cb354788a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 18 Aug 2025 18:19:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 18 Aug 2025 18:19:21 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 18 Aug 2025 18:19:21 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 18 Aug 2025 18:19:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 18 Aug 2025 18:19:27 GMT
ENV JAVA_VERSION=25
# Mon, 18 Aug 2025 18:19:27 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_windows-x64_bin.zip
# Mon, 18 Aug 2025 18:19:27 GMT
ENV JAVA_SHA256=85bcc178461e2cb3c549ab9ca9dfa73afd54c09a175d6510d0884071867137d3
# Mon, 18 Aug 2025 18:19:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 18 Aug 2025 18:19:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c177312ecef37e4a536f63a5305d51b4cd6aeaf04af37ddd4b333b010623a4`  
		Last Modified: Mon, 18 Aug 2025 18:27:14 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adb831e56b364c28f0d193daa9cf20479b8ff52cad075b2552eb313f0c16dbf`  
		Last Modified: Mon, 18 Aug 2025 18:27:19 GMT  
		Size: 384.2 KB (384205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c857f73b2b0ff68b53d40b01f9e44ddcbd92087502fca892e4a708fd09a217`  
		Last Modified: Mon, 18 Aug 2025 18:27:24 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f1865248e506d0f4fb872013e71a27d465a483b3cab9b2a9efa1dd18511a2b`  
		Last Modified: Mon, 18 Aug 2025 18:27:29 GMT  
		Size: 367.5 KB (367474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3e72563d7caed9846fcab8f36b7567053468ae15287fad71226faa0579cb5c`  
		Last Modified: Mon, 18 Aug 2025 18:27:36 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8adb61384619cb129b0d9e24ed2fe4cd419eeee5555e0b92b6bc5d0313fdfe8`  
		Last Modified: Mon, 18 Aug 2025 18:27:39 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4c7b25838eb0779304df12e4437f41a095cb6d9254bccf3c04e28ff969a0ad`  
		Last Modified: Mon, 18 Aug 2025 18:27:46 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785bdd7f5ca8781a4b1bc71e516403587b6c16714a0112f1f04d293943aad4ea`  
		Last Modified: Mon, 18 Aug 2025 19:08:50 GMT  
		Size: 219.0 MB (218955531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bc527e28a7cadf3ebfddb991a5dd1331e451aa6315f0ed660d766fc0dbd78a`  
		Last Modified: Mon, 18 Aug 2025 18:27:50 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
