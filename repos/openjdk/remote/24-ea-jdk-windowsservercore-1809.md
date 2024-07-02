## `openjdk:24-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:6fd38e03c9783782e772786004772fa2f8646dec3c4282529ec28e51fbac363b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:24-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:07b613582ef426417ddcfa25f4c74ed0898b511ffb9b32238cf020a93c58bbf9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2428017063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94eebeaf6a796ef8a1df3d090e5ed5d9eaa6b547d823c9a8e19b3095109f926f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Tue, 02 Jul 2024 00:57:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jul 2024 00:59:10 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:59:10 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 02 Jul 2024 00:59:35 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:59:35 GMT
ENV JAVA_VERSION=24-ea+4
# Tue, 02 Jul 2024 00:59:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_windows-x64_bin.zip
# Tue, 02 Jul 2024 00:59:36 GMT
ENV JAVA_SHA256=49def475d4ac8b16fc13e9f43cb195b1da28c70cbfa438466e25f7b82c5c55a2
# Tue, 02 Jul 2024 01:00:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 02 Jul 2024 01:00:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576b05aa6cfc9b0f90b35036fbca23f1b4521dbfd96b5c17a270dbf39faca1c4`  
		Last Modified: Tue, 02 Jul 2024 01:00:27 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2af6637cad12d78a155dba53b7254da1061f4561c75a67b4a55e81244c3599b`  
		Last Modified: Tue, 02 Jul 2024 01:00:28 GMT  
		Size: 486.6 KB (486574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa1a1ae88453744b49872a2dd531b2f566c498fddebc4e4ddfa7da6cb9077ac`  
		Last Modified: Tue, 02 Jul 2024 01:00:27 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7b7e65ebf9e738d4b179cb861461264492f4a6b5266408e72f40eefc02d00e`  
		Last Modified: Tue, 02 Jul 2024 01:00:28 GMT  
		Size: 341.3 KB (341254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915a01238d030449bfe898b374723db1bbdddef91ca5a158bc2a4b51018aa6e4`  
		Last Modified: Tue, 02 Jul 2024 01:00:26 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac799793af619f2e0fd4d5aa582872d04ed31db4e3a7c08193d4fd4b6009393`  
		Last Modified: Tue, 02 Jul 2024 01:00:26 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc81c8d8cab25cfa605502f99b4a6e8f1d4bbf2b7a413b52ee2bbc17f530165`  
		Last Modified: Tue, 02 Jul 2024 01:00:26 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3dd44a16534fba5d6ad31011f1c8429f708f6ecfcd86158367a1d70ec8953b`  
		Last Modified: Tue, 02 Jul 2024 01:00:37 GMT  
		Size: 206.5 MB (206500271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738d6df23d3bfa1cdc449f4d160e2b734f552a61ff657f292186d7226298c300`  
		Last Modified: Tue, 02 Jul 2024 01:00:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
