## `openjdk:25-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:93427c5f34dfb85abf11f9b6edfdf8934259e5e37c73adc9c66a1848037d6219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `openjdk:25-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:28ef61f7f012fb42dd9888549ebe132a0013d93868483dbf842231cbd61e5499
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605190364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a21ade6abdd5b85963089e0cbf7a7a0964f1956f54ed2ba10b3ed852be6d70`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Mon, 05 May 2025 17:35:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 05 May 2025 17:35:48 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:35:51 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 05 May 2025 17:36:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:36:02 GMT
ENV JAVA_VERSION=25-ea+21
# Mon, 05 May 2025 17:36:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_windows-x64_bin.zip
# Mon, 05 May 2025 17:36:07 GMT
ENV JAVA_SHA256=50dc1f432a184e23ec8364a00fb4a5f8f791d3eed3a4d36226a041d7de9047e0
# Mon, 05 May 2025 17:36:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 05 May 2025 17:36:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Thu, 08 May 2025 17:36:06 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dc1da20dd7d9d66beced684a90f4859dade9e83ec2aac06a0cda2f32b90418`  
		Last Modified: Mon, 05 May 2025 17:36:38 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385128f8e202473808c7de73ddbf3661a28dc9281ca8149c262b66aed6e68886`  
		Last Modified: Mon, 05 May 2025 17:36:38 GMT  
		Size: 391.6 KB (391590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480086c53bfc672e0ee5d52f9f3ff30bbac7761df23f90c90bb598ec3c089f9c`  
		Last Modified: Mon, 05 May 2025 17:36:38 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9460df07f40ad4c56d41deac5cd729ae9ba4a3b75b5e8ba6564d5800c68fa6b0`  
		Last Modified: Mon, 05 May 2025 17:36:38 GMT  
		Size: 374.7 KB (374711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920e99fd7087652f68664fcf6e5e6e03b0b8e080cb8174697bd6111f7b40593e`  
		Last Modified: Mon, 05 May 2025 17:36:36 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c8169f4efe0081182d1906c41dc6f26ede7dceba957fa5324b0c6c16073e8f`  
		Last Modified: Mon, 05 May 2025 17:36:36 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6562b557d0f6ec04818ed22039d36a565b1df9bdfa6ee808936144715985aaab`  
		Last Modified: Mon, 05 May 2025 17:36:36 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f25f2253c13feacc4b7a68d57791154e5a84c3e8ad367035a719df517e6bf5`  
		Last Modified: Mon, 05 May 2025 17:36:50 GMT  
		Size: 209.3 MB (209254866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d51423187e6601617dfc769b0100176125ff68016f435d4940528a8daead750`  
		Last Modified: Mon, 05 May 2025 17:36:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
