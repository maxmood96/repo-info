## `openjdk:24-jdk`

```console
$ docker pull openjdk@sha256:4c93da528884e6effc2c94dd62849aa0aff4867cac28be2941880737cdbaaf98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:7608a0a78acbc5602a991e9ef6dbe186b6adb27f9a4977f58e2feaa1d201619e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310705208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90bec810e1c80c14cee80d53c86e87a76d99651909dd7a2398e28046bdd8412`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Feb 2025 19:48:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
CMD ["/bin/bash"]
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Tue, 04 Feb 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='bf5289b474e53b34a9ece42dcd3ae073e5ef7df63fcb9c44fbcac92496dedd99'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='96e6ce86751c7aceb6e5f435be31ecbd0629592097abbd67d1c0f5c5b85c8f78'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c46ec965fc0d0493229ac200d2975b7c89fa91892ea0f2a83327878381a32e`  
		Last Modified: Wed, 05 Feb 2025 21:08:50 GMT  
		Size: 48.8 MB (48767695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a653d7c72fd91d9241eade741ac19fca245803f40f557e73aad38fab842146ad`  
		Last Modified: Wed, 05 Feb 2025 21:08:52 GMT  
		Size: 212.8 MB (212840210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:78bcd58a5793a146ac20d10d14160afbd2a4ff5a780adec8320ef952a03525f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9ba1ebc18152a4ffbfc28f1382c0283f2c7d4ab78b0c68aebf043c376fa604`

```dockerfile
```

-	Layers:
	-	`sha256:61456936950abffae6809e3644a6af9489564603ba15649a2e5084fd25204891`  
		Last Modified: Wed, 05 Feb 2025 21:08:49 GMT  
		Size: 4.9 MB (4911371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20854bfd706524b5737485cf8571306ce23e51041300d7dad0919592e6e9f619`  
		Last Modified: Wed, 05 Feb 2025 21:08:49 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:20d1b805ace29898e7fbfd763e6d7449398d11c79f26d32a2952f407049fa3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307655389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabb183e8ebcd71c8d0c6fb5f9c1c617652a5a567d1521fdaf97e8fb3f45527e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Feb 2025 19:48:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
CMD ["/bin/bash"]
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Tue, 04 Feb 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='bf5289b474e53b34a9ece42dcd3ae073e5ef7df63fcb9c44fbcac92496dedd99'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='96e6ce86751c7aceb6e5f435be31ecbd0629592097abbd67d1c0f5c5b85c8f78'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1354218c5a9ae45d85db8f8a7c222a5a95ac10891fc8bc4e58bc61dffb50dcd3`  
		Last Modified: Wed, 05 Feb 2025 21:14:50 GMT  
		Size: 49.2 MB (49193687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f747b566d4c3bb74047988ca17f596db62421b8b97e7b8d91e8e4b3bcd8fc567`  
		Last Modified: Wed, 05 Feb 2025 21:15:47 GMT  
		Size: 210.8 MB (210792292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:0204aee70c54ffd197aef648ba4a810d9fbb060eeadc88efbf7065e369a569c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4929166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5e7c06e2bb95ee4db52043a49b7d8a6d616cdf8cebb709896ce0e995dac338`

```dockerfile
```

-	Layers:
	-	`sha256:d2f305660408c61811aae3f8c1b8a8665a71f977e6f0b9206a71c972d915c0cd`  
		Last Modified: Wed, 05 Feb 2025 21:15:42 GMT  
		Size: 4.9 MB (4909133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a868400f1d91890d2d14bcb4506c1fe66cd097656347d1c1225f6f78d11a3209`  
		Last Modified: Wed, 05 Feb 2025 21:15:42 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:fc8163ca14d5e39f143eb9e3f151d7f8af99b4928b5652698786927163a7d3ff
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2710001773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f402f0ecd841444caa56bc329d19f8e96a65458eb4c8c3c2b61f5d7e8837bbd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Tue, 04 Feb 2025 23:35:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Feb 2025 23:35:33 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:35:33 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 04 Feb 2025 23:35:39 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:35:39 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 23:35:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_windows-x64_bin.zip
# Tue, 04 Feb 2025 23:35:40 GMT
ENV JAVA_SHA256=1d56c9650251685d5d3007781088385fe316738b84a354ef2d3a42b83a38bd46
# Tue, 04 Feb 2025 23:35:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:35:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e815cf122d326a1f2d021f101771ff87b88fb83c556b1aa4e6316068f6cec522`  
		Last Modified: Tue, 04 Feb 2025 23:36:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040b0044124cd4bf7ba45e2111b4630a6134ea3f32a9a48c05e14119163d0237`  
		Last Modified: Tue, 04 Feb 2025 23:36:02 GMT  
		Size: 392.7 KB (392690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc2b0bd242db40cadea3dc3f5fa7fb0d1fe34ad179013078a36bc47ef011503`  
		Last Modified: Tue, 04 Feb 2025 23:36:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e4f831c38698dfddef2a0e305a8af7c3ba915cae4754b623cb34b9670d4214`  
		Last Modified: Tue, 04 Feb 2025 23:36:01 GMT  
		Size: 377.2 KB (377156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b5973dfe16f4a3259d2d15ad8b3df686b60888e38da82e037d0b89197ee99e`  
		Last Modified: Tue, 04 Feb 2025 23:36:01 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cfb32741a297613d2b0772f95dffce34b2d208e49d1168caf3b5e73d429101`  
		Last Modified: Tue, 04 Feb 2025 23:36:00 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc73c6d1c43e8d2edd47e9074786ac605944dab41ad0a939a652637b88b4002`  
		Last Modified: Tue, 04 Feb 2025 23:36:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61b0ef4a1a35f09c92f16711181f7eab4abf111fb318e28f011aa1956b75e91`  
		Last Modified: Tue, 04 Feb 2025 23:36:13 GMT  
		Size: 208.9 MB (208946587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8510759c673a1be4bf5f84e452f7b72580c8ae4fd3ae86a3e62e941287d2cc90`  
		Last Modified: Tue, 04 Feb 2025 23:36:01 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-jdk` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:09e030b949cc2e69c1757d1b1bcdab4e75261266bfda0534f6318397fc9fc041
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471952089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8961db783aabdf78f66c36057fa9e8dbaf5f18d86a723464bcf34a003c9012`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 04 Feb 2025 23:31:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Feb 2025 23:32:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:32:59 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 04 Feb 2025 23:33:12 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:33:12 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 23:33:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_windows-x64_bin.zip
# Tue, 04 Feb 2025 23:33:17 GMT
ENV JAVA_SHA256=1d56c9650251685d5d3007781088385fe316738b84a354ef2d3a42b83a38bd46
# Tue, 04 Feb 2025 23:33:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:33:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05882df6f8da50016aa567c66b23091c8af56572c4b9ab1b6af994f38ae90596`  
		Last Modified: Tue, 04 Feb 2025 23:33:57 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a41ef58d03434f8e5bf7d6149e8336123f6d2db1fea34c600e7651e1d11397`  
		Last Modified: Tue, 04 Feb 2025 23:33:57 GMT  
		Size: 365.0 KB (365019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05d41d6606ba5eb6b4e7d32820b927fc90800a78d0386c0e89d77ff634430c8`  
		Last Modified: Tue, 04 Feb 2025 23:33:56 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290f2b5e0f9a9d843a00121ff3b8c5f6bfd5af045b1cd83bd2496c9c09de0b8f`  
		Last Modified: Tue, 04 Feb 2025 23:33:56 GMT  
		Size: 312.5 KB (312484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bc437ffe8eda74c89eb06ccf88cd1f7a2f1a4f5b0f61160cc0a89b0de98141`  
		Last Modified: Tue, 04 Feb 2025 23:33:55 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5380f7ff3459bdcc2794ac0a8256d908a5e718f58d12f900dfb3bf255436dd75`  
		Last Modified: Tue, 04 Feb 2025 23:33:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef3016435f40a5dcd18ef8ecdd28596abb6179d7fb54b5953e2587778886ae`  
		Last Modified: Tue, 04 Feb 2025 23:33:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d2abd11df77799b007570098ea8414ff660bbc2eabf96d2d0b1157463536b`  
		Last Modified: Tue, 04 Feb 2025 23:34:06 GMT  
		Size: 208.9 MB (208881621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c005b5ad1ab12374ef0804af65fa587c9c8a6a5e63ca707c9051addc2247fb`  
		Last Modified: Tue, 04 Feb 2025 23:33:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-jdk` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:d623f8dbcf1bd1ffb70172a44c8489cd3561e09558e3dbc537fe7a2dfe2777a0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331789524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afd9d83614222ca5fa91c2d5a82a8e281893762529c5e8b22b1b5b82e28f3a0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 04 Feb 2025 23:31:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Feb 2025 23:32:57 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:32:57 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 04 Feb 2025 23:33:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:33:10 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 23:33:11 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_windows-x64_bin.zip
# Tue, 04 Feb 2025 23:33:12 GMT
ENV JAVA_SHA256=1d56c9650251685d5d3007781088385fe316738b84a354ef2d3a42b83a38bd46
# Tue, 04 Feb 2025 23:33:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:33:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9eefe89536b84b640bc3328da635887d46a08366f45c3c9ed76c7dab41e6bd`  
		Last Modified: Tue, 04 Feb 2025 23:34:01 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238ccb5f45f9b6fe33def8b28972062451c43b5eeb5c1aabfba3b889f6d370cf`  
		Last Modified: Tue, 04 Feb 2025 23:34:00 GMT  
		Size: 341.7 KB (341688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4793b5cc4cc0e5e73b287b7abbe099c62364d2410843fe04663f5f1ae83a5e93`  
		Last Modified: Tue, 04 Feb 2025 23:34:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f864f2021d9f4aefe4404683dfd532a5d961bffbafd40811a4ce13786c8303d`  
		Last Modified: Tue, 04 Feb 2025 23:34:00 GMT  
		Size: 332.1 KB (332072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c5e5ef8c1fdc6b7d53a379033c860556ca88444ad4336ba7556f5c569e6706`  
		Last Modified: Tue, 04 Feb 2025 23:33:59 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e94a33006fbc0793982ece6ba767dc8f05627caa205dfd779402b704d44407`  
		Last Modified: Tue, 04 Feb 2025 23:33:59 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5abd32a8823fe8443dfc616eeb9cb17ff024878729bba6333da9bd0927551`  
		Last Modified: Tue, 04 Feb 2025 23:33:59 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81caaf5e64f03c1b93a1468f2303566f8e209ce483f88efc04eb1ae7802c3374`  
		Last Modified: Tue, 04 Feb 2025 23:34:10 GMT  
		Size: 208.9 MB (208895780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55483bc13561a9fd6f8d9b4da538e3e96d28f32641a0a3ae84d0c56480295723`  
		Last Modified: Tue, 04 Feb 2025 23:33:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
