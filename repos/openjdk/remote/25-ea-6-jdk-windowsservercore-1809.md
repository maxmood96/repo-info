## `openjdk:25-ea-6-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:feaa70b0edd1dddff198be56fba159374f133a62eac1a1b70cc0bb64bb3915e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-ea-6-jdk-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:1f563dc20b9d496aee9897df8cf31cc0231544e6ea055e96797beb06ac1881a3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330622881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfa71678216bab3d77215fbb187c88f3e84057e708e9c9228c24cd594beac93`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 22 Jan 2025 02:35:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 02:36:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 22 Jan 2025 02:36:17 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 22 Jan 2025 02:36:23 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 22 Jan 2025 02:36:23 GMT
ENV JAVA_VERSION=25-ea+6
# Wed, 22 Jan 2025 02:36:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_windows-x64_bin.zip
# Wed, 22 Jan 2025 02:36:25 GMT
ENV JAVA_SHA256=291c57a76ce4ef742a0402b2af6ae2b2eab2614738b9bc0e335ab9d06f105d33
# Wed, 22 Jan 2025 02:36:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 02:36:48 GMT
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
	-	`sha256:2a323b23d7592fc0f17809cd668bd07aa8accf0563d1e3c3e8321e8624ffced8`  
		Last Modified: Wed, 22 Jan 2025 02:36:52 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b46ca6abcc0aba42563c0fffd5b68b6bdbeba24a2d8e2d08e44be6bdac79293`  
		Last Modified: Wed, 22 Jan 2025 02:36:52 GMT  
		Size: 340.5 KB (340526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1761192db589bddf390c8f0200acfc01f4fd843216c16a691560d23a2f0e4bcf`  
		Last Modified: Wed, 22 Jan 2025 02:36:52 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65722b3c2ad28fc5e7b022d6c050abe50ce9a593995830cb1bbe2c5b07ceb4e`  
		Last Modified: Wed, 22 Jan 2025 02:36:52 GMT  
		Size: 330.9 KB (330933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f7874d40aff761ab309b9c4d18a44197e3dee1209e30b7e0f24b110269baba`  
		Last Modified: Wed, 22 Jan 2025 02:36:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d8d35d9aace4b016908a48c6ebe8d118bc8d932953e01bb65dfc94849e4b32`  
		Last Modified: Wed, 22 Jan 2025 02:36:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26ca632c0c1a0285bbcd15e34be85c6c0a5f95a3dbbf8bfedebfbbba80e9100`  
		Last Modified: Wed, 22 Jan 2025 02:36:51 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33da9bb82d158fb9a3dc19ec7f53d9d489cdf7d2346f2080cf09527086640da6`  
		Last Modified: Wed, 22 Jan 2025 02:37:03 GMT  
		Size: 207.7 MB (207731483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a812430d1612fca963e173b4fce0fcfb7e9703860d18582389794ed70960435`  
		Last Modified: Wed, 22 Jan 2025 02:36:51 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
