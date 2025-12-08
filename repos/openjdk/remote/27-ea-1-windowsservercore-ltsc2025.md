## `openjdk:27-ea-1-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:b55442dd6388dfedb90b61fe301186d63dd8e8ef812894cb607af96d6753fcb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `openjdk:27-ea-1-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull openjdk@sha256:da19337b056e71381b7720ccd2d8cdd651349e849e1167ed6fbf47ff453f2c0e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3461856792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccaef46fba35d1216579433be352d86f11440594aae72649f5b40c8da20cfe99`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Sat, 06 Dec 2025 00:41:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 06 Dec 2025 00:41:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 06 Dec 2025 00:41:45 GMT
ENV JAVA_HOME=C:\openjdk-27
# Sat, 06 Dec 2025 00:41:51 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 06 Dec 2025 00:41:52 GMT
ENV JAVA_VERSION=27-ea+1
# Sat, 06 Dec 2025 00:41:52 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_windows-x64_bin.zip
# Sat, 06 Dec 2025 00:41:53 GMT
ENV JAVA_SHA256=77d566459162b6597396e779186334a870aeee1837fe453aac80662b023659c1
# Sat, 06 Dec 2025 00:42:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 06 Dec 2025 00:42:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f428ca9cd9bb94e68dfe55d9698529d22889757a1d75c8987c44d6b0dd08529`  
		Last Modified: Sat, 06 Dec 2025 01:00:19 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525f3ae39df5de711f4c1d4813b764a175197f29736a0ba95375707c93cd0939`  
		Last Modified: Sat, 06 Dec 2025 01:00:18 GMT  
		Size: 390.7 KB (390654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6fd42d52691a69f7b6aded91a04efe8f7452f3a92da5ea8047fdd6c033118e`  
		Last Modified: Sat, 06 Dec 2025 01:00:18 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b996dbccb434c4fd209d3a99c7f1db9511f5ca80f5e1b54baacf9442b90412c`  
		Last Modified: Sat, 06 Dec 2025 01:00:21 GMT  
		Size: 364.9 KB (364851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b9d6b57b43aab04856687f795b0b3801b147cc6cc699634d153dec57e61ec2`  
		Last Modified: Sat, 06 Dec 2025 01:00:19 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b6701ebb6de7667c593540a1f027001936b05d89a944fb17a1ffa4f7362ccc`  
		Last Modified: Sat, 06 Dec 2025 01:00:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b79b226fbe70cefd68f74369069ac09bd335b8d76c3dda1bc19ef5930ec5e21`  
		Last Modified: Sat, 06 Dec 2025 01:00:20 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee3d002b722d98bbdf065c1857b1929c4b84ba0a66ae25bde2bc7ec50b91be3`  
		Last Modified: Sat, 06 Dec 2025 01:00:31 GMT  
		Size: 225.6 MB (225637675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0df5843bc625611e709badc57423a3f5669e745f481f9cb99ebd9d146bc85f`  
		Last Modified: Sat, 06 Dec 2025 01:00:20 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
