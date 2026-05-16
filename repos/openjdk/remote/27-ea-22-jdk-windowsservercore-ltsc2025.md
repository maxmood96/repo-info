## `openjdk:27-ea-22-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:0c189895dc6d4c39ca15dadb8c55806f2a884e0e1b557058145da9c30965075e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `openjdk:27-ea-22-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull openjdk@sha256:35d6e71f7f1e802461342b476c01e408cdcd57f85ae2c1ab06c298d340189096
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2431968714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979df0baff7a1516dfda4ba1ce6b9f3abe410e55abd2599128c231859113d837`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Fri, 15 May 2026 21:10:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 21:11:02 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 15 May 2026 21:11:04 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 15 May 2026 21:11:11 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 15 May 2026 21:11:12 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 21:11:12 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_windows-x64_bin.zip
# Fri, 15 May 2026 21:11:13 GMT
ENV JAVA_SHA256=8f070229867cab472c5d736b8a2b08d610772c4da7d6e451ab494e77fa4ad88d
# Fri, 15 May 2026 21:12:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 15 May 2026 21:12:28 GMT
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
	-	`sha256:915521ee20f379f50a06d4f22330e0f6b880411357921aceff959d4549c62fde`  
		Last Modified: Fri, 15 May 2026 21:12:35 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b6e349719dd85cb482ff567e3d7f785bd84849f2f198dcccdef658a6ea4a75`  
		Last Modified: Fri, 15 May 2026 21:12:35 GMT  
		Size: 361.3 KB (361283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e234040c4048269a05c53ee25ef9fe75bd01c137abc58fe06ca1c2c38b0ebc9`  
		Last Modified: Fri, 15 May 2026 21:12:35 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c07fa7d71a965015cc4bab16430f7f83f750021fd7430d375b789ef12933eb0`  
		Last Modified: Fri, 15 May 2026 21:12:35 GMT  
		Size: 347.5 KB (347533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8663b0d39c4e9b37542a978d9e84b650b99265e844731522289077af6d3d0a6d`  
		Last Modified: Fri, 15 May 2026 21:12:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b334f34deab3ec5a5c347a95ad24c15e31c0583d3ddf19f8015361de5ff80b`  
		Last Modified: Fri, 15 May 2026 21:12:33 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb8bcd1d3f468ec6541749ea988cd0ca9e28d2899e3ee3db2622b8433fa67c0`  
		Last Modified: Fri, 15 May 2026 21:12:33 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79705a2c75733b509f4c4bb49814b29351dd347c0795ebcf7004a4419449d80`  
		Last Modified: Fri, 15 May 2026 21:12:48 GMT  
		Size: 225.3 MB (225310301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3f8635e9146f0a176a18d7d34d35a294c0ec6ac451df0a9c1fb28875699f80`  
		Last Modified: Fri, 15 May 2026 21:12:33 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
