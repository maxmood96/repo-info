## `openjdk:24-ea-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:8507dac05361b2dff77ab2ed82ed1fe61b8db2fd1566e500f020d239efae93d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:24-ea-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

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
