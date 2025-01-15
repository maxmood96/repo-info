## `openjdk:25-ea-5-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:5314f830de0e4c1a1b86185a7e3ebe5d97bd0341a04ace9ff11d82057ec57065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `openjdk:25-ea-5-jdk-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull openjdk@sha256:a7e4b5f6ec736dedea444c49a06ff23f53e82e7cef641c7b073989251bf37a6c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2463598482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ff51548be06609f4a375fb3ff858dbb2f7725c220ea8cb5f43716299c4c73f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Sat, 11 Jan 2025 02:28:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 11 Jan 2025 02:29:59 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 11 Jan 2025 02:30:00 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 11 Jan 2025 02:30:09 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 11 Jan 2025 02:30:10 GMT
ENV JAVA_VERSION=25-ea+5
# Sat, 11 Jan 2025 02:30:10 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_windows-x64_bin.zip
# Sat, 11 Jan 2025 02:30:11 GMT
ENV JAVA_SHA256=1fa831a6d9973fe9a64841dfd9c44759e07112be15da766d10c6f5e1b3eff4fe
# Sat, 11 Jan 2025 02:30:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 11 Jan 2025 02:30:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Fri, 13 Dec 2024 16:30:53 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c878281c2f98ea59bff23ae9e255bd95460d1a906cce0b90ccdfa151d4d7f1`  
		Last Modified: Sat, 11 Jan 2025 02:30:48 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f00be3b1e0ee8c913eb597f84195fb605026a1809935e92aafc1285bfa76df`  
		Last Modified: Sat, 11 Jan 2025 02:30:48 GMT  
		Size: 360.7 KB (360744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715151a62da56d1df6f7998d9714dc421f04858ad7d27701f2efd238d518937c`  
		Last Modified: Sat, 11 Jan 2025 02:30:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf432f394e5552c6a231ea50c7c71598c17058c816e4225042513df967b25d43`  
		Last Modified: Sat, 11 Jan 2025 02:30:48 GMT  
		Size: 348.1 KB (348130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d4b5fa4844995272a6841f615a7283ee011ab76967f75700e7124dca41f73b1`  
		Last Modified: Sat, 11 Jan 2025 02:30:46 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64ffa588c50dc3f201418457a92a32ab71ab57271029ede765a8abb20f64b64`  
		Last Modified: Sat, 11 Jan 2025 02:30:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96aaabb43312b38764d1107124c304bfe13740de2897a603d909c71f386f1162`  
		Last Modified: Sat, 11 Jan 2025 02:30:46 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd482210070620b17a2fb1d235c0ce209d1595925b453f21a5695a5e3070368`  
		Last Modified: Sat, 11 Jan 2025 02:30:57 GMT  
		Size: 209.0 MB (209008145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18274009b5d4a734e8b89b4244d508cca7b475bf1d4a40efe40d33097bfd7923`  
		Last Modified: Sat, 11 Jan 2025 02:30:46 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-5-jdk-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:336f0692cbc2538cd8ff9a48a9f847ae858f32ddefc96afae7fd060094e8e3e3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2223980472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887ad5b9c9107b6bdd90e83c537b608b5a197731736bd292b8cfa2d770c782e8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Sat, 11 Jan 2025 02:28:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 11 Jan 2025 02:30:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 11 Jan 2025 02:30:17 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 11 Jan 2025 02:30:25 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 11 Jan 2025 02:30:25 GMT
ENV JAVA_VERSION=25-ea+5
# Sat, 11 Jan 2025 02:30:26 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_windows-x64_bin.zip
# Sat, 11 Jan 2025 02:30:27 GMT
ENV JAVA_SHA256=1fa831a6d9973fe9a64841dfd9c44759e07112be15da766d10c6f5e1b3eff4fe
# Sat, 11 Jan 2025 02:31:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 11 Jan 2025 02:31:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272705a9967b96c82274de9e50a2a233dc0842381a7e25a99619fc5cc04a17cb`  
		Last Modified: Sat, 11 Jan 2025 02:31:24 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dded742292f3156ec8b88f2f1cb712bcbeb3594b9b72c52260572306fb32f24`  
		Last Modified: Sat, 11 Jan 2025 02:31:23 GMT  
		Size: 473.8 KB (473752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9642a55ba3e9b24db80c012d18dec50bc2d39ed41013f505ed70d71faf2c5d`  
		Last Modified: Sat, 11 Jan 2025 02:31:23 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258fcd306bcc9d2ac1cf34925722c09afa25d385e77e1716b95b06e200f16416`  
		Last Modified: Sat, 11 Jan 2025 02:31:23 GMT  
		Size: 331.3 KB (331255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b8c3dbf65dbbe412089c8d003e4f6d50f739f5e653abca2b6a886ff23a1a09`  
		Last Modified: Sat, 11 Jan 2025 02:31:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb7909e73c6b9fa6e34af8df8add6c298c6661e6e578905157a4a38b3e52512`  
		Last Modified: Sat, 11 Jan 2025 02:31:22 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14659a672e7b076ab957ab91cd3dbe763700987c5651a05af7b1786350db10d2`  
		Last Modified: Sat, 11 Jan 2025 02:31:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75eef43b105ad37cff5031d70c13e56572162bd2ce230b3e6a295d9f0f2593c`  
		Last Modified: Sat, 11 Jan 2025 02:31:34 GMT  
		Size: 209.0 MB (208997475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a6748634a85aff020430b55dee752da82f7b35d60d795790811f98300077ba`  
		Last Modified: Sat, 11 Jan 2025 02:31:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
