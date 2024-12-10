## `openjdk:24-ea-27-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:a505fec2a028545255d38bc8b68fbba3154df472cc9697dde67badc25558004a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `openjdk:24-ea-27-jdk-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull openjdk@sha256:31cc87a8db803cd455571ea922c5f3b76185f89c3482fe11f28b1d6c13290712
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2220343069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f2c2aa00d9dba382fbecbf7f86a182cde2578882e17b75dde975192b9ae75`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Mon, 09 Dec 2024 23:30:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Dec 2024 23:31:24 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 09 Dec 2024 23:31:25 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 09 Dec 2024 23:31:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 09 Dec 2024 23:31:38 GMT
ENV JAVA_VERSION=24-ea+27
# Mon, 09 Dec 2024 23:31:38 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_windows-x64_bin.zip
# Mon, 09 Dec 2024 23:31:39 GMT
ENV JAVA_SHA256=d3c4c15520262f2d3de174d973e37053081a8b627a66e8f4939419b4af8b4823
# Mon, 09 Dec 2024 23:32:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 09 Dec 2024 23:32:14 GMT
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
	-	`sha256:0beca1b0facdf17d26085b6280fc012ea6df001863585b197b601ba5b929ff9a`  
		Last Modified: Mon, 09 Dec 2024 23:32:18 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f807baf2304ae2884b3503a4a505391b5366341cde1bf59631d3e1a478e47b`  
		Last Modified: Mon, 09 Dec 2024 23:32:18 GMT  
		Size: 503.7 KB (503672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc346e08062cf4bfc60866ad131d71ed3c6864af0d0c8f814d8a4552b21cdeb2`  
		Last Modified: Mon, 09 Dec 2024 23:32:18 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3c6c15e6a3e69c4aa563549f1dabd9d332fe93a48978a12233c86b31b89e07`  
		Last Modified: Mon, 09 Dec 2024 23:32:18 GMT  
		Size: 348.4 KB (348434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd39db0e1c7ff301f8ad9327917f821a646387f00b22d741a98f9baf94ca7042`  
		Last Modified: Mon, 09 Dec 2024 23:32:17 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3da6e4cd50a59357f1e77ee9b3ce70a5e844fe4e4960f915c1d766ff43ac90`  
		Last Modified: Mon, 09 Dec 2024 23:32:17 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f835f39c6cfe1822b5388fc8d2414c80b1007aeec039a612d815d48a9e9a9724`  
		Last Modified: Mon, 09 Dec 2024 23:32:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0b9836fb1e443243585796130c8f28681c66f016c375aac72aac9e28a8daba`  
		Last Modified: Mon, 09 Dec 2024 23:32:28 GMT  
		Size: 208.8 MB (208829407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18736c445c8ca9c4f2c9af353e3a9bb1a5f49ee93a06e2e1075b1486b26b14ab`  
		Last Modified: Mon, 09 Dec 2024 23:32:17 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
