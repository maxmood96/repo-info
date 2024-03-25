## `openjdk:23-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:1c64845a17e344bddd2bbdd54255e307cbc25025e0e8109ca74069e831fb5777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `openjdk:23-ea-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull openjdk@sha256:ac0262dbdb43256501c84b54981f7d261256bcb2506f436b613a9134c9f8ab2b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323513797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e639f6a29cc723e263c394f3fc5ecb4bed212943b93cdb6902430bb2322fa3b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Mon, 25 Mar 2024 19:12:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Mar 2024 19:13:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 25 Mar 2024 19:13:27 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 25 Mar 2024 19:13:54 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 25 Mar 2024 19:13:54 GMT
ENV JAVA_VERSION=23-ea+15
# Mon, 25 Mar 2024 19:13:55 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_windows-x64_bin.zip
# Mon, 25 Mar 2024 19:13:55 GMT
ENV JAVA_SHA256=990a13730f096e195392211ecd4623c364cae742a9aedb5aae232c629b08f2b6
# Mon, 25 Mar 2024 19:15:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 25 Mar 2024 19:15:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ce779cbfb22f401e8d5c556f71e8c90160dfd5b2d1fafc6342ab1bd9af0317`  
		Last Modified: Mon, 25 Mar 2024 19:15:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f78e58f09f2cd12c4d3071c2aa5cea5ae564ac896cf164147de5a6ff90e533`  
		Last Modified: Mon, 25 Mar 2024 19:15:34 GMT  
		Size: 499.4 KB (499384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69458586865f6c2e6c06d233c24740903d4d06e564fdb4e633593866e3fd2be3`  
		Last Modified: Mon, 25 Mar 2024 19:15:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae832d578388a04ff6f307044f96dae9b6c0fbdc3d5e032eee9c64cc89c24b75`  
		Last Modified: Mon, 25 Mar 2024 19:15:33 GMT  
		Size: 350.8 KB (350831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fecd58f0c432ada491e7c8eb0ce0827c2a3fb7dd45d72a2f33dcb606a3376b5`  
		Last Modified: Mon, 25 Mar 2024 19:15:31 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397ecb025be40a4180ec4f0b5abada2bfe2c1c2537170c5e60be68269885af92`  
		Last Modified: Mon, 25 Mar 2024 19:15:32 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b05333eec4b8574c88a845e9bb482c0af5f0dd9f357c039a3770d6b2ad57924`  
		Last Modified: Mon, 25 Mar 2024 19:15:32 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d75eac12b817d0758382e3e87f8282b87a768d2e15408a72add5cfc1f4d8d4`  
		Last Modified: Mon, 25 Mar 2024 19:15:44 GMT  
		Size: 197.6 MB (197555868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d919a774c212eaad50de52369b0ecf373cf927f89f9a62515520f62c9273d1f3`  
		Last Modified: Mon, 25 Mar 2024 19:15:32 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
