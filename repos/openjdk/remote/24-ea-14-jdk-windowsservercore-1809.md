## `openjdk:24-ea-14-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:8b56736a948c5456ef1102eeddd49426610baffb515cd4841116b6eee1f7175a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `openjdk:24-ea-14-jdk-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

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
