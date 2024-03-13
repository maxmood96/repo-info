## `openjdk:23-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:e4caa8af69724be051b1362241bcf68bbf0d013fea0c60b2ad30ca9707ae4491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `openjdk:23-ea-windowsservercore` - windows version 10.0.20348.2340; amd64

```console
$ docker pull openjdk@sha256:42f9ab5ccc626eaac98901f84999b1f3e7949696fa2e5f9f2964b230cbe9864f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2155850999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16650828315302799e435c786371ac027728b280e937c33e6010a087ed47cd4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:07:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 00:07:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 13 Mar 2024 00:07:25 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 13 Mar 2024 00:07:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 13 Mar 2024 00:07:32 GMT
ENV JAVA_VERSION=23-ea+13
# Wed, 13 Mar 2024 00:07:33 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_windows-x64_bin.zip
# Wed, 13 Mar 2024 00:07:33 GMT
ENV JAVA_SHA256=f8ee056a7c33a543e7562d171b9f032a45db3be0f5fc2ecc6d5b4eb70aaeed87
# Wed, 13 Mar 2024 00:07:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 13 Mar 2024 00:07:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee8511fb889a434b260e4e5fca58e30e58267d34294ad920b944ccf2fd3b95d`  
		Last Modified: Wed, 13 Mar 2024 00:08:01 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9c053e1a10828b9eebabebc46419ba6a9ebcb0949b59fdb91317747420eba4`  
		Last Modified: Wed, 13 Mar 2024 00:08:02 GMT  
		Size: 499.5 KB (499542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e67e30b9986c8c862f9578677dab755d08a6a6c64fefdcb1c37440f3855e96`  
		Last Modified: Wed, 13 Mar 2024 00:08:01 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de7c8aa2a9a423c667e3ae5809414634505d5663f6c8c15275e5beed546a15f`  
		Last Modified: Wed, 13 Mar 2024 00:08:01 GMT  
		Size: 348.3 KB (348267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19d8f9a3850dde2b67d3218fddfbfe652eeec3efc19d1cacadeec57d379a2ed`  
		Last Modified: Wed, 13 Mar 2024 00:08:00 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83de863d017cec82f1574d79254771ebf6165158ccd79c201caf1704b9892fbd`  
		Last Modified: Wed, 13 Mar 2024 00:08:00 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf65910e7c33872d120ccfabbdc77f9287f3ad059b7eb81fc8f0df27b3925f2`  
		Last Modified: Wed, 13 Mar 2024 00:08:00 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab9db09c4f81a5cee6dcafb3991b6730367e9f0476dc242e450ae216336d28`  
		Last Modified: Wed, 13 Mar 2024 00:08:11 GMT  
		Size: 197.5 MB (197536172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee600f144a5c0b49a18c6c192ee602b5b8443b5a71a9f2d899fcf5393ed02c1`  
		Last Modified: Wed, 13 Mar 2024 00:08:00 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull openjdk@sha256:836fbe87d04db44db833852b31cc9bfc673b9cefa0e3baa8e1c3df2ebb188014
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323457625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715e8e18dcbcdfa228512ef23c4721fe7032c1c1971f588243bdf77c50d1dbd5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:14:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 00:14:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 13 Mar 2024 00:14:45 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 13 Mar 2024 00:15:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 13 Mar 2024 00:15:06 GMT
ENV JAVA_VERSION=23-ea+13
# Wed, 13 Mar 2024 00:15:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_windows-x64_bin.zip
# Wed, 13 Mar 2024 00:15:07 GMT
ENV JAVA_SHA256=f8ee056a7c33a543e7562d171b9f032a45db3be0f5fc2ecc6d5b4eb70aaeed87
# Wed, 13 Mar 2024 00:15:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 13 Mar 2024 00:15:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b84738d8d9b75277c3998d990329009f49d86c017fa39c51698c703d108fd1d`  
		Last Modified: Wed, 13 Mar 2024 00:15:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2000fc3d3c413a9cbf245536f737c62247a39944a3a048e49a5aedf9f17fca`  
		Last Modified: Wed, 13 Mar 2024 00:15:55 GMT  
		Size: 490.6 KB (490613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693842fa233e16cfbe580c1dff185de2ed2f32492c4eaa8382ac6404f62fc6bc`  
		Last Modified: Wed, 13 Mar 2024 00:15:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3b03669423be7f32369e6e2cfc448827e9b7034c853fa12dcb68c3862420be`  
		Last Modified: Wed, 13 Mar 2024 00:15:55 GMT  
		Size: 334.1 KB (334131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8498bfb24bb1a550a5c41f0ca7ccb99e1816c4b03f1815a2cb9afba735da06`  
		Last Modified: Wed, 13 Mar 2024 00:15:53 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7411d6f348108e8adeb6f89d44b34d220ddf679e6b599939e7131c2a4fe6ed1`  
		Last Modified: Wed, 13 Mar 2024 00:15:53 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2496154444ce71ce8b9fee79a6c263138758eb7a3bed8349f2d83b6f37a315b`  
		Last Modified: Wed, 13 Mar 2024 00:15:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ddf507f2cd78b6a75ac285102379f27c4537b2d28dcbc8b813caeeca6ec6b6`  
		Last Modified: Wed, 13 Mar 2024 00:16:05 GMT  
		Size: 197.5 MB (197525173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7379222298b54d8d4c6e1c7602cf1dd2979dd282c8d4d9053fa926cb42b46a86`  
		Last Modified: Wed, 13 Mar 2024 00:15:53 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
