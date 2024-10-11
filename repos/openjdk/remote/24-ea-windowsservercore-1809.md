## `openjdk:24-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:d3c0049166fcbb3c2f811e7e9af65088b1bcea30323a8077bb0591b793cc8514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `openjdk:24-ea-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull openjdk@sha256:47fc7b514d6314e19670e2789e9de92f8f3493e36aba0fc5c81a6b6ff24cdda8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2110982334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc51364f2910b2c00432ee374660657a0e417e395acea3207721b8ebd9d44b8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Fri, 11 Oct 2024 19:07:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Oct 2024 19:07:55 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 11 Oct 2024 19:07:55 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 11 Oct 2024 19:08:02 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 11 Oct 2024 19:08:02 GMT
ENV JAVA_VERSION=24-ea+19
# Fri, 11 Oct 2024 19:08:03 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_windows-x64_bin.zip
# Fri, 11 Oct 2024 19:08:03 GMT
ENV JAVA_SHA256=c90e6e8d5c865f3712dc302b6bec4f6c9f66d372764d0dbef55391fb52198a08
# Fri, 11 Oct 2024 19:08:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 11 Oct 2024 19:08:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4119de7f787d7aa6b10c5678f32329e2c5ffda57532aa657e0f973fb0635d867`  
		Last Modified: Fri, 11 Oct 2024 19:08:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a53d919b4a1db194c76b37bad66ae8e62409e60ad62476dd1014eccc9ed3e6e`  
		Last Modified: Fri, 11 Oct 2024 19:08:32 GMT  
		Size: 467.0 KB (466988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a9a4d9453364788dcaeaeff0a619620852361482dbb107749a81107571fca1`  
		Last Modified: Fri, 11 Oct 2024 19:08:32 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e3fc5932e19104de4b55fe9accab1c04d4c5b454ef75fe08062175635ce63b`  
		Last Modified: Fri, 11 Oct 2024 19:08:32 GMT  
		Size: 311.1 KB (311083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63bd2f53a34d5b3e8ce27fc55c6cc5aacfb24dc9b8aa29d5454ef648c399f6a`  
		Last Modified: Fri, 11 Oct 2024 19:08:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514d6474085c05dd1442e46f330e7d866bbeb18001df60b5c7373bd204af53e6`  
		Last Modified: Fri, 11 Oct 2024 19:08:31 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71088721cf6e2c0d280c473ca98bef7316210be645df17466f08ff079026b172`  
		Last Modified: Fri, 11 Oct 2024 19:08:30 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07286ff74d8d567ef00e5be7f4b809745c2d27cf337aed15b85681c3e222ed66`  
		Last Modified: Fri, 11 Oct 2024 19:08:42 GMT  
		Size: 208.4 MB (208371210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed393fe977e2528d455973f8faa97d4829180b6072dd5a65ff56504e079b3b6`  
		Last Modified: Fri, 11 Oct 2024 19:08:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
