## `openjdk:23-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:a866c6c39aea6ea1feb26cf55e49ed73e717bb6d355f872d6e5f3cb638cb246b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `openjdk:23-jdk-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull openjdk@sha256:3f8090e06919ac5f12e476e155a73bd2e52d4d9fb023b04b73a4de3cf2eefac5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331645126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2682672378226828f8634bb12193791585e6707034d42ee0121fb98ac58fa541`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Fri, 05 Apr 2024 17:51:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 05 Apr 2024 17:54:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 05 Apr 2024 17:54:24 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 05 Apr 2024 17:54:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 05 Apr 2024 17:54:54 GMT
ENV JAVA_VERSION=23-ea+17
# Fri, 05 Apr 2024 17:54:55 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_windows-x64_bin.zip
# Fri, 05 Apr 2024 17:54:56 GMT
ENV JAVA_SHA256=d370ad95643e427d9a9f79c527dc3dfbd3fa07ebda3684fe18acba87d4342d57
# Fri, 05 Apr 2024 17:55:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 05 Apr 2024 17:55:51 GMT
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
	-	`sha256:039e6816d763571d464037acbaf8db3f58940f1fbb948fc8a6b6607ccaa06674`  
		Last Modified: Fri, 05 Apr 2024 17:56:00 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8885e274de2bbb520f75cad69ef9e626290f7727ee88b0e334a5289d9170ef66`  
		Last Modified: Fri, 05 Apr 2024 17:56:00 GMT  
		Size: 500.6 KB (500622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b54bedf2041020077b0d71904ed0f3efeaf0586d44942feed5d8a5900756c70`  
		Last Modified: Fri, 05 Apr 2024 17:56:00 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bb7f5c6781bda6ff00c6123489fa31b0f7437041b8870d5a3fd0c375cad04d`  
		Last Modified: Fri, 05 Apr 2024 17:56:00 GMT  
		Size: 352.7 KB (352682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c824f0ddab5d45814805ec16394cd619eb0d9248b373faf53dd88798e7f022c0`  
		Last Modified: Fri, 05 Apr 2024 17:55:58 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6e31143dcb1314952ecac4f64e51afc482cbc0db3c1725fb5331fe583b32c8`  
		Last Modified: Fri, 05 Apr 2024 17:55:58 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9ec713cd8620e5802431c467f53ca52c4e1bb10c85f7a6199e181afbbc9c50`  
		Last Modified: Fri, 05 Apr 2024 17:55:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74c8f6e2f7018e15e6de94774b1aed8fa8203c2e04efaa0c41de27a1713110e`  
		Last Modified: Fri, 05 Apr 2024 17:56:08 GMT  
		Size: 205.7 MB (205684100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f38581ad5c75f86347e515f59677dbed08553eae592d0b234d043c2217f0173`  
		Last Modified: Fri, 05 Apr 2024 17:55:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
