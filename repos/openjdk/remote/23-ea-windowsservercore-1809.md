## `openjdk:23-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:08f9ac85a0925bf659bd1855ad08f463e7acaf4d174ab9c58fdd33a2b63d027d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:23-ea-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:4976a4fda0f81f6154aae299edf5224c00cc7c111a99506f9a170478b94cd7d4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268491325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2148461248e14e9ac2cde7f80223df269dee1fceaade284627b3bf14148575`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Fri, 26 Jan 2024 23:49:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Jan 2024 23:51:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 26 Jan 2024 23:51:44 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 26 Jan 2024 23:52:04 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 Jan 2024 23:52:05 GMT
ENV JAVA_VERSION=23-ea+7
# Fri, 26 Jan 2024 23:52:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_windows-x64_bin.zip
# Fri, 26 Jan 2024 23:52:06 GMT
ENV JAVA_SHA256=ed56621259542fefdd1f8719171f0b87d695f984be01061164420c2b90b8ba62
# Fri, 26 Jan 2024 23:52:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 Jan 2024 23:52:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82aecaa30b59d6e1a3382c8baeb021fd9453fd2f31001d711ee8f5e98026e7fd`  
		Last Modified: Fri, 26 Jan 2024 23:52:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396e5c8fb75ae0116e221cea5e07c357f59cc1ba837fe85da7bddfbf111e52ab`  
		Last Modified: Fri, 26 Jan 2024 23:52:58 GMT  
		Size: 511.4 KB (511353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ce301a4680b186affd4d51bfb5387f6db311e802aeaae84d6d8485d7b1657f`  
		Last Modified: Fri, 26 Jan 2024 23:52:58 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f54a2259e0b8d19af72484a8ee89c81e072d3791313fa9e0d5a4dbb8c2876a4`  
		Last Modified: Fri, 26 Jan 2024 23:52:58 GMT  
		Size: 357.2 KB (357186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2f8ce661ccefffae106b201e965f3d6015774ba2d6864cd886747b24444f4a`  
		Last Modified: Fri, 26 Jan 2024 23:52:57 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2911dedef576431295772d2e716dc90586fa4232a690d7aab1bb857b783596f1`  
		Last Modified: Fri, 26 Jan 2024 23:52:57 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9439f106ad539dcbd697b9d6dad563320e1b3a1e031b6c5e211194a15d41a0`  
		Last Modified: Fri, 26 Jan 2024 23:52:57 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8ab7a5230ba47c0695cbc1ab2df503e6724bb376f473f56251db1bf2f11b9d`  
		Last Modified: Fri, 26 Jan 2024 23:53:07 GMT  
		Size: 197.9 MB (197892532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd27fdb0313fa5bb51a8d1710962a08b2770f2066e6368c93d2ce78c9649c02`  
		Last Modified: Fri, 26 Jan 2024 23:52:57 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
