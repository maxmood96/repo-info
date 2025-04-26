## `openjdk:25-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:e4f3c0f2da075daf3cc4388ed4f03cd0c6c625ffbbe85d6f9277c4bdcfbdf64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:98d3b1b4fb38212cd0b0b379ab08926ec5f525eb75819bc5710879946ebc03f4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2374313465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e8af045d0304835e067d9cb0a76052badb0a7120dcab47c1598426e0652767`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 25 Apr 2025 21:53:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 25 Apr 2025 21:53:59 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:54:00 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 25 Apr 2025 21:54:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:54:07 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 21:54:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_windows-x64_bin.zip
# Fri, 25 Apr 2025 21:54:09 GMT
ENV JAVA_SHA256=189b22f424bd7f7ef01de23f6e41fd183bc3b28da7db090dacba784054fe1f43
# Fri, 25 Apr 2025 21:54:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:54:33 GMT
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
	-	`sha256:44708318aa6fa727bca5437e69a38ca42f81a8a38fb1386e9de5c7219ccb2a16`  
		Last Modified: Fri, 25 Apr 2025 21:54:38 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2139b257125f1e49adb9b165465a2fd98b4e43e0467a16d282f76ffbce34812d`  
		Last Modified: Fri, 25 Apr 2025 21:54:38 GMT  
		Size: 361.5 KB (361491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b45f999363531345643f51f22094404b375521b6c7f414f1f23d26f118e451b`  
		Last Modified: Fri, 25 Apr 2025 21:54:38 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bc4489557c3b6984ee55bbfb8b823ed9afa7a968bd755df438699774e4cd06`  
		Last Modified: Fri, 25 Apr 2025 21:54:38 GMT  
		Size: 340.4 KB (340404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c36f9f4a65b8a25c0b5a059bd7e14b7268a5bfb504d1c66cbf8c3265eb8302e`  
		Last Modified: Fri, 25 Apr 2025 21:54:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dab5f1f4dce2a82d514bee758bd61fe736a88c83929780b2504fdcb821a6eaf`  
		Last Modified: Fri, 25 Apr 2025 21:54:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe5ea44145253a3bade1c3535ab8ec54a7fa8f325ede936fe6c97b6c3f6e66e`  
		Last Modified: Fri, 25 Apr 2025 21:54:37 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846582d5c0b66811b53d57ac52d7d2a848f3366dd0b91868848a8a6cee947a14`  
		Last Modified: Fri, 25 Apr 2025 21:54:49 GMT  
		Size: 208.1 MB (208078001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2ad30f44bd17defd3c9b5ee6abfa57ef22a3586689c4a87eb2c1befe5f3668`  
		Last Modified: Fri, 25 Apr 2025 21:54:37 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
