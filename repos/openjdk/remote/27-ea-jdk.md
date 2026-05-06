## `openjdk:27-ea-jdk`

```console
$ docker pull openjdk@sha256:df20ffaf8ece933d0d6611eff27c4c91ed15d45ec3b8a1a1e9c9bb76fdb20db1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `openjdk:27-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:8863e5ad04933d7a13d8bfe36b6203bb779dce1aaad7ccf4868c136821cf4056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.2 MB (309230477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01deb3d558152bf59e378348745a7cecdef8a6fcfbddfca6296f51915f039aa7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 22:03:00 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:03:00 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2026 23:02:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 05 May 2026 23:02:51 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 05 May 2026 23:02:51 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:02:51 GMT
ENV LANG=C.UTF-8
# Tue, 05 May 2026 23:02:51 GMT
ENV JAVA_VERSION=27-ea+20
# Tue, 05 May 2026 23:02:51 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 05 May 2026 23:02:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec2c75dc3bcdc3cbe3d81597cf6bc4be9a4be0da377a5e9e20a8ca4ce05ceafe`  
		Last Modified: Mon, 04 May 2026 22:03:10 GMT  
		Size: 43.1 MB (43077903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4d1b9a15d22b55f24dd92483a1996076e044e82e19cbfc38420e330fd7a386`  
		Last Modified: Tue, 05 May 2026 23:03:14 GMT  
		Size: 37.7 MB (37678657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70f23a14e1fbc561de0c7a06a49a53be33edcb28d39665d6eee23db201555cc`  
		Last Modified: Tue, 05 May 2026 23:03:18 GMT  
		Size: 228.5 MB (228473917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:c7e91b3fdb96090e2dba2ca985f481198cd3af90216fbced377b02fa2ed2a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2cbc49240d0a9566c9c0fed2baf580deda0ea4f699a9435999e2922956b5d1`

```dockerfile
```

-	Layers:
	-	`sha256:134827b1676a3149c287cb6b0d7dcaaf531b74b5b717b1d8d59ffe38f36e4284`  
		Last Modified: Tue, 05 May 2026 23:03:12 GMT  
		Size: 2.4 MB (2367759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54d7efcf2febd708f8efba9a7c6e09305e4296197f30ad05c205b079214e9af3`  
		Last Modified: Tue, 05 May 2026 23:03:12 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ae8ffcdf52fadf5c0ab03d2c1f25b6f5f5eade953cec852ead618645cad36f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305604557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2032e8ed0b049618686868a1528d6bb7b838b4e17cac7ce4db715b7c3d2a7d73`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 21:01:45 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:45 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2026 23:02:48 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 05 May 2026 23:02:59 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 05 May 2026 23:02:59 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:02:59 GMT
ENV LANG=C.UTF-8
# Tue, 05 May 2026 23:02:59 GMT
ENV JAVA_VERSION=27-ea+20
# Tue, 05 May 2026 23:02:59 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 05 May 2026 23:02:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5668b0574ccb4784e2840d685216839b685818991f45396bc2df53f234772cca`  
		Last Modified: Mon, 04 May 2026 21:01:55 GMT  
		Size: 41.5 MB (41471545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92a87701ef34527a61b398666616cc8e6b4e19212bb38abc1100606df4ad0dd`  
		Last Modified: Tue, 05 May 2026 23:03:21 GMT  
		Size: 37.7 MB (37698072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccffa9d312bd28f643d08f668768b9628ac18318062afcb26463e6c0096c7e64`  
		Last Modified: Tue, 05 May 2026 23:03:26 GMT  
		Size: 226.4 MB (226434940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:e8df939a8f3c29b27c89c334ecfaf51cd326c48c049fcc7a3aeab4deeadc7c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f6c3346b444fd90e1d85a7b6c41a5a6796fa9c83bc0cc312a9a892431ffc6c`

```dockerfile
```

-	Layers:
	-	`sha256:53aaebb0b18da07ac384cf36165ed1911c79b89a9cdc791826c136aa2cc61770`  
		Last Modified: Tue, 05 May 2026 23:03:20 GMT  
		Size: 2.4 MB (2367287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47101be2b67ca791632bd3281adfa8e5c64528b5add138395af3b54002037fa0`  
		Last Modified: Tue, 05 May 2026 23:03:20 GMT  
		Size: 18.1 KB (18064 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - windows version 10.0.26100.32690; amd64

```console
$ docker pull openjdk@sha256:2ac8a82b75b0cc92073499a1fae982f917dec978b8df8c5657886c676d76d479
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355726950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74b3f0882f7a711b627a00ff60021b8ce3efc1412b34b4b5651fe8b26aedbb8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 05 May 2026 22:59:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 May 2026 23:00:56 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 05 May 2026 23:00:57 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 05 May 2026 23:01:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 05 May 2026 23:01:04 GMT
ENV JAVA_VERSION=27-ea+20
# Tue, 05 May 2026 23:01:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_windows-x64_bin.zip
# Tue, 05 May 2026 23:01:06 GMT
ENV JAVA_SHA256=5499df903e0ea0fb9652da36292197a89324f03f18fc670d4af55d54c5a75687
# Tue, 05 May 2026 23:01:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 05 May 2026 23:01:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba25f10142e04eaa4f1a4b100591667fb5223281f472a85ba0715fa43973b42c`  
		Last Modified: Tue, 05 May 2026 23:01:49 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2c391f78a3c64fcd513c117a4524f93e9f8f6b808f8a5a5ff84c7acdc85082`  
		Last Modified: Tue, 05 May 2026 23:01:49 GMT  
		Size: 370.7 KB (370693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce38463a8d0ab9af10e93337a3361fe18969f4eaa8d96a0f3c0777eeb054544`  
		Last Modified: Tue, 05 May 2026 23:01:49 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2bcfac10a308f61ecab150b4b3f64a0c902f5591c5c7a5d3232e9334e5e3a44`  
		Last Modified: Tue, 05 May 2026 23:01:49 GMT  
		Size: 371.3 KB (371338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1221112cc13a8c99673908638c51f4f674d2d057962f65646f349187dbdc35`  
		Last Modified: Tue, 05 May 2026 23:01:47 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b23fd73c144b7808bc6ddbae8c365ef4a2a7ca89f84d9ffbc3fc6922d0c946`  
		Last Modified: Tue, 05 May 2026 23:01:47 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae7b0e63c608559d8b65a8414e09503e6d6b346f43169a6dc472eb12d097bfb`  
		Last Modified: Tue, 05 May 2026 23:01:47 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03792966c2c3fb38e7f27aca5544b55503316d3a4dc16d8db6fb190d96c8c1b6`  
		Last Modified: Tue, 05 May 2026 23:02:03 GMT  
		Size: 225.0 MB (224991023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9091292491ea459e809847a9d1bee1760f8d23966b57a5175f112ea7dfb0fea4`  
		Last Modified: Tue, 05 May 2026 23:01:47 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-jdk` - windows version 10.0.20348.5020; amd64

```console
$ docker pull openjdk@sha256:3af02388d6ecb2961378b5310ca4f7e0156b9809d23b49b3e721f356c06cc6b6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296019714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b573c0573f6c3f33ea3f0b84af944ae4a9128415aa2181aedb3b987f640d3a2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 05 May 2026 23:00:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 May 2026 23:01:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 05 May 2026 23:01:14 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 05 May 2026 23:01:23 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 05 May 2026 23:01:24 GMT
ENV JAVA_VERSION=27-ea+20
# Tue, 05 May 2026 23:01:25 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_windows-x64_bin.zip
# Tue, 05 May 2026 23:01:26 GMT
ENV JAVA_SHA256=5499df903e0ea0fb9652da36292197a89324f03f18fc670d4af55d54c5a75687
# Tue, 05 May 2026 23:02:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 05 May 2026 23:02:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdd9ce40371c9ec789b1e772bfe08819d562afa0f8fbe3276f8ee03e83a1868`  
		Last Modified: Tue, 05 May 2026 23:02:15 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59be0aa233d1cdefb8d3fd8dcdb843328246ebd8c9fdb0941c1ba4f5cab4345b`  
		Last Modified: Tue, 05 May 2026 23:02:15 GMT  
		Size: 482.3 KB (482258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac8488ea48fdcea8f7619f864416279171be676eaed46228d874ea79582e5db`  
		Last Modified: Tue, 05 May 2026 23:02:15 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4815d4fca2874e3b889eabae82e0c6f506f7daca18d13434eeb4e6f8714c7e`  
		Last Modified: Tue, 05 May 2026 23:02:15 GMT  
		Size: 346.3 KB (346280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e68c476df70ad4687debb73a565344599aa5064bed353a750e0f0683593e80`  
		Last Modified: Tue, 05 May 2026 23:02:13 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0be45a7b1d5ab4d4a4457c0db5cfccf06945b5aa3e456b5115abfb2e38967b`  
		Last Modified: Tue, 05 May 2026 23:02:13 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe359530f00788995b7e61f0a43ae08fd38d05cd86f862a0600e46aa91f1ed3`  
		Last Modified: Tue, 05 May 2026 23:02:13 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b49a5d55a11d68f593a8d6b6bb3ba15c48cd6de91f962d8768ec8fa9a7490`  
		Last Modified: Tue, 05 May 2026 23:02:29 GMT  
		Size: 225.0 MB (224972026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc57782d1b5b62efdbc1ca6fd42cc92a68dd0985d1ca393df86a86d6aa0295c9`  
		Last Modified: Tue, 05 May 2026 23:02:13 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
