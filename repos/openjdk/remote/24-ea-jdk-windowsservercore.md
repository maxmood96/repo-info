## `openjdk:24-ea-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:d5dbf798dbb1af66ac3284d631f749f356caf48c4a91aceb3edf9da149f9861a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `openjdk:24-ea-jdk-windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull openjdk@sha256:26c3c664ff1857856722a5a92c33b548626ed885a2a40c9ec5e47f6e7229e522
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2462874703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a353d3305f12e4828862f50db2ef9b83fb10befe8a5587d9983172d0e333cef`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:10:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:10:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:10:18 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 14 Nov 2024 20:10:25 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:10:27 GMT
ENV JAVA_VERSION=24-ea+23
# Thu, 14 Nov 2024 20:10:28 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_windows-x64_bin.zip
# Thu, 14 Nov 2024 20:10:30 GMT
ENV JAVA_SHA256=9fb6091495ba5cf912000206d77fcacbcb294c4cb27a11538fa5b1eb69ffc1d6
# Thu, 14 Nov 2024 20:10:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:10:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f74bc27198767647376bb07ea46e29b1a4688dadf18283735943e8ebb25e132`  
		Last Modified: Thu, 14 Nov 2024 20:10:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f8dd3cb4408526b377b17c696adb94aeef4c51562ebf22a326ada036b418a2`  
		Last Modified: Thu, 14 Nov 2024 20:10:58 GMT  
		Size: 356.1 KB (356128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dd02bc3d989c373c55b07ef0672d1beb310aa4179676f11d8146441115ae86`  
		Last Modified: Thu, 14 Nov 2024 20:10:57 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c8710de72bee99af3e8606cbf039c2b6905d9fb109fcdc2c4477d590a27a86`  
		Last Modified: Thu, 14 Nov 2024 20:10:58 GMT  
		Size: 340.0 KB (339961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720345e52748d00e2807c8aa19da686a68f6e361f0da22a7d143d4b3c75e4ac8`  
		Last Modified: Thu, 14 Nov 2024 20:10:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60dcd7a5b6670c0c2111533654fbeff94bbacf6effd327e4fd97304bdd0f4925`  
		Last Modified: Thu, 14 Nov 2024 20:10:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bcdf760c8266637168a3ab824860fc465c7ff9d42da31389e17a52f93099e3`  
		Last Modified: Thu, 14 Nov 2024 20:10:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a3b765d492ad3ce33ebabaa9bed323aaa58a36d1ff87d0c5b4056a09938b0c`  
		Last Modified: Thu, 14 Nov 2024 20:11:07 GMT  
		Size: 209.7 MB (209686652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b464a6c11e859aaa99dd763010fa73831e00e6fc4e10bdf2e3c37b45026ceb4e`  
		Last Modified: Thu, 14 Nov 2024 20:10:55 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-jdk-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull openjdk@sha256:873e5dc61a6716ade93b3b78a05a895640f0c21e7bbdfb73a78e5f2a66377ea7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221231693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c11015095ca37a5d06a0a1a82d3057e13034e33e99d7f309fe0e258065f40b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:18:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:19:30 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:19:30 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 14 Nov 2024 20:19:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:19:37 GMT
ENV JAVA_VERSION=24-ea+23
# Thu, 14 Nov 2024 20:19:39 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_windows-x64_bin.zip
# Thu, 14 Nov 2024 20:19:39 GMT
ENV JAVA_SHA256=9fb6091495ba5cf912000206d77fcacbcb294c4cb27a11538fa5b1eb69ffc1d6
# Thu, 14 Nov 2024 20:20:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:20:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047255a5b4c230ba449a5a416cac7169f0617d248be31bd36a2f8db084ddf06e`  
		Last Modified: Thu, 14 Nov 2024 20:20:14 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367d6a90f60098c635836c84b50d303b4fa488cf7b50003f9391ab0b5a0fa8e1`  
		Last Modified: Thu, 14 Nov 2024 20:20:14 GMT  
		Size: 500.6 KB (500637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94176e645fad954789f8b762c201e3aeb7d3e39d7f35a5487398ab4784b075b`  
		Last Modified: Thu, 14 Nov 2024 20:20:14 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35f821593c3b807bcbf4c6a842c7eeda9b85a58675fe0b842c918175329ef84`  
		Last Modified: Thu, 14 Nov 2024 20:20:14 GMT  
		Size: 345.3 KB (345285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df15b3a2ed62a5dac7e8e2d3e5f4ec5658ef32e8abfea1ea0368b8738757af68`  
		Last Modified: Thu, 14 Nov 2024 20:20:13 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9185d51019b97beb4012493dfd5d8ebd03a459d286e8095e2cd53f77e74c39d8`  
		Last Modified: Thu, 14 Nov 2024 20:20:13 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb18693fe8a4340c7bf3f7ad4c089d773e3416e4e55fe031cfb43f7de6637176`  
		Last Modified: Thu, 14 Nov 2024 20:20:13 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb739d47b45e398a33e713f060fe619cd18033203a76f416b80729a266849aa`  
		Last Modified: Thu, 14 Nov 2024 20:20:24 GMT  
		Size: 209.7 MB (209724079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe73adee5f59ef6c0c7f7930925add3ea940c47ff8f9aca480e04231f79266`  
		Last Modified: Thu, 14 Nov 2024 20:20:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
