## `openjdk:24-ea-3-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:883e9527755acebce007cdbb2d936b99991dd73ff75d3a613691451008b70f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `openjdk:24-ea-3-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull openjdk@sha256:e864988b2c32af8faf2182040577b050d30c3b0da26af3ce9014d624e3c6baa8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325437324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5171520f59a9e6098344d31bc1ca3e12b0af58d596f4754e3d219e17dc3c038f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Sat, 22 Jun 2024 01:05:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Jun 2024 01:05:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:05:27 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 22 Jun 2024 01:05:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:05:33 GMT
ENV JAVA_VERSION=24-ea+3
# Sat, 22 Jun 2024 01:05:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/3/GPL/openjdk-24-ea+3_windows-x64_bin.zip
# Sat, 22 Jun 2024 01:05:34 GMT
ENV JAVA_SHA256=dadb681c56ce901258f2c4dc34514ff6eb2b62bddf51f507bebdabac55556dbb
# Sat, 22 Jun 2024 01:06:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:06:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d188e1a6b4ee7366ccc7a82d2f679c796ea79ae531f63715b3007d0717d4b1d`  
		Last Modified: Sat, 22 Jun 2024 01:06:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e5ac21c3ac7ec3766413554f120057b0f85b796f91a5def14d00ea0acd1705`  
		Last Modified: Sat, 22 Jun 2024 01:06:07 GMT  
		Size: 359.1 KB (359125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ed8df641846649e53b81f84f53b33bd1eaacbf48f52b188ed4c20bd48a8eed`  
		Last Modified: Sat, 22 Jun 2024 01:06:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8125212605659ee3ba337510b4682117d7fbc01fdc2b98732565bd6c04e1c6a4`  
		Last Modified: Sat, 22 Jun 2024 01:06:07 GMT  
		Size: 344.0 KB (344040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cfefcc9c575adfdb254edc48b397943eedd9210325b660fe7d91fa80eea022`  
		Last Modified: Sat, 22 Jun 2024 01:06:06 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8354faf79fbe25d20ea8ecdde3e0919167a7a120e66824622a3a3314ede363e2`  
		Last Modified: Sat, 22 Jun 2024 01:06:06 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18c2ce97cba73160d611b99cfc5d64e2b660447d30c5bd527befa8dbed57880`  
		Last Modified: Sat, 22 Jun 2024 01:06:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af68d8f3700f449fbe8382bfa70084f5ba01a003cc8de319ea2c87450e67a19`  
		Last Modified: Sat, 22 Jun 2024 01:06:17 GMT  
		Size: 206.5 MB (206536160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5a49744170d3c288de41114b171543500ecde84d76b5ade3c05c8aa7afb2eb`  
		Last Modified: Sat, 22 Jun 2024 01:06:06 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
