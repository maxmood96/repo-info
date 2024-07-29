## `openjdk:23-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:8aa6aee357c94e6999a81e00a3572e1ab152e32bd2b9eac67a33c0f8a8ce36b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `openjdk:23-ea-windowsservercore` - windows version 10.0.20348.2582; amd64

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

### `openjdk:23-ea-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:750ea48123028267aa60554009a53a3fce2486a744b41257d763908457481aeb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2445723868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0800ccacdf18c81d76e6e1adc25a92151a9f4dd860169c0d00f94ce732e408f1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Mon, 29 Jul 2024 16:56:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Jul 2024 16:57:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 29 Jul 2024 16:57:43 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 29 Jul 2024 16:58:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 29 Jul 2024 16:58:05 GMT
ENV JAVA_VERSION=23-ea+34
# Mon, 29 Jul 2024 16:58:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_windows-x64_bin.zip
# Mon, 29 Jul 2024 16:58:06 GMT
ENV JAVA_SHA256=a3f168df024882d3e2bdb72ead2dee9f16f03e7b0fb701e4a31a70e9bb543dee
# Mon, 29 Jul 2024 16:58:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 29 Jul 2024 16:58:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e155327da0d263ef57f5121f510169e1d6d93c1ccb6dc63516605bd4c127c987`  
		Last Modified: Mon, 29 Jul 2024 16:58:56 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3dafb2a4316eaca9512301ee7ab2e03284da2a962bf3b531fc3f0359f91322`  
		Last Modified: Mon, 29 Jul 2024 16:58:56 GMT  
		Size: 500.3 KB (500299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d01cac8abba6f4be839ab52d99f8652339ee68028389322f6036fe17634ec9`  
		Last Modified: Mon, 29 Jul 2024 16:58:56 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7ae793fdd03170ec6989681d890e07d90502bea4e64d52e5333e47d3a68642`  
		Last Modified: Mon, 29 Jul 2024 16:58:56 GMT  
		Size: 344.6 KB (344638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19351854a97e538b99d47ca6f9cef37ff769539fde616c83ab32448462942ec`  
		Last Modified: Mon, 29 Jul 2024 16:58:54 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c06485f9f0aaaa3bb335a23ff22dd57355cedb61ed49bcfd2176c06ae21ad1e`  
		Last Modified: Mon, 29 Jul 2024 16:58:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34b16aeb3c8aab24762ca40b2379b7b265f16604d9a05214c03e464be946dee`  
		Last Modified: Mon, 29 Jul 2024 16:58:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b2104f38742aaf1ed2ab8518681940a210ac27867cf39614f1280b18ad2156`  
		Last Modified: Mon, 29 Jul 2024 16:59:05 GMT  
		Size: 206.4 MB (206441669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2757b5343992267b1dc56e64eb5cbf3f99b3df3b4d935fedd4abce41e915bdad`  
		Last Modified: Mon, 29 Jul 2024 16:58:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
