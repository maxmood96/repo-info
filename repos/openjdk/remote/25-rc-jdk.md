## `openjdk:25-rc-jdk`

```console
$ docker pull openjdk@sha256:93dff9f92a5051ea978e6564dfc2f8e97841d3730aef8aa0db096d184077c71c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `openjdk:25-rc-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:b86fa57dc930a686fb02b4abad846b4c3f2ad5bb4a17c5ca8877f5cf7471f28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310572770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b42c0e65bb14cbb625e7ec50ee6f162eea396a4f8ae6405c596749fd600dde7`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:58:59 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:58:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:10aec8a104c7ecf055b7137fb34a3666fce4dff1b9f6d210fb88eaddd4c8c329`  
		Last Modified: Thu, 07 Aug 2025 23:49:00 GMT  
		Size: 49.5 MB (49497127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2e59f9a91047c70671f0111ff4bf1a5bc4d559bca5e6bb22f83d743c143e91`  
		Last Modified: Mon, 18 Aug 2025 18:17:03 GMT  
		Size: 38.0 MB (38007234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9c740b492dde7a71ed7871f62b7a797273c5db472e3a031651677d1535932b`  
		Last Modified: Mon, 18 Aug 2025 21:36:55 GMT  
		Size: 223.1 MB (223068409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:117d8f4c50ae141f011e25d0a2c302d2a80f8a0833ebc2ea3975a816962ea990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3657300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382a0c64549d3a6800f8592899ccd2dfdf3d3b07d8386ceef2f08d0f52e9e045`

```dockerfile
```

-	Layers:
	-	`sha256:f93e67094444e939131dd379e0906315a38cdf1ef8c4e6fe45cb9eee0b039270`  
		Last Modified: Mon, 18 Aug 2025 21:23:24 GMT  
		Size: 3.6 MB (3639418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba6eb82463a28dad04207b481ff9b52f98cffe6ef69c25128cc52a71a5361ef0`  
		Last Modified: Mon, 18 Aug 2025 21:23:25 GMT  
		Size: 17.9 KB (17882 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-rc-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:19ecc23a61eb4621fd827f16ce51e58b070763dd4dcb008956557fbfc4a0b351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307365568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de0111f97136cf5d4806cdf238cfd94ddfb3d15227ce6ee1b0d6a43e1cfdc80`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:59:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:59:57 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9c27940f400cbdef01d301fb84d1331162f6c76466797e235ea774e439f357`  
		Last Modified: Mon, 18 Aug 2025 22:21:13 GMT  
		Size: 38.4 MB (38409969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bede8aa2cca3e1f421e557147221cd5d1046b7936655046e896c4e78da3efc5`  
		Last Modified: Tue, 19 Aug 2025 00:43:10 GMT  
		Size: 220.9 MB (220868688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:f2f6e4737953e95be3f7c6cde84da34d76f08b72b5e4ac64da8a0fdf1efcc412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3655205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef23305da8e9590f8a18625a6d1b8fa20083b2e4c392c65a8fb933bc38143776`

```dockerfile
```

-	Layers:
	-	`sha256:14b21294e8f7591a34baefd9f65f0f808cee25537f56366efc1b0515b0bd050d`  
		Last Modified: Tue, 19 Aug 2025 00:23:33 GMT  
		Size: 3.6 MB (3637108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c75783c8a72266fa3ca174dc6bc364236cd79be8cf773d164b28838dd5e354ce`  
		Last Modified: Tue, 19 Aug 2025 00:23:34 GMT  
		Size: 18.1 KB (18097 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-rc-jdk` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:cab96658709c7178416a658468702b8fa2298c29a23680f202255294a93c184a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3718545717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46374309e7a88fa84da845af329dc846e82ca4dbb08063c9fa89f03cb354788a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 18 Aug 2025 18:19:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 18 Aug 2025 18:19:21 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 18 Aug 2025 18:19:21 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 18 Aug 2025 18:19:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 18 Aug 2025 18:19:27 GMT
ENV JAVA_VERSION=25
# Mon, 18 Aug 2025 18:19:27 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_windows-x64_bin.zip
# Mon, 18 Aug 2025 18:19:27 GMT
ENV JAVA_SHA256=85bcc178461e2cb3c549ab9ca9dfa73afd54c09a175d6510d0884071867137d3
# Mon, 18 Aug 2025 18:19:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 18 Aug 2025 18:19:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c177312ecef37e4a536f63a5305d51b4cd6aeaf04af37ddd4b333b010623a4`  
		Last Modified: Mon, 18 Aug 2025 18:27:14 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adb831e56b364c28f0d193daa9cf20479b8ff52cad075b2552eb313f0c16dbf`  
		Last Modified: Mon, 18 Aug 2025 18:27:19 GMT  
		Size: 384.2 KB (384205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c857f73b2b0ff68b53d40b01f9e44ddcbd92087502fca892e4a708fd09a217`  
		Last Modified: Mon, 18 Aug 2025 18:27:24 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f1865248e506d0f4fb872013e71a27d465a483b3cab9b2a9efa1dd18511a2b`  
		Last Modified: Mon, 18 Aug 2025 18:27:29 GMT  
		Size: 367.5 KB (367474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3e72563d7caed9846fcab8f36b7567053468ae15287fad71226faa0579cb5c`  
		Last Modified: Mon, 18 Aug 2025 18:27:36 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8adb61384619cb129b0d9e24ed2fe4cd419eeee5555e0b92b6bc5d0313fdfe8`  
		Last Modified: Mon, 18 Aug 2025 18:27:39 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4c7b25838eb0779304df12e4437f41a095cb6d9254bccf3c04e28ff969a0ad`  
		Last Modified: Mon, 18 Aug 2025 18:27:46 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785bdd7f5ca8781a4b1bc71e516403587b6c16714a0112f1f04d293943aad4ea`  
		Last Modified: Mon, 18 Aug 2025 19:08:50 GMT  
		Size: 219.0 MB (218955531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bc527e28a7cadf3ebfddb991a5dd1331e451aa6315f0ed660d766fc0dbd78a`  
		Last Modified: Mon, 18 Aug 2025 18:27:50 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-rc-jdk` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:e7499d7786422dd4726a36fa3eaefabf4d999201c107d3b1eb808edbc9da939d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2501340872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d0b8391a64ca59141187d3bcd3494b877364941769d08a3b71f3323992e406`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 18 Aug 2025 18:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 18 Aug 2025 18:19:06 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 18 Aug 2025 18:19:07 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 18 Aug 2025 18:19:13 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 18 Aug 2025 18:19:14 GMT
ENV JAVA_VERSION=25
# Mon, 18 Aug 2025 18:19:15 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_windows-x64_bin.zip
# Mon, 18 Aug 2025 18:19:16 GMT
ENV JAVA_SHA256=85bcc178461e2cb3c549ab9ca9dfa73afd54c09a175d6510d0884071867137d3
# Mon, 18 Aug 2025 18:19:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 18 Aug 2025 18:19:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4f4df2eeb43897d5f74a9ae36aab86f7e26e94928eff558f3ad468f78d7dff`  
		Last Modified: Mon, 18 Aug 2025 18:21:15 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df091f9ac333bf9570fff6a63ce4a64a3a4022f03b942475e890df51bb534ef`  
		Last Modified: Mon, 18 Aug 2025 18:21:18 GMT  
		Size: 362.3 KB (362301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb5e91fc3a932ee8d9a453817066bd975bf05b5d2de703f56f945327aed238d`  
		Last Modified: Mon, 18 Aug 2025 18:21:19 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cc569b1e03338e0fd5a680caf41769c69198922f70d0274879f83e95360533`  
		Last Modified: Mon, 18 Aug 2025 18:21:19 GMT  
		Size: 351.5 KB (351501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfc2b76fc3e7f91ce5baf3c2d561a708df24daaf8ac5d42f51d80f1789954a1`  
		Last Modified: Mon, 18 Aug 2025 18:21:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8139b8ab5c33cd15688966e0c8121091dca2dbcac26bcd5a64945ce08043a931`  
		Last Modified: Mon, 18 Aug 2025 18:21:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9caf1fedc8c1bc45402b0c45820be76fe3d7bf0861f304ee09d7ffc3e903d63`  
		Last Modified: Mon, 18 Aug 2025 18:21:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f6099efa6b6d114fdf35baa8285b4fc7e69683582e711795cd65431159950d`  
		Last Modified: Mon, 18 Aug 2025 19:08:58 GMT  
		Size: 218.9 MB (218927412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc40bfe89cda8b975e4970ecc7c566902008f2336e41b2cea0c1bd67bde734bc`  
		Last Modified: Mon, 18 Aug 2025 18:21:25 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
