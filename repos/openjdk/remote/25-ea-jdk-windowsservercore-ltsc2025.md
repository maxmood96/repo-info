## `openjdk:25-ea-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:381916934ce35d3bb78fab95219e4e3c67485a430201b2269b6edbd6f1a84769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `openjdk:25-ea-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:1aedf3471e71036706ea98b366c21125393a1eeb2df0b00d3c41a265751eeb33
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3604719979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81c7fc16229afe5d6b2635c7db503af36b7b3a24649129fa1f1e472ccb2e95c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Mon, 12 May 2025 19:17:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 May 2025 19:17:15 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 May 2025 19:17:16 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 12 May 2025 19:17:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 May 2025 19:17:23 GMT
ENV JAVA_VERSION=25-ea+22
# Mon, 12 May 2025 19:17:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_windows-x64_bin.zip
# Mon, 12 May 2025 19:17:24 GMT
ENV JAVA_SHA256=8b16ab02467967b98cf7d8743da9c9688d3ff39b4a693b66b6d9fe84cc0bb55a
# Mon, 12 May 2025 19:17:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 May 2025 19:17:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c0b062ce4db415952fb23c36269d5758fb92126221e405502d71771a7a3281`  
		Last Modified: Mon, 12 May 2025 19:17:48 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e259e73de06795b5f438ccf4816de99b2c3655cc6c0a625160efb9c9df7a83fe`  
		Last Modified: Mon, 12 May 2025 19:17:48 GMT  
		Size: 400.5 KB (400502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1773ef7e42560b155d01b041e7631016bd9fd700120516a88fcd796e7c37d847`  
		Last Modified: Mon, 12 May 2025 19:17:48 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad2fddd8938d65fe7d88c00f47fae7bd46c03236fdcb75a06b1240c47f5c668`  
		Last Modified: Mon, 12 May 2025 19:17:48 GMT  
		Size: 380.1 KB (380086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bce5cf8ef94e5c208008232d07bdf2d8ef0f09caf583dc144491d2d2972b0b7`  
		Last Modified: Mon, 12 May 2025 19:17:47 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59467a5dfa107aa907494c1bef9243f09352665626b2771ef25b57ea69635fd7`  
		Last Modified: Mon, 12 May 2025 19:17:47 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2570bb870486abf19454ccd561cc729780b64216df62dff03b660fe7bda1d4c1`  
		Last Modified: Mon, 12 May 2025 19:17:47 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafe2c711ff8cb0881aa4ca3838c6b5c9a801441fc3de3b4508a8cf136d9c744`  
		Last Modified: Mon, 12 May 2025 19:18:00 GMT  
		Size: 208.8 MB (208770128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca462f4454b944e30e35d4bfd4ca8ccb949049d40477501d46386857394ceb92`  
		Last Modified: Mon, 12 May 2025 19:17:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
