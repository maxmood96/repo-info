## `openjdk:25-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:0fdbe1aece9db8ab4b6bd6cbc4ea6669a70d2634164bd28f9d890a31267f230e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-jdk-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:e87db0ac62015739354288728d009b0542574e53f037431bad9b122edf18bbe1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2708935320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a7ec8d15e6a2addf248573e5ad58d3a1f71b2c9f8effdce74ebe16a7e698b1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 31 Jan 2025 22:29:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 22:29:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:29:17 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 31 Jan 2025 22:29:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:29:23 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 22:29:23 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_windows-x64_bin.zip
# Fri, 31 Jan 2025 22:29:24 GMT
ENV JAVA_SHA256=3ea9473d90c2a51f51d40081e60eb97a8fd26b8f787d9b44a51f102714942cf6
# Fri, 31 Jan 2025 22:29:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:29:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789e240b6ca4edd94eea73033ddd6cb81efdbfdbae912cc81c0f2ae8ec56aca1`  
		Last Modified: Fri, 31 Jan 2025 22:29:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b043d0d44a4013839901be345a9d6a2d55ffe90e1ea55a4c4176aaba1a21c9`  
		Last Modified: Fri, 31 Jan 2025 22:29:45 GMT  
		Size: 393.7 KB (393675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c8730d8e619a13b07df385ef40a92ab645cce8da882d24892add7f16f3bee0`  
		Last Modified: Fri, 31 Jan 2025 22:29:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8539e717fe13546ef9445e7add6a35dd448f93134bc0874c639d648b6e8f44c`  
		Last Modified: Fri, 31 Jan 2025 22:29:45 GMT  
		Size: 368.1 KB (368114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c169841c8cc6b79796217126bcd4ac55c6aacd68aba4a10055e0fc07c4307e`  
		Last Modified: Fri, 31 Jan 2025 22:29:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a9337b2a91091e54b93c62ccd1c38e707c927a24880aa9d865f2cda537935`  
		Last Modified: Fri, 31 Jan 2025 22:29:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df25961ef7a8e26f93b3d8cc656e314925c42aa41e3ebbf2417f250c75c1a6af`  
		Last Modified: Fri, 31 Jan 2025 22:29:44 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0a33e292e7a3d4ec393b35f91288306deec07b4c092bd20d32d81bd00c9873`  
		Last Modified: Fri, 31 Jan 2025 22:29:57 GMT  
		Size: 207.9 MB (207888192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a145308567f61aacb54508d6f9fe3e10a2cfd07d2f6a0fec7db4df1295f92efb`  
		Last Modified: Fri, 31 Jan 2025 22:29:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:1fcdef628e17a3484212e562f28ee874fbad429a9bfc4a56284eeeb74d4a68e5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470882360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbab32008d48f89b4b481aadfca3a5e0b501f68bc876c77eac7ffc2c45a4475f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 31 Jan 2025 22:25:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 22:27:34 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:27:36 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 31 Jan 2025 22:27:46 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:27:47 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 22:27:49 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_windows-x64_bin.zip
# Fri, 31 Jan 2025 22:27:51 GMT
ENV JAVA_SHA256=3ea9473d90c2a51f51d40081e60eb97a8fd26b8f787d9b44a51f102714942cf6
# Fri, 31 Jan 2025 22:28:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:28:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71f85c9141db75f8fc9268ca5711e72eb0aebe7dd6a36abbe915f9a25b867dc`  
		Last Modified: Fri, 31 Jan 2025 22:28:30 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32886b9bccd03909abd9bd7f2c7b010cc032c3e467a0b3319146701d3bed0616`  
		Last Modified: Fri, 31 Jan 2025 22:28:30 GMT  
		Size: 365.1 KB (365134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541de414409d9a1bd158da2596368f3c72494381e41649bb566c4e55037eba3f`  
		Last Modified: Fri, 31 Jan 2025 22:28:30 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc839431119e5c92250d8e32357cbcfef99ce1c7b88c92250bfe33f2711fd123`  
		Last Modified: Fri, 31 Jan 2025 22:28:30 GMT  
		Size: 312.7 KB (312670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988ec8e38b236ebe94453749be3271c37c619673d48bc1ef9a9056bbcaafbbae`  
		Last Modified: Fri, 31 Jan 2025 22:28:28 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c72dc12907c4deb46f88646b3c29463b5cf71ae397f4da5e6ac1e2ee693d7fc`  
		Last Modified: Fri, 31 Jan 2025 22:28:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20d223b0839ab6e81252769c96f7871ecf1afc6ce090346386d43cc18db5b6a`  
		Last Modified: Fri, 31 Jan 2025 22:28:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7e9c483440fa0de44b91e2ae75d2060293b261072da56c4d7c22fc57d73e90`  
		Last Modified: Fri, 31 Jan 2025 22:28:39 GMT  
		Size: 207.8 MB (207811427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9ab527f8f9a73f9d3130ff650c66a3d9766cd151f167acebbf8504bf900347`  
		Last Modified: Fri, 31 Jan 2025 22:28:28 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:9f20696c0a390bd3ec8bb36b13fca3e8759ff76065faf65b5e24126264e874ad
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330732650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9176ef8a0a9227d5730ebfa156bb9b53a87274a64a530e27a82ab2568391781`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 31 Jan 2025 22:25:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 22:27:20 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:27:21 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 31 Jan 2025 22:27:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:27:31 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 22:27:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_windows-x64_bin.zip
# Fri, 31 Jan 2025 22:27:32 GMT
ENV JAVA_SHA256=3ea9473d90c2a51f51d40081e60eb97a8fd26b8f787d9b44a51f102714942cf6
# Fri, 31 Jan 2025 22:28:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:28:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d814447db0c64d6643ac83787d41f5feb0f0d0839821c103fb8dcfd368b171`  
		Last Modified: Fri, 31 Jan 2025 22:28:15 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e1bfb1a53782ac86fca66a4f7c49aed747fe51f57d7aeffb3dd8c527c30b5`  
		Last Modified: Fri, 31 Jan 2025 22:28:15 GMT  
		Size: 341.9 KB (341942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0740fe5e74442f58a075e266f6124dd5798d6c31758a1d0531f81d0ad5b544`  
		Last Modified: Fri, 31 Jan 2025 22:28:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601442e1c4921de89048e5db73834991674e5a67a27a1ccd539310eddd338608`  
		Last Modified: Fri, 31 Jan 2025 22:28:15 GMT  
		Size: 332.2 KB (332153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056d5a4d6b273cdcd02665c0fd0561ad0108956a0e61204a68b60db5ec4e6e71`  
		Last Modified: Fri, 31 Jan 2025 22:28:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0525e73b9fb2105a33d11ed0adcde5239b338971507e91f3fa3cdb5a76bbbf9`  
		Last Modified: Fri, 31 Jan 2025 22:28:14 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af222e521a45820e52cd8929f0272c1b727590f5773d5af76532332fac593e1`  
		Last Modified: Fri, 31 Jan 2025 22:28:14 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34135800246333aab2c9f24d644be2bab0e23871ab7a208d272b2c564d69ccdc`  
		Last Modified: Fri, 31 Jan 2025 22:28:24 GMT  
		Size: 207.8 MB (207838507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698bc11035faf34b25ef0ee7decfad106e48695b2b6211cf7b4b03cb245ea7d3`  
		Last Modified: Fri, 31 Jan 2025 22:28:14 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
