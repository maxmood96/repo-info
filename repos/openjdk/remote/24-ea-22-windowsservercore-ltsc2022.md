## `openjdk:24-ea-22-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:6dca2989949d540a118febcf9dc7dc785ef00e43df26adf03266546c3905562f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `openjdk:24-ea-22-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull openjdk@sha256:8d24648e622a86999d1043f1d07c1933b75b15759e6808b7acf494314099eebe
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2008435267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0806fb89796505a4ad3dc450bd658387f7d92a18931fd33c90079fdc47d439`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Mon, 04 Nov 2024 23:07:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 23:08:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 04 Nov 2024 23:08:17 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 04 Nov 2024 23:08:24 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 04 Nov 2024 23:08:24 GMT
ENV JAVA_VERSION=24-ea+22
# Mon, 04 Nov 2024 23:08:25 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_windows-x64_bin.zip
# Mon, 04 Nov 2024 23:08:26 GMT
ENV JAVA_SHA256=3ab8853c76cbab5121e3c33e96b120f81d15b6979f56d1b4cc935ec94868413d
# Mon, 04 Nov 2024 23:08:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 04 Nov 2024 23:08:56 GMT
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
	-	`sha256:8df525ac0ebc3860930ef72be17bfb43a7cfa8c9535c1856c00b59d94e1f1348`  
		Last Modified: Mon, 04 Nov 2024 23:09:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72310977e90f8dcce705c8d63235f542cc0f3dd7fb1cd20d6cab44d746ec020c`  
		Last Modified: Mon, 04 Nov 2024 23:09:00 GMT  
		Size: 482.8 KB (482758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ae9e5a976f0a9db0a5dd39729ebe8b71d7a8adb34b3729a4c73c2f7805ee5f`  
		Last Modified: Mon, 04 Nov 2024 23:09:00 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb38bdabdfe61a694ca942bc148263fe5f5a13229cc635df17c91691b113140`  
		Last Modified: Mon, 04 Nov 2024 23:09:00 GMT  
		Size: 301.0 KB (301024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0ef8123c63b558e3627020f635753087ec206d903fb2232ea77c5d2d41c89a`  
		Last Modified: Mon, 04 Nov 2024 23:08:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af4d3aa4107b80ef4767f1817d7d0f2fd33319211797171aa8d99002502224a`  
		Last Modified: Mon, 04 Nov 2024 23:08:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b939bcdabf3399f3d7e39fe33e099ed5ea67513a9cf85c297d2e4d1423716318`  
		Last Modified: Mon, 04 Nov 2024 23:08:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb55c3912f573cca7bc688e38a600b4b0bdbbb15bbcf9b08fe79b997e0c3ee7c`  
		Last Modified: Mon, 04 Nov 2024 23:09:10 GMT  
		Size: 208.3 MB (208302219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679f7fce1df5eaff277092e9b574bc0156623d495a4ad2637af2da1981fcf781`  
		Last Modified: Mon, 04 Nov 2024 23:08:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
