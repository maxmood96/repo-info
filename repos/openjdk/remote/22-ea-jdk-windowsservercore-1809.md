## `openjdk:22-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:b13fd52c37a437e9dcedc33b50c9279b374c9a1af7c9801790a4a1ad17a4ecc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:22-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:668c0e2679cbca11b7b7e4db464541a10f3b5119813cc7353d6653ee08ab4646
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268270108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd389cd3b2c0493b9639b9fa5e0470389b98f6ce85769a15f187d21b1e6d51e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Sat, 13 Jan 2024 01:14:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 13 Jan 2024 01:15:39 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 13 Jan 2024 01:15:40 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 13 Jan 2024 01:16:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 13 Jan 2024 01:16:01 GMT
ENV JAVA_VERSION=22-ea+31
# Sat, 13 Jan 2024 01:16:02 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_windows-x64_bin.zip
# Sat, 13 Jan 2024 01:16:02 GMT
ENV JAVA_SHA256=4b5b81fcbe9e209bde075929fc5e99b71fd2ec4b2ad046404aec3476daf5c148
# Sat, 13 Jan 2024 01:16:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 13 Jan 2024 01:16:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34560556ae62825aa774d8d57f017e3c154dfad25274d9dcd117868a1479b782`  
		Last Modified: Sat, 13 Jan 2024 01:16:49 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937117536e19a1d1bb93b7e9d6683cf61b5f4207ddf9b65d0b234610d903dc5e`  
		Last Modified: Sat, 13 Jan 2024 01:16:50 GMT  
		Size: 483.5 KB (483522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe4e33c5bab19d5b21c131548cbcc77be9a66668655aecfcc55b2ee2044e41b`  
		Last Modified: Sat, 13 Jan 2024 01:16:49 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf1913863f6a9ac2e34e8a29852cec610fa4b2e4ad9d240a4bde8e19a1d89ba`  
		Last Modified: Sat, 13 Jan 2024 01:16:49 GMT  
		Size: 330.9 KB (330914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb989e9a99c9e0d9f8303ac8ceaf99562097b0491a4c532a3a435807320f31cd`  
		Last Modified: Sat, 13 Jan 2024 01:16:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c482937e1d2f1f795304d6ed1a0ca3a7fa3b8df3a0b06a964acdd681747f2d`  
		Last Modified: Sat, 13 Jan 2024 01:16:47 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f3824e82eaa28654569560821999cf0336ca16559ea91c44bf6c4e4a2b4999`  
		Last Modified: Sat, 13 Jan 2024 01:16:47 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2df24feeadf6f2c7a8a10fab253afed6cbb5874a5c20bb403306eaab93b7f7`  
		Last Modified: Sat, 13 Jan 2024 01:16:59 GMT  
		Size: 197.7 MB (197725383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d3d7223beb59f27f098a1647cb6e556520798a05954fd63bf1b643c93a82f2`  
		Last Modified: Sat, 13 Jan 2024 01:16:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
