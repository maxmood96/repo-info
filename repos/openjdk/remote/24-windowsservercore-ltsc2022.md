## `openjdk:24-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:7b781ebaa6130bdd1630d7080019b0e6267c6589d82e0e0537fd87db204c1d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `openjdk:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull openjdk@sha256:075b7dae900e97a6aab450e7ff932cddbb252c131563c558daf5d4487c08de1c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346891830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce3f25f5c8383c0b82276141d05ec811589701c4f454f6803cda58174b622fd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 10 Jul 2024 17:04:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 17:05:07 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Jul 2024 17:05:07 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 10 Jul 2024 17:05:13 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Jul 2024 17:05:14 GMT
ENV JAVA_VERSION=24-ea+5
# Wed, 10 Jul 2024 17:05:14 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_windows-x64_bin.zip
# Wed, 10 Jul 2024 17:05:15 GMT
ENV JAVA_SHA256=6311a1a2de647471859f4eda1f035e7da59a26882c2bc3e456a97e88b9e9647b
# Wed, 10 Jul 2024 17:05:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 10 Jul 2024 17:05:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69044c447a99edc9329b13edaf54c766056701697f015216580b8936a21da5db`  
		Last Modified: Wed, 10 Jul 2024 17:05:41 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6cc6f9dc572c55c5923b3f3be27ef1969be5b884717bc2c3dc6992a62a3666`  
		Last Modified: Wed, 10 Jul 2024 17:05:41 GMT  
		Size: 358.9 KB (358910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b423f5ec8a969dbe188018e8c7413b12e19fc374c9af0108a43d11c83050f9`  
		Last Modified: Wed, 10 Jul 2024 17:05:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abf6e60432a2e919450d6e73177925190e033e676c164348ef94ed0f0530923`  
		Last Modified: Wed, 10 Jul 2024 17:05:40 GMT  
		Size: 347.0 KB (347026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fb9efdfa14a42b8b5577acc4edf795ae48981fbe0d0dc0bd40b0b37a24641d`  
		Last Modified: Wed, 10 Jul 2024 17:05:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3d09c110db0195ca8db53ae2bd346433542f0ebe916916edf9d3abc35b1a72`  
		Last Modified: Wed, 10 Jul 2024 17:05:38 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c664e62ea6a1f75866d0549073b82ddfba6717ff7c86c7fafe98e9d11e431c01`  
		Last Modified: Wed, 10 Jul 2024 17:05:38 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1949636779a894efa8131f4343dda306d6f0db8d2037e67512b759d8846ec215`  
		Last Modified: Wed, 10 Jul 2024 17:05:49 GMT  
		Size: 206.6 MB (206577662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e48d205aaaf43ea5db4f63a225cc8018c085b5e13477ce10219bd24e73668dd`  
		Last Modified: Wed, 10 Jul 2024 17:05:38 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
