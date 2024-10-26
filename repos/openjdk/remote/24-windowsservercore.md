## `openjdk:24-windowsservercore`

```console
$ docker pull openjdk@sha256:08de4c07df20f620c67e250937dfbe586fce72651ef709f8a6d598ab2c4d9970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `openjdk:24-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull openjdk@sha256:b6aab75bd90ba8f9f464d7b3685a6de4671f93e0bdd5ee1e8b7ab417e520ec62
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2008713157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5416a582f92783745d6e828d4d9970ec544e5ee956050b0a2c51df410e5983`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Fri, 25 Oct 2024 22:56:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 25 Oct 2024 22:57:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 25 Oct 2024 22:57:44 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 25 Oct 2024 22:57:51 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 25 Oct 2024 22:57:52 GMT
ENV JAVA_VERSION=24-ea+21
# Fri, 25 Oct 2024 22:57:52 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_windows-x64_bin.zip
# Fri, 25 Oct 2024 22:57:53 GMT
ENV JAVA_SHA256=fadb0a1bfaab7f1299965f76ad4c30a3b4e9f2e7325c0f99ff51b4592e12903c
# Fri, 25 Oct 2024 22:58:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 25 Oct 2024 22:58:27 GMT
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
	-	`sha256:08506d8b567e570bcf2cb0df591b01c7fe950b1933bdd1c05d8b38a0d8e852e7`  
		Last Modified: Fri, 25 Oct 2024 22:58:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba338bae83eac042fde96bd3efa6d715c88e6dfa332e7d2c6cb0674faf328979`  
		Last Modified: Fri, 25 Oct 2024 22:58:32 GMT  
		Size: 493.0 KB (492988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba0f1abf251abfbac3aea851ef6c3616e66c3e3cff7c5d68a7a55afc262cde7`  
		Last Modified: Fri, 25 Oct 2024 22:58:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbc3620f99abe710fa8661ae16c5fce52c1d3292073d20eb4ca0eb4496f5d3e`  
		Last Modified: Fri, 25 Oct 2024 22:58:32 GMT  
		Size: 311.5 KB (311501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9caad59c450879c2926fdbee39ab6354f3206cf7170ab6a03080fd0eb2957a94`  
		Last Modified: Fri, 25 Oct 2024 22:58:31 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30dc05abed6a0a4f187f565df9a181e0a8215132a149adc595a5a89bc947fff`  
		Last Modified: Fri, 25 Oct 2024 22:58:31 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce4884c80a77da44438a28e8ff6c8b6811a3c45081e198d47b8a3bf38a4748c`  
		Last Modified: Fri, 25 Oct 2024 22:58:31 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12978881d169ef6d96f1738dbcd0a8fab96919165ba986e2e92993f865b248e4`  
		Last Modified: Fri, 25 Oct 2024 22:58:42 GMT  
		Size: 208.6 MB (208559303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b6c0df9ce59526b6368b871f9ae98d4b200294360c457b86fed6b28d6f3e90`  
		Last Modified: Fri, 25 Oct 2024 22:58:31 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
