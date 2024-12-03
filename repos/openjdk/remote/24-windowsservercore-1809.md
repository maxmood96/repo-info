## `openjdk:24-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:f04cfbb89d231ad91a915fb886bef1d2474338b9eb63303c7ac28f5574c368ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `openjdk:24-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull openjdk@sha256:c13831675a15fc14660c4123ab11d73c44a129a8ecf924bc0d0bbe8b8751c25d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2220205040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bec4582f581fb8ea3f48d24f4c2e2ec09987c05a87684ee0a49fc0a11fad4f6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Tue, 03 Dec 2024 16:31:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Dec 2024 16:32:52 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 03 Dec 2024 16:32:53 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 03 Dec 2024 16:33:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 03 Dec 2024 16:33:05 GMT
ENV JAVA_VERSION=24-ea+26
# Tue, 03 Dec 2024 16:33:06 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/26/GPL/openjdk-24-ea+26_windows-x64_bin.zip
# Tue, 03 Dec 2024 16:33:06 GMT
ENV JAVA_SHA256=b22083fee813d8800a38db2020160bff319d2f6134df449d8c82d9889d120096
# Tue, 03 Dec 2024 16:33:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 03 Dec 2024 16:33:37 GMT
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
	-	`sha256:47eb95768c1174905f64969e79f72975bce8bb22a40396f70c1568a864ff3f0b`  
		Last Modified: Tue, 03 Dec 2024 16:33:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fc619d7cf278ed6bca8f181852774fa262f23e77ef886d44e2f5be0f6bc8d5`  
		Last Modified: Tue, 03 Dec 2024 16:33:41 GMT  
		Size: 493.3 KB (493269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2e0e9a76c6dba1fc02d2b8760deca609929536ce100a7919974d2051b4cf6f`  
		Last Modified: Tue, 03 Dec 2024 16:33:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da184795cdfa2cccaf8e221bffc979f575f34569c67232f7f60f674f488db51`  
		Last Modified: Tue, 03 Dec 2024 16:33:41 GMT  
		Size: 337.2 KB (337244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f95d19e4fd842e05ee0c8b28f74231530e98a954353422c4bc5ea67c285a7b`  
		Last Modified: Tue, 03 Dec 2024 16:33:40 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e662881c96fdc3b1f39231846af0152dcee18cb5d99f02cf81fa3a5733fb109`  
		Last Modified: Tue, 03 Dec 2024 16:33:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62350e4de71e35d08362522c7b7c22aa48c4c44bffa0a9289984214d719f99b`  
		Last Modified: Tue, 03 Dec 2024 16:33:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a964337733a2f3649e67d9471b13c0d67ffc3e79d154d64cb22064958ea267`  
		Last Modified: Tue, 03 Dec 2024 16:33:50 GMT  
		Size: 208.7 MB (208712978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dc083b04a3936e6b5205db0c9c4add513dede10b80ee84395d08a75d575db5`  
		Last Modified: Tue, 03 Dec 2024 16:33:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
