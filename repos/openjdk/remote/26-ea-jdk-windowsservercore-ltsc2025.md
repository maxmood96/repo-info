## `openjdk:26-ea-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:fc8c20f09097ce71449e9b3f2f7cc22dad7b33977e8a7eaedede079d3a312f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `openjdk:26-ea-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull openjdk@sha256:09e4231cf6f2c44b0da2cd621af1d9b5515f987c2c53cf03e82c714eb934df0e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459773353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2ea8c7ca9828d7d4c742ec3b84ccc0a98b8b521abff5b2146129f8ac33d00d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 18 Nov 2025 00:19:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 00:42:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 18 Nov 2025 00:42:02 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 18 Nov 2025 00:42:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 18 Nov 2025 00:42:08 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 00:42:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_windows-x64_bin.zip
# Tue, 18 Nov 2025 00:42:09 GMT
ENV JAVA_SHA256=9b59e5ab2fbe51399288d84d2710135e705f8399b618a54aa95498654a9841c1
# Tue, 18 Nov 2025 00:42:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 18 Nov 2025 00:42:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7cef4a3415e4a64bcfbd4e853e4a6f58af113e4c2fe90d11e7cbba12594bc6`  
		Last Modified: Tue, 18 Nov 2025 00:41:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d267b8462ce57eb7da712d3f47f6f1111cb523e1e2586a15256bf8ae2c2b6b6`  
		Last Modified: Tue, 18 Nov 2025 00:43:19 GMT  
		Size: 393.3 KB (393335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159990fca1045705e08dec5fd194d505fc905e391f4c8bea878fe6e5048daf73`  
		Last Modified: Tue, 18 Nov 2025 00:43:19 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa613f0c8c857853c786dd0e34e8606e7f88ecd27df78c02a35eefc08adac02`  
		Last Modified: Tue, 18 Nov 2025 00:43:19 GMT  
		Size: 358.2 KB (358174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8282b585c05eec76f85649a10ae9f95e34265f2bf433a8f49560d26f62c7a4`  
		Last Modified: Tue, 18 Nov 2025 00:43:19 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a723b72e39bfe6feb6a12473386ab2705f6864e79dad996f51833c54e09e439`  
		Last Modified: Tue, 18 Nov 2025 00:43:19 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053d5bb8a2b7aa7600bbfd9e32951c1565fc21cd158393bc48a8c72e92a02137`  
		Last Modified: Tue, 18 Nov 2025 00:43:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aa0d0d338f3e83aa7ae535d881c8c239fc23fe008f1b2b2091e0399d119bec`  
		Last Modified: Tue, 18 Nov 2025 01:24:03 GMT  
		Size: 223.6 MB (223558282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45032a2d12d52d71b5e3c8fb6840ffa44b4d0eba46ce53b04e35c6b6e9c7e7f`  
		Last Modified: Tue, 18 Nov 2025 00:43:19 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
