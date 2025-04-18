## `openjdk:25-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:d75d5c8edf9b94c32fc77a668763d998cc7feb1efc157a78d543ac1ac92848e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:f8ca6002cabd2b286006ff93adda9b36ab026987461510afd63b94dfa798e442
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2374211595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f218a75df2454054c4539b9dc57950e4d04910b9669951ce29800222cb23270`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 18:45:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 18:46:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 18:46:35 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 18 Apr 2025 18:46:41 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 18:46:42 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 18:46:42 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_windows-x64_bin.zip
# Fri, 18 Apr 2025 18:46:43 GMT
ENV JAVA_SHA256=29058ee51e7562ec5fb02d09a78c3540286db223bf48aacf93c4a95ed664fc7a
# Fri, 18 Apr 2025 18:47:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 18:47:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c2286616a9cf51bf70fbe01ae2f107b8954f3b5529cafb8af97d59e6ffb8a8`  
		Last Modified: Fri, 18 Apr 2025 18:47:08 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa42d3ea10fdb65a03cba8d1171a2005e6edaabcb0978a877d7257de2a008ccd`  
		Last Modified: Fri, 18 Apr 2025 18:47:09 GMT  
		Size: 339.6 KB (339644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e155a3f8b4c4f4f7cbdf80b4a98c27a7ac28d0ecfd8d3e14b0ea4f9d1b3c798`  
		Last Modified: Fri, 18 Apr 2025 18:47:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0eb16ee30e34018a91730c1a08529da674ad522855e289f52904d038333ea90`  
		Last Modified: Fri, 18 Apr 2025 18:47:09 GMT  
		Size: 319.7 KB (319746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6e515b73b3208d0cdace5a9149cd7980102656dd487478fb1ce30a74060070`  
		Last Modified: Fri, 18 Apr 2025 18:47:07 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9899e7fef6e60bc2eb0fe6be362c23854c9bf06951e18046e82a8dcae68b1087`  
		Last Modified: Fri, 18 Apr 2025 18:47:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f05aae98227052ffc23e6a1dd7d0ca7ea3ba2ca23ca7d06563781ff5ebd863`  
		Last Modified: Fri, 18 Apr 2025 18:47:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e150f68d66b2c326cebc913b0717e2ee4e9ca8f3869f419d82e2eceda729536`  
		Last Modified: Fri, 18 Apr 2025 18:47:19 GMT  
		Size: 208.0 MB (208018560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac3e83cb092acd40d85f603cafa01bf8752d5480da1dd2c28b0d6221698c12a`  
		Last Modified: Fri, 18 Apr 2025 18:47:07 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
