## `openjdk:24-ea-31-windowsservercore`

```console
$ docker pull openjdk@sha256:12eb7089df00d7e8f31f4f65628a5e2e4fbbf87d6db49f219e67c443fe9dc0fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-31-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:c16ae757b84df433ea4b301f343b97af5a6422a6bfa374972e1a583df0b5f801
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709958197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2f27b59b776a8f408a07c9f491cce2c32b3eba027ca4d96ee92fe83c39c3d1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:35:15 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:16 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 22 Jan 2025 20:35:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:22 GMT
ENV JAVA_VERSION=24-ea+31
# Wed, 22 Jan 2025 20:35:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_windows-x64_bin.zip
# Wed, 22 Jan 2025 20:35:23 GMT
ENV JAVA_SHA256=72536bad2fa20c7ead0367944940a684a359e43649870d3cdbccd46bcc3b4009
# Wed, 22 Jan 2025 20:35:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:41 GMT
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
	-	`sha256:e8bd841cc0d825daabb93db6619d756edf96f4c6293eeb6577e53fc19d94b02e`  
		Last Modified: Wed, 22 Jan 2025 20:35:47 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cc44586db333a7a77f4125ff06eaf0fff2827bb14891d1cdf98708c832603e`  
		Last Modified: Wed, 22 Jan 2025 20:35:48 GMT  
		Size: 401.1 KB (401088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe29df44c98ebf38363407dd0dc99eea3c180a87e373d97560e6f9ab026ffe8`  
		Last Modified: Wed, 22 Jan 2025 20:35:47 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93745b4e5b1d10effb6fabe25934f7f47e28ec93a527419ebbb36d670208449`  
		Last Modified: Wed, 22 Jan 2025 20:35:48 GMT  
		Size: 384.8 KB (384769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b095452fda03a1696f0d16de6c73f054355b9b77fbe066f71f929b85ca2c4bf`  
		Last Modified: Wed, 22 Jan 2025 20:35:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc296e6df43f5f129b38a87640d0934f1a29070a2fda4f5ab5bcb60e2f447bc`  
		Last Modified: Wed, 22 Jan 2025 20:35:45 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff5f1ed761204bd44aef370c0e0f541846ff0e36b860d38ce86ad9777dc8cac`  
		Last Modified: Wed, 22 Jan 2025 20:35:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5d17d0f26109f6b7960f9f28f3627a66213d3cba00771e7e922d944155b251`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 208.9 MB (208886933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3cdf08d446396d700628fd84247165fcfa13ce1f76e4ccb63537a86823a995`  
		Last Modified: Wed, 22 Jan 2025 20:35:45 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-31-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:b9c95bf6321affaa36d9afa505e9726455f46193a289dc409fe5b5ec9d935aa9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471931050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce0435d3d3738be5128defcb30b3992792dbe0bcd31b4918cc1181ecd7f36e0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:37:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:37:36 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:37:37 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 14 Jan 2025 23:37:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:37:42 GMT
ENV JAVA_VERSION=24-ea+31
# Tue, 14 Jan 2025 23:37:43 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_windows-x64_bin.zip
# Tue, 14 Jan 2025 23:37:43 GMT
ENV JAVA_SHA256=72536bad2fa20c7ead0367944940a684a359e43649870d3cdbccd46bcc3b4009
# Tue, 14 Jan 2025 23:38:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:38:02 GMT
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
	-	`sha256:7da954ca904eb925ca2c1399d3914db57c138133242c2338863e7e5946300c25`  
		Last Modified: Tue, 14 Jan 2025 23:38:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ad67c317d55d748daead122964a38ecf07c3976fc899cb0dc2f5f29b66321a`  
		Last Modified: Tue, 14 Jan 2025 23:38:09 GMT  
		Size: 360.8 KB (360788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3ae78e5e579474d64c094b6d2a9a1b4e59f5d48a3eb1379c8783c4d4c9056f`  
		Last Modified: Tue, 14 Jan 2025 23:38:08 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94da7a3f45345b654966ad6d0f0ca7181ae4e27e54608b9b5878ee807fa5c9e2`  
		Last Modified: Tue, 14 Jan 2025 23:38:09 GMT  
		Size: 344.4 KB (344380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f650ccc353f60f41de872d8abc0b04fd6ec6ae68893886b2add558637a3f1c21`  
		Last Modified: Tue, 14 Jan 2025 23:38:07 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1099a3c234d1188056953e97f774df1de3632803e5cbcb84634815a56ccd357`  
		Last Modified: Tue, 14 Jan 2025 23:38:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e2546f1ccef89d7572bd6b9f928c74c2f0d71db3b1eac37bc8bb064a4c3f79`  
		Last Modified: Tue, 14 Jan 2025 23:38:06 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6fb71ed0588cc6fd2e3d8b002031c0b098b89a58ea555e206e54e43e61eaa9`  
		Last Modified: Tue, 14 Jan 2025 23:38:18 GMT  
		Size: 208.8 MB (208832901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e758ecaad71f9c6b8d9fb3f1079a2dd3f48227a6fe76d152b3028050c7a2335`  
		Last Modified: Tue, 14 Jan 2025 23:38:06 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-31-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:7943054362fbdf0f0cd24a687b3bfcd2695d4d1c016aade376c8077f79d2b990
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331653020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616c4a0375872db2f9f57fb83d2e189aaf2f66878b1a9805fb4acac5d53bffac`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:43:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:44:22 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:44:22 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 14 Jan 2025 23:44:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:44:29 GMT
ENV JAVA_VERSION=24-ea+31
# Tue, 14 Jan 2025 23:44:29 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_windows-x64_bin.zip
# Tue, 14 Jan 2025 23:44:30 GMT
ENV JAVA_SHA256=72536bad2fa20c7ead0367944940a684a359e43649870d3cdbccd46bcc3b4009
# Tue, 14 Jan 2025 23:44:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:44:55 GMT
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
	-	`sha256:f5749b6a6e8ad8b0595ce97d114cbb758f1e990ee62fb8d672ed73419bf8236a`  
		Last Modified: Tue, 14 Jan 2025 23:45:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1c2782b639d1e6e04a2142aec07d41d6d7911761aca21b00f26e0ecc17528a`  
		Last Modified: Tue, 14 Jan 2025 23:45:02 GMT  
		Size: 320.3 KB (320330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ec5810411e41809bc941204fb1623b1e19624c3ca85406b9412cd01648ff33`  
		Last Modified: Tue, 14 Jan 2025 23:45:02 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072cd8bcd60d21fb6b88936828a2be1bee36617b0d6d744156aa2e6c65f492f1`  
		Last Modified: Tue, 14 Jan 2025 23:45:02 GMT  
		Size: 305.5 KB (305537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835a281bf4b7d506a153202c411a91fa57778901d1ce5ec1ce10ee7fe1e8d1f0`  
		Last Modified: Tue, 14 Jan 2025 23:45:00 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3417a1709badaeb53ecd647dcd537f0afcb3e8c33e24d4fe508b1413a2b8e7c`  
		Last Modified: Tue, 14 Jan 2025 23:45:00 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3723505b9c91d8260cdd509e429243a831cc31c3276cc83262fe711340d4c8`  
		Last Modified: Tue, 14 Jan 2025 23:45:00 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881d31b5e828a961221df8527cc8fc5782978df421c98e4b7f019864ce532d47`  
		Last Modified: Tue, 14 Jan 2025 23:45:12 GMT  
		Size: 208.8 MB (208806782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18930c450c2c65ad2a894a777b6d4dea342e032e098029dfd9e39543ebbfe58f`  
		Last Modified: Tue, 14 Jan 2025 23:45:00 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
