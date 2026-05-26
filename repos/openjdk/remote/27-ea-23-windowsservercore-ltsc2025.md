## `openjdk:27-ea-23-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:9e41b0c8f993517f54075a5fb6d6ebd6dac481d4709480703ff8818d947d121b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `openjdk:27-ea-23-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull openjdk@sha256:79bafb23ebe47335dccae88025085a2a371709d63bc2e80de78ddffdee88ddcc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2431959630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434e8029e744d1b45ae167e298c22171a3a840d982cc8545c6212a5b0bb3e18d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 26 May 2026 19:14:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2026 19:15:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 26 May 2026 19:15:26 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 26 May 2026 19:15:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 26 May 2026 19:15:34 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:15:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_windows-x64_bin.zip
# Tue, 26 May 2026 19:15:37 GMT
ENV JAVA_SHA256=7a3570aa872e47b54f71fd9c142dc466b4b796ffc20ebd57cd26987efab6546f
# Tue, 26 May 2026 19:16:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 26 May 2026 19:16:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bba8ce69ea3c2c1dc61eae975c3e5c01e5eba038c6953ebd7963198d5be4b20`  
		Last Modified: Tue, 26 May 2026 19:16:58 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b8c6ba57244681d379c4e2a8b443adfad61fcaa045e7594b9661eda1c21b2e`  
		Last Modified: Tue, 26 May 2026 19:16:58 GMT  
		Size: 389.2 KB (389197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc9692fc6d3e3d2c1d0dc84e33efe2f0b6abc274f699552d11375f7c7145ee2`  
		Last Modified: Tue, 26 May 2026 19:16:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa33a9c9981bb572e7bf646475288620d1074a459c165d6d3009b60d67d01383`  
		Last Modified: Tue, 26 May 2026 19:16:58 GMT  
		Size: 334.3 KB (334334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632607d87c51351820c3bf690e22b92de568c94a8c05ac9cf20dc96a5e3a1050`  
		Last Modified: Tue, 26 May 2026 19:16:56 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb9f5cdb504b31e895d83e88994a029fcfd38f1e3f0533849da3d56603662dc`  
		Last Modified: Tue, 26 May 2026 19:16:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65733d780f40e4633347e4446fc3cd4fdd4d5af07d8a142cda947beb5f2f3399`  
		Last Modified: Tue, 26 May 2026 19:16:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d47509ed73e207b30fdfbb8ab42305a200f8c192e5744afe69cb94f60ca1f7b`  
		Last Modified: Tue, 26 May 2026 19:17:10 GMT  
		Size: 225.3 MB (225286467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08272f4e9cff37ef4682f1dd138e35af5bf17b5d5dd360042129636b115ee46`  
		Last Modified: Tue, 26 May 2026 19:16:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
