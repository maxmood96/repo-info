## `openjdk:24-ea-33-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:8fe19bcf771cc38158ffd00e3f6c227ea0c0ccf338278818e8f0ae9b2544965b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:24-ea-33-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:21b22d616a2cb1cf2a129169ab22a06ebe001e9c81666b670f1d3a6175bf5265
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709984323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eb3719f47bb6ac15599287fd85d9c2568bfe70f203bf5ca93dca46d92b5e3d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 29 Jan 2025 00:30:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Jan 2025 00:30:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 29 Jan 2025 00:30:26 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 29 Jan 2025 00:30:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 29 Jan 2025 00:30:31 GMT
ENV JAVA_VERSION=24-ea+33
# Wed, 29 Jan 2025 00:30:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_windows-x64_bin.zip
# Wed, 29 Jan 2025 00:30:32 GMT
ENV JAVA_SHA256=2c9091018c7bf3181421a86a3aabfe9ea9c375ed3720c8525be78fb54aa5516d
# Wed, 29 Jan 2025 00:30:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 29 Jan 2025 00:30:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcec2f762abf75d8fe04e570d0e608763288d403c8e01b37e0186bafbf72053`  
		Last Modified: Wed, 29 Jan 2025 00:30:57 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9ab6d542b2c2d3f642ea03a03c4b79d81e72ca1a4fd3b8fcefbbd91fa77ed4`  
		Last Modified: Wed, 29 Jan 2025 00:30:57 GMT  
		Size: 401.4 KB (401445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db12d2d4d39a58ba015aac4a76f74f74b111b744414d0e99964bcefec2a3c3ce`  
		Last Modified: Wed, 29 Jan 2025 00:30:57 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6bac522672d3c4e0337ce3ea5c7e1bfae24d5b7b150e6a5d06f6fa55410df8`  
		Last Modified: Wed, 29 Jan 2025 00:30:58 GMT  
		Size: 385.2 KB (385181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f551b99649da12dcc88c2cc531185affcd9e4129d92210cf2578fd5d3b7b68`  
		Last Modified: Wed, 29 Jan 2025 00:30:55 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6017804ca325ce13fec8c013837481154291abc5ed4a0e44750a0dff2b417d29`  
		Last Modified: Wed, 29 Jan 2025 00:30:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8447961997026e718806515a971d26d1048104a12e266ef590b1a03928f9303`  
		Last Modified: Wed, 29 Jan 2025 00:30:55 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785a826ec1e3ee0fa3835355fd6f01ea8eecd209a88dc04d764856ccee4790ba`  
		Last Modified: Wed, 29 Jan 2025 00:31:08 GMT  
		Size: 208.9 MB (208912241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d96d4d86cae6e82230e1bb39125323e9c73dd893132f6e97976f3838d846309`  
		Last Modified: Wed, 29 Jan 2025 00:30:55 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
