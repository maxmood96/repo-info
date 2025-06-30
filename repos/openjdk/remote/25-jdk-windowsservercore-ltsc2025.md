## `openjdk:25-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:f8456f06bbd86fc0b5dccf4916b3f20a427de5571de7f898b731532c43edb0e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `openjdk:25-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:acf5f59999512f6ea1c15582061e89cd34d73dfd6a0124a63faeab8c259e056b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3695880398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3549407f67fcbd654cdd917d8dfe8d3eea2d9cd48c8387bdc1e020601c72891`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Mon, 30 Jun 2025 17:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 30 Jun 2025 17:34:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:34:17 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 30 Jun 2025 17:34:23 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:34:24 GMT
ENV JAVA_VERSION=25-ea+29
# Mon, 30 Jun 2025 17:34:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_windows-x64_bin.zip
# Mon, 30 Jun 2025 17:34:25 GMT
ENV JAVA_SHA256=397a0df027bd02d080370a97f2ef38cd9130020afb8e124d86949c681e2cf191
# Mon, 30 Jun 2025 17:34:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:34:45 GMT
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
	-	`sha256:e5ce60371b30b92ee83806dafb4392b1739cd6221758f36d160e71c49a7d814a`  
		Last Modified: Mon, 30 Jun 2025 17:38:12 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86940ce2ed1474859f47a4b2a88b2892bc48b925d3807250355a279e86c43012`  
		Last Modified: Mon, 30 Jun 2025 17:38:12 GMT  
		Size: 403.5 KB (403485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6085b77f73c31521d773d475b17009ca1ef5c319f5f65004cba55d259441e4ea`  
		Last Modified: Mon, 30 Jun 2025 17:38:12 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b3fc94f1a479a4419b8c4e95e59e9d084df7be6015719487643a9d94c5fa7a`  
		Last Modified: Mon, 30 Jun 2025 17:38:12 GMT  
		Size: 384.7 KB (384739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce506488f3dc9ce87228f7c1d2647aebdddf1422e6d24539901c171e2474da2`  
		Last Modified: Mon, 30 Jun 2025 17:38:12 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b66d1c24189e25845057d8f7bc131298b18506f83d144cc70d605cf701b7c3`  
		Last Modified: Mon, 30 Jun 2025 17:38:12 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f6efbbc7ec85c8e9d968eb6497091c728ff1ddb089aac46c8df07a09169916`  
		Last Modified: Mon, 30 Jun 2025 17:38:12 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33ab5529f598d3db69e9b5be9a047f8340b58cd1e2da849a2fba28d389d244b`  
		Last Modified: Mon, 30 Jun 2025 18:10:12 GMT  
		Size: 218.9 MB (218910072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820a5ff5b2ed28c0d1e10a685f4047646d2e345c03e9f118383d3a0865335cfd`  
		Last Modified: Mon, 30 Jun 2025 17:38:12 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
