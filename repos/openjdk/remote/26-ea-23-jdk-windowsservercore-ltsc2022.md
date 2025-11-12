## `openjdk:26-ea-23-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:248e1e64af35c7644d2f07b3196d46e14d975a86d801ddc8ac7e099d51410fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `openjdk:26-ea-23-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull openjdk@sha256:956e0212cfda17321a5f15a843be5e4e3235ba842f13244ab5ec547cbd798fa0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1992494488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc8e1b476afd2444241c02623431fd71cdf6b02700c20330843c681544c714d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:28:06 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:28:06 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 11 Nov 2025 19:28:11 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:28:12 GMT
ENV JAVA_VERSION=26-ea+23
# Tue, 11 Nov 2025 19:28:12 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_windows-x64_bin.zip
# Tue, 11 Nov 2025 19:28:13 GMT
ENV JAVA_SHA256=41b399a48fae2944ecad52c8f821b2ce5195449fb10eb54a18542b013146fe59
# Tue, 11 Nov 2025 19:28:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:28:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c47b7190b9ffc37d6229c244251af53d022884b4b7dab60e0c54d9354c4adc5`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddaae9ad1eb924ebcbb5f1dc26f2fe2d38198cd8f6d7dd3e6ea80465962108c8`  
		Last Modified: Tue, 11 Nov 2025 19:29:09 GMT  
		Size: 490.8 KB (490761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac2bff1e1e009ddb926cc431c74545f3dc38c254803bf27f5ab828601323708`  
		Last Modified: Tue, 11 Nov 2025 19:29:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6b62d41529f0c98dd003d885bd491c22e25dc520dc8bbbc9efab9b060de601`  
		Last Modified: Tue, 11 Nov 2025 19:29:09 GMT  
		Size: 337.3 KB (337326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5658bb790ed7f7ddf682bfe78355a4a1b24206fecd89e21d428a0edf02bf983`  
		Last Modified: Tue, 11 Nov 2025 19:29:09 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa3fe6fd647be08e65c72f3e9280dcfac0d722f207b660e4833ea15e12bf341`  
		Last Modified: Tue, 11 Nov 2025 19:29:09 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e1a8672bd1f83813633d0fd1d4d345517a011c1bb1aec120b096bf883c10bd`  
		Last Modified: Tue, 11 Nov 2025 19:29:09 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7593e58c88654a9fafa8b04cd9fc1db0bb401987d5c110deb26c35578ee5471`  
		Last Modified: Tue, 11 Nov 2025 22:24:12 GMT  
		Size: 221.7 MB (221697038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f0e720df16d527abea2ab040e50f3047167fb2fd3fd68d87caeae417df3281`  
		Last Modified: Tue, 11 Nov 2025 19:29:09 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
