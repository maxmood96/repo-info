## `openjdk:28-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:d59d237ed76914dc24e1cc6ebb01b8cc5926cb8491683acc958b87c6b6c2560b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `openjdk:28-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:699ea0a6899a8b34f2c53ca6a2f4094b16cf01a35f9c5efb0cd50e92847c2a8b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2503890563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34e2dfe5e24d0257eb70944d6a6290201f4ed6428aba1e018e221de1edd32ee`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 16 Jun 2026 23:38:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Jun 2026 23:39:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 16 Jun 2026 23:39:14 GMT
ENV JAVA_HOME=C:\openjdk-28
# Tue, 16 Jun 2026 23:39:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 16 Jun 2026 23:39:23 GMT
ENV JAVA_VERSION=28-ea+2
# Tue, 16 Jun 2026 23:39:23 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_windows-x64_bin.zip
# Tue, 16 Jun 2026 23:39:24 GMT
ENV JAVA_SHA256=6e0811bf75540123fa28845352ebc400893f45c2b1ad8bedcf7837395fce7e5e
# Tue, 16 Jun 2026 23:40:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 16 Jun 2026 23:40:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a298932495c13e91f62335a0e5296c0ae05289913cf23ab2b14a96762d146045`  
		Last Modified: Tue, 16 Jun 2026 23:40:18 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f8646ae131f2e0dfb955d73c396f289956d627dd2d67ea29fc31957d86db37`  
		Last Modified: Tue, 16 Jun 2026 23:40:19 GMT  
		Size: 396.4 KB (396420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da9242152f2dd0f314fd3e47e4324a3e732dd5a880bb7f7ac4b9ae0f75b9ef1`  
		Last Modified: Tue, 16 Jun 2026 23:40:18 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601787c3a581561d148ead7f38fc2d96c09c354181fd47e3076b2b099ab17b71`  
		Last Modified: Tue, 16 Jun 2026 23:40:19 GMT  
		Size: 385.7 KB (385656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515d1b7ec672ee336ac997468fd2a77aebc198a803a6d84ff22136d5b8e8621b`  
		Last Modified: Tue, 16 Jun 2026 23:40:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd9b3cc6a77aa84795adfd5ee18e38e14d1192df4cb604ee4bf460b8a915f3e`  
		Last Modified: Tue, 16 Jun 2026 23:40:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9f1c75ca71dee3c93ed21acefe9d1e9b249bf5c9a8e1e4e4c6b036e605d160`  
		Last Modified: Tue, 16 Jun 2026 23:40:17 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9555db5abdfbbd37e72fd02835d39dd26cbbd33a3ebad410b0858995ae783f70`  
		Last Modified: Tue, 16 Jun 2026 23:40:31 GMT  
		Size: 224.0 MB (223957753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cefae35cdc92300c17343df10892024a2bc82f8433b3ba7c0edd45711e621a4`  
		Last Modified: Tue, 16 Jun 2026 23:40:17 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
