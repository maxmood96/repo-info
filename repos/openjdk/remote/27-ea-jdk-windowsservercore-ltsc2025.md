## `openjdk:27-ea-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:c2a60c227f9ccf68e8b6e01d5155dbc5479244190d6394d8129f88e41a45482e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `openjdk:27-ea-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:95778ee06762dbdad9ab0d7d9841b59ff12c6398e8a8c34a948d3b2c7d95301d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2503421109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8df2bbe78e5c406e4c752d08c57d0a0de8a151d97f0f1868bb17ad1b642ad6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:13:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:24:53 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:24:53 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 09 Jun 2026 22:24:59 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:24:59 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 22:25:00 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_windows-x64_bin.zip
# Tue, 09 Jun 2026 22:25:01 GMT
ENV JAVA_SHA256=ca4af1429ae7dc73528c0743f3134fe111133e114e23908c3e729538c6e203a3
# Tue, 09 Jun 2026 22:25:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:25:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde3f87c92fa7d0ae280c09db445ee43c8fe0d6469fc2c7ef39eccb597a279d6`  
		Last Modified: Tue, 09 Jun 2026 22:15:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e1ff36d89cd1ee2d0e44dd6237e4a88dccf1b6babd7716371f9c3703a19ce5`  
		Last Modified: Tue, 09 Jun 2026 22:25:29 GMT  
		Size: 387.5 KB (387459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a2ceffd1734ee5e91a622a39eee555c6eacc10e80fd75e59c5a0a0fefc7f16`  
		Last Modified: Tue, 09 Jun 2026 22:25:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70412fb2931200118c0e6dfe8c6df8605ba5d81e6505c5ed5432d7bee645e487`  
		Last Modified: Tue, 09 Jun 2026 22:25:29 GMT  
		Size: 370.5 KB (370509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192f89933bef71794d11001402304b82f0ffde2afdc9684eeca4cfba8adbcbe6`  
		Last Modified: Tue, 09 Jun 2026 22:25:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3fcabb69313d325c87148c43d468e13c79d6e8342ec54d49eacf861fd6c4b8`  
		Last Modified: Tue, 09 Jun 2026 22:25:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e35814dc77511e79732d987fb85105c0cfeb03948a6c10f1ccf00dd2145984`  
		Last Modified: Tue, 09 Jun 2026 22:25:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2917348d58675ad00273c5d358c3c31fcbb22ef5b930b45a81a4e24343ebd4`  
		Last Modified: Tue, 09 Jun 2026 22:25:43 GMT  
		Size: 223.5 MB (223512368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00179f524605030d444d7b4db0043a1ce48645157b2bf34beaa5dcb5ac6825d4`  
		Last Modified: Tue, 09 Jun 2026 22:25:27 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
