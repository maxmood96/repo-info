## `openjdk:24-ea-23-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:cc59fdfa760f3e0d61fd35f264f91c6e1adb6a511bf6425cf50eef677c6a96fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `openjdk:24-ea-23-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

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
