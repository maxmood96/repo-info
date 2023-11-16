## `openjdk:22-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:c858f726bf41a3cc3805c5b3ad7c5fb8d786ac35adb5887c3a4535c7e7665a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `openjdk:22-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull openjdk@sha256:e09c2f296f1dec472d3be1e7cc0336e74e1bdbe51dfbe4c0756b1f5b80761714
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2087770200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3355f7200d366bcbd9b0381fff86b6f860d4c08fb1405903eb844b9002e79089`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 05:18:36 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 16 Nov 2023 05:18:37 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 16 Nov 2023 05:18:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 16 Nov 2023 05:18:57 GMT
ENV JAVA_VERSION=22-ea+23
# Thu, 16 Nov 2023 05:18:58 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/23/GPL/openjdk-22-ea+23_windows-x64_bin.zip
# Thu, 16 Nov 2023 05:18:59 GMT
ENV JAVA_SHA256=25e3fa403b5e501bf5e66189205dd806161aeef87a3a35b861fa3f46ab286852
# Thu, 16 Nov 2023 05:19:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 16 Nov 2023 05:19:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c484d21f80984bc956d2a7ca187c7250676fd3af73a362efb91125bb6255aa10`  
		Last Modified: Thu, 16 Nov 2023 05:26:11 GMT  
		Size: 453.2 KB (453223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaf9eb81e5d07980ecf0f7d31f640ebd53980837baa8588ca770fa56963edd6`  
		Last Modified: Thu, 16 Nov 2023 05:26:11 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be91ce40f73c6eaafd338b1fc738f4394dc6542fd074fc12e651a47dfd49e6f3`  
		Last Modified: Thu, 16 Nov 2023 05:26:11 GMT  
		Size: 263.4 KB (263380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d40036d0564f1cd5c20cd138543dcccb4f381f7797131bf7af94ed4722f69`  
		Last Modified: Thu, 16 Nov 2023 05:26:09 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69dfbdd411f2378da8f1d6a8ed54a39e4f47a62cdd9a15158341bfcfde0b202`  
		Last Modified: Thu, 16 Nov 2023 05:26:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa86781ea7b6f9a783b9270139f3925847b8ea15390b3c7a0460f0c7e1cc698`  
		Last Modified: Thu, 16 Nov 2023 05:26:09 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acb5cdd65908e07cb4bc89253add3ffa8410457401ee938dbe4621206ae2aba`  
		Last Modified: Thu, 16 Nov 2023 05:26:29 GMT  
		Size: 200.3 MB (200264251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46128ab4defdaf4fd730c08956aceaed0b42474de58de04fd3dc4b6906c1657a`  
		Last Modified: Thu, 16 Nov 2023 05:26:09 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
