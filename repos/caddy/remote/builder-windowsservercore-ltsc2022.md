## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:dddb064f09509678ed9eb72e38deeae3ea5388a470e38a917c6871448ff879f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull caddy@sha256:76159f32d9647e38cb6d6459a2a24c0f053f8875bcd1009520b8ceeb4a21783a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1611414081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c037161b9a45eeaacf942646ebacc350fe414a89bad683e3a3955cb0dcbc392e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 01:39:57 GMT
ENV GIT_VERSION=2.23.0
# Sat, 24 Jun 2023 01:39:58 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Sat, 24 Jun 2023 01:39:59 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Sat, 24 Jun 2023 01:40:00 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Sat, 24 Jun 2023 01:40:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Sat, 24 Jun 2023 01:40:34 GMT
ENV GOPATH=C:\go
# Sat, 24 Jun 2023 01:40:55 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Jul 2023 19:14:09 GMT
ENV GOLANG_VERSION=1.19.11
# Tue, 11 Jul 2023 19:16:44 GMT
RUN $url = 'https://dl.google.com/go/go1.19.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '25f04babf4ebb51cebca329d3479771b29721433c924c5707f3b0689878d5232'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 11 Jul 2023 19:16:46 GMT
WORKDIR C:\go
# Tue, 11 Jul 2023 19:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jul 2023 19:48:28 GMT
ENV XCADDY_VERSION=v0.3.4
# Tue, 11 Jul 2023 19:48:29 GMT
ENV CADDY_VERSION=v2.6.4
# Tue, 11 Jul 2023 19:48:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 Jul 2023 19:48:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('542b4c083852d41081186c79757b66ff3c26248f72ed461dbc038b51687d0a8a8ce8eee69e3b5a1d43360c48b3405b611b940fa378debe98aaa0b3c5aebfa218')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 Jul 2023 19:48:53 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a725a5b1d95b19c55801da205e401134949a3ef3b2bb040c785986202ad134`  
		Last Modified: Sat, 24 Jun 2023 02:16:35 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94771fd18b203dc5bc66c78c94d318edc726e0d3622915884225783fae93b5d`  
		Last Modified: Sat, 24 Jun 2023 02:16:33 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c970e5e0e48292f70cad71999574a45005b6e3963bda38cfde70630ada11e37`  
		Last Modified: Sat, 24 Jun 2023 02:16:33 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6de2df6562966a148a26d7f00bf85d056d4d22c71ebe170634f84253f0b559`  
		Last Modified: Sat, 24 Jun 2023 02:16:33 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d888c846778cfed7da69e726b491b06cbec333bdbe711985b03844e3948608`  
		Last Modified: Sat, 24 Jun 2023 02:16:38 GMT  
		Size: 25.4 MB (25401467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ac5846332b11bb977d027d06552fe067f700a9d5a62560972a0e3c561e19be`  
		Last Modified: Sat, 24 Jun 2023 02:16:31 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0157f348cbd78f039722165c2f836f19d234498082d52f2bb0b601aca16fab`  
		Last Modified: Sat, 24 Jun 2023 02:16:31 GMT  
		Size: 264.3 KB (264272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a56d3f545573239966385a720517b901dfbdae72c838458d0397e9029dd3b17`  
		Last Modified: Tue, 11 Jul 2023 19:28:36 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da227820c9b9cca9a43a21a96e39b3f6c3c70314d667913f76c2828f22ed45e4`  
		Last Modified: Tue, 11 Jul 2023 19:29:11 GMT  
		Size: 157.8 MB (157754980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c53326f470fd8b5e80d1c62d4ba253a7d0c5b606e4fc619d8494bdc79d39259`  
		Last Modified: Tue, 11 Jul 2023 19:28:36 GMT  
		Size: 1.6 KB (1558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6a4c3ecfa4a0cb08ace58e17c41d14a165db7cc19ffedcf35d1a1f995f598d`  
		Last Modified: Tue, 11 Jul 2023 19:51:18 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9526272b78daddae1e6eac67bd3e4bdbf2b9c21416360c73e6c37162e66512f4`  
		Last Modified: Tue, 11 Jul 2023 19:51:15 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba40256fd8e7f1d43ef34a3091979be78ee7fb933dcdbdc4bef5d0d98ab1278f`  
		Last Modified: Tue, 11 Jul 2023 19:51:16 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2a82691e07a2e55077a1c22ea6f9e332339502bbaec6fe824e50f35a583f8c`  
		Last Modified: Tue, 11 Jul 2023 19:51:15 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b4361ad576fa2153b4568368c1e5f0b984cc5e58f7f567380c34dc8a902b10`  
		Last Modified: Tue, 11 Jul 2023 19:51:16 GMT  
		Size: 1.7 MB (1676666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91fc2b28dca4dd1afcde9a3955a81f10c2b279926068588f635e5530e03be11`  
		Last Modified: Tue, 11 Jul 2023 19:51:15 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
