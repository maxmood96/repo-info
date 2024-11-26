## `openjdk:24-ea-25-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:ccf648076d91b4db103c380ea728931989ebca03fb668d6f584631acc2576fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `openjdk:24-ea-25-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull openjdk@sha256:39be385a3b11d6c76057891bf4c0f16d57dfb65735a063d2b84e853d0f961fe9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2461978355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6166e8eb32818ac7b5d9490fc3dd9c757d77e04e4e001fdeb942d5c706e780`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Mon, 25 Nov 2024 23:24:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Nov 2024 23:25:27 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 25 Nov 2024 23:25:28 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 25 Nov 2024 23:25:36 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 25 Nov 2024 23:25:37 GMT
ENV JAVA_VERSION=24-ea+25
# Mon, 25 Nov 2024 23:25:37 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_windows-x64_bin.zip
# Mon, 25 Nov 2024 23:25:38 GMT
ENV JAVA_SHA256=3f5d0f9ac7a7a748bad67a34671556be063e7fc8eda4cb079478238095698786
# Mon, 25 Nov 2024 23:26:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 25 Nov 2024 23:26:10 GMT
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
	-	`sha256:bf8b109f15059c39969476b2e97c9f1e6a212394688142e659bab95aa01b6579`  
		Last Modified: Mon, 25 Nov 2024 23:26:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e97c787bc31cf60f5e9b721051c58e3128dfa84b6431a8e6bd312541f383657`  
		Last Modified: Mon, 25 Nov 2024 23:26:14 GMT  
		Size: 364.7 KB (364746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeca69aa2727106a5effcac70b10fb3035ff65974a241e90a1818a6fc49e76e`  
		Last Modified: Mon, 25 Nov 2024 23:26:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5567a2e8fe44047ad84debc563168755b710c32be4e5878678bdc4b77b18f345`  
		Last Modified: Mon, 25 Nov 2024 23:26:14 GMT  
		Size: 313.0 KB (313031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e51e26bc72ee3a63e41277954c77b31c3a8d043e666db5d6a532c09bca1a03`  
		Last Modified: Mon, 25 Nov 2024 23:26:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a18cfe25a2385830857c049c7593ac2a4d5921cf19e377e49e30bcac0eab24b`  
		Last Modified: Mon, 25 Nov 2024 23:26:13 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d0aaf0bf6265cde5d715452732052bd98633e4cd4deff95600bc98f3d1c71f`  
		Last Modified: Mon, 25 Nov 2024 23:26:13 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33e8acfd907f4d4c87ab4226e8e2dbba30c5769f39d3c430238b8e463193ee2`  
		Last Modified: Mon, 25 Nov 2024 23:26:24 GMT  
		Size: 208.8 MB (208808628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4115d2e7d3baa9cd71775a65e85e4e46de030942cb29d19a92fd45ee8f210015`  
		Last Modified: Mon, 25 Nov 2024 23:26:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
