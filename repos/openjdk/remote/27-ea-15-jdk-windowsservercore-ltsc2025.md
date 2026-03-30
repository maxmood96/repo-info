## `openjdk:27-ea-15-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:4ebcbcf220737de781cce64ea0b149ab7d64264d758efca095faafb3c1f4d57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `openjdk:27-ea-15-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:7accd34f8c829d37dc5f9fb70801a624b4405cb05c166b1a8be4d155fc9a3082
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2306784804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd41daa3bfa7a2471045a34b46be9a575d86faea61720e4f476fae2dcb08c22`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Mon, 30 Mar 2026 17:54:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 30 Mar 2026 17:55:42 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 30 Mar 2026 17:55:42 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 30 Mar 2026 17:55:51 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 30 Mar 2026 17:55:52 GMT
ENV JAVA_VERSION=27-ea+15
# Mon, 30 Mar 2026 17:55:53 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_windows-x64_bin.zip
# Mon, 30 Mar 2026 17:55:54 GMT
ENV JAVA_SHA256=c92682fdb3296015613f5a3618a274035eb14eda9c766cf4d96c37da415e698f
# Mon, 30 Mar 2026 17:57:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 30 Mar 2026 17:57:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf5ac1a0e6016df258b49485933e1647417c0ccc66f6689be4c67237f1a24c3`  
		Last Modified: Mon, 30 Mar 2026 17:57:27 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7390b0a6edfb524a49be51c2732a9497fe8d4312f94e70282da922ddb7fdac57`  
		Last Modified: Mon, 30 Mar 2026 17:57:28 GMT  
		Size: 406.9 KB (406930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715c9c180e033ab57eb34ad666e263c4c4ac437734b7ab25d8aa75f040996f70`  
		Last Modified: Mon, 30 Mar 2026 17:57:28 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec092ade9916c4485674e35c137081a95d732d9eb911bdc70c0cea485042e03`  
		Last Modified: Mon, 30 Mar 2026 17:57:28 GMT  
		Size: 349.4 KB (349444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da31719b1605f0adcf510a440b546f0993e7063f08e749fbd706a18943f566`  
		Last Modified: Mon, 30 Mar 2026 17:57:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04de6b8a1d2171b50ea1063cce854d09a22415b2ad7170cb2190c2fb26677301`  
		Last Modified: Mon, 30 Mar 2026 17:57:26 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfdc6356c97669063807948fe6faa827c39101bc09070e9b50f7d1886c265ea`  
		Last Modified: Mon, 30 Mar 2026 17:57:26 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411df1faa57791eb87dfb34c317cdcd81bce815927150e3a2550aaf558aec9c0`  
		Last Modified: Mon, 30 Mar 2026 17:57:40 GMT  
		Size: 224.8 MB (224824520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae8e3410b9acb76afe8d5b185e3b4e6199431895539f97a9d92b4c91d8c06df`  
		Last Modified: Mon, 30 Mar 2026 17:57:26 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
