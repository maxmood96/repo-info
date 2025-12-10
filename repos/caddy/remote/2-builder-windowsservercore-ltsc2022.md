## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:e39885097d94efb777158b434049a2a7f30e7f6a5f74f11fddd8ceb9f1c7ea76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull caddy@sha256:08793def72e1d84f0fafda97a9ab204518ade3a5707882b224e78cbb84d12c47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896385778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0115111de5aa3f3b76b57e939b14ef2653f010278025e95355101269cbe4e8d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:40:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:41:43 GMT
ENV GIT_VERSION=2.48.1
# Tue, 09 Dec 2025 20:41:43 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 09 Dec 2025 20:41:44 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 09 Dec 2025 20:41:45 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 09 Dec 2025 20:42:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:42:13 GMT
ENV GOPATH=C:\go
# Tue, 09 Dec 2025 20:42:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:42:19 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 20:43:55 GMT
RUN $url = 'https://dl.google.com/go/go1.25.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ae756cce1cb80c819b4fe01b0353807178f532211b47f72d7fa77949de054ebb'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:43:56 GMT
WORKDIR C:\go
# Tue, 09 Dec 2025 21:18:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 21:18:18 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 09 Dec 2025 21:18:19 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 09 Dec 2025 21:18:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Dec 2025 21:18:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Dec 2025 21:18:26 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6381426f6db953d9a70cba6759e20f0456f0b12bdb617e9dc982295e4d1c410`  
		Last Modified: Tue, 09 Dec 2025 20:41:33 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f148c26323c93f615ca508b193712a39f7c1a253217ee17b536aa5333db5bf16`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0678a53d729d5770d53e0a2df79db61466f0731975e73cd61dc6d8f34f478caa`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b85501a3ac4a80ddb1616e95f5465e32a289be5754e2bbd34c4c84a8117edca`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28613216243e696ea74ce0587ccc8435639adc4efab69c086bd2f08818478f86`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0adfd8afb28d6c19753b94a29ee62ffc3239782f87d168cbd2bb219ca08a2645`  
		Last Modified: Tue, 09 Dec 2025 20:44:36 GMT  
		Size: 51.3 MB (51330976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5983c826c590b9d992c4fbf25185d44eafd4459604413aac5bd615dc9c40ca`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6339af4cdc57a9413ae462f51e3bff8b6bb130c058c821e3415cbde286d05d6d`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 328.4 KB (328368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd165d2766362e7b847e3f2d63c43d2bd269075fa0bf7b7b56b7821a23bcec1`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714939082fef4f8863aa9a64308a8815dcc040b0a831d71dce144724da0354bd`  
		Last Modified: Tue, 09 Dec 2025 20:44:35 GMT  
		Size: 62.6 MB (62556260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd79dd767758fbe9d751a512e4d6f551afbbbcb3e663f7f540293316b10d1ae7`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 1.5 KB (1467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa563f8fb211823676e51ba60ddbbb1056ffb2ab2ea916491357a14e55d38d0d`  
		Last Modified: Tue, 09 Dec 2025 21:18:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2380b591143cab579f2856f38c60231155169298395640bfc80bea807ece878b`  
		Last Modified: Tue, 09 Dec 2025 21:18:38 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b014e4e24cf8c17f928835ad4c918d945622aef69fd399918086c3371c4057`  
		Last Modified: Tue, 09 Dec 2025 21:18:38 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5726ec34a62cfec66e6cc24b57e0bc436de350b51729f9a93cc18d4d9b4124`  
		Last Modified: Tue, 09 Dec 2025 21:18:48 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158bbd9d71f946cae34ce06ee04b8f1b345c83edca47742e0fa9996334a4e9d0`  
		Last Modified: Tue, 09 Dec 2025 21:18:38 GMT  
		Size: 2.3 MB (2273703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0e24bfad60ab3ad4d1d69a1cb33b6bca135aab0ed0daf450565ded842a7045`  
		Last Modified: Tue, 09 Dec 2025 21:18:38 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
