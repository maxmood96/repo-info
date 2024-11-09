## `openjdk:24-ea-23-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:d9a22bad9b70b3f8d4c6805590309ef6dfd8ac17a979f5d80a08d1dbf2f8e7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `openjdk:24-ea-23-jdk-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull openjdk@sha256:058498ed0a4b223a45802935140b701ba29b02440e3e2d203b41fe7116978e19
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2009844213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07712de216130c461922e720580bd5749c5d8bedb4f36dbaaca16dc832a008e6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Sat, 09 Nov 2024 02:03:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 09 Nov 2024 02:04:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 09 Nov 2024 02:04:24 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 09 Nov 2024 02:04:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 09 Nov 2024 02:04:31 GMT
ENV JAVA_VERSION=24-ea+23
# Sat, 09 Nov 2024 02:04:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_windows-x64_bin.zip
# Sat, 09 Nov 2024 02:04:32 GMT
ENV JAVA_SHA256=9fb6091495ba5cf912000206d77fcacbcb294c4cb27a11538fa5b1eb69ffc1d6
# Sat, 09 Nov 2024 02:05:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 09 Nov 2024 02:05:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd5bed3ade7fff0edc5a7892cc49918710c780c9009fef47c98fad854ccaa44`  
		Last Modified: Sat, 09 Nov 2024 02:05:10 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77be1ef8fe770ed749b7730f8bbf82f2f34e906d87e9f3310db7d5e73608b941`  
		Last Modified: Sat, 09 Nov 2024 02:05:10 GMT  
		Size: 494.4 KB (494418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab1df8e0cd45ce6bc916ce0d1cd86ced99c90de9b01f4d3021f38ec31d035da`  
		Last Modified: Sat, 09 Nov 2024 02:05:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499eff960881ac01b5dee295b93d4c89cb683f47bbf31677d85fff073d242623`  
		Last Modified: Sat, 09 Nov 2024 02:05:10 GMT  
		Size: 312.5 KB (312455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca36a6c7ac4f8c6941a39213a727a117861875c92f85c248c8f9fc98feddc73`  
		Last Modified: Sat, 09 Nov 2024 02:05:09 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747e3c3c8253945e7056accb866d34c0d2d9cb1ce48ab12584d19053f9330289`  
		Last Modified: Sat, 09 Nov 2024 02:05:09 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d03b329872ef228cf770d27f2405e9db131d4026c853c6306fe419cddf09ada`  
		Last Modified: Sat, 09 Nov 2024 02:05:09 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7ca5d54ff506dbcda9c5ac572d07ba2bac5b76f54c8eb22054cfd0172e696c`  
		Last Modified: Sat, 09 Nov 2024 02:05:20 GMT  
		Size: 209.7 MB (209687869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6a0460e9a46e82a01281fe6889503e853b0acf1322dca2730a4d75afd49e99`  
		Last Modified: Sat, 09 Nov 2024 02:05:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-23-jdk-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull openjdk@sha256:969e04b557642c564e3b396f524d52cb27d3ae9dee8d45e3334b7a6356f7c2ed
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2112328068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4898223c88d4d8bafbc3dac1f57f9aca161cfe45dbe3e4bfcb467c2453a558`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Sat, 09 Nov 2024 02:03:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 09 Nov 2024 02:05:21 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 09 Nov 2024 02:05:21 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 09 Nov 2024 02:05:36 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 09 Nov 2024 02:05:37 GMT
ENV JAVA_VERSION=24-ea+23
# Sat, 09 Nov 2024 02:05:38 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_windows-x64_bin.zip
# Sat, 09 Nov 2024 02:05:38 GMT
ENV JAVA_SHA256=9fb6091495ba5cf912000206d77fcacbcb294c4cb27a11538fa5b1eb69ffc1d6
# Sat, 09 Nov 2024 02:06:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 09 Nov 2024 02:06:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002c2d759819c27ad539edf635efe2a5722966bd693186c8a7ecbe6e69f43cef`  
		Last Modified: Sat, 09 Nov 2024 02:06:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49834833d3d2d88cc57ddd545f00bca8519d6066d7761974e8bef53c5ce0d986`  
		Last Modified: Sat, 09 Nov 2024 02:06:26 GMT  
		Size: 474.0 KB (474042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54356a46c464ab9098df5907f25ec1f2326af518df1d0589b5709cee93cc3279`  
		Last Modified: Sat, 09 Nov 2024 02:06:26 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be58a390034e73d8f9b2e084c5f0f907c29751565b5317e4c12ed25604c8a723`  
		Last Modified: Sat, 09 Nov 2024 02:06:25 GMT  
		Size: 317.1 KB (317091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134eb492068655fb17a022262100fd22f73ff8a23432088ce68d36aed30db45f`  
		Last Modified: Sat, 09 Nov 2024 02:06:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1667b37fa5dd7780fc617d650f36b4b0e66b202a422360a02c01f2e62bd548`  
		Last Modified: Sat, 09 Nov 2024 02:06:23 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2c409aebc42380d89d3da3b6e9a374fc468cfefeb8906960846c73c9cdac0f`  
		Last Modified: Sat, 09 Nov 2024 02:06:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b051327a094398e8876c9416aac74fb2a4111c29e54bfda1326c4472c9195c8e`  
		Last Modified: Sat, 09 Nov 2024 02:06:34 GMT  
		Size: 209.7 MB (209703925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e587b222b6a7b2f480cc9938989ee8e8546e95f7415c6b6c070963816f12150c`  
		Last Modified: Sat, 09 Nov 2024 02:06:23 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
