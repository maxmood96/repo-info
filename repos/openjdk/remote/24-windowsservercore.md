## `openjdk:24-windowsservercore`

```console
$ docker pull openjdk@sha256:2e9942ae36d8d636df1abf7e74756fc71df06efc05a03c0755a1d9010451e018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `openjdk:24-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull openjdk@sha256:dd27fbf434011feb9ed358fd0e14bc4418ea9673946fcafc0d0277230aa6bc1c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1670880164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b25899c4a726b5b91fd26737821ea6ebe9e71b81260c69faa96dd9dd281127`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:05:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:05:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:05:46 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 11 Sep 2024 00:05:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:05:56 GMT
ENV JAVA_VERSION=24-ea+14
# Wed, 11 Sep 2024 00:05:57 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_windows-x64_bin.zip
# Wed, 11 Sep 2024 00:05:58 GMT
ENV JAVA_SHA256=d302c4d8be4955ea17267c66b8321f205212748df83273e4e0d9ccc0d1c4b1a2
# Wed, 11 Sep 2024 00:06:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:06:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c083dbe4899aa80edc0b3da05d5550f4f6266c39dcaa60cbe6c6efbedda26ea6`  
		Last Modified: Wed, 11 Sep 2024 00:06:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db50d237b35e81f0d6928f3ba8fc54ac920d814cec557b40ebe6c817f144461`  
		Last Modified: Wed, 11 Sep 2024 00:06:36 GMT  
		Size: 350.3 KB (350272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae6fb62d256c807fb5e8cf71226d89e798a131bad7747dc6873af847bf331b0`  
		Last Modified: Wed, 11 Sep 2024 00:06:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5da85c27f59e4765def4b8a91d01012e5ae490c6561a23a3d7b285a9b54bbdb`  
		Last Modified: Wed, 11 Sep 2024 00:06:36 GMT  
		Size: 334.4 KB (334384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80eea04ec36e869c78e327a6cb581f645ed5db74ea99e1d2bf20efbf879fb50e`  
		Last Modified: Wed, 11 Sep 2024 00:06:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a6eae4fbe508742cfc8cf1c138644e811c573d938b72e274b4ad09145b1e9b`  
		Last Modified: Wed, 11 Sep 2024 00:06:35 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f906f1534fb8e742202030975053d2347538a937e51f6848c1ba7ea1fe74e754`  
		Last Modified: Wed, 11 Sep 2024 00:06:35 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fe23ef12e2d275172bde28df3cf71d00fd9d1845730f6609d923d5a9daf4f6`  
		Last Modified: Wed, 11 Sep 2024 00:06:46 GMT  
		Size: 208.0 MB (207995190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef47a3d3dda447bb6ebdb64d2ba1b101d8ad6f5bc615598f8640fbec73439d55`  
		Last Modified: Wed, 11 Sep 2024 00:06:35 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull openjdk@sha256:b6eb09f8c9d15934afd65a0826d8a758baaa1b286a7357d24c29bda324c51bbb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1928945265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a545230b25cf1a45284d5fa2d0b31b2c4345b2331d0d29fe4b3f3bb8060934`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:04:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:05:00 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:05:00 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 11 Sep 2024 00:05:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:05:10 GMT
ENV JAVA_VERSION=24-ea+14
# Wed, 11 Sep 2024 00:05:11 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_windows-x64_bin.zip
# Wed, 11 Sep 2024 00:05:12 GMT
ENV JAVA_SHA256=d302c4d8be4955ea17267c66b8321f205212748df83273e4e0d9ccc0d1c4b1a2
# Wed, 11 Sep 2024 00:05:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:05:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326c5813accafbcd1f1c0387849f28862d1ea4afd85fb083471f6f94115d18ed`  
		Last Modified: Wed, 11 Sep 2024 00:05:54 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df4033bd2962354ca92def3ab9e0596cf56954c6bf73ff59cf4bfcd8b17454c`  
		Last Modified: Wed, 11 Sep 2024 00:05:55 GMT  
		Size: 343.8 KB (343783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cae26b9113f0621a70ecb9d1fd6149dc0c0143d733d1089413ece35be8770c`  
		Last Modified: Wed, 11 Sep 2024 00:05:54 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123b176758bf7a7f5577c2a50fe31d7d78fcc512ad18594f4f272917c714bc9b`  
		Last Modified: Wed, 11 Sep 2024 00:05:55 GMT  
		Size: 330.1 KB (330092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36beb21a7e22624e0e793aa13e5e91303b4db8787c2afc9a6867c10db8e47083`  
		Last Modified: Wed, 11 Sep 2024 00:05:53 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8261675c8fabc36e464c0aa83d5f1917c18d617046c82e59775e4a65637c5c`  
		Last Modified: Wed, 11 Sep 2024 00:05:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6b072c3c62285b2fa0f9382eb32cb3a901473ccd723f52da14aab4141fbd91`  
		Last Modified: Wed, 11 Sep 2024 00:05:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff351f71740d0c2fff83f4c2eb26079e7756ab58d58348fa7e424806303de84`  
		Last Modified: Wed, 11 Sep 2024 00:06:04 GMT  
		Size: 208.0 MB (207995284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9b1a2c6dccf1bc0323e2f2b25d0f3bf4eaa55552a7848f808dd64e32b21753`  
		Last Modified: Wed, 11 Sep 2024 00:05:53 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
