## `openjdk:26-ea-2-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:87974cc54bf4f385a3786238ba6b85ff8fa10ff32692260e80dfc1871df145b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `openjdk:26-ea-2-jdk-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:e7738f7272419e976a8581a3c4a5fa6e98955c295f86aa2270381f7510dc7174
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3695736242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5e21bf08e798c349acb3630aeeabe546c6cc694e30aacea1cf70f07e0e2d48`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Mon, 16 Jun 2025 17:56:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Jun 2025 17:56:28 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 16 Jun 2025 17:56:30 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 16 Jun 2025 17:56:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 16 Jun 2025 17:56:39 GMT
ENV JAVA_VERSION=26-ea+2
# Mon, 16 Jun 2025 17:56:41 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_windows-x64_bin.zip
# Mon, 16 Jun 2025 17:56:42 GMT
ENV JAVA_SHA256=a9f823b291381b908d5f1a0ffaf16b5ff2b8749780ab76db3b8e8fde9bf04be0
# Mon, 16 Jun 2025 17:57:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 16 Jun 2025 17:57:04 GMT
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
	-	`sha256:ffb4e9ac69db5330ec2ffd3d7316079b7bc261ee06297d591f1db9147d900212`  
		Last Modified: Mon, 16 Jun 2025 18:00:35 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffdcb2820a23d8664e4a34410beabcd0966492a0d777f3fed832fda8b2dcb6`  
		Last Modified: Mon, 16 Jun 2025 18:00:36 GMT  
		Size: 404.5 KB (404541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4338a1f01c990f38548885294090261041e8df0fb096952368ff4def12b18b86`  
		Last Modified: Mon, 16 Jun 2025 18:00:36 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5befc4860767a48e07206d6c9da671b09ef2938ca842403b6b50c98241462c41`  
		Last Modified: Mon, 16 Jun 2025 18:00:36 GMT  
		Size: 385.9 KB (385865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17851a54a4189ae5b2c214714d828d4f9f31d9f2b2b4318deb649a6340064185`  
		Last Modified: Mon, 16 Jun 2025 18:00:36 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e7bc921e0e741a0a38f9262ede81743addebfde3a2b16a76ccce87946f9aa2`  
		Last Modified: Mon, 16 Jun 2025 18:00:36 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61dd1d1f15481d0df6d14448c19684684cfe7c3b60652b435aa6543ce210787`  
		Last Modified: Mon, 16 Jun 2025 18:00:36 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00831ed440681c1e666835552e58c0c09f51725973ce406908f40c14a10872c2`  
		Last Modified: Mon, 16 Jun 2025 18:09:16 GMT  
		Size: 218.8 MB (218763814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cc4b232ba17d2136b2d19e322290d951c543023eb1606d659b6ae8361cc92e`  
		Last Modified: Mon, 16 Jun 2025 18:00:37 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
