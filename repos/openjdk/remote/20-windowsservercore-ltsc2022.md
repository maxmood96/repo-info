## `openjdk:20-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:2a0d9e2c975f0a6927ce366a7630a79126e0d37928ef4bdcba0ae47499f1c564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.768; amd64

### `openjdk:20-windowsservercore-ltsc2022` - windows version 10.0.20348.768; amd64

```console
$ docker pull openjdk@sha256:49130bb9f65c6e942150b51a19439fab8410398285b3fd829fe4a5a8449d6e06
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2472446705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38253345dbfb810bab0db3516958a2ab8713252a27334bee8b47750800ae76f2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 09 Jun 2022 04:32:50 GMT
RUN Install update 10.0.20348.768
# Wed, 15 Jun 2022 12:13:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 19:30:14 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 16 Jun 2022 01:14:39 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 16 Jun 2022 01:15:08 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 28 Jun 2022 00:14:58 GMT
ENV JAVA_VERSION=20-ea+3
# Tue, 28 Jun 2022 00:15:00 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/3/GPL/openjdk-20-ea+3_windows-x64_bin.zip
# Tue, 28 Jun 2022 00:15:01 GMT
ENV JAVA_SHA256=d6bd89dafc55e34638d75e312e32bea22f8b2132baf19c2749e8dbe5fda7c5bb
# Tue, 28 Jun 2022 00:15:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 28 Jun 2022 00:15:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6c71967ff41928927e4c407171e4ffbac3c9ab4221eb64f5ca5a34ff4c230567`  
		Size: 841.6 MB (841600427 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dec0338feaf01f35eb916b7fd9ecc08b719354163254885d5215e513c1a3eb2e`  
		Last Modified: Wed, 15 Jun 2022 12:49:26 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b6e059d50cccbff94037bf242f1b94acf1cc939d701dff58c07f4fcfdc9767`  
		Last Modified: Wed, 15 Jun 2022 20:02:04 GMT  
		Size: 632.3 KB (632288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e4ff554b66055922423d154f7282c8144066ebe31d1393200cf475fb56555f`  
		Last Modified: Thu, 16 Jun 2022 01:26:02 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a207dedd7fa079f899254dd9a6ea4b20cbb4e77f9880ed19716901e210c1e42f`  
		Last Modified: Thu, 16 Jun 2022 01:26:02 GMT  
		Size: 564.2 KB (564202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2af4ee24347f154b1cf7fcb4aa2f97a75e82031c6e7f85474281553e37f2a5`  
		Last Modified: Tue, 28 Jun 2022 02:20:28 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d334f11f87fa4f9130548a41ce4eaf125c5cf80ac1c80b7e48888a1e0ce9ffe`  
		Last Modified: Tue, 28 Jun 2022 02:20:28 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dfb423ee6f29077b4623f20b91fbed731edc97e08ab19d70afcc519b43239e`  
		Last Modified: Tue, 28 Jun 2022 02:20:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aef8f8682b9dc25941354dc8cc65d34f5865d601f3b416feed15610359b95cf`  
		Last Modified: Tue, 28 Jun 2022 02:20:49 GMT  
		Size: 192.8 MB (192777648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8f8b91950493bcc4bc5c0754cbfd0331d3bbf2df4cffc3b6c5f047a6165a36`  
		Last Modified: Tue, 28 Jun 2022 02:20:28 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
