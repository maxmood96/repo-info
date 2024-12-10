## `openjdk:25-ea-1-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:0323df2d69b19a609f939b67d822b2b45d0d9aa20a2ca5e06379cc7282460435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `openjdk:25-ea-1-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull openjdk@sha256:cecd75e09367bcc34c77eae00e02890eae5273f541a6ddf6b178ef8b974d3e4a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2220419857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783468780688e94afa2f1a9ae718fb13c7e4b9edd955491e84beacb5c77ef05f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Mon, 09 Dec 2024 23:29:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Dec 2024 23:31:30 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 09 Dec 2024 23:31:31 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 09 Dec 2024 23:31:41 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 09 Dec 2024 23:31:42 GMT
ENV JAVA_VERSION=25-ea+1
# Mon, 09 Dec 2024 23:31:43 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_windows-x64_bin.zip
# Mon, 09 Dec 2024 23:31:43 GMT
ENV JAVA_SHA256=e613057ce9dd454d410ac2462a504dd7679eeec29d28c18c9d16c6d12f12f346
# Mon, 09 Dec 2024 23:32:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 09 Dec 2024 23:32:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6fd3dfa20c1d65d0268634885e1faf52e6ba86925cd04767a5dc79d3af0777`  
		Last Modified: Mon, 09 Dec 2024 23:32:36 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5a2a5b466475e162ebc994d3e4ca0c223fc4eb0505b61f7492ffd17b22a55b`  
		Last Modified: Mon, 09 Dec 2024 23:32:36 GMT  
		Size: 493.5 KB (493481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fc9291fb3e0bac7eb383f54a5b6e187421a8246239ee999bd35deac416e855`  
		Last Modified: Mon, 09 Dec 2024 23:32:36 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d4e432b4ac9849e7414b7eb7acbe9b3162618f4decaa49d0a9babe008f0f40`  
		Last Modified: Mon, 09 Dec 2024 23:32:36 GMT  
		Size: 337.4 KB (337383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1d15bffa3da761d4a7e8fc12a1ddb6efdd261c5a52eae000c9a9fb99f7bbee`  
		Last Modified: Mon, 09 Dec 2024 23:32:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c428588222e233ad3d18afa39e9ac45d429f82702a5c8dee415b2d3df28b08`  
		Last Modified: Mon, 09 Dec 2024 23:32:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940130d3bd5135d42d05418c978115e11f4c7fd8408ceba7302ec66e220960bf`  
		Last Modified: Mon, 09 Dec 2024 23:32:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9fca6b37d9e796d535c5032975bbe4cb25c7958c09b2a536cd0ee4c952fa16`  
		Last Modified: Mon, 09 Dec 2024 23:32:46 GMT  
		Size: 208.9 MB (208927455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91996e0f386cdeef116835bfd2973420be828ec1a11b9504ea1413cbf92b9bf0`  
		Last Modified: Mon, 09 Dec 2024 23:32:35 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
