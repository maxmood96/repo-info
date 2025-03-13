## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:d48d8f9399531ad270f384b8a92190257a03fdc0b9edb8e5761d1862894828c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull caddy@sha256:154340f67e2b70751bf770d85360ae763994f9e6e0e9ac914ada85040eafe801
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2282884886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed01b36360fce93259184ad8bab06fe5cce0a501db2ef285afa361656a47ac7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Thu, 13 Mar 2025 17:55:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Mar 2025 17:55:03 GMT
ENV GIT_VERSION=2.48.1
# Thu, 13 Mar 2025 17:55:04 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 13 Mar 2025 17:55:05 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 13 Mar 2025 17:55:06 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 13 Mar 2025 17:55:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 13 Mar 2025 17:55:37 GMT
ENV GOPATH=C:\go
# Thu, 13 Mar 2025 17:55:46 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Mar 2025 17:55:47 GMT
ENV GOLANG_VERSION=1.23.7
# Thu, 13 Mar 2025 17:56:57 GMT
RUN $url = 'https://dl.google.com/go/go1.23.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'eba0477381037868738b47b0198d120a535eb9a8a17b2babb9ab0d5e912a2171'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 13 Mar 2025 17:56:58 GMT
WORKDIR C:\go
# Thu, 13 Mar 2025 18:17:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Mar 2025 18:17:40 GMT
ENV XCADDY_VERSION=v0.4.4
# Thu, 13 Mar 2025 18:17:41 GMT
ENV CADDY_VERSION=v2.9.1
# Thu, 13 Mar 2025 18:17:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 13 Mar 2025 18:18:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 13 Mar 2025 18:18:05 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733770158767b00c4f725e67a536d2ba28438d1a82382a706f535d5f2dd9d882`  
		Last Modified: Thu, 13 Mar 2025 17:57:07 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b0554c437fe02856443406fc90fd3446d67b5e9062af9dc8d7484fdf51fb0f`  
		Last Modified: Thu, 13 Mar 2025 17:57:07 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57c017dc37c206fd810594138869fe107ab574c4ffebb10aff710e4e13a7ff3`  
		Last Modified: Thu, 13 Mar 2025 17:57:05 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb80a140da04e4c1caef53bc7985e51bb90b8f71364980c8e9666585eb0fb33`  
		Last Modified: Thu, 13 Mar 2025 17:57:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59229be1dcc6ff436106dad59fc88576a796b6cba7e53e1f33ce6a07492f2f12`  
		Last Modified: Thu, 13 Mar 2025 17:57:05 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696f3ef6e1ca397c1961490ecfd72c9991ba8a5a05f86b525f0a42ed35113ead`  
		Last Modified: Thu, 13 Mar 2025 17:57:11 GMT  
		Size: 51.2 MB (51206852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb6d46680c2521fca24415661c34d5d6ddba3e81025fcf65cb822291add6ad5`  
		Last Modified: Thu, 13 Mar 2025 17:57:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686862c16d9005f48b2a13caa0b27d53ab8ff9e412e550b43b8da6ef11ae5816`  
		Last Modified: Thu, 13 Mar 2025 17:57:03 GMT  
		Size: 345.0 KB (345020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47342f2e3df393a0a9e30153b304c5f70765cb24da420b411afbcec68e80a1fe`  
		Last Modified: Thu, 13 Mar 2025 17:57:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5704b716543a5e1aa8ef4815d02f74aaaa8e7d51960079a5eeb52f9b9733a6b4`  
		Last Modified: Thu, 13 Mar 2025 17:57:15 GMT  
		Size: 77.4 MB (77376059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6335d98e09b879a8989fe034ea1d46bcfa76582476ad8ad037699898ffc02d02`  
		Last Modified: Thu, 13 Mar 2025 17:57:03 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f475fdac6617572185dfa9f6b4efdfd2ffb2349f3afb86412fcb377da8a13a14`  
		Last Modified: Thu, 13 Mar 2025 18:18:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92723da560b1b8a3953fcc3975dac6744aa38f0c63c88c7f98686599e24664cb`  
		Last Modified: Thu, 13 Mar 2025 18:18:09 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d669063d6470f0ac7f381268217930818255986b3dcd267146119885160afb1e`  
		Last Modified: Thu, 13 Mar 2025 18:18:09 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ace00a034c35f8e320886395690daf5c8714862c3be36f2882a5ecb493af867`  
		Last Modified: Thu, 13 Mar 2025 18:18:09 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1fdcb3bc3569343bd9280cc5fbdf764456aff308e3cad59b92e66ffab557df`  
		Last Modified: Thu, 13 Mar 2025 18:18:10 GMT  
		Size: 2.3 MB (2305302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a21eb03a97328a27d9b098175c2140ca1116cec6b6790670aa5438702f784fd`  
		Last Modified: Thu, 13 Mar 2025 18:18:09 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
