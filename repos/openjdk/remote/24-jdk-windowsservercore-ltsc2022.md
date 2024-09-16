## `openjdk:24-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:6ec1fe0f5e39b455d757ff2804259d10bbdfddc63338bbd4d5f70b08f1bba677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `openjdk:24-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull openjdk@sha256:6eb4d7e75f5b56e229856843d35c6e5cc3055baab1a10d5901e2cfce18cc1a86
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1670896015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea72dded6c19883841917d8676d99e5dbb436094d7d17dfc477ee442cd00f6b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Mon, 16 Sep 2024 18:57:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Sep 2024 18:58:33 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 16 Sep 2024 18:58:34 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 16 Sep 2024 18:58:40 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 16 Sep 2024 18:58:40 GMT
ENV JAVA_VERSION=24-ea+15
# Mon, 16 Sep 2024 18:58:41 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_windows-x64_bin.zip
# Mon, 16 Sep 2024 18:58:41 GMT
ENV JAVA_SHA256=eef80af228bec40c318932471d2263a3ee6998dd635f9b1e60c432cf26d3c4d8
# Mon, 16 Sep 2024 18:59:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 16 Sep 2024 18:59:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ef27b6c8090f6896371ec9eb5543810593416ba4a510b64b2eee9e5f2ebdaa`  
		Last Modified: Mon, 16 Sep 2024 18:59:10 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60161ef3c2f2a60ac39f5b92de51569642e97199b5a82580631124b8440d7fff`  
		Last Modified: Mon, 16 Sep 2024 18:59:10 GMT  
		Size: 350.7 KB (350735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a9cd75456157cf6f64693370e20beae84aa2d2414fe4d0da7874ceb5b76e50`  
		Last Modified: Mon, 16 Sep 2024 18:59:10 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0712c6b05d28296383a953360b19b27876c74d96eba90f9685168a7f1cea1c57`  
		Last Modified: Mon, 16 Sep 2024 18:59:10 GMT  
		Size: 334.7 KB (334704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765cd56241300bdbd1bd204600b9941e0db4372912a950d43155433164223f5e`  
		Last Modified: Mon, 16 Sep 2024 18:59:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246207d39f6867729bafd5939410b2f370576368899e99e2ce7a2f51faf89bef`  
		Last Modified: Mon, 16 Sep 2024 18:59:08 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43e18eb5e0ccba6e7f868a21577575da44a1bd33fa0a2bc5d5fd17a9c807807`  
		Last Modified: Mon, 16 Sep 2024 18:59:08 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3b21c60f129547a3f5a603f3c6106b4462f92c550556b55e769f33036d6ab9`  
		Last Modified: Mon, 16 Sep 2024 18:59:20 GMT  
		Size: 208.0 MB (208010462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ac0988e4a96de417d28e670d9d14d3557e0aec57591c1f953e5307c514ffa0`  
		Last Modified: Mon, 16 Sep 2024 18:59:08 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
