## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:54cae743132dc6913616def124b35f8dec0014ded2f5b74d76cb1da9a7f6f08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull caddy@sha256:9594d0808254d72284be83640c15c56cc0f9551a3e2110ef6175928280db050d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1886575288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f1e3d2021857c8af1860b9ba144ff5271cb3fdf3c457a585f047b476996fdc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:21:45 GMT
ENV GIT_VERSION=2.48.1
# Tue, 11 Nov 2025 19:21:46 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 11 Nov 2025 19:21:46 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 11 Nov 2025 19:21:47 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 11 Nov 2025 19:22:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:22:02 GMT
ENV GOPATH=C:\go
# Tue, 11 Nov 2025 19:22:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:22:07 GMT
ENV GOLANG_VERSION=1.25.4
# Tue, 11 Nov 2025 19:23:40 GMT
RUN $url = 'https://dl.google.com/go/go1.25.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '6dad204d42719795f22067553b2b042c0e710b32c5a00f6c67892865167fdfd0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:23:41 GMT
WORKDIR C:\go
# Tue, 11 Nov 2025 20:17:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 20:17:11 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 11 Nov 2025 20:17:12 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 11 Nov 2025 20:17:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 Nov 2025 20:17:20 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 Nov 2025 20:17:21 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c47b7190b9ffc37d6229c244251af53d022884b4b7dab60e0c54d9354c4adc5`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e13f584c63654736fde4a175df8216409c15c6d7643ad9295de8a5abd2a4978`  
		Last Modified: Tue, 11 Nov 2025 19:24:20 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33739290334e540f49bac24464ef1cb56f154b41ac539feec548ed45ceba4dea`  
		Last Modified: Tue, 11 Nov 2025 19:24:20 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651148c569cba4ca28fc1a1a7e66b91d22bf248394b9e58fc7216718954d3d19`  
		Last Modified: Tue, 11 Nov 2025 19:24:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab9605f909b523b9d51e51e3594dd6393bd61f38075f6e1d80104dcc92a9512`  
		Last Modified: Tue, 11 Nov 2025 19:24:20 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a539a132a5c8c3884aeb9cd5d02c954e5ad7b16ae8111bcd5b32b7541069c416`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 51.4 MB (51355994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90651daee37041e751301786280046bf16d511bac6be140920137ddd93eb87f6`  
		Last Modified: Tue, 11 Nov 2025 19:24:20 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aba66b9244c160f1d7a4d876a11cadfb22bfade0fbaf21bdfe0284fc54e82a8`  
		Last Modified: Tue, 11 Nov 2025 19:24:20 GMT  
		Size: 345.9 KB (345917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1671c87189dd54542bcad772db6a5d01eec18455920d98e6d327823b96fcac0`  
		Last Modified: Tue, 11 Nov 2025 19:24:20 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4f6d6ea4acabdae52e7c4bd183a07c154acce63861c3312c4ab25e5982ed3e`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 62.6 MB (62568634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fda6eccbd8f7a48b7f4b9c7cb9a77ad2df38738eb523a57901d8b485d80f001`  
		Last Modified: Tue, 11 Nov 2025 19:24:19 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0897d23f3cdb97b5a66374968d878f3ab77359d4ae402bea1110f92b46c111db`  
		Last Modified: Tue, 11 Nov 2025 20:17:45 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7161a749e46d079a37af3a50f3da69dc4cfe9e487f3c5709febee61aca159b3f`  
		Last Modified: Tue, 11 Nov 2025 20:17:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf9d23cae18043d6e224478ea732492bba0e06711df87645b2ee5ae45975994`  
		Last Modified: Tue, 11 Nov 2025 20:17:46 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af09a0521fc25cfe8154503c9c640086af5e45dcf82dbb6a2ee371f5bbd10b51`  
		Last Modified: Tue, 11 Nov 2025 20:17:46 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d520633e45c829856995c04de150f18890ecb76e6f25843376eaeab11fbe7f0`  
		Last Modified: Tue, 11 Nov 2025 20:17:47 GMT  
		Size: 2.3 MB (2326026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172720edaa9d6b281586894b89a884a42a976ff9e6537a028ef1f177409a47e3`  
		Last Modified: Tue, 11 Nov 2025 20:17:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
