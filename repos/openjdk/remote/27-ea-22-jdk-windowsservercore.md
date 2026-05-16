## `openjdk:27-ea-22-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:233dee647dc5d046a6a2991164e9618d64718a02f51bf19d28e4700da6548b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `openjdk:27-ea-22-jdk-windowsservercore` - windows version 10.0.26100.32860; amd64

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

### `openjdk:27-ea-22-jdk-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull openjdk@sha256:2735f40ba892a7a2014bcc81e76b8fe573ce21786455220513132ee343f95bfd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348641977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67be72b2b6578087cfb3b90777f8d4c86d9a7ae45931b65cc79db2026e7482f8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Fri, 15 May 2026 20:39:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 20:40:31 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 15 May 2026 20:40:32 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 15 May 2026 20:40:39 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 15 May 2026 20:40:40 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 20:40:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_windows-x64_bin.zip
# Fri, 15 May 2026 20:40:42 GMT
ENV JAVA_SHA256=8f070229867cab472c5d736b8a2b08d610772c4da7d6e451ab494e77fa4ad88d
# Fri, 15 May 2026 20:41:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 15 May 2026 20:41:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd4acf5065d2387bdf6560dbeefafc544ff9e00260a8c40d1631cff4a5aeb93`  
		Last Modified: Fri, 15 May 2026 20:41:20 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc9293fa70683c115ba9e34ce61cf8c47d413582df71dfcdd0e53966c44394d`  
		Last Modified: Fri, 15 May 2026 20:41:20 GMT  
		Size: 516.2 KB (516199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f5ae04cad74d2cdd49ae2d2d256fa443edb4d71ac801358bbc4e38280ba279`  
		Last Modified: Fri, 15 May 2026 20:41:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0afc5d026b3a384322069086353d1e15be1ddbad62e746d6b19d8327f144ff7b`  
		Last Modified: Fri, 15 May 2026 20:41:20 GMT  
		Size: 361.0 KB (360965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a581af4b07befb8bdade24c47ae4e97f09e31588192cc943f7e3912081d26f`  
		Last Modified: Fri, 15 May 2026 20:41:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0585e87d942475b8c7b05f2a023ce00420bc93feb5ffa03cdfc468509726cd31`  
		Last Modified: Fri, 15 May 2026 20:41:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2b54c1752d87e27efcf942a04b050b34101260cd8461f05ae849e2a23f7ba2`  
		Last Modified: Fri, 15 May 2026 20:41:18 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb1221a40f1929cc57d113ca48c54589c17b84bd6b9b192dc75479f70ef7631`  
		Last Modified: Fri, 15 May 2026 20:41:34 GMT  
		Size: 225.3 MB (225336334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779c0dffd3e971ac310fad82726e92890b9e9fd3d75cdc43ddf6583f08dd73a5`  
		Last Modified: Fri, 15 May 2026 20:41:18 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
