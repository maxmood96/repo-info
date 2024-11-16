## `openjdk:24-windowsservercore`

```console
$ docker pull openjdk@sha256:7dbde77dee3ef6df3974b822ac0fbfb7c14df4af62f0743e24b1725fa3ba7c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `openjdk:24-windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull openjdk@sha256:540a0fa22fef3c0543666997ecb243b0dae0c40d2a64b49eac13d821b2687094
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471200411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1920f5260a9b238a22f47f75906a9193c1fd7e51a7b660e210f0f82d19d6a1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Fri, 15 Nov 2024 23:11:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 Nov 2024 23:11:41 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 15 Nov 2024 23:11:42 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 15 Nov 2024 23:11:47 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 15 Nov 2024 23:11:48 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 23:11:48 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_windows-x64_bin.zip
# Fri, 15 Nov 2024 23:11:49 GMT
ENV JAVA_SHA256=403403eb4a5860551cdfc63a2395f87cf7526bf93e5437ea5fd17168572fd51a
# Fri, 15 Nov 2024 23:12:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 15 Nov 2024 23:12:09 GMT
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
	-	`sha256:55a50bfc4a6c23d4423657c38fd801af499a6f07385aac6bc4de89349efd74a5`  
		Last Modified: Fri, 15 Nov 2024 23:12:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8685fed0880fa63804a38da03e6726d5b87af3470b1000e3850658442ab163e`  
		Last Modified: Fri, 15 Nov 2024 23:12:15 GMT  
		Size: 361.4 KB (361396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c9f9952eb61cfe35b6ae63510d1a3eec4a1d973df226f2c33bee7ab7092757`  
		Last Modified: Fri, 15 Nov 2024 23:12:15 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fe30b86acfebbf39c2a385395a465e1e1d746e47d944d371d26ec4c30c7106`  
		Last Modified: Fri, 15 Nov 2024 23:12:18 GMT  
		Size: 345.7 KB (345748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682f1a38d4f3e90d9ac6c98b9c0dad114fb26e7c2d7a885e98ef022e082454a3`  
		Last Modified: Fri, 15 Nov 2024 23:12:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1abf23c2a71e46129f71f9a9664a231f487fb970025a12ccecb5ba4b0430c64`  
		Last Modified: Fri, 15 Nov 2024 23:12:13 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e87fc0af2adb498a0fbc6ee6bb959c19304a8024a288a8cd66d770cb570cb`  
		Last Modified: Fri, 15 Nov 2024 23:12:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb30d1730e4e5ca26d22cd14fb78e8e03b9a19aee06c79f3b0bf84da0626ae87`  
		Last Modified: Fri, 15 Nov 2024 23:12:25 GMT  
		Size: 218.0 MB (218001331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b233d0f611de1e1f888f8bfed8ae55ea1615011ee9f38e58cdcd6a370fdf1b94`  
		Last Modified: Fri, 15 Nov 2024 23:12:13 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull openjdk@sha256:38419d99f190430797c994d1786a4343b11c2969002df108f53b8614e27864cb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229502792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ace56a105bc37f3eb07f562006c5fd29219b0cce3dd2979f6b7d86fd18e2e13`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Fri, 15 Nov 2024 23:04:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 Nov 2024 23:06:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 15 Nov 2024 23:06:02 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 15 Nov 2024 23:06:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 15 Nov 2024 23:06:22 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 23:06:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_windows-x64_bin.zip
# Fri, 15 Nov 2024 23:06:23 GMT
ENV JAVA_SHA256=403403eb4a5860551cdfc63a2395f87cf7526bf93e5437ea5fd17168572fd51a
# Fri, 15 Nov 2024 23:06:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 15 Nov 2024 23:06:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fecedf989bf78ec7c563a5ce533ea5ef3405e8bc70347dc2eea9d25aaf49745`  
		Last Modified: Fri, 15 Nov 2024 23:07:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e9abf92dcbe4382036e597ce2e628ce6c0f83f89f11fb56cd2db409d3b9e2d`  
		Last Modified: Fri, 15 Nov 2024 23:07:06 GMT  
		Size: 494.0 KB (493953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b83b95abb262cd2d7bd8c41d7d00e1ed1f139426745f5c87ca2091deeb0a8cb`  
		Last Modified: Fri, 15 Nov 2024 23:07:06 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c24d4b751569e580e4b4664d55c2401d570ece3c34082d12b6b51909f3c21bc`  
		Last Modified: Fri, 15 Nov 2024 23:07:06 GMT  
		Size: 338.0 KB (338005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badb0c837ee95f21c0a134239fc9f84edebf442e21229898b6260c506751407f`  
		Last Modified: Fri, 15 Nov 2024 23:07:04 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce007f8d8872b22925529b05d016855bac4d3ec9467b943836cf703ad85b356`  
		Last Modified: Fri, 15 Nov 2024 23:07:04 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7768931be92a708c019f1bf47eb1abd848ee96f378f054423088ee1f2fc4ee`  
		Last Modified: Fri, 15 Nov 2024 23:07:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60e7c9e03dba687f180ed9e9263107b1db1dfcbb51f9dcc0282d7f3c981e9ab`  
		Last Modified: Fri, 15 Nov 2024 23:07:17 GMT  
		Size: 218.0 MB (218009268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323ec0c8fcde3b8c2ab2eda3de192884cd0f93d712e80665fcc4035aacc60394`  
		Last Modified: Fri, 15 Nov 2024 23:07:04 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
