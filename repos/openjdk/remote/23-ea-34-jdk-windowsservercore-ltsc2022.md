## `openjdk:23-ea-34-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:e9cbe476328ef2d2b136ffffa8b685b90814ef8f8398ed8aecd6a9823b4855fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `openjdk:23-ea-34-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull openjdk@sha256:40078ca34024a76c49745654c7ca4a59e665523738ada49efd7d61fc3273d2da
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346717970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f59ae1202f87830b367418e2289e43d353c82a0a057e14ba5125649b4338e6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Mon, 29 Jul 2024 16:56:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Jul 2024 16:57:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 29 Jul 2024 16:57:19 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 29 Jul 2024 16:57:25 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 29 Jul 2024 16:57:25 GMT
ENV JAVA_VERSION=23-ea+34
# Mon, 29 Jul 2024 16:57:26 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_windows-x64_bin.zip
# Mon, 29 Jul 2024 16:57:26 GMT
ENV JAVA_SHA256=a3f168df024882d3e2bdb72ead2dee9f16f03e7b0fb701e4a31a70e9bb543dee
# Mon, 29 Jul 2024 16:57:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 29 Jul 2024 16:57:50 GMT
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
	-	`sha256:b29131b06d84defd5064cb7c706cb85ad81c73e2e7f2a874694716b3049abdb8`  
		Last Modified: Mon, 29 Jul 2024 16:57:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685a1f87eea30f1d83b83c11db3f626a358ae0230f2c70da71e91c1d9b83a62d`  
		Last Modified: Mon, 29 Jul 2024 16:57:57 GMT  
		Size: 354.1 KB (354141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6710ee66f552edb298440649a33efe80d9adb9d660c1bdec1c7d98cd3876d9a7`  
		Last Modified: Mon, 29 Jul 2024 16:57:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35ea50529cc8f2b143256185575a1ae2b96ecd58e5bb4cd77606bc99b72fade`  
		Last Modified: Mon, 29 Jul 2024 16:57:57 GMT  
		Size: 339.4 KB (339362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e3af797bf43077b04de7aab9c7ed7d78d42162e172fbf84ed048dba8869992`  
		Last Modified: Mon, 29 Jul 2024 16:57:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d659c7ba04d28387c125cd1e8749e6e142de0fb61915882e4ad6d13de17df8`  
		Last Modified: Mon, 29 Jul 2024 16:57:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551d7682dc6d99e14696fc93a67dc461167512ff56725ca947cdbcb489aa5dcd`  
		Last Modified: Mon, 29 Jul 2024 16:57:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a231b6987348fee37227c582a90e8c5e9e1c09e2b177f56f886e72d7e52bca`  
		Last Modified: Mon, 29 Jul 2024 16:58:05 GMT  
		Size: 206.4 MB (206416427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc9e95645ad23d8363494dcf3a3a2f1d3cf0058108fad75f3102809a52f3598`  
		Last Modified: Mon, 29 Jul 2024 16:57:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
