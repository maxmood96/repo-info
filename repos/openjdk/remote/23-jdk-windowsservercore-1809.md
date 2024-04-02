## `openjdk:23-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:d958cf4bcb7f342e8da1eb8bff2ce11b64c9092674870c3bfe3cb1240d917188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `openjdk:23-jdk-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull openjdk@sha256:f8a070132c577f1da9466c02116eab17a6f7e01a150c5110990acd1aa2cc7872
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331585899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5a27d5fe95b84c0b1634ab41e73d22e8bac6d47c9420a9822aa51deb46f707`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Mon, 01 Apr 2024 23:49:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 01 Apr 2024 23:51:49 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 01 Apr 2024 23:51:50 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 01 Apr 2024 23:52:15 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 01 Apr 2024 23:52:16 GMT
ENV JAVA_VERSION=23-ea+16
# Mon, 01 Apr 2024 23:52:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_windows-x64_bin.zip
# Mon, 01 Apr 2024 23:52:17 GMT
ENV JAVA_SHA256=d8f0d3c652a3ea74356d51353fc92684c73b07dba66500430adaec9353a30266
# Mon, 01 Apr 2024 23:53:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 01 Apr 2024 23:53:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d6ba42d24f660142d119af8afe7671f1bda7443560d3b4e21ef8c4d9ae5abd`  
		Last Modified: Mon, 01 Apr 2024 23:53:18 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6499f3691ebedaed539e4b5a88c36ee52415ad9ba2a311d445213a5e2f69b221`  
		Last Modified: Mon, 01 Apr 2024 23:53:18 GMT  
		Size: 487.0 KB (487025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e2eb61e5219bbc3f379f15b9d69b0051d82c131bb6fb457a59cbdba1582f6`  
		Last Modified: Mon, 01 Apr 2024 23:53:18 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224219d9e4deb8ffb675e1f8c4fd21b1f5a88eea3c838d81c2a0c127f24cf399`  
		Last Modified: Mon, 01 Apr 2024 23:53:18 GMT  
		Size: 339.2 KB (339247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab2aa3d6d6a2720b096709155caf5a3b8c9c9e359e7a17591980c0152bddb8d`  
		Last Modified: Mon, 01 Apr 2024 23:53:16 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55a1625676f74ba3f582d144b190dd03630a436dce1fdaa21bab1593975b0e9`  
		Last Modified: Mon, 01 Apr 2024 23:53:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08392bc9f673313bdedc20ef4547c5c7c172286f8197dc1ebee2000e522424f5`  
		Last Modified: Mon, 01 Apr 2024 23:53:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a50dae9c827cc32128c32844e144290fc82a878875870eead0df9b3c722dfe`  
		Last Modified: Mon, 01 Apr 2024 23:53:27 GMT  
		Size: 205.7 MB (205651860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803460924a372a273cd6d7007444955e74dfac955e709b23b776f33dabec9a11`  
		Last Modified: Mon, 01 Apr 2024 23:53:16 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
