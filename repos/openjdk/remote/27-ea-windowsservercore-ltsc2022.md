## `openjdk:27-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:b4e7e5d35ec77f9cea3257fe6cdafe92b119432d7cbbdc18e1d965e0787822b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:a90c99cb8a02f0732aee563280b2ff6d0a961a7480f5a9db2d6462fe10ca5dbd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2088196183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a63f1d76f8cf9344312187d9ec90c495bd2d833c1b027576ff679775733ef4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Mon, 02 Mar 2026 21:31:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 02 Mar 2026 21:32:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 02 Mar 2026 21:32:19 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 02 Mar 2026 21:32:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 02 Mar 2026 21:32:29 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:32:30 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_windows-x64_bin.zip
# Mon, 02 Mar 2026 21:32:31 GMT
ENV JAVA_SHA256=1ddea09bd3dbc807656ba83c0c62c5c0853849c254ca1d8b04786f58bc8d2341
# Mon, 02 Mar 2026 21:34:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 02 Mar 2026 21:34:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb32d8d4cdda12590dd7b8059d3fd077d0a54988de5f46849a98a6a87aeea4cc`  
		Last Modified: Mon, 02 Mar 2026 21:34:30 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79692db1cfa7f9fa3e2d44b6786497d9da26038843a9ed777f998072f746e4b`  
		Last Modified: Mon, 02 Mar 2026 21:34:31 GMT  
		Size: 513.1 KB (513113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e85f6ac7856f87f3fd32db2cd12cdc94a11c5e759754fa4489f3f8939d50f`  
		Last Modified: Mon, 02 Mar 2026 21:34:30 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b173b84a69e9a13c4ea8595fd5ab902e1f76111ff97fb2410a713e3eb474b8fe`  
		Last Modified: Mon, 02 Mar 2026 21:34:31 GMT  
		Size: 326.3 KB (326278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78eb30508a9e4a57d6543d1632b982f558b9d7aad05ec5aaa3893e350b24dfc5`  
		Last Modified: Mon, 02 Mar 2026 21:34:29 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed81e81ee5bc3b661f1491d894793e9c7e3a8906cbbffb5c9e68a325c6d330d5`  
		Last Modified: Mon, 02 Mar 2026 21:34:29 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703cd17f3d3dd7091d62dda1518a7e58cab64c49165eeffeb1e45d3e6316402f`  
		Last Modified: Mon, 02 Mar 2026 21:34:29 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec8224147f07b2868dfe0fa0180c7e7aef209b17b40c17f603b9d6216ea1971`  
		Last Modified: Mon, 02 Mar 2026 21:34:45 GMT  
		Size: 224.7 MB (224691651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b061d82a0880bd8593fc64aa1b8bd0aeb5047dd475cf3529f93dd0c295d2f9`  
		Last Modified: Mon, 02 Mar 2026 21:34:29 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
