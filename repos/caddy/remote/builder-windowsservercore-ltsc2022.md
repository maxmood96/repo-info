## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:72c51053d82a9ac0b1d0b152cac71e68d9782764609b58bef5075dbd10972766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull caddy@sha256:f6727e355005ede6d8d9f7512cceba6126a35afaafeee810638c1645882e2c75
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2106141696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e357d6ef56bcee081e27a23747ebddc32ac0ba52f7d8660acaa0dfdc92bcd76`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 07 Apr 2026 21:19:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 21:19:56 GMT
ENV GIT_VERSION=2.48.1
# Tue, 07 Apr 2026 21:19:58 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 07 Apr 2026 21:20:00 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 07 Apr 2026 21:20:02 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 07 Apr 2026 21:22:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 21:22:11 GMT
ENV GOPATH=C:\go
# Tue, 07 Apr 2026 21:22:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 21:22:20 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:24:30 GMT
RUN $url = 'https://dl.google.com/go/go1.26.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '98eb3570bade15cb826b0909338df6cc6d2cf590bc39c471142002db3832b708'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 21:24:32 GMT
WORKDIR C:\go
# Tue, 07 Apr 2026 21:58:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 21:58:39 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 07 Apr 2026 21:58:41 GMT
ENV CADDY_VERSION=v2.11.2
# Tue, 07 Apr 2026 21:58:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 07 Apr 2026 21:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 07 Apr 2026 21:58:53 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35beb243c485edbbbeb4a9664d1cceb4e5365b872545bee1ef562541078328a7`  
		Last Modified: Tue, 07 Apr 2026 21:24:42 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c60b05743686cc43640794f061c188fe5a87af38f4f933e953485f52da3c418`  
		Last Modified: Tue, 07 Apr 2026 21:24:42 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a24e7efb11147615f48771da348381a4311c2717f808ee544f69192a35d38a`  
		Last Modified: Tue, 07 Apr 2026 21:24:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2937ddd8463035501a98a617793534d0493aab0e14a46b616cd4f0ebeba4e2`  
		Last Modified: Tue, 07 Apr 2026 21:24:40 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66013528778561c754c6d999c3f9b18bce76a5c6c13e7c2c774eaf126234926`  
		Last Modified: Tue, 07 Apr 2026 21:24:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca9bc9b15448da74b431fb5172188e158dfa278a800f3aafd42c155c4e96ef6`  
		Last Modified: Tue, 07 Apr 2026 21:24:47 GMT  
		Size: 51.4 MB (51377184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c531705324d97f73c4f0eabe4ace0fb206048640c462398fe91ac78565414c41`  
		Last Modified: Tue, 07 Apr 2026 21:24:39 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d140edba8c31a224e1264274534a17a49d47e42bda7eb8a25f441272fb087bf2`  
		Last Modified: Tue, 07 Apr 2026 21:24:39 GMT  
		Size: 329.4 KB (329350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734acc068ddc9608c4904b0bb065f9295bebc374835b1b9dd9c180fcba1c9ae3`  
		Last Modified: Tue, 07 Apr 2026 21:24:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d43ebc52cb2408b64f3384d22fd203742c8f3cb22839d1cf330b5e2f4a380bf`  
		Last Modified: Tue, 07 Apr 2026 21:24:51 GMT  
		Size: 69.8 MB (69824918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0ac5807acf70f37c4783bb931188362a740c107963065ea412056e1667aeab`  
		Last Modified: Tue, 07 Apr 2026 21:24:39 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f272b5beb4f4bf9aeec68acf4f04ac315197cb641560ca88f1991018a7c2ce`  
		Last Modified: Tue, 07 Apr 2026 21:58:59 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c486feefef3fd2f434132c9a70f871a821e10d1af2aee5dcd269e4b14963b0a2`  
		Last Modified: Tue, 07 Apr 2026 21:58:58 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7592c29beca07e4be8cda00f4bdb03c41a8d696f4bf1582f050b810d35d80669`  
		Last Modified: Tue, 07 Apr 2026 21:58:58 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cad630818ef630c80cc4de886a5ffa492417cff8fb671114e350b1469daffd`  
		Last Modified: Tue, 07 Apr 2026 21:58:58 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e72fd75feb7c3bfce21a237e382d2e2ce1f831fc9ef5d540e9d8f28b63a793`  
		Last Modified: Tue, 07 Apr 2026 21:58:59 GMT  
		Size: 2.3 MB (2311635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8162eafd7bb43d20dad64c00b9263a2b0721f95d92802d8431ad78795c9047`  
		Last Modified: Tue, 07 Apr 2026 21:58:58 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
