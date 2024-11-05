## `openjdk:24-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:ea683b0d8ad15234a6c61fdaa78d47d586d130161906d2e21efc37af339602a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `openjdk:24-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull openjdk@sha256:5a2d1eb52e73eeb3f6de5828f324255a439f9cca64bda9a7d71f81c9e4578c81
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2110962827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cdddf8dfdf434395b3f0b62c7db6bd51eac66f02bfec5db4fe98328706546d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Mon, 04 Nov 2024 23:07:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 23:09:04 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 04 Nov 2024 23:09:05 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 04 Nov 2024 23:09:17 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 04 Nov 2024 23:09:17 GMT
ENV JAVA_VERSION=24-ea+22
# Mon, 04 Nov 2024 23:09:18 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_windows-x64_bin.zip
# Mon, 04 Nov 2024 23:09:18 GMT
ENV JAVA_SHA256=3ab8853c76cbab5121e3c33e96b120f81d15b6979f56d1b4cc935ec94868413d
# Mon, 04 Nov 2024 23:09:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 04 Nov 2024 23:09:56 GMT
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
	-	`sha256:e2eae996a46d273cb03c06eb66cb4f5c91491f932f0e75fd5be174fc0dfe0f20`  
		Last Modified: Mon, 04 Nov 2024 23:10:01 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a0298e3726208dacc3deb1d4d9ec56bb90a3255b7959114da276cdce3501c2`  
		Last Modified: Mon, 04 Nov 2024 23:10:01 GMT  
		Size: 473.9 KB (473862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d80d4f451d5218d787eb07259480da08e383c24be85c8eae06f6c8e2f9dec0`  
		Last Modified: Mon, 04 Nov 2024 23:10:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808c6e1f0f3da9da3982a7e873bd3aa62286af52918960203d2b26f3894b0aea`  
		Last Modified: Mon, 04 Nov 2024 23:10:01 GMT  
		Size: 317.1 KB (317126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbcb4f1e457af82aa4bdf618dcb93d94a990adad2e9e982d329c4d4f59fe491`  
		Last Modified: Mon, 04 Nov 2024 23:10:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbd3318bf73a6e7995919a47cf50277db584aed79d9c5b590127b87289a8147`  
		Last Modified: Mon, 04 Nov 2024 23:10:00 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24998f0249770e052cc238dd06756dea9ff11b71f76145c03a71ae08a95962dc`  
		Last Modified: Mon, 04 Nov 2024 23:10:00 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978a212ddd002569afc5d75504b57ac5d31501cb64cc13cea30ac03b3f7f362f`  
		Last Modified: Mon, 04 Nov 2024 23:10:10 GMT  
		Size: 208.3 MB (208338774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f2832b6bbf2e39d503a3ab61a4611bd508697bb48c58fa3c8a3215f5114b7`  
		Last Modified: Mon, 04 Nov 2024 23:10:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
