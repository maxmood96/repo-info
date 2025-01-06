## `openjdk:24-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:6b48d5d5d709e23c63e6fd2568b50f02454649707c0fc10df4af6c58b454fcbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `openjdk:24-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull openjdk@sha256:bdb81a16ea6a9b3af42db33a2fe1c3769533c9514ad30e16401056b18278d068
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2463319483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fdbd8f95c714e49647a70ef909d345562e92832ec9ad43493f71e57987f871`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Sat, 14 Dec 2024 00:29:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 14 Dec 2024 00:30:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 14 Dec 2024 00:30:44 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 14 Dec 2024 00:30:54 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 14 Dec 2024 00:30:55 GMT
ENV JAVA_VERSION=24-ea+28
# Sat, 14 Dec 2024 00:30:55 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_windows-x64_bin.zip
# Sat, 14 Dec 2024 00:30:56 GMT
ENV JAVA_SHA256=ea0199fbcac35f83c9729678556b6d924f9e88b2a0669d982af3dc0cd06c3c84
# Sat, 14 Dec 2024 00:31:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 14 Dec 2024 00:31:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca98d559f45c275245b61c483f5cdc80533f6bdeb9f6c0a73b67f58cf793a83`  
		Last Modified: Sat, 14 Dec 2024 00:31:30 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3fe848074159664ea9cff95769729722f6db6151f1456b69d8fccddc822b08`  
		Last Modified: Sat, 14 Dec 2024 00:31:30 GMT  
		Size: 348.9 KB (348935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b01eb54dc9c5b458447812b14e18e01d460c3de370bb81f6d3f8e15b7aa4c8a`  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc61b7d2cac2c765f8481b8b1fadbe96e539698321e975ff31b5e2a69f2cbebf`  
		Last Modified: Sat, 14 Dec 2024 00:31:30 GMT  
		Size: 301.0 KB (301013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b15c7f7fb4e73f3d87f72cfb4e20ff2a8ef1ee1cbf0d248289bf59bf7d572a`  
		Last Modified: Sat, 14 Dec 2024 00:31:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d55ca2042e97647720b89e2c38d9c2b2261e579baba0f8004271fc46679544f`  
		Last Modified: Sat, 14 Dec 2024 00:31:29 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7bd6b90cb2e5d5b62f589ff0fbbbfb8af81169e1cf4e1f2eb0ed4ba800a4f6`  
		Last Modified: Sat, 14 Dec 2024 00:31:29 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05d8c8bc412785316ef52eb764ae3ae0afc233b05d53996a68a5b3c3b55c951`  
		Last Modified: Sat, 14 Dec 2024 00:31:39 GMT  
		Size: 208.8 MB (208788212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4554e9ce5380ff7dc335badcf29aad1f690c5aed9277fcd0515d3f7df6d4c23e`  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
