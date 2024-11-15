## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:50f6e3111cb9c9d53306e2b1575ee01fb63c1a437acdc978c15eaab99b8fcf82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `golang:1-windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull golang@sha256:1864708a7770cfb0e76cc2265f470957cc00b6c4fd5fc18d4f1d953abc87357a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355659632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a56634989cb3458ed0cbb9cd443b3740ecbdba8e9908834ff53406304c695da`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:21:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:21:05 GMT
ENV GIT_VERSION=2.23.0
# Thu, 14 Nov 2024 20:21:06 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 14 Nov 2024 20:21:07 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 14 Nov 2024 20:21:07 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 14 Nov 2024 20:21:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:21:27 GMT
ENV GOPATH=C:\go
# Thu, 14 Nov 2024 20:21:32 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Nov 2024 20:21:33 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 14 Nov 2024 20:22:39 GMT
RUN $url = 'https://dl.google.com/go/go1.23.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '81968b563642096b8a7521171e2be6e77ff6f44032f7493b7bdec9d33f44f31d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:22:40 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9823cf794cdc6b131959ef3fd911eb792cde7fe57ba485246abcd2a87e11211`  
		Last Modified: Thu, 14 Nov 2024 20:22:47 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe89cc0c4b3209642d17eb9cdfcf090b77b9f0669ccba2f7a1cdb6408911d75c`  
		Last Modified: Thu, 14 Nov 2024 20:22:47 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a9bb1c79295d487a50e4192ad8894145f48abb94d04782589921bb3d673683`  
		Last Modified: Thu, 14 Nov 2024 20:22:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5e20a61ba5f492fc164b2acd288cc48615b99c92886060724f77e33e394c1d`  
		Last Modified: Thu, 14 Nov 2024 20:22:45 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacdad877274f45130856029a878c17a45d442a65b8f4ab110a89cc8dcab10ff`  
		Last Modified: Thu, 14 Nov 2024 20:22:45 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abc01af7c3927b2ae518885ee8fb5d621ad3872b89e146a2ab15caad465a04a`  
		Last Modified: Thu, 14 Nov 2024 20:22:48 GMT  
		Size: 25.5 MB (25453632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a014da4f6e2c462c5f10cdf9391bb8d4e1b3b75fafcda6cb26e3fb153d0eab`  
		Last Modified: Thu, 14 Nov 2024 20:22:44 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e91379f96289a57a1e4022a208139f35cf898f57c96fb5bc10df3e20f6ee897`  
		Last Modified: Thu, 14 Nov 2024 20:22:44 GMT  
		Size: 357.5 KB (357497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49edf46a848cfbd52d30501ace77bbaf6d8a3059313ab6d7f6208ce0dfa67427`  
		Last Modified: Thu, 14 Nov 2024 20:22:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f673b5e160116a001ff227b14f723d017b162b809b61081301ceb1a35a8fcdd`  
		Last Modified: Thu, 14 Nov 2024 20:22:57 GMT  
		Size: 77.4 MB (77353827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519c672468c81d41cf97550250f6e947bd8695c9ca49911d6ca2842794bd6a52`  
		Last Modified: Thu, 14 Nov 2024 20:22:43 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull golang@sha256:88c1a0bdbeda0814408ed852950f7745ed0e9a9a97b9ad1651d4976fc1b0c5e0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2113953772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b8cffce73aef5e324adb631b7bd00af9946a9e68faa4b8365039e4c7d2e81b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:23:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:23:51 GMT
ENV GIT_VERSION=2.23.0
# Thu, 14 Nov 2024 20:23:51 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 14 Nov 2024 20:23:52 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 14 Nov 2024 20:23:52 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 14 Nov 2024 20:24:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:24:57 GMT
ENV GOPATH=C:\go
# Thu, 14 Nov 2024 20:25:03 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Nov 2024 20:25:03 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 14 Nov 2024 20:26:50 GMT
RUN $url = 'https://dl.google.com/go/go1.23.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '81968b563642096b8a7521171e2be6e77ff6f44032f7493b7bdec9d33f44f31d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:26:51 GMT
WORKDIR C:\go
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
	-	`sha256:7d52f4c013c77270259a2f26570ebb97024133f39e5f0d0d19bd21fd1d1796e6`  
		Last Modified: Thu, 14 Nov 2024 20:26:56 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3489509c6b25c07ceb11893b75bde11cf7c7b819674bdc97234f73bb3ff0ae7`  
		Last Modified: Thu, 14 Nov 2024 20:26:56 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715e1895f4e13c156164e502d11014398c76a8f9dd8636a3855ae21bf04e1a95`  
		Last Modified: Thu, 14 Nov 2024 20:26:55 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2bbcafc8c9f05fdaecff0555bc092b7e0461e80478bf63950ae7784a89b780`  
		Last Modified: Thu, 14 Nov 2024 20:26:55 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874b8db3d7c4c5af75f7032d17e668c06dac0de0594b07904de11ee5bae7f530`  
		Last Modified: Thu, 14 Nov 2024 20:26:55 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64df1cbde32408f8c5df6b4503cc5b073e33da80975ae4b3cb9ec52fb3a0b9bb`  
		Last Modified: Thu, 14 Nov 2024 20:26:58 GMT  
		Size: 25.6 MB (25595821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997ffdbcaacba4dba95391b8b8969bb9fce2730508cc3becf801317e9d156af8`  
		Last Modified: Thu, 14 Nov 2024 20:26:54 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8dcc61e95c50185b9fce6d34bef8fbea61a1a94ab559e124bc3f40319dd2c2`  
		Last Modified: Thu, 14 Nov 2024 20:26:54 GMT  
		Size: 350.5 KB (350480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba863396492f1dd427318fd428534b657c92c328ffd927fe49edf1acf78b5589`  
		Last Modified: Thu, 14 Nov 2024 20:26:54 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cc7e08b3db3451f8a6a9f6ca0c75462003691d4398f66739233026febb413a`  
		Last Modified: Thu, 14 Nov 2024 20:27:06 GMT  
		Size: 77.3 MB (77343118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4013366b353c80d248772e41afb787ff69271bef3e0dbb4735f0bcc3a865ac5f`  
		Last Modified: Thu, 14 Nov 2024 20:26:54 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
