## `openjdk:22-rc-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:6587743782e5a03ad7eafa5e1a8eb7b4b09e26cb378ec2be59b338123ae66983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `openjdk:22-rc-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull openjdk@sha256:8c083eeb23c7f10bea82dc294756cc305f60d53fa4394f8eb5178ddc9f1b9799
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098780895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2340c26a29a33565627c822072d49a83b6f74ace5b1aa83f65cd5e4860b68c00`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Mon, 12 Feb 2024 21:54:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Feb 2024 21:55:27 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 Feb 2024 21:55:28 GMT
ENV JAVA_HOME=C:\openjdk-22
# Mon, 12 Feb 2024 21:55:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Feb 2024 21:55:34 GMT
ENV JAVA_VERSION=22
# Mon, 12 Feb 2024 21:55:35 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_windows-x64_bin.zip
# Mon, 12 Feb 2024 21:55:36 GMT
ENV JAVA_SHA256=66546cc473f6f4ebb8161a8664afc6e04fa80cdf5c93a33e07f57eb1c27d6682
# Mon, 12 Feb 2024 21:56:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Feb 2024 21:56:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3c92a169aff0fbe39f90be6e7bf78ad308fc207e4d5d00c6da8a89c6cee856`  
		Last Modified: Mon, 12 Feb 2024 21:56:12 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28bcd82b19e407e4a06b721810648213702f181084f9dad729b6673ebce8948`  
		Last Modified: Mon, 12 Feb 2024 21:56:12 GMT  
		Size: 487.7 KB (487671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbc6176c976ab9b643ead029cae643ada7fe83381046a0fbdbdb576ffd7e214`  
		Last Modified: Mon, 12 Feb 2024 21:56:11 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2974f7a2d571d414b99ca2d5f42722a049ac381372bfb8913829a11ce0dc5be`  
		Last Modified: Mon, 12 Feb 2024 21:56:12 GMT  
		Size: 338.9 KB (338860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99179ed1c951dc67a51b5114d5846f714d429f3445d898d5f81fa0534ab305bc`  
		Last Modified: Mon, 12 Feb 2024 21:56:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6afb562ca2ecac5098878175089b002626d611fbab7050aa359f44d68a1232`  
		Last Modified: Mon, 12 Feb 2024 21:56:09 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb89efe3125560b0cd05fc8448bff3e41f87419af1b6bf9374aff880e94ea15`  
		Last Modified: Mon, 12 Feb 2024 21:56:09 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5478e1c9d936842287b71b5a54aa792ab3bb6fdf9c103879d0b47d6775bd6808`  
		Last Modified: Mon, 12 Feb 2024 21:56:20 GMT  
		Size: 197.7 MB (197733861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff55eb7b5cfa9dffd040895617be281a9105acddfcbc05eabc937c560b34ae2`  
		Last Modified: Mon, 12 Feb 2024 21:56:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
