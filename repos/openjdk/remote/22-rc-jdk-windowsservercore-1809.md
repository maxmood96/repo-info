## `openjdk:22-rc-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:3ffbe33590f8f4e4a2cf04859ef34d5347edace06f03a7a86c7e8c8d570a8050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `openjdk:22-rc-jdk-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull openjdk@sha256:d724f78f259c28e3cff16e5c98a119bee4071c836772b884a41730b3cc0994cb
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279046906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5435036613c56f08feb283680193651364c4316489ef62dc21532032e97972a3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 20:07:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:08:36 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:08:37 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 14 Feb 2024 20:08:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:08:58 GMT
ENV JAVA_VERSION=22
# Wed, 14 Feb 2024 20:08:58 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_windows-x64_bin.zip
# Wed, 14 Feb 2024 20:08:59 GMT
ENV JAVA_SHA256=66546cc473f6f4ebb8161a8664afc6e04fa80cdf5c93a33e07f57eb1c27d6682
# Wed, 14 Feb 2024 20:09:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:09:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58e2e783697209b91448fdcfc77d256d42e17f17df7b84c82ce6ebf6c5204d6`  
		Last Modified: Wed, 14 Feb 2024 20:09:45 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0fb6eb859c9b0bdbf92705402263e3bfe3a7efc166f685c3617f777886f32c`  
		Last Modified: Wed, 14 Feb 2024 20:09:46 GMT  
		Size: 497.4 KB (497433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3c2369ea10bd2ed1cf46c922cd7a31483bcf5d3871d12f1b71b139414848b6`  
		Last Modified: Wed, 14 Feb 2024 20:09:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924441615f2e1ef18727a8a44831466e504da6862c3f3e63ef1090fbe0094841`  
		Last Modified: Wed, 14 Feb 2024 20:09:46 GMT  
		Size: 344.9 KB (344871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7cb7e3e13ea05cd0fa033a081e6082ce09c81ce0b2d85c278e3be28e18c41c`  
		Last Modified: Wed, 14 Feb 2024 20:09:43 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731f4d8c45f158e66ad0b462e447106f603f08c7aca04e6f3b672a48f4500564`  
		Last Modified: Wed, 14 Feb 2024 20:09:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954a43ec174d080f054db3b5d83eb19588e69cb85b5107f7801d5a4eada45d0c`  
		Last Modified: Wed, 14 Feb 2024 20:09:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015d385860387ff5ce2c4114efa1d3da33d0423f6481a517c13b11c535739a03`  
		Last Modified: Wed, 14 Feb 2024 20:09:54 GMT  
		Size: 197.7 MB (197748006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a7ba4f3385703af9d9d2c95d11c8a568f77acb7eb01ec966439b14e458d4da`  
		Last Modified: Wed, 14 Feb 2024 20:09:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
