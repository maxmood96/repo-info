## `openjdk:25-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:d6f287b485ed3e3ef95feaa1cb24a019110813c74d06e6b8600b9cc9b931b262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-ea-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:c29770f9d4572d1dafd50a0426f499911e7ce05f65c06b14f0bb70f5bcd63e1c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2374133422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9776b442dcd072a308f6d189df817a688589106c679d760346bb4e26ec0d3f39`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:27:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:28:34 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:28:35 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 18 Apr 2025 03:28:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:28:43 GMT
ENV JAVA_VERSION=25-ea+18
# Fri, 18 Apr 2025 03:28:44 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_windows-x64_bin.zip
# Fri, 18 Apr 2025 03:28:45 GMT
ENV JAVA_SHA256=41f24482b5d173e5a8f242d81909835bd7e85fdb131b901bff9a150186c3c03c
# Fri, 18 Apr 2025 03:29:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:29:11 GMT
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
	-	`sha256:1dcf0e933af42f2adb64ec36fdeecef1b4437da625c2c42f08a84d8682d73029`  
		Last Modified: Fri, 18 Apr 2025 03:29:16 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c166f5327e9b569c3c4803c406d6f8e536f45b2b1d08c0f003e93089e4bf3f`  
		Last Modified: Fri, 18 Apr 2025 03:29:16 GMT  
		Size: 340.2 KB (340197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddde71f727ab53698aa7bc94278b0480331c0f83b4c1d8085d1d227813a14e6a`  
		Last Modified: Fri, 18 Apr 2025 03:29:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699fc8af9439e8bf0ec170d38deafff3650e6b04cccf573d73c79d87c55aa71`  
		Last Modified: Fri, 18 Apr 2025 03:29:15 GMT  
		Size: 320.1 KB (320079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbcfc682ddff07b2f4b8bf8812f88e8de1ad82d445b4c2aac87f42dcced5f6ca`  
		Last Modified: Fri, 18 Apr 2025 03:29:14 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050614f3834cf49c91dd5ff30ffe5e8b993c4540626f829941f519ef3e58878b`  
		Last Modified: Fri, 18 Apr 2025 03:29:14 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd9fc57dbeec7e2d35b6bb5b0f31527de58b53f1ba0f65fda31c67e7605dd04`  
		Last Modified: Fri, 18 Apr 2025 03:29:14 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd33c2583f1e16bffa78eea019c1f0f0293ed523aefdf674146f0e2bae7e6494`  
		Last Modified: Fri, 18 Apr 2025 03:29:26 GMT  
		Size: 207.9 MB (207939428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055ddf0167dd7ba0a3907d6b3c829c6b2657d09f54b5def2deb3ac0ed8f1e6f7`  
		Last Modified: Fri, 18 Apr 2025 03:29:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
