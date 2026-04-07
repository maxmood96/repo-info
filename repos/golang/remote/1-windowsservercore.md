## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:bbd725e3fa5b73e4a362b45a6a58c7b20b00b70265b1c04e622b1a0c45850fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `golang:1-windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull golang@sha256:8234845a29eca2ec2b5b3176d4d7e688bfbf17b94bbbae787dc058a2ef622567
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2202675001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da96d708d160f344b9144d805978260ec34f272001b94adaa4fd9f4d17c0b87b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 07 Apr 2026 21:16:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 21:16:05 GMT
ENV GIT_VERSION=2.48.1
# Tue, 07 Apr 2026 21:16:06 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 07 Apr 2026 21:16:08 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 07 Apr 2026 21:16:10 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 07 Apr 2026 21:17:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 21:17:54 GMT
ENV GOPATH=C:\go
# Tue, 07 Apr 2026 21:18:02 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 21:18:02 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:20:01 GMT
RUN $url = 'https://dl.google.com/go/go1.26.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '98eb3570bade15cb826b0909338df6cc6d2cf590bc39c471142002db3832b708'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 21:20:03 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c05594f5b6a5ee35f1df97ff1e9812e26edb6c7f470f8f746554c8b06f4240`  
		Last Modified: Tue, 07 Apr 2026 21:20:23 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f9f91c2370a29c9ab08df42ade834aac855e8410c789d15d4ba997bdcbd691`  
		Last Modified: Tue, 07 Apr 2026 21:20:23 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f0044343910ef777753aa092055a320105c26a9e885c8d983bdd277ab120aa`  
		Last Modified: Tue, 07 Apr 2026 21:20:22 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a1b08fa657f048a1d25e440854e669ab6a6430e1be6711a1a22ca1f0c73d6b`  
		Last Modified: Tue, 07 Apr 2026 21:20:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e6301e5ad1b052e0eee054f9478bc50b797a09729e0f8dd73694cd0efa3710`  
		Last Modified: Tue, 07 Apr 2026 21:20:22 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6475ed77d84e216e78d87a7fc73aa32b4d408d69a8d020aa3b1e023e36fcb620`  
		Last Modified: Tue, 07 Apr 2026 21:20:28 GMT  
		Size: 51.3 MB (51270495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662ea69fd556d2b8aaee3239e5b4a4b7b62e021b56354b6d0db222d41fd9c9c7`  
		Last Modified: Tue, 07 Apr 2026 21:20:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3714d1abbfe29a18553d3a97267a845e994b6575a8d12f43c65b1805ca541934`  
		Last Modified: Tue, 07 Apr 2026 21:20:20 GMT  
		Size: 354.1 KB (354100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed1a366b28c27db1a53b2799d8ffca916f0a0b22ba0c0f5803a567e99c907f1`  
		Last Modified: Tue, 07 Apr 2026 21:20:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a7609cd3012ef7dc05f8e4f77f633a4ba1907b42651e59f833e3ee88e69531`  
		Last Modified: Tue, 07 Apr 2026 21:20:32 GMT  
		Size: 69.8 MB (69843823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408097dbec7994ec48521937aa50f887606cb198647e1b95e8f31c09e5bcd3d4`  
		Last Modified: Tue, 07 Apr 2026 21:20:20 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull golang@sha256:80b07addeab556791eabe13f7dfb50555b585ed5296617907b4dfd059ef51f05
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2103823439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0997be02c419a4496b37c5c17e38db1eeb0f2e1315dbad597f1dd63b56f7a579`
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
