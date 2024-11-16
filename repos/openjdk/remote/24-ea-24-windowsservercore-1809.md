## `openjdk:24-ea-24-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:4b90f5e388ad83a8747cec8a6031ce6b2d7f3693355831b53a0b37d9a851470f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `openjdk:24-ea-24-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

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
